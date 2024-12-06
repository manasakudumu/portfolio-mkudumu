---
title: "Project Phase 5: Beta Release"
layout: doc
---

# Project Phase 5: Beta Release

## Deployment
- [Vercel](https://oscar-kappa.vercel.app/)
- [Github repository](https://github.com/angelwhipple/oscar)

## Concepts
1. Grouping
   - [Data model & actions](https://github.com/angelwhipple/oscar/blob/main/server/concepts/grouping.ts)
   - [Components](https://github.com/angelwhipple/oscar/tree/main/client/components/Grouping)
   - [Data store](https://github.com/angelwhipple/oscar/blob/main/client/stores/group.ts)
2. Permissioning
   - [Data model & actions](https://github.com/angelwhipple/oscar/blob/main/server/concepts/permissioning.ts)
   - [Components](https://github.com/angelwhipple/oscar/tree/main/client/components/Permission)
   - [Data store](https://github.com/angelwhipple/oscar/blob/main/client/stores/user.ts)
3. Accounting
    - [Data model & actions](https://github.com/angelwhipple/oscar/blob/main/server/concepts/accounting.ts)
4. Messaging
   - [Data model & actions](https://github.com/angelwhipple/oscar/blob/main/server/concepts/messaging.ts)
5. Notifying
   - [Data model & actions](https://github.com/angelwhipple/oscar/blob/main/server/concepts/notifying.ts)
   - [Components](https://github.com/angelwhipple/oscar/tree/main/client/components/Notifying)

## Syncs
- [routes.ts](https://github.com/angelwhipple/oscar/blob/main/server/routes.ts)

## Design Revisions
1. **Factored Grouping into Grouping & Accounting:** 
- Change: Decoupled the payment and accounting logic from the concept of grouping users together.
- Rationale: 
2. **Expanded scope of Permissioning:**
3. **Deprioritized Scheduling:**
4. **Revised Notifying:** Notifying now has an inbox feature rather than an alert so that users can keep an account of all their notifications

## User Test Planning

#### Participants
1. User & brief rationale
2. User & brief rationale
3. User & brief rationale

#### Prepopulated data
- Include screenshot

#### Task list
**Prompt:**

|          Title          | Instruction |   Rationale    |
|:-----------------------:|:-----------:|:--------------:|
|    Organize a ROSCA     | Register as an organizer, create a new ROSCA group, set the rules, and add a member  | This task checks to see how easy it would be create an account as an organizer and how well users understand the process of creating and managing a group. This tests our permissioning and grouping functionalities.  |
|   Make a contribution   | Contribute $100 to a ROSCA that you are a part of | This would test our accounting functionality. It will check whether the user can easily perform basic financial actions within the ROSCA and also verifies if insuffiecient funds are appropriately handled (the pot can have a negative value) |
| Send a payment reminder | As an organizer, send a payment reminder to your group who has not contributed funds on time  | This task tests the notifying feature’s usability. It explores whether the user can efficiently send reminders and how effectively the system supports immediate communication between organizers and members.   |
|   Distribute the pot    | As an organizer, distribute the pooled amount to a member  | Along with testing role specific permsissions, it assesses whether an organizer is supported dnough to handle key financial operations like payouts while restricting such actions for members of the ROSCA.  |
|  Start a conversation   | Navigate to your groupchat and send a message to remind the members about an upcoming meeting  | This would evaluate the mesasaging functionality and how it integrates with grouping. It would help identify potential hurdles in navigating or messaging that could hinder communication with the group  |
