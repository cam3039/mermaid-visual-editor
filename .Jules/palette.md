## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.
## 2026-04-01 - Component Accessibility: Accordion Sections
**Learning:** Found an accessibility issue with the accordion toggle button where it lacks `aria-expanded` and `aria-controls` attributes. The content wrapper is also conditionally rendered (`{open && <div>}`), which breaks `aria-controls` functionality when closed.
**Action:** Always ensure accordion sections have an `aria-expanded={open}` attribute on their control buttons, an `aria-controls` tied to a unique ID for the content panel, and toggle the `display` property rather than conditionally rendering the component.
