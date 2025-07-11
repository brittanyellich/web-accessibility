---
theme: apple-basic
title: Accessible by Design
info: |
  Web Accessibility Essentials for Developers
drawings:
  persist: false
mdc: true
layout: intro
---

# Accessible by Design

Web accessibility essentials for developers

<div class="absolute bottom-10">
  <p class="font-700">
    Brittany Ellich, GitHub | <a href="https://brittanyellich.com" target="_blank">brittanyellich.com</a>
  </p>
  <a href="https://github.com/brittanyellich/web-accessibility" target="_blank">
    <carbon:logo-github /> brittanyellich/web-accessibility
  </a>
</div>

<!--
Getting started.
Welcome.
Check out the slides at the repo link.

Welcome to my talk: Accessible by Design - Web accessibility essentials for developers

-->

---
transition: slide-left
layout: image-right
image: 'images/alttext.png'
---

# About me

- Senior software engineer at GitHub
- Speaker, educator, advocate for developers
- Newsletter, podcast, and blog posts
- Amateur meme creator

<!--
Hello my name is Brittany Ellich - Software engineer at GitHub, speaker, and educator helping developers build better software, stronger careers, and a more inclusive tech industry.

Disclaimer: 
I’m not an expert. 
These are my own thoughts, opinions, and learnings, and don’t reflect the opinions of my employer
GitHub does care a lot about accessibility, though! - https://accessibility.github.com/

Meme: Usefulness of alt text (ironic because this image has no alt text) - make it descriptive but not a novel
-->

---
transition: slide-left
---

# What we're going to talk about

- Understanding web accessibility
- Common barriers and how users may experience the web
- Techniques for developers to improve accessibility
- Accessibility testing
- Demo

<!--
Here's what we're going to talk about today

I hate when people do talks with a lot of theory and don't explain "okay but how do you do this in real life", so there's quite a bit of practical "how to do this" information in here
-->

---
layout: section
---

# Objectives

1. Convince you that accessibility should be one of your key skillset investments

2. Give you the tools to get started making the web a more accessible place

<!--
You have lots of “ilities” (readability, scalability, maintainability, availability, etc). Software engineering is a field of tradeoffs. Accessibility should be one of them!
-->

---
layout: section
---

# Understanding web accessibility

---
layout: default
---

# What is accessibility?

<!--
What do YOU think it is?
-->

---
layout: default
---

# What is accessibility?

“The inclusive practice of ensuring there are <bold>no barrier</bold>> that prevent interaction with, or access to, websites online by people with physical disabilities, situational disabilities, and socio-economic restrictions on bandwidth and speed.”

<!--
A lot of people think of the physical disabilities

Situational disabilities (I’m driving a car so can’t read something, or holding a baby, or cooking, etc)

Restrictions on bandwidth and speed - Having a giant javascript bundle that has to be loaded will create a barrier to information
-->

---
layout: default
---

# Anne Gibson - An Alphabet of Accessibility Issues

A is blind, and has been since birth. He’s always used a screen reader, and always used a computer. He’s a programmer, and he’s <a href="http://blog.austinseraphin.com/2010/06/12/my-first-week-with-the-iphone/" target="_blank">better prepared to use the web</a> than most of the others on this list.

B fell down a hill while running to close his car windows in the rain, and <a href="http://www.nhs.uk/conditions/broken-finger/Pages/Introduction.aspx" target="_blank">fractured multiple fingers</a>. He’s trying to surf the web with his left hand and the keyboard.

C has a blood cancer. She’s been on chemo for a few months and, despite being an MD, is finding it harder and harder to remember things, read, or have a conversation. It’s called <a href="http://www.cancer.org/treatment/treatmentsandsideeffects/physicalsideeffects/chemotherapyeffects/chemo-brain" target="_blank">chemo brain</a>. She’s frustrated because she’s becoming more and more reliant on her smart phone for taking notes and keeping track of things at the same time that it’s getting harder and harder for her to use.

