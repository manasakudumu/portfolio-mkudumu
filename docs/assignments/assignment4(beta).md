---
title: Assignment 4- Backend (Beta)
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

### App Definition
```
app Noor
    include Authenticating
    include Posting[User, Item]
    include Sessioning[User]
    include Reading[Item, Message, Post]
    include Messaging[User, Item]
    include Alerting[User]
    include Monitoring[User]
```

### Abstract Data Model
Assignment 4-5
<img src="./images/Assignment 4-5.jpg" alt="A$ data model" width="800px">

## Data Representation and RESTful Routes:
 - Link to Backend Github repo: [Github repo](https://github.com/manasakudumu/noor-backend)

## Deployment
- Link to Vercel Deployment: [Vercel Deployment](https://vercel.com/manasa-kudumus-projects/noor_backend)

## Design Reflection
- While designing and implementing the backend for my app, it revealed several ambiguities and omissions from my previous concepts in A3. Initially the design focused on features like commenting and filtering (biases and harm) which is when I realised that the commenting feature would not be required for that reason (due to harm online). Hence, I pivoted to the concepts with Messaging and Sessioning as these seemed more related to my storyboards from A2 and worked better with the implementation of my app. I received a lot of clarity after redrawing my data models (image above) to make the flows more cohesive.

- I also worked on implementing a reCAPTCHA API (imported axios). This decision was made after further reflecting on my interview with Dino where he emphasized the importance of including a basic CAPTCHA that can be read by a screenreader instead of an image. I hence found it important to include. This was a significant challenge for me, trying to figure out how to manage the API responses without working on my frontend framework, but I hope to improve this on A5!

## Acknowledgements:
Thank you to TA Sophia for helping me figure out how to implement the Google reCAPTCHA API and helping me with my RESTful routes.


