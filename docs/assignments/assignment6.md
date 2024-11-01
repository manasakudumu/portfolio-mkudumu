---
title: Assignment 6- User Testing
layout: doc
---

# Assignment 6- User Testing


interface Task {
  title: string;
  description: string;
  purpose: string;
}

interface Feedback {
  task: string;
  details: string;
  suggestions?: string;
}

interface UserTest {
  userName: string;
  userDescription: string;
  feedback: Feedback[];
  overallImpressions: string;
}

interface ImprovementOpportunity {
  title: string;
  issue: string;
  solution: string;
}

// Task List for User Testing
const tasks: Task[] = [
  {
    title: "Register",
    description: "User registers a new account with the app",
    purpose: "Required for initial use of the app’s safety and social features."
  },
  {
    title: "Emergency Alert",
    description: "User activates the emergency alert feature",
    purpose: "Tests ease of use and critical response time for a visually impaired user during an emergency."
  },
  {
    title: "Trusted Contacts",
    description: "User views, adds, and removes trusted contacts",
    purpose: "Ensures smooth management of trusted contacts for security purposes."
  },
  {
    title: "Messaging",
    description: "User sends and reads messages from their trusted contacts",
    purpose: "Tests intuitiveness and accessibility of the messaging feature."
  },
  {
    title: "Check-In",
    description: "User initiates a routine check-in and records their status",
    purpose: "Measures accessibility and reliability for routine wellness check-ins."
  },
  {
    title: "Post Update",
    description: "User posts a status update for their trusted contacts to view",
    purpose: "Tests discoverability of social features and ease of sharing information with trusted individuals."
  },
  {
    title: "Navigation",
    description: "User explores and moves between various pages (profile, settings, alerting, etc.)",
    purpose: "Assesses consistency, linguistic clarity, and navigation accessibility."
  },
  {
    title: "Logout/Login",
    description: "User logs out and attempts to log back in to see how easy it is to resume use",
    purpose: "Evaluates ease of access and security in logging back in."
  }
];

// User Test 1
const userTest1: UserTest = {
  userName: "Lakshmi Parthasarathy",
  userDescription: "Lakshmi, age 68, is testing Noor to see if it helps her stay connected and safe. Even though she is not visually impaired she falls under the category of elderly users",
  feedback: [
    {
      task: "Register",
      details: "Lakshmi found the registration process straightforward, though she needed help with setting a password."
    },
    {
      task: "Emergency Alert",
      details: "She quickly understood the purpose of the emergency alert button and appreciated the placement at the bottom right corner for easy access.",
      suggestions: "Add a voice confirmation to indicate that the alert has been sent."
    },
    {
      task: "Trusted Contacts",
      details: "Lakshmi viewed her list of trusted contacts but accidentally removed one.",
      suggestions: "A confirmation prompt for removing contacts could prevent accidental removals."
    },
    {
      task: "Messaging",
      details: "Lakshmi could open messages but had difficulty composing one.",
      suggestions: "Add a verbal or haptic confirmation when a message is sent."
    },
    {
      task: "Check-In",
      details: "She successfully initiated a check-in but was unsure if it registered her status.",
      suggestions: "Provide a confirmation message for a successful check-in."
    },
    {
      task: "Post Update",
      details: "Lakshmi found it enjoyable to post updates, though she wasn’t sure if others could see them.",
      suggestions: "Add a notification for visibility of posts to trusted contacts."
    },
    {
      task: "Navigation",
      details: "She initially confused the Settings and Profile tabs, which caused misnavigation."
    },
    {
      task: "Logout/Login",
      details: "She accidentally logged out and couldn’t recall her login details.",
      suggestions: "Implement a 'Confirm Logout' prompt."
    }
  ],
  overallImpressions: "Lakshmi found the app mostly intuitive but would like clearer confirmations for actions like emergency alerts, check-ins, and message sending."
};

// User Test 2
const userTest2: UserTest = {
  userName: "Vedhanandini Parthasarathy",
  userDescription: "Vedhanandini, age 46, is testing Noor to see if it would help her mother, Lakshmi, stay safe and in touch with her family.",
  feedback: [
    {
      task: "Register",
      details: "Vedhanandini found the registration straightforward but noted that an option for biometrics would be helpful for elderly users."
    },
    {
      task: "Emergency Alert",
      details: "She liked the placement of the emergency alert button but expected a confirmation message.",
      suggestions: "Add a vibration or confirmation for successful alert activation."
    },
    {
      task: "Trusted Contacts",
      details: "She found adding and removing contacts smooth.",
      suggestions: "Consider adding a 'favorites' feature for main contacts."
    },
    {
      task: "Messaging",
      details: "She found messaging user-friendly.",
      suggestions: "Add read receipts or message status indicators."
    },
    {
      task: "Check-In",
      details: "She completed the check-in process easily.",
      suggestions: "Add reminders for routine check-ins at specific times."
    },
    {
      task: "Post Update",
      details: "She enjoyed the simplicity of posting.",
      suggestions: "Display posts on the home screen for easy access."
    },
    {
      task: "Navigation",
      details: "Navigation was smooth, but she suggested using icons with text for clarity."
    },
    {
      task: "Logout/Login",
      details: "Similar to Lakshmi, she found the logout function too easy to trigger.",
      suggestions: "Add a 'Confirm Logout' prompt."
    }
  ],
  overallImpressions: "Vedhanandini appreciated the app’s clean layout and felt it would help her mother stay connected. She recommended minor enhancements for navigation and action confirmations."
};

// Opportunities for Improvement
const improvementOpportunities: ImprovementOpportunity[] = [
  {
    title: "Action Confirmation Messages (Error Tolerance)",
    issue: "Users were unsure if emergency alerts, messages, or check-ins were successfully sent or registered.",
    solution: "Add verbal confirmations, vibrations, or on-screen messages to indicate successful actions, especially for emergency alerts."
  },
  {
    title: "Enhanced Navigation (Linguistic + Physical Heuristics)",
    issue: "Users confused similar page names, like 'Settings' and 'Profile'.",
    solution: "Use icons along with text labels to improve differentiation and add clarity to the navigation."
  },
  {
    title: "Feedback on Messages and Posts (Information Scent)",
    issue: "Users were unsure if their posts and messages were visible to others or had been read.",
    solution: "Add indicators or notifications to show if messages or posts are viewed by trusted contacts."
  },
  {
    title: "Biometric or Alternative Login Options (Usability)",
    issue: "Recalling passwords or IDs for login was difficult for elderly users.",
    solution: "Implement biometric logins (such as fingerprint or face recognition) or a PIN code option for easier access. This solution suggested by Vedhanandini is complex to implement but it is a very interesting idea."
  }
];

export { tasks, userTest1, userTest2, improvementOpportunities };


- New Deployment: [Vercel Deployment](https://vercel.com/manasa-kudumus-projects/noor-frontend-1)