D is <a href="http://en.m.wikipedia.org/wiki/Color_blindness" target="_blank">color blind</a>. Most websites think of him, but most people making PowerPoint presentations or charts and graphs at work do not.


<!--
Anne Gibson article: An Alphabet of Accessibility Issues
-->

---
transition: slide-left
layout: image-right
image: 'images/a11y.png'
---

# What is accessibility?

<!--
Accessibility -> A11y , 11 letters between the A and the y
(Not to be confused with ally)
-->

---
layout: default
---

# What is accessibility?

The absence of barriers to information.

---
layout: default
---

# What is accessibility?

Accessibility is <bold>good design</bold>. 
Making a website more accessible makes it more usable for <bold>every user</bold>.

<!--
Some users have preferences for accessibility features (ex. Reduced motion)

Some accessibility features become widely used (ex. Background on blur)
-->

---
layout: default
---

# Reasons to learn about accessibility

- Make your website available to everyone
- Expand your app’s potential audience
- Be more competitive in the job market
- Legal (you probably have legal obligations, but I am not a lawyer)
- Moral and ethical reasons to do so


<!--
Relevant to both frontend and backend engineers - You're likely your websites biggest user, you have influence!

Legal
If you’re just trying to meet regulations, you’re already behind
The number of ADA Title 3 cases in the US are filed at 1 per hour

Morally/ethically
It is your responsibility as a steward of access to information on the internet to do this and do it correctly
The law makes this a basic human right to not be discriminated against, and access to information is a requirement for equal access to society


AI Caveat: This is particularly important in the days of AI where our job is moving from writing software to reviewing it

-->

---
layout: default
---

# Impact of inaccessibile websites on users

- 1.3 billion people globally have disabilities (15-25%)
- 75% of Americans with disabilities use the internet daily
- Over 96% of the top one million web pages had accessibility issues in 2023
- In 2022, US courts saw over 4,060 web accessibility cases


Source: https://themeisle.com/blog/web-accessibility-statistics/#gref


<!--

-->

---
layout: default
---

# Impact of inaccessibile websites on users

- 1 out of 4 people have a disability, but 4 out of 4 have an access need
- There is a trap when you are just considering ROI from users with a disability, when accessibility improves access for all users



<!--

-->

---
layout: default
---

# Impact of inaccessibile websites on users

- 1 out of 4 people have a disability, but 4 out of 4 have an access need
- There is a trap when you are just considering ROI from users with a disability, when accessibility improves access for all users



<!--

-->

---
layout: default
---

# Key Principles - <a href="https://www.w3.org/TR/WCAG22/" target="_blank">WCAG 2.2</a>

Web Content Accessibility Guidelines 2.2 - recommendations for making web content more accessible

- Perceivable: Making content accessible to all senses
- Operable: Navigable and usable by all users
- Understandable: Clear and intuitive design and content
- Robust: Compatibility and future-proofing


<!--
Perceivable: Information and user interface components must be presentable to users in ways they can perceive. Text alternatives to non-text content, distinguishable (colors)

Operable: User interface components and navigation must be operable. Keyboard accessible, enough time, navigable, etc

Understandable: Information and the operation of the user interface must be understandable. Readable, Predictable

Robust: Content must be robust enough that it can be interpreted by a wide variety of user agents, including assistive technologies.

-->

---
layout: default
---

# Accessibility standards are ever-evolving

- No one really has it “all figured out”
- Once you’re “accessible”, it doesn’t mean you will be accessible forever

<!--

-->

---
layout: section
---

# Common barriers and how users may experience the web

---
layout: default
---

# Low vision

- Screen readers
- Braille readers
- High contrast mode
- Zoom and screen magnification

<!--

-->

---
layout: default
---

# Motor and mobility impairments

- Keyboard-only navigation
- Mouse-only navigation
- Switches
- Mouth sticks
- Eye-tracking software
- Voice dictation software

<!--

-->

---
layout: default
---

