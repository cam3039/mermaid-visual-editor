## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-05-25 - Accordion Accessibility and Persistent DOM presence
**Learning:** Collapsible accordion components need persistent DOM presence for screen readers so that `aria-controls` references remain valid when the accordion is collapsed. Conditional rendering `{open && <div>}` removes the element from the DOM entirely.
**Action:** When building collapsible UI components, always render the container and toggle its CSS `display` property (`display: open ? 'block' : 'none'`). Always include `aria-expanded`, `aria-controls` linked to a unique ID (via `useId()`), and visible keyboard focus states (`focus-visible:ring-2`).
