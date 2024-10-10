---
title: Assignment 4- Backend (Alpha)
layout: doc
---

# Assignment 4- Backend (Beta)

## Important Links

 - Link to Backend Github repo: [Github repo](https://github.com/manasakudumu/noor-backend)

- Link to A3 (Convergent Design): [A3-mkudumu-portfolio](https://manasakudumu.github.io/portfolio-mkudumu/assignments/assignment3.html)

- Link to Vercel Deployment: [Vercel Deployment](https://vercel.com/manasa-kudumus-projects/noor_backend)

## Corrections to A3 states and actions
1. Concept : Authenticating
```
Purpose: Authenticates users and ensures login

Operational Principle: 
After registering with a username, password, and accessible CAPTCHA, users can authenticate and access their accounts.

State:
registered: set User
username: User -> one String
password: registered -> one String
captcha: registered -> one String

```

2. Concept : Posting[User, Item]
```
Purpose: 
Enable users to post content for others to \\\.

Operational Principle: 
After registering with a username, password, and accessible CAPTCHA, users can authenticate and access their accounts.

State:
posts: set Post
author: Post → one User
content: Post → one String
time: Post -> one Date

```
3. Concept : Sessioning[User]
```
Purpose: 
enable authenticated actions for a period of time.

Operational Principle: 
After registering with a username, password, and accessible CAPTCHA, users can authenticate and access their accounts.

State:
active: set Session
user: active -> one User

```
4. Concept : Reading[Item, Message, Post]
```
Purpose: 
Ensures that all content (messaging, alt-text on posts, etc.) in the app is fully optimized for screen readers, providing enhanced accessibility through clear labeling, logical structure, and streamlined navigation to enable visually impaired users to easily consume and interact with posts and other app elements.

Operational Principle: 
after a user encounters a post or message on the app, they can easily read the alt-text on the image and the message in a more accessible and streamlined manner.

State:
items: set Item
labels: Item -> one String        
structure: Item -> one Page       
summaries: Item -> one String 
```

5. Concept : Messaging[User, Item]
```
Purpose: 
 Allow users to receive and send messages

Operational Principle: 
After a user encounters a post/ receives any hate/ biased content, they can choose to add a filter where they can get posts from their trusted contacts.

State:
messages: set Message
to: Message -> one User
time: Message -> one Date
content: Message -> one String
from: Message -> one User
```

6. Concept : Alerting[User]
```
Purpose: 
Allow users to send emergency alerts along with location data to trusted contacts.

Operational Principle: 
after a user sends a message to another user, they can receive a message as well. 

State:
location: Alert -> one String
emergencyContacts: Alert -> one User
alertStatus: Alert -> one Boolean
```

7. Concept : Monitoring[User]
```
Purpose: 
Ensure that caregivers or family members can periodically check in on the elderly user's well-being by receiving scheduled updates or prompts for user responses.

Operational Principle: 
After setting up trusted contacts, the system monitors the user at regular intervals, prompting them to check in.

State:
trustedContacts: Contact -> one User
status: Contact -> one Boolean
checkInSchedule: Contact -> one Date
```
### Abstract Data Model
Assignment 4-5
<img src="./images/Assignment 4-5.jpg" alt="A$ data model" width="700px">

## Data Representation and RESTful Routes:
 - Link to Backend Github repo: [Github repo](https://github.com/manasakudumu/noor-backend)

## Deployment
- Link to Vercel Deployment: [Vercel Deployment](https://vercel.com/manasa-kudumus-projects/noor_backend)

## Design Reflection