# Cognitive and neurological disabilities

- Predictable page structure and design
- Consistency
- Reading level
- Supplemental diagrams/imagery
- Reduce animation motion


<!--

-->

---
layout: default
---

# Hearing impairments

- Captions
- Sign language
- Transcripts

<!--

-->

---
layout: section
---

# Techniques for developers to improve accessibility

---
layout: default
---

# How to do it

- An internal and external policy on accessibility
- For re-designs: Involve accessibility early in the design process
- For ongoing work: Work it into existing bug fixes/updates
  - Use accessibility linting and accessibility in tests
- Use design systems
- Design for all devices
- <a href="https://github.blog/2024-05-01-empowering-accessibility-githubs-journey-building-an-in-house-champions-program/" target="_blank">Accessibility Champions at GitHub</a>

<!--
Policy: A north star to guide your organization

Designers: Links made to be buttons and buttons made to be links

Design Systems: Ex labels. You no longer have to worry about adding a label on each input component because the design system does it for you.

-->

---
layout: default
---

# Use Semantic HTML

```html
  <button onclick=”doTheThing()”>
    Click Me!
  </button>
```

VS. 

```html
  <div role=”button” aria-pressed=”false” tabindex=”0” class=”btn”>
    Click Me!
  </div>
```

```js
  btn.addEventListener(“keydown”, e => (
    If (e.key === “ “ || e.key === “Enter” || e.key === “Spacebar”) {
      doTheThing();
    }
  );
```

<!--
Much longer to develop, easier to get wrong

I'm going to go through a bunch of high-level things to consider with semantic HTML. Get the slides online and save them for later :) 
-->

---
layout: default
---

# Use Semantic HTML

```html
  <!DOCTYPE html>
  <html lang=”en”>
    <head>
      <meta charset utf-8>
      <title>My Cool Site</title>
    </head>

```


- There should be a DOCTYPE on the page
- `<html>` tag with the lang set (en for english)
- Make sure the head has a meta charset, like utf-8
- There should be a page title, and it should be unique to other pages and descriptive of the page contents



<!--

-->

---
layout: default
---

# Semantic HTML - Landmarks


```html
  <header></header>
  <nav></nav>
  <main></main>
  <aside></aside>
  <footer></footer>
```


- Headers, navs, main, footer, aside
- There should always be a main landmark


<!--

-->

---
layout: default
---

# Semantic HTML - Navigation

- This is boring to listen to and at the top of every page
- Let screen reader and keyboard users skip it

<!--

-->

---
layout: default
---

# Semantic HTML - Headings



```html
  <h1>Title</h1>
  <h2>Subtitle 1</h2>
  <h3>Key Point 1</h3>
  <h3>Key Point 2</h3>
  <h2>Subtitle 2</h2>
  <h3>Key Point 1</h3>
  <h3>Key Point 2</h3>
```


- h1 through h6
- Only one h1 on the page (should match the page title)
- Headings are one of the ways a screen reader user can skim across a page
- Heading levels should be in descending order
- Don’t use specific heading levels for styling

<!--
Don’t use headings to style text. HTML is used to describe the content and CSS is used to style it.
-->

---
layout: default
---

# Semantic HTML - Buttons and Links

- Button vs. Link
  - Button - For Actions
  - Link - For navigation or change of context
- Links
  - Should have enough text to understand what it is for
  - Accessibility properties in Google Chrome shows calculated accessible names for each link
  - Navigation links should always be in the same order on every page
  - Links without text should have an accessible name (also useful for SEO)


<!--
This is very common to get wrong
-->

---
layout: default
---

# Semantic HTML - Images

```html
  <img src=”img_dog.jpg” alt=”A blue heeler dog”>
```

- Avoid text in images (use an alt tag if needed)
- Alt attribute
  - Descriptive
  - Don’t need to say “an image of”
  - Accessibility chrome devtool 
  - Don’t duplicate the caption and alt text
  - If the image is just there for vibes, describe the vibes!
