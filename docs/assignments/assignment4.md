---
title: Assignment 4- Backend (Alpha)
layout: doc
---

# Assignment 3- Backend (Alpha)

## Important Links

 - Link to A4 Github repo: [Github repo](https://github.com/manasakudumu/noor-backend)

- Link to A3 (Convergent Design): [A3-mkudumu-portfolio](https://manasakudumu.github.io/portfolio-mkudumu/assignments/assignment3.html)

- Link to Vercel Deployment: [Vercel Deployment](https://vercel.com/manasa-kudumus-projects/noor_backend)

## Abstract Data Models

## implementation for two concepts
**Alerting:**
```ts
import { ObjectId } from "mongodb";
import DocCollection, { BaseDoc } from "../framework/doc";
import { NotAllowedError, NotFoundError } from "./errors";

export interface AlertDoc extends BaseDoc {
  userId: ObjectId;
  location: string;
  status: boolean; // true means alert is active, false means it's not
}

/**
 * concept: Alerting [User]
 */
export default class AlertingConcept {
  public readonly alerts: DocCollection<AlertDoc>;

  constructor(collectionName: string) {
    this.alerts = new DocCollection<AlertDoc>(collectionName + "_alerts");
  }

  // Activate emergency alert
  async activateEmergencyAlert(userId: ObjectId, location: string) {
    const existingAlert = await this.alerts.readOne({ userId });
    if (existingAlert && existingAlert.status) {
      throw new NotAllowedError("Emergency alert already active for this user.");
    }
    await this.alerts.createOne({ userId, location, status: true });
    return { msg: "Emergency alert activated!" };
  }

  // Deactivate emergency alert
  async deactivateEmergencyAlert(userId: ObjectId) {
    const alert = await this.alerts.readOne({ userId });
    if (!alert || !alert.status) {
      throw new NotFoundError("No active emergency alert found for this user.");
    }
    await this.alerts.partialUpdateOne({ userId }, { status: false });
    return { msg: "Emergency alert deactivated!" };
  }

  // Update location during active alert
  async updateLocation(userId: ObjectId, newLocation: string) {
    const alert = await this.alerts.readOne({ userId });
    if (!alert || !alert.status) {
      throw new NotAllowedError("No active alert to update location.");
    }
    await this.alerts.partialUpdateOne({ userId }, { location: newLocation });
    return { msg: "Location updated successfully!" };
  }
}
```

**Monitoring:**
```ts
import { ObjectId } from "mongodb";
import DocCollection, { BaseDoc } from "../framework/doc";
import { NotAllowedError, NotFoundError } from "./errors";

export interface CheckInScheduleDoc extends BaseDoc {
  userId: ObjectId;
  schedule: Date;
}

export interface UserCheckInStatusDoc extends BaseDoc {
  userId: ObjectId;
  status: boolean;
}

/**
 * concept: Monitoring [User]
 */
export default class MonitoringConcept {
  public readonly checkInSchedules: DocCollection<CheckInScheduleDoc>;
  public readonly checkInStatus: DocCollection<UserCheckInStatusDoc>;

  constructor(collectionName: string) {
    this.checkInSchedules = new DocCollection<CheckInScheduleDoc>(collectionName + "_schedules");
    this.checkInStatus = new DocCollection<UserCheckInStatusDoc>(collectionName + "_status");
  }

  // Schedule a check-in for a user
  async scheduleCheckIn(userId: ObjectId, schedule: Date) {
    const existing = await this.checkInSchedules.readOne({ userId });
    if (existing !== null) {
      throw new NotAllowedError("User already has a scheduled check-in.");
    }
    await this.checkInSchedules.createOne({ userId, schedule });
    return { msg: "Check-in scheduled successfully!" };
  }

  // Record a check-in for a user
  async recordCheckIn(userId: ObjectId) {
    const checkIn = await this.checkInSchedules.readOne({ userId });
    if (!checkIn) {
      throw new NotFoundError("No check-in schedule found for user.");
    }
    await this.checkInStatus.createOne({ userId, status: true });
    return { msg: "User check-in recorded successfully!" };
  }

  // Get check-in status
  async getCheckInStatus(userId: ObjectId) {
    const status = await this.checkInStatus.readOne({ userId });
    if (!status) {
      throw new NotFoundError("No check-in status found for user.");
    }
    return status;
  }

  // Alert trusted contacts if no check-in was recorded
  async alertContacts(userId: ObjectId) {
    const status = await this.checkInStatus.readOne({ userId });
    if (!status || !status.status) {
      return { msg: "Alerting trusted contacts!" };
    }
    return { msg: "No alerts needed. User checked in successfully." };
  }
}
```

## Initial outline of RESTful Routes
```ts
  // Alerting Routes

  @Router.post("/alert")
  async activateEmergencyAlert(session: SessionDoc, location: string) {
    const user = Sessioning.getUser(session);
    return await Alerting.activateEmergencyAlert(user, location);
  }

  @Router.post("/alert/deactivate")
  async deactivateEmergencyAlert(session: SessionDoc) {
    const user = Sessioning.getUser(session);
    return await Alerting.deactivateEmergencyAlert(user);
  }

  @Router.patch("/alert/location")
  async updateLocation(session: SessionDoc, newLocation: string) {
    const user = Sessioning.getUser(session);
    return await Alerting.updateLocation(user, newLocation);
  }

  
    //rest of the concepts
  @Router.post("/comments/:itemId")
  async commentOnItem(itemId: string, comment: string) {
  // Comment on an item (post/message)
  }


  @Router.delete("/comments/:commentId")
  async deleteComment(commentId: string) {
    // Delete a specific comment
  }


  @Router.post("/filtering/apply")
  async applyFilter(userId: string, settings: object) {
    // Apply filter rule
  }


  @Router.get("/filtering/:userId")
  async getFilterSettings(userId: string) {
    // Fetch all applied filter rules for a user
  }


  @Router.delete("/filtering/remove")
  async removeFilter(userId: string, ruleId: string) {
    // Remove a filter rule from the user's settings
  }


  @Router.post("/reading/label")
  async labelElement(elementId: string, label: string) {
    // Label a UI element for screen readers
  }


  @Router.post("/reading/summary/:postId")
  async generateSummary(postId: string) {
    // Generate a summary for a post
  }
```

