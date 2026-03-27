## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.
## 2026-03-27 - Accordion Accessibility (ARIA & Focus)
**Learning:** Collapsible accordion sections require static content containers with `id`s linked to `aria-controls` on the toggle button. Conditionally rendering the DOM node (e.g., `{open && <div>}`) breaks the `aria-controls` reference for screen readers when closed. They also need `aria-expanded` and visible focus states (`focus-visible:ring-2`).
**Action:** When building collapsible UI, always render the content container but toggle its `display` (e.g., `display: open ? 'block' : 'none'`), use `useId()` to link the toggle and content, and apply `focus-visible` classes.
