title: Assignment 5- Frontend (Beta)
layout: doc
---

# Assignment 5- Frontend (Beta)

## Important Links
- Link to Wireframes from A3: [Wireframes](https://www.figma.com/design/WKxhMFRzPR1yDqL3s9WpRt/A3%3A-Convergent-Design-Wireframes?node-id=0-1)

- Visual Design Study: [GoogleSlides] (https://docs.google.com/presentation/d/1ouKBGiXmLINlYdwhRDZHCbO4tV3JcxqJd3ckFfD2f7U/edit#slide=id.p)

- Link to A5 Github repo: [Github repo](https://github.com/manasakudumu/noor-frontend)

- Deployment: [Vercel Deployment](https://vercel.com/manasa-kudumus-projects/noor-frontend)


## Heuristic evaluation and writeup
### Usability:
#### Accessibility:
- My wireframes use large, labeled buttons and inputs which makes it accessible to users with visual impairments and motor disabilities. I also made sure to have a simpler UI for easier screen reader navigation
- However, there could be issues with contrasting issues win terms of text and background which could make it difficult for users with low vision
- Improvement: I will increase the contrast between the text and the background and use ARIA labels to support screen readers better.
#### Error Tolerance: 
- The current design has basic error messages when a user enters any invalid inputs like incorrect passwords.
- There might be confusions in the specificity of the error. Most of my errors say “Invalid input” where instead it could rather say “Password must be at least 6 characters” or “Email address is invalid”
- Improvement: I would like to enhance my error messages by making them more specific and actionable.

### Physical Heuristics:
#### Fitts Law: 	
- Primary actions like submit, emergency alert are large and placed at the part of the screen that can be clicked easily (center).
- Especially in an emergency situation it is important to have the alert button be present in each page and be large enough to be clicked.
- To improve, I would improve the spacing of the buttons, by making the more frequently used buttons more prominent on the page. This is especially important on mobile devices.
#### Situational Context:
- Wireframes show where the users are within the app including a bar on the side of the page including all the pages on the app
- To improve I would want to re-instantiate the title of the page on every page to make sure the users know what they are using at that moment.
- I would also like to add more loading conformations like “Success!” after logging in or “Submitted” after sending a routine monitor reflection.

### Linguistic Level:
#### Speak a users language:
- My wireframes use simple and straightforward language that the user could easily understand. 
- Similar to error tolerance, after including the CAPTCHA feature, I would like to make it a little less technical and easier to understand
#### Information Scent: 
- The wireframe uses clear labels for navigating like emergency alerting, monitoring, and posting. 
- I would like to make navigation a little more intuitive especially since the user would have to use a screen reader to navigate through the page. 
