# 100Devs Interview Questions Bank (Behavioral / Technical)

- [Behavioral Questions](#behavioral-questions)
- [Technical Questions - HTML](#html)
- [Technical Questions - CSS](#css)
- [Technical Questions - JavaScript](#javascript)
- [Technical Questions - JS General](#javascript-general)
- [Technical Questions - Node](#node)
- [Technical Questions - CS Theory](#cs-theory)
- [Questions to ask your interviewer](#questions-to-ask-your-interviewer)
- [Whiteboard](#whiteboard)
- [Resources](#resources)

Any questions on this list are fair game for technical interviews. 
Resources with most answers at the end.

## Behavioral Questions

1. Give me an example of the project or initiative that you started on your own. It can be a non-business one. What prompted you to get started?
    - __Cause__: During bootcamp, I was active in the mental health channel, trying to support people who were struggling with trauma, depression or other obstacles while trying to work through course material & then job hunt.
    - __Action__: I created an LLC & to use as a web development company & brought on three people from bootcamp who had graduated & were on the job hunt.
    - __Result__: I built projects with them for clients & acted as a reference for them, helping them to gain professional experience & land better jobs at other companies.

1. Tell me about a time you had to work on several projects at once. How did you handle this?
    - __Cause__: At the EMR where I worked, I had to work on multiple projects all the time because we were a small company & had to get a lot done to stay competitive.
    - __Action__: I would prioritize projects to work on the most impactful tasks first. With those done, I'd then work on the rest by handling simpler projects first to make as much progress as I could in the shortest amount of time.
    - __Result__: I was able to hand off deliverables to where they were needed in a timely manner & push other projects ahead so that there was continual progress every day.

1. Describe a situation in which you felt you had not communicated well enough. What did you do? How did you handle it?
    - __Cause__: Early in my clinical design career, I shared specs for a pressure ulcer tracking tool with our clinical advisory panel which included technical specifications & data mappings with other parts of our system & other vendor applications that we integrated with. The technical details confused & worried the clinical advisors.
    - __Action__: After their confusion became clear, I revised my specs into two documents, one for the development team & another for clinicians which included real-world user scenarios that tied features to how nursing staff would use the tool.
    - __Result__: Feedback improved significantly, allowing the advisors to offer suggestions that improved my design & build a robust & easy-to-use tracking tool that made sense to nurses. I always made two versions of the design specs from that point on, one for the developers & another for clinicians.

1. Tell me about when you had to deal with conflict within your team. How was the conflict solved? How did you handle that? How would you deal with it now?
    - __Cause__: We were under a tight deadline to release changes to stay abreast with CMS updates & a developer pushed back when I sent late UI changes from our clinical advisory panel to the Body Diagram tool that I'd previously submitted & he was already building.
    - __Action__: I let him know that I understood that the timing was rough & asked to talk through the changes to see what could be done. We met for 30 mins & broke the updates down into "must-haves" and "next release" items so he could finish on time.
    - __Result__: We delivered the critical updates on time & the remaining items were added the next week. The experience taught me to really analyze user requests in smaller chunks to help support our dev team & ensure progress at a maintainable pace.

1. Give me an example of a time you had to take a creative and unusual approach to solve coding problem. How did this idea come to your mind? Why do you think it was unusual?
    - __Cause__: Clinical staff were frustrated by having to fully re-enter assessments every time one was needed, especially when there were only a few changes. Some tools had hundreds of fields, and re-inputting everything was time-consuming, leading to burnout and data entry errors.
    - __Action__: I proposed, designed & had to fight very hard for a new feature to amend assessments. It went against our founder's view of how assessments should be completed & I had to leverage our clinical review panel for backup.
    - __Result__: After months of development, the "Amendment" feature was added to clinical assessments & risk tools. It let users copy a previous assessment (within 90 days), preserving data that wouldn't change (chronic conditions, demographic info, historical notes, etc.) but NOT copying information for things that could change (vitals, cognition, wound status, etc.). Credentialed counter-signatures were necessary to finalize the forms. Clients LOVED it & it became the single most time-saving feature of the application.

1. Describe a situation in which you worked diligently on a project and it did not produce the desired results. Why didn't you get the desired results? What did you learn from the experience?
    - __Cause__: I redesigned the wound section of the skin assessment tool with a pain intensity slider for individual wounds. The design looked great but clinical advisory panel didn't care for it. The interface slowed them down when they needed to document quickly during their assessments.
    - __Action__: After speaking with them, I learned that they preferred simple drop-downs or checkboxes over a colorful slider with pain intensity faces & I redesigned that part of the interface with numbered checkboxes.
    - __Result__: We rolled out a simplified update with checkboxes that followed a 1-10 scale & didn't need typing. Pain assessment became faster & more precise with the specific scale degrees. I learned that for clinicians, speed & function were more important than flashy presentation.

1.  Give an example of an important project goal you reached and how you achieved it.
    - __Cause__: At the EMR, every April there are significant updates from CMS that affect the entire nursing home industry. We have to keep up with all of them to stay compliant & protect our client facilities.
    - __Action__: Every year, I stay on top of the updates, like changing from ICD-9 to ICD-10 & other major changes. I review proposals, monitor for updates & look for final versions & build along with all of them to give us as much lead time as possible so we can implement & test updates as they affect every part of our system. 
    - __Result__: We've never fallen behind with updates. Other EMRs have & it cost facilities money & increased their stress levels significantly. Some lost business because of the inability to stay current with federal regulations. Some of those facilities came to us, resulting in more clients & more business.

1. Describe a situation in which you experienced difficulty in getting others to accept your ideas? What was your approach? How did this work? Were you able to successfully persuade someone to see things your way
    - __Cause__: I found that there was no method to coordinate progress between clinicians & departments to complete federal MDS forms. Our founder didn't think this tool was necessary because clinicians should already know their workflows & MDS Coordinators should have systems in-place to manage & track needed data facility-wide.
    - __Action__: I leaned into what she had taught me about always keeping the viewer oriented during presentations, applying the thought to UX when using an application & to orienting the entire team to keep them on target.
    - __Result__: It made my proposal make sense to her & my team backed my idea up. I designed a highly-touted dashboard that became a key feature & selling point of our software.

1. Tell me about a situation when you were responsible for project planning. Did everything go according to your plan? If not, then why and what kind of counteractions did you have to take?
    - __Cause__: We were updating our EMR software to be able to automatically populate the federal MDS form using clinical data from assessments. I found that there was no method to coordinate progress between clinicians & departments.
    - __Action__: I read Information Dashboard Design by Stephen Few & designed a dashboard for our application, including planning & managing development for the whole system.
    - __Result__: It completely won over our clients, brought clarity to their workflows & became a centerpiece when demoing our system to potential new clients during presentations.

1. Tell me about a situation when you made a mistake at work. What happened exactly and how did you deal with it? What steps did you take to improve the situation?
    - __Cause__: When designing the MAR (Medication Administration Record) I defaulted the "administered by" field to the logged-in user, as is the norm for the other tools in our system. I didn't know that some facilities used laptops on rolling carts as shared bedside stations for multiple nurses which resulted in the wrong nurses being documented as administering meds to residents.
    - __Action__: A client reported that the wrong staff members were being logged for medication entries. I worked with development to add a warning modal when accessing the MAR to confirm that the nurse who was logged in was the nurse who administered meds.
    - __Result__: The fix was live within 24 hours & we didn't lose any clients, but it made me review other point-of-care tools to make sure that they were being used only by logged-in staff who were at the bedside.

1. Tell me about a time when you worked with someone who was not completing his or her share of the work. How did you handle the situation? Did you discuss your concern with your coworker? With your manager? If yes, how did your coworker respond to your concern? What was your manager's response?
    - __Cause__: We wanted to grow our development team at the EMR. The person we wanted to hire wasn't available to join us & recommended her son. We hired him & he didn't share his mother's work ethic or integrity or improve after being given many chances over 2 years.
    - __Action__: My team was demoralized by his lack of effort & his focus on entertainment but was afraid to upset his mother, a friend of our lead developer. I wasn't afraid. I explained the situation to our lead & our founder & learned they were aware but reluctant to sour the relationship between our lead & the new hire's mother.
    - __Result__: I convinced them to make the hard choice because we were being taken advantage of. The new hire's mother said she knew about his performance already. He was let go, morale improved & his mother respected our decision & remained friends with our lead.

1. Describe a situation when you worked effectively under pressure. How did you feel when working under pressure? What was going on, and how did you get through it?
    - __Cause__: We had a system crash, wiping out our main application server. After restoration, I found that the backups were also corrupted. This was crippling to our company & clients, with 3 months of data lost & potential litigation to both them & us. It was a nightmare for EVERYONE.
    - __Action__: I drove to downstate client facilities & collected paper copies of all of the lost data & had distant clients mail their data. I assembled a team of HIPAA-certified people to reinput the data & then I corrected dates & signatures in the database after determining the order in which to reinput all of the records based on MDS & assessment schedules.
    - __Result__: Over 6 weeks we restored all of the data & saved the company & our clients from lawsuits & hundreds of thousands of dollars of fines each. I also took over backups.

1. Tell me about yourself.
    - I'm a father of 2 girls, a foodie, I dabble in electric bass & I'm a huge fan of metal & a bunch of adjacent genres of music. For most of my career, I worked at an EMR company, designing clinical software for nursing homes. I began contributing code in 2019 after initially building parts of the interface using WYSIWYG tools. I don't get to dabble in my hobbies as much anymore, but I used to run tabletop RPG games, read a lot of fantasy, sci-fi, & horror, watched the same stuff & enjoyed learning about different aspects of art history, neuroscience, psychology & delving into global metal scenes (I'm friends with a lot of teachers, librarians & ethnomusicologists who focus on metal & write books & papers & make video documentaries). I like code, too.

1. Tell me about your experience at 100Devs. 
    - Its the best programmer community on the internet. It looks like a web development bootcamp from the outside, but once you join, you learn that its more of a jobs program that uses web development as a set of tools to help people gain employment at high-paying jobs for upward mobility. Its a form of activism for Leon Noel, the founder, & that ethos filters down to other members of the community. The community there is amazing. They're the most positive & supportive group I've ever met online. They're connected with all-stars in the programming world & they actively empower people to grow, better themselves & carry others up with them.

1. What do you know about our company?
    - __Cause__:
    - __Action__:
    - __Result__:

1. Why do you want to work for us?
    - __Cause__:
    - __Action__:
    - __Result__:

1. Why are you interested in this opportunity?
    - __Cause__:
    - __Action__:
    - __Result__:

1. Tell me about your dream job?  What do you really want to do with your career?
    - __Cause__:
    - __Action__:
    - __Result__:

1. Tell me a time when you failed.
    - __Cause__:
    - __Action__:
    - __Result__:

1. What do you read on a regular basis?
    - __Cause__:
    - __Action__:
    - __Result__:

1. What's some critical feedback you've gotten recently?
    - __Cause__:
    - __Action__:
    - __Result__:

1. Do you have any questions?
    - __Cause__:
    - __Action__:
    - __Result__:

## Technical Questions

### HTML

1. What does a doctype do?
1. How do you serve a page with content in multiple languages?
1. What kind of things must you be wary of when design or developing for multilingual sites?
1. What are data- attributes good for?
1. Consider HTML5 as an open web platform. What are the building blocks of HTML5?
1. Describe the difference between a cookie, sessionStorage and localStorage.
1. Describe the difference between \<script>, \<script async> and \<script defer>.
1. Why is it generally a good idea to position CSS \<link>s between \<head>\</head> and JS \<script>s just before \</body>? Do you know any exceptions?
1. What is progressive rendering?
1. Why you would use a srcset attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
1. Have you used different HTML templating languages before?

### CSS

1. What is CSS selector specificity and how does it work?
1. What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
1. Describe floats and how they work.
1. Describe z-index and how stacking context is formed.
1. Describe BFC (Block Formatting Context) and how it works.
1. What are the various clearing techniques and which is appropriate for what context?
1. Explain CSS sprites, and how you would implement them on a page or site.
1. How would you approach fixing browser-specific styling issues?
1. How do you serve your pages for feature-constrained browsers? What techniques/processes do you use?
1. What are the different ways to visually hide content (and make it available only for screen readers)?
1. Have you ever used a grid system, and if so, what do you prefer?
1. Have you used or implemented media queries or mobile specific layouts/CSS?
1. Are you familiar with styling SVG?
1. Can you give an example of an @media property other than screen?
1. What are some of the "gotchas" for writing efficient CSS?
1. What are the advantages/disadvantages of using CSS preprocessors?
1. Describe what you like and dislike about the CSS preprocessors you have used.
1. How would you implement a web design comp that uses non-standard fonts?
1. Explain how a browser determines what elements match a CSS selector.
1. Describe pseudo-elements and discuss what they are used for.
1. Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
1. What does * { box-sizing: border-box; } do? What are its advantages?
1. What is the CSS display property and can you give a few examples of its use?
1. What's the difference between inline and inline-block?
1. What's the difference between a relative, fixed, absolute and statically positioned element?
1. What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
1. Have you played around with the new CSS Flexbox or Grid specs?
1. Can you explain the difference between coding a web site to be responsive versus using a mobile-first strategy?
1. How is responsive design different from adaptive design?
1. Have you ever worked with retina graphics? If so, when and what techniques did you use?
1. Is there any reason you'd want to use translate() instead of absolute positioning, or vice-versa? And why?

### Javascript

1. Explain event delegation
1. Explain how this works in JavaScript
1. Explain how prototypal inheritance works
1. What do you think of AMD vs CommonJS?
1. Explain why the following doesn't work as an IIFE: function foo(){ }();. What needs to be changed to properly make it an IIFE?
1. What's the difference between a variable that is: null, undefined or undeclared? How would you go about checking for any of these states?
1. What is a closure, and how/why would you use one?
1. Can you describe the main difference between a .forEach loop and a .map() loop and why you would pick one versus the other?
1. What's a typical use case for anonymous functions?
1. How do you organize your code? (module pattern, classical inheritance?)
1. What's the difference between host objects and native objects?
1. Difference between: function Person(){}, var person = Person(), and var person = new Person()?
1. What's the difference between .call and .apply?
1. Explain Function.prototype.bind.
1. When would you use document.write()?
1. What's the difference between feature detection, feature inference, and using the UA string?
1. Explain Ajax in as much detail as possible.
1. What are the advantages and disadvantages of using Ajax?
1. Explain how JSONP works (and how it's not really Ajax).
1. Have you ever used JavaScript templating? If so, what libraries have you used?
1. Explain "hoisting".
1. Describe event bubbling.
1. What's the difference between an "attribute" and a "property"?
1. Why is extending built-in JavaScript objects not a good idea?
1. Difference between document load event and document DOMContentLoaded event?
1. What is the difference between == and ===?
1. Explain the same-origin policy with regards to JavaScript.
1. Make this work: duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
1. Why is it called a Ternary expression, what does the word "Ternary" indicate?
1. What is "use strict";? what are the advantages and disadvantages to using it?
1. Create a for loop that iterates up to 100 while outputting "fizz" at multiples of 3, "buzz" at multiples of 5 and "fizzbuzz" at multiples of 3 and 5
1. Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
1. Why would you use something like the load event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
1. Explain what a single page app is and how to make one SEO-friendly.
1. What is the extent of your experience with Promises and/or their polyfills?
1. What are the pros and cons of using Promises instead of callbacks?
1. What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
1. What tools and techniques do you use debugging JavaScript code?
1. What language constructions do you use for iterating over object properties and array items?
1. Explain the difference between mutable and immutable objects.
1. Explain the difference between synchronous and asynchronous functions.
1. What is event loop? What is the difference between call stack and task queue?
1. Explain the differences on the usage of foo between function foo() {} and var foo = function() {}
1. What are the differences between variables created using let, var or const?
1. What are the differences between ES6 class and ES5 function constructors?
1. Can you offer a use case for the new arrow => function syntax? How does this new syntax differ from other functions?
1. What advantage is there for using the arrow syntax for a method in a constructor?
1. What is the definition of a higher-order function?
1. Can you give an example for destructuring an object or an array?
1. ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?
1. Can you give an example of a curry function and why this syntax offers an advantage?
1. What are the benefits of using spread syntax and how is it different from rest syntax?
1. How can you share code between files?
1. Why you might want to create static class members?

### Javascript General

1. Can you name two programming paradigms important for JavaScript app developers?
1. What is functional programming?
1. What is the difference between classical inheritance and prototypal inheritance?
1. What are the pros and cons of functional programming vs object-oriented programming?
1. What are two-way data binding and one-way data flow, and how are they different?
1. What is asynchronous programming, and why is it important in JavaScript?

### Node

1. What is Node.js? Where can you use it?
1. Why use Node.js?
1. What are the features of Node.js?
1. How do you update NPM to a new version in Node.js?
1. Why is Node.js Single-threaded?
1. Explain callback in Node.js.
1. What is callback hell in Node.js?
1. How do you prevent/fix callback hell?
1. Explain the role of REPL in Node.js.
1. Name the types of API functions in Node.js.
1. What are the functionalities of NPM in Node.js?
1. What is the difference between Node.js and Ajax?
1. What are “streams” in Node.js? Explain the different types of streams present in Node.js.
1. Explain chaining in Node.js.
1. What are Globals in Node.js?
1. What is Event-driven programming?
1. What is Event loop in Node.js work? And How does it work?
1. What is the purpose of module.exports in Node.js?
1. What is the difference between Asynchronous and Non-blocking?
1. What is Tracing in Node.js?
1. How will you debug an application in Node.js?
1. Difference between setImmediate() vs setTimeout()?
1. What is process.nextTick()
1. What is package.json? What is it used for?
1. What is libuv?
1. What are some of the most popular modules of Node.js?
1. What is EventEmitter in Node.js?

### CS Theory 

1. What is recursion and give an example using javascript?
1. What are types?
1. What are data structures?
1. What is an algorithm? 
1. What is scope / lexical scope in javascript? 
1. What is polymorphism?
1. What is encapsulation? 
1. What is a Linked List
1. What is a Doubly Linked List
1. What is a Queue
1. What is a Stack
1. What is a Hash Table
1. What is a Heap
1. What is a Trie
1. What is a Tree
1. What is a Binary Search Tree
1. What is a Disjoint Set
1. What is a Bloom Filter
1. Demonstrate Bubble Sort and explain when you might use it?
1. Demonstrate Insertion Sort and explain when you might use it?
1. Demonstrate Merge Sort and explain when you might use it?
1. Demonstrate Quicksort and explain when you might use it?

### Questions to ask your interviewer

1. How does Bob’s Burgers measure the success of their engineers?
1. What challenges can an engineer come across working at Bob’s Burgers?
1. Can you explain "thing you read on their engineering blog" and how it affects Bob’s Burgers Engineers?
1. What traits in an engineer are hard to find in an engineer that Bob’s Burgers would like to have?
1. How is critique given to engineers at Bob’s Burgers?
1. Do you have any questions or concerns about my qualifications?

Helpful list of other reverse interview questions: https://github.com/viraptor/reverse-interview

### Whiteboard

Expected to solve, determine edge cases, and explain complexity 
- Every project assigned
- Every coding challenge (codewars ect...) you have solved / pushed to github

### Resources:

- [Eloquent JavaScript](https://eloquentjavascript.net/)
- [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS)
- [Front-End Interview Handbook](https://github.com/yangshun/front-end-interview-handbook)
- [Medium: 10 Interview Questions Every JS Developer Should Know](https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95)
- [SimpliLearn: Node.JS Interview Questions and Answers](https://www.simplilearn.com/node-js-interview-questions-and-answers-article)
- [Medium: Frequently Asked Node.JS Interview Questions and Answers](https://medium.com/@vigowebs/frequently-asked-node-js-interview-questions-and-answers-b74fa1f20678)
