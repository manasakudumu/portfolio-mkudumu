---
title: Assignment 6- User Testing
layout: doc
---

# Assignment 6- User Testing


# Assignment 6 - User Testing

## Task List for User Testing

| Title              | Description                                                              | Purpose                                                                                                     |
|--------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Register           | User registers a new account with the app                               | Required for initial use of the app’s safety and social features.                                           |
| Emergency Alert    | User activates the emergency alert feature                               | Tests ease of use and critical response time for visually impaired users during emergencies.               |
| Trusted Contacts   | User views, adds, and removes trusted contacts                           | Ensures smooth management of trusted contacts for security purposes.                                        |
| Messaging          | User sends and reads messages from their trusted contacts                | Tests intuitiveness and accessibility of the messaging feature.                                             |
| Check-In           | User initiates a routine check-in and records their status               | Measures accessibility and reliability for routine wellness check-ins.                                      |
| Post Update        | User posts a status update for their trusted contacts to view            | Tests discoverability of social features and ease of sharing information with trusted individuals.          |
| Navigation         | User explores and moves between various pages (profile, settings, alert) | Assesses consistency, linguistic clarity, and navigation accessibility.                                     |
| Logout/Login       | User logs out and attempts to log back in                                | Evaluates ease of access and security in logging back in.                                                   |

---

## User Test 1: Lakshmi Parthasarathy

Lakshmi, age 68, is testing Noor to see if it helps her stay connected and safe. Even though she is not visually impaired, she falls under the category of elderly users.

### Feedback

- **Register:** Lakshmi found the registration process straightforward, though she needed help with setting a password.
- **Emergency Alert:** She quickly understood the purpose of the emergency alert button and appreciated the placement at the bottom right corner for easy access.
  - **Suggestions:** Add a voice confirmation to indicate that the alert has been sent.
- **Trusted Contacts:** Lakshmi viewed her list of trusted contacts but accidentally removed one.
  - **Suggestions:** A confirmation prompt for removing contacts could prevent accidental removals.
- **Messaging:** Lakshmi could open messages but had difficulty composing one.
  - **Suggestions:** Add a verbal or haptic confirmation when a message is sent.
- **Check-In:** She successfully initiated a check-in but was unsure if it registered her status.
  - **Suggestions:** Provide a confirmation message for a successful check-in.
- **Post Update:** Lakshmi found it enjoyable to post updates, though she wasn’t sure if others could see them.
  - **Suggestions:** Add a notification for visibility of posts to trusted contacts.
- **Navigation:** She initially confused the Settings and Profile tabs, which caused misnavigation.
- **Logout/Login:** She accidentally logged out and couldn’t recall her login details.
  - **Suggestions:** Implement a 'Confirm Logout' prompt.

**Overall Impressions:** Lakshmi found the app mostly intuitive but would like clearer confirmations for actions like emergency alerts, check-ins, and message sending.

---

## User Test 2: Vedhanandini Parthasarathy

Vedhanandini, age 46, is testing Noor to see if it would help her mother, Lakshmi, stay safe and in touch with her family.

### Feedback

- **Register:** Vedhanandini found the registration straightforward but noted that an option for biometrics would be helpful for elderly users.
- **Emergency Alert:** She liked the placement of the emergency alert button but expected a confirmation message.
  - **Suggestions:** Add a vibration or confirmation for successful alert activation.
- **Trusted Contacts:** She found adding and removing contacts smooth.
  - **Suggestions:** Consider adding a 'favorites' feature for main contacts.
- **Messaging:** She found messaging user-friendly.
  - **Suggestions:** Add read receipts or message status indicators.
- **Check-In:** She completed the check-in process easily.
  - **Suggestions:** Add reminders for routine check-ins at specific times.
- **Post Update:** She enjoyed the simplicity of posting.
  - **Suggestions:** Display posts on the home screen for easy access.
- **Navigation:** Navigation was smooth, but she suggested using icons with text for clarity.
- **Logout/Login:** Similar to Lakshmi, she found the logout function too easy to trigger.
  - **Suggestions:** Add a 'Confirm Logout' prompt.

**Overall Impressions:** Vedhanandini appreciated the app’s clean layout and felt it would help her mother stay connected. She recommended minor enhancements for navigation and action confirmations.

---

## Opportunities for Improvement

1. **Action Confirmation Messages (Error Tolerance)**
   - **Issue:** Users were unsure if emergency alerts, messages, or check-ins were successfully sent or registered.
   - **Solution:** Add verbal confirmations, vibrations, or on-screen messages to indicate successful actions, especially for emergency alerts.

2. **Enhanced Navigation (Linguistic + Physical Heuristics)**
   - **Issue:** Users confused similar page names, like 'Settings' and 'Profile'.
   - **Solution:** Use icons along with text labels to improve differentiation and add clarity to the navigation.

3. **Feedback on Messages and Posts (Information Scent)**
   - **Issue:** Users were unsure if their posts and messages were visible to others or had been read.
   - **Solution:** Add indicators or notifications to show if messages or posts are viewed by trusted contacts.

4. **Biometric or Alternative Login Options (Usability)**
   - **Issue:** Recalling passwords or IDs for login was difficult for elderly users.
   - **Solution:** Implement biometric logins (such as fingerprint or face recognition) or a PIN code option for easier access. This solution suggested by Vedhanandini is complex to implement but it is a very interesting idea.

---

### New Deployment
- [Vercel Deployment](https://vercel.com/manasa-kudumus-projects/noor-frontend-1)



- New Deployment: [Vercel Deployment](https://vercel.com/manasa-kudumus-projects/noor-frontend-1)