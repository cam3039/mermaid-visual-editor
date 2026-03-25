## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-05-25 - Collapsible UI Accessibility (Accordion)
**Learning:** The `AccordionSection` component in the Inspector Panel was acting as a collapsible UI but lacked proper ARIA attributes and visible focus states for keyboard users.
**Action:** When building or modifying collapsible UI components, ensure accessibility by including `aria-expanded`, `aria-controls` linked to a unique ID (via `useId()`), a descriptive `aria-label`, hiding decorative icons with `aria-hidden="true"`, and adding visible keyboard focus states (e.g., `focus-visible:ring-2 focus-visible:ring-indigo-500`).
