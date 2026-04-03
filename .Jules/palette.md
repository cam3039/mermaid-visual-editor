## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-06-05 - Accordion Accessibility and Stable DOM IDs
**Learning:** Collapsible UI components (like Accordions) shouldn't use conditional React rendering (`{isOpen && <div/>}`) for their content if `aria-controls` is used. Removing the content element from the DOM breaks the ID reference, causing screen readers to point to a missing element.
**Action:** When building collapsible sections, always render the container and toggle its visibility using CSS `display: none` / `display: block`. Ensure the button has `aria-expanded`, `aria-controls` mapped to a unique ID (via `useId()`), and a clear keyboard focus state (`focus-visible:ring-2`).
