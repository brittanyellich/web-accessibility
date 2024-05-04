# Techniques for Developers

## Overview

- Have an internal and external policy on accessibility if you don't already have one. This will be a north star to guide your organization.
- For re-designs and new products: Consider accessibility early in the design process
- For ongoing work: Work it into existing bug fixes/updates/the pull request process
  - Use accessibility linting and accessibility tests
- Use design systems! Solve your accessibility issues once and then reuse the same components everywhere
- Design for all devices, in portrait and landscape mode

## Semantic HTML

- Use the HTML tags like they’re meant to be used
- An accessibility tree is built when a web page loads which can be used by assistive technologies to convey information to the user
- Deviating from semantic HTML, for example using `<div>`s for everything, misses a lot of built-in functionality of semantic HTML elements
  - Roles
  - Focus
  - Names
  - Interactivity (onclick, onblur, etc)

```html
<button onclick="doTheThing()">
  Click Me!
</button>
```

vs.

```html
<div role="button" aria-pressed="false" tabindex="0" class="btn">
  Click Me!
</div>
```

```javascript
btn.addEventListener("keydown", e=> (
    if(e.key === "" || e.key === "Enter" || e.key === "Spacebar") {
        doTheThing();
    }
));

// focus, mousedown events, etc
```

### Semantic HTML Overview

- There should be a DOCTYPE on the page
- `<html>` tag with the lang set (en for english)
- Make sure the head has a meta charset, like utf-8
- There should be a page title, and it should be unique to other pages and descriptive of the page contents

```html
<!DOCTYPE html>
<html lang=”en”>
<head>
<meta charset utf-8>
<title>My Cool Site</title>
</head>
</html>
```

### Semantic HTML Landmarks

- Headers, navs, main, footer, aside
- There should always be a main landmark

```html
<header></header>
<nav></nav>
<main></main>
<aside></aside>
<footer></footer>
```

### Semantic HTML Navigation

- This is boring to listen to and at the top of every page
- Let users skip it

### Semantic HTML Headings

- h1 through h6
- Only one h1 on the page (should match the page title)
- Headings are one of the ways a screen reader user can skim across a page
- Heading levels should be in descending order
- Don’t use specific heading levels for styling

```html
<h1>Title</h1>
<h2>Subtitle 1</h2>
<h3>Key Point 1</h3>
<h3>Key Point 2</h3>
<h2>Subtitle 2</h2>
<h3>Key Point 1</h3>
<h3>Key Point 2</h3>
```

### Semantic HTML Buttons and Links

- Button vs. Link
  - Button - For Actions
  - Link - For navigation or change of context
- Links
  - Should have enough text to understand what it is for
  - Accessibility properties in Google Chrome shows calculated accessible names for each link
  - Navigation links should always be in the same order on every page
  - Links without text should have an accessible name (also useful for SEO)

### Semantic HTML Images

- Avoid text in images (use an alt tag if needed)
- Alt attribute
  - Descriptive
  - Don’t need to say “an image of”
  - Don’t duplicate the caption and alt text
  - If the image is just there for vibes, describe the vibes!
- Graphs and diagrams should have a description of the content and what they are trying to convey

```html
<img src=”img_dog.jpg” alt=”A blue heeler dog”>
```

### Semantic HTML Lists

- Use ordered lists and unordered lists where appropriate
- Any list of more than three items should be a list

### Semantic HTML Tables

- Only used for tabular data
- Should be implemented properly with heading tags, scopes (col vs. row)
- Should have a summary with a description of the data within

```html
<table>
  <tr>
    <th></th>
    <th scope=”col”>City</th>
    <th scope=”col”>State</th>
  </tr>
  <tr>
    <td>Boise</td>
    <td>Idaho</td>
  </tr>
</table>
```

### Semantic HTML Forms

- Lots of pitfalls
- Use types on inputs (i.e., email)
- All fields should have a label
- Communicate which elements are required
- Use disabled tags on any input that is disabled
- Be as explicit as possible about errors

### Semantic HTML Text

- Use rems for text - allows for better changes in text size
- Text copy:
  - Keep it understandable
  - Think about reading level - hemingwayapp.com
  - Avoid technical jargon and acronyms
