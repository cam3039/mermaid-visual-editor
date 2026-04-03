## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2025-02-14 - Accordion Accessibility and Conditional Rendering
**Learning:** React's conditional rendering (`{open && <div>}`) completely removes elements from the DOM. If a trigger button points to this element using `aria-controls`, the screen reader is left with a broken reference when closed, leading to a confusing accessibility experience.
**Action:** When building collapsible UI components like accordions, always keep the target container in the DOM and toggle its visibility using CSS (`display: open ? 'block' : 'none'`). This ensures `aria-controls` always points to a valid ID.
