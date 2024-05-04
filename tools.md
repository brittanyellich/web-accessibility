# Tools for Accessibility Testing

[Accessibility Testing Checklist](./testing-checklist.md)

## Automated Testing

- Good first step! But will only catch around 30% of accessibility bugs
- HTML Validation
  - Checks for low-hanging fruit
  - [HTML Validator](https://validator.w3.org/nu)
- WAVE - Web Accessibility Evaluation Tool by WebAIM
  - Contrast checker and other tools based on WCAG
  - Chrome extension
- AXE by Deque
  - Chrome extension, adds the axe tab to your devtools
  - [Check it out here](https://www.deque.com/axe/devtools/)
- JS Testing/Linters
  - eslint-plugin-jsx-a11y
  - Axe-core: Library to write tests with axe

## Manual Testing

- Screen readers
  - Available screen readers
    - macOS and iOS - VoiceOver
    - Windows - NVDA
    - Android - Talkback
  - Screen readers can:
    - Read all text visible on page
    - Read tags that a sighted user wouldn't see, like ARIA
    - List all headers and links
  - What to test:
    - All information is read
    - Visual elements are read
    - State and content changes are read
    - Everything can be navigated to
    - Your page has a logical flow from top to bottom
- Keyboard
  - Use the 'tab' key
  - Make sure you can navigate to each feature
  - Make sure you know where the focus is
    - Type `document.activeElement` in the javascript console if you need to see what is currently focused
  - Make sure you don't get trapped anywhere (radio buttons/checkboxes)
  - Make sure that the keyboard interaction makes sense
- Mouse/Touch
  - Action on release, not on a "down event" (so it can be cancelled)
  - Abort or undo a click by navigating off of it
- Timing
  - Users should have plenty of time
  - If there's a time limit, users should be able to turn it off, adjust it, or extend it
- Visual
  - Color contrast is acceptable
  - Color alone doesn't convey information
  - Feature is usable when zooming
  - All screen sizes are tested
  - Visible in portrait and landscape mode
- Media
  - Images have alt text
  - Videos/audio have transcripts
  - Videos have captions
  - Videos/audio shouldn't automatically start playing
- Semantics
  - See [Semantic HTML](./techniques-for-developers.md#semantic-html)