- Graphs and diagrams should have a description of the content and what they are trying to convey

<!--
Try to make unbiased descriptions of Graphs :) It's hard
-->

---
layout: default
---

# Semantic HTML - Lists

- Use ordered lists and unordered lists where appropriate
- Any list of more than three items should be a list

<!--
-->

---
layout: default
---

# Semantic HTML - Tables


```html
  <table>
  <tr>
    <th></th>
    <th scope=”col”>City</th>
    <th scope=”col”>State</th>
  </tr>
  <tr>
    <td>Portland</td>
    <td>Oregon</td>
  </tr>
</table>
```

- Only used for tabular data
- Should be implemented properly with heading tags, scopes (col vs. row)
- Should have a summary with a description of the data within


<!--
Scope specifies whether a header cell is a header for a column, row, or group of columns or rows

-->

---
layout: default
---

# Semantic HTML - Forms


- Lots of pitfalls
- Use types on inputs (i.e., email)
- All fields should have a label
- Communicate which elements are required
- Use disabled tags on any input that is disabled
- Be as explicit as possible about errors



<!--

-->

---
layout: default
---

# Semantic HTML - Text

- Use rems for text - allows for better changes in text size
- Text copy:
  - Keep it understandable
  - Think about reading level - <a href="https://hemingwayapp.com" target="_blank">hemingwayapp.com</a>
  - Avoid technical jargon and acronyms

<!--
Technical jargon: Every website for every framework and library ever throwing around words like “unopinionated” and “verbose”. Just describe things in terms that area easy to pick up.
-->

---
layout: section
---

# Accessibility testing

---
layout: default
---

# Automated testing

- Good first step! But will only catch around 30% of accessibility bugs
- HTML Validation
- WAVE - Web Accessibility Evaluation Tool by WebAIM
- AXE by Deque
- JS Testing/Linters


<!--

-->

---
layout: default
---

# HTML Validation

- Checks for low-hanging fruit
- https://validator.w3.org/nu

<!--

-->

---
layout: default
---

# WAVE - Web Accessibility Evaluation Tool by WebAIM

- Contrast checker and other tools based on WCAG
- Chrome extension


<!--

-->

---
layout: default
---

# AXE by Deque

- Chrome extension, adds the axe tab to your devtools
- https://www.deque.com/axe/devtools/

<!--

-->

---
layout: default
---

# JS testing/Linters

- eslint-plugin-jsx-a11y
- Axe-core: Library to write tests with axe


<!--

-->

---
layout: default
---

# Manual testing

- Screen readers
- Keyboard
- Mouse/Touch
- Timing
- Visual
- Media
- Semantics

<!--
This is the most important testing to do
-->

---
layout: default
---

# Manual testing - Screen readers

- Available screen readers
  - macOS and iOS - VoiceOver
  - Windows - NVDA
  - Android - Talkback
- Screen readers can:
  - Read all text visible on a page
  - Read some tags that a sighted user won’t see, like ARIA tags
  - List all headers and links
