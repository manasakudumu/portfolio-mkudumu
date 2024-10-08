---
title: Assignment 1- Social Media Needfinding
layout: doc
---

# Assignment 1: Social Media Needfinding


1. Hunch: 
“How might I design a social media app for people with visual impairments, particularly in elderly age groups? I want to be able to help an underserved community stay connected with others in their community and be able to learn and perform tasks a sighted person could perform using social media.”


2. Interview Plan
- The “who” and the “why”: 
I interviewed two visually impaired people who have used social media in the past. Dino is a 61-year-old man who has been blind since birth. He has used apps like Facebook (along with Messenger), LinkedIn, Twitter, Myspace, and a little bit of Mastodon and Whatsapp. Sheri is a 53-year-old woman who had sight but became completely blind a couple of years ago. She used apps like Facebook, MySpace, and Youtube when she was sighted and also when she became blind. Neither participants are currently associated with a college which makes them different from me in terms of age, experience, and disability. Dino being blind all his life gives him a deeper familiarity with accessibility tools, whereas Sheri losing her sight later, gives insight on the transition from sighted to visually impaired use of social media. I chose to interview people with visual impairments from my previous projects helping this marginalized community. In high school, I built an app using the MIT App Inventor to help provide scribes to students with visual disability in government schools in Bangalore, India and in college, making generative AI more accessible. Having friends and family with visual impairments has also motivated me to continue developing similar projects!

- Recruiting participants:
I recruited participants via emailing local disability organizations in the New England area to see who would be interested in this study. Four participants replied but only two participants followed up and agreed to participate in the interview given that there was no compensation.

- The interview process:
I have attached the links to the questions I asked them and also some notes I took during the interview. There are more detailed notes further down this page in the Interview Report. 
    - Dino interview notes (50 minutes): [A1: Needfinding - Dino](https://docs.google.com/document/d/170otM-AH38uf5A3_LtiznRsTd_8buBoF-gMXoyBLzZ4/edit)
    -  Sheri’s interview notes (47 minutes): [A1: Needfinding - Sheri](https://docs.google.com/document/d/1O3Awv7jwsRzLFwJMR2wUyjO0jKBuOFi1O5osYhgW1IA/edit)


3. Interview Report
    1. Dino:
        - Dino: Dean, who likes to go by Dino, is a 61-year-old visually impaired individual who uses apps like Facebook for entertainment and communication and LinkedIn for business posts and forming connections. He critiques the inconsistency of labels on features across different social media apps. After sharing his screen, we looked at how he uses Facebook on his laptop in detail. We noticed there were at least 20-30 unlabeled buttons which were unreadable by his screen reader and navigating through the several features was hard. I was so surprised to see this. Dino noted “I would like to make sure that, like I was mentioning, that every element has an appropriate label, has the appropriate markup, that every region and heading is structured, structured in such a way that, you know, I can navigate it either by region or heading so I know exactly what area on the page I'm in because Facebook is broken up into several different regions and it can be tricky if things aren't labeled clearly”. I could tell he was frustrated with his screen reader when he said things like “Shut up, I already know you (JAWS screen reader) can’t read the buttons” and “Okay, so that'll ramble”. This made me think about making my app to have features arranged in a less complicated way to allow the screen reader to read everything easily.

        - He mostly uses Facebook to post his restaurant’s menu and participate in disability support groups, where he can "ask cooking questions" and share professional insights. However, he’s hesitant to engage more broadly, as he “does not trust strangers” and fears privacy breaches. By creating features that enable clear, controlled content visibility, my app could help users engage more freely without fear of oversharing or encountering untrust worthy individuals. Dino’s experience with Discord and Amazon and the CAPTCHA feature was a frustrating barrier, where the verification system blocked him from logging in. Dino’s suggestion to avoid inaccessible verification methods is important for my app's user onboarding and security. Integrating alternative verification systems—such as audio-based or haptic CAPTCHA would help my users. Therefore,  by incorporating privacy controls, accessible verification systems, and including alt text on images and audio descriptions on videos, my app can empower users like Dino to participate more fully in social media without frustrations. 
       
    2. Sheri: 
        - Sheri is a 53-year-old blind woman who makes sure to check up on her friends and family daily on Facebook. Despite being able to call her friends occasionally, she faces a lot of frustration with some of the app's key features which highlights some contradictions with Facebook’s accessibility features. For instance, she expressed irritation with Facebook Messenger, noting that "every time I click a message, the screen reader starts from the very first message in the chat," forcing her to scroll endlessly to find the most recent content. This made me think about how such small tasks can be extremely daunting when accessibility is not prioritized, that sighted users take for granted. With the help of a more streamlined screen reader support tool, this process can become much easier. I want to ensure that no user feels frustrated by basic functions on the app. Sheri's transition from sighted to blind also gave rise to some emotional tension in how she now interacts with social media. She fondly remembered playing games on Facebook when she had sight, but said, "I can’t play the games anymore (on Facebook), they’re not accessible." Sheri's experience with AI also surfaced in both humor and frustration. She shared a story about an AI tool in Messenger that incorrectly identified her black and white cat as a cow, joking, "I laughed—it was ridiculous, but kind of what I expected." While she found humor in the situation, it underscores the broader challenges of AI-driven tools for blind users. A lot of blind users use AI tools for image descriptions and there can be dangerous situations that can arise if not handled properly. Sheri also talked about her desire for a more personalized experience, even suggesting a simple filter to "only see close friends and family." This creates an opportunity for my app to provide customizable feed filters that allow users to prioritize posts from close friends and family.

        - Overall, Sheri’s insights have spurred many ideas to design an accessible social media app that caters to the needs of visually impaired users and is easy to use for elderly individuals in the community. Focusing on better screen reader navigation, accessible gaming/ entertainment options, feed filters, and more reliable AI description tools, I hope to provide an enjoyable experience to users like Sheri.


4. Design Opportunities
    - Streamlined Screen Reader Navigation- Develop a system that allows users to quickly access different sections of the app. This should include clear and consistent labeling of elements and logical grouping of content to prevent disorientation
    - Including labeled buttons, alt- text, and audio descriptions.
    - Content filters: Implement a feature that allows users to filter their feed based on preferences, such as prioritizing posts from close friends and family. 
    - AI Tools for image description: Integrate advanced AI tools that provide accurate and contextually relevant descriptions for images,
    - Accessible Games: Create or adapt games and interactive content to be fully accessible for blind users
    - Accessible  CAPTCHA: Develop CAPTCHA alternatives that are accessible to blind users, avoiding issues like those Dino faced with traditional CAPTCHA systems.
    - Accessible messaging for screen reader: Enhance the messaging experience by ensuring screen reader compatibility
    - Assistance feature: Implement a system that allows users to reach out to a network of volunteers or friends who are available to assist with tasks that may be challenging to complete independently. 


5. Acknowledgements:
I want to thank TAs Peilin and Sophia for helping me with my questions and being patient with me during office hours. I also used ChatGPT to help me generate some interview questions I could ask my participants. This was the prompt: " Please generate some interview questions I can ask participants with visual impairments who have used social media in the past and present. Make it in such a way which doesn't include biases, stereotypes, or any other offensive language to the community."