- [Deque Screen Reader Shortcuts](https://dequeuniversity.com/screenreaders/)


<!--
Get comfy with using a screen reader
-->

---
layout: default
---

# Manual testing - Screen readers - What to test

- All information is read
- Visual elements are read
- State and content changes are read
- Everything can be navigated to
- Your page has a logical flow from top to bottom

<!--

-->

---
layout: default
---

# Manual testing - Keyboard navigation - What to test

- Use the ‘tab’ key
- Make sure you can navigate to each feature
- Make sure you know where the focus is 
  - Type `document.activeElement` in the javascript console if you need to see what is currently focused
- Make sure you don’t get trapped anywhere (radio buttons/checkboxes)
- Make sure that the keyboard interaction makes sense


<!--

-->

---
layout: default
---

# Manual testing - Mouse/Touch - What to test

- Action on release, not on a “down-event”
- Abort or undo a click when navigating off of it

<!--

-->

---
layout: default
---

# Manual testing - Timing - What to test

- Users should have plenty of time
- If there’s a time limit, users should be able to turn it off, adjust it, or extend it


<!--

-->

---
layout: default
---

# Manual testing - Visual - What to test

- Color contrast is acceptable
- Color alone doesn’t convey information
- Feature is usable when zooming
- All screen sizes are tested
- Visible in portrait and landscape mode

<!--

-->

---
layout: default
---

# Manual testing - Media - What to test

- Images have alt text
- Videos/audio has transcripts
- Videos have captions
- Videos/audio shouldn’t automatically start playing


<!--

-->

---
layout: section
---

# Demo

https://github.com/brittanyellich/web-accessibility/blob/main/testing-checklist.md

<!--
I didn't even have to create a demo for this
-->

---
layout: image
image: '/images/color-game.png'
---


<!--
https://projects.brittanyellich.com/color-game
-->

---
layout: image-right
image: '/images/html-validation.png'
---

# HTML Validation

- Clean up trailing slash warnings, but nothing terrible

<!--
https://projects.brittanyellich.com/color-game
-->

---
layout: image-right
image: '/images/axe-scan.png'
---

# Axe Devtools Scan

- Color contrast (on completed game)
- Links must have discernible text (search icon)

<!--
https://projects.brittanyellich.com/color-game
-->

---
layout: image-right
image: '/images/voiceover.png'
---

# Screen reader test

- VoiceOver has no idea what’s going on

<!--
https://projects.brittanyellich.com/color-game
-->

---
layout: default
---

# Keyboard test

- Can’t navigate to the game elements at all

<!--
https://projects.brittanyellich.com/color-game
-->

---
layout: default
---

# Mouse/touch testing

- Seems good! Action on release instead of down click
- Action cancels when I navigate off before releasing


<!--
https://projects.brittanyellich.com/color-game
-->

---
layout: default
---

# Timing

- No timing elements to speak of

<!--
https://projects.brittanyellich.com/color-game
-->

---
layout: default
---

# Visual

- Color contrast is acceptable 
- Color alone isn’t used to convey information
- Feature is usable when zooming
- All screen sizes are tested
- Visible in portrait and landscape mode

😬

<!--
https://projects.brittanyellich.com/color-game
-->

---
layout: default
---

# Semantic HTML Check

- HTML Overview (doctype, html tag, language, charset, title)
- Landmarks (main landmark, landmarks are used where they make sense)
- Navigation (skip link if navigation is lengthy)
- Headings are used correctly
- Buttons and links are used correctly
- Lists are used where needed
- Tables are used for tabular data and have proper scopes and a summary
- Forms are correct (types on inputs, all fields have a label, required fields communicated, errors are explicit)
- Text copy is understandable and free of technical jargon and acronyms


<!--

-->

---
layout: default
---

# Issues

- Clean up trailing slash warnings
- Remove or fix search icon
- [Create skip link for navigation](https://css-tricks.com/how-to-create-a-skip-to-content-link/)
- Add h1 to match title
- Explain what RGB is and what the goal of the game is for users
- Fix color contrast on page title
- Make colors keyboard navigable and selectable by screen reader
- [Add alternate tag for what the color may be called for low vision users](https://stackoverflow.com/questions/69141635/how-to-convert-rgb-color-to-color-name-string-in-javascript)



<!--

-->

---
layout: default
---

# Issues

## TODO at a later date:

- Clean up trailing slash warnings
- Remove or fix search icon
- [Create skip link for navigation](https://css-tricks.com/how-to-create-a-skip-to-content-link/)

## Part of demo:

- Add h1 to match title
- Explain what RGB is and what the goal of the game is for users
- Fix color contrast on page title
- Make colors keyboard navigable and selectable by screen reader
- [Add alternate tag for what the color may be called for low vision users](https://stackoverflow.com/questions/69141635/how-to-convert-rgb-color-to-color-name-string-in-javascript)

<!--

-->

---
layout: default
---

# Add h1 to match the title

```html
  <div className="color-game__title">
    <div className="color-game__title-text">THE GR
EAT</div>
    <div className="color-game__title-color-text">
      RGB({colors[correctIndex][0]}, {colors[correctIndex][1]},{" "}
      {colors[correctIndex][2]})
    </div>
    <div className="color-game__title-text">COLOR GAME</div>
  </div>
```

TO. 

```html
  <h1 className="color-game__title">The Great RGB Color Game</h1>
  <h2 className="color-game__title-color-text">RGB({colors[correctIndex][0]}, {colors[correctIndex][1]},{" "}
      {colors[correctIndex][2]})</h2>
```

<!--

-->

---
layout: default
---

# Explain what RGB is and the goal of the game

```html
  <p>RGB (Red, Green, Blue) is a color model used to create a vast variety of colors
       by combining red, green, and blue (the three primary colors of light) together to
       create a large variety of colors. The goal of this game is to take the RGB value
       below and guess which of the color block options corresponds to the value. Each
       RGB value can be between 0 and 255. As a hint, the larger the number, the more of
       that value is present. <a href="https://en.wikipedia.org/wiki/RGB_color_model">Learn more about RGB values here!</a></p>
```

<!--
Hemingwayapp: Grade 2
Note the link text!
-->

---
layout: default
---

# Fix color contrast

```css
/* Move style tag to color-game__play-area div
# Add the following CSS to color-game__play-area: */

   padding: 16px;
   border-radius: 16px;
   margin-bottom: 32px;
```

<!--

-->

---
layout: default
---

# Make color blocks keyboard navigable

```css
// Turn the divs into buttons
// Add the following styles to the buttons:
.dark {
 .color-game-block-accessible {
   border: 4px solid #a9a9b3;
 }
}
.light {
 .color-game-block-accessible {
   border: 4px solid #161209;
 }
}
```

<!--

-->

---
layout: default
---

# Add name for each color 


```css
/* Add name that color.js: https://chir.ag/projects/ntc/
 Compute hex value for each color
 Add Color type
 Add styles for button text: */
       color: "white",
       fontWeight: "bold",
       fontSize: "1.5rem",

```

<!--

-->

---
layout: default
---

# Issues

## TODO at a later date:

- Clean up trailing slash warnings
- Remove or fix search icon
- [Create skip link for navigation](https://css-tricks.com/how-to-create-a-skip-to-content-link/)

## Part of demo:

- Add h1 to match title
- Explain what RGB is and what the goal of the game is for users
- Fix color contrast on page title
- Make colors keyboard navigable and selectable by screen reader
- [Add alternate tag for what the color may be called for low vision users](https://stackoverflow.com/questions/69141635/how-to-convert-rgb-color-to-color-name-string-in-javascript)

<!--

-->

---
layout: section
---

# Objectives

1. Convince you that accessibility should be one of your key skillset investments

2. Give you the tools to get started making the web a more accessible place

<!--
Are you convinced?
Did you learn something new?
-->

---
layout: default
---

# Visual

- [https://github.com/brittanyellich/web-accessibility](https://github.com/brittanyellich/web-accessibility)
- [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
- [Deque screen reader shortcuts](https://dequeuniversity.com/screenreaders/)
- [Hemingway app for writing text and assessing reading level](https://hemingwayapp.com/)
- [An Alphabet of Accessibility Issues](https://www.linkedin.com/pulse/alphabet-accessibility-issues-anne-gibson-parimala-hariprasad/)
- [Global Accessibility Awareness Day May 16th](https://accessibility.day/)

## Thank you!

My website is [brittanyellich.com](https://brittanyellich.com), let's be internet friends!

<a href="https://github.com/brittanyellich" target="_blank">
    <carbon:logo-github />
</a>

<a href="https://www.linkedin.com/in/brittanyellich/" target="_blank">
    <carbon:logo-linkedin />
</a>

<!--

-->