## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-05-25 - Accordion Accessibility and Content Rendering
**Learning:** The collapsible Inspector Accordion components were conditionally rendering their content wrappers (`{open && <div>}`). This removed the content from the DOM entirely when collapsed, breaking the screen reader `aria-controls` reference. Focus states on the toggle buttons were also missing.
**Action:** When building or modifying collapsible components, always include `aria-expanded`, ensure visible focus states, and link `aria-controls` to the content ID. Critically, never conditionally render the content wrapper itself; instead, toggle its CSS `display` property (`open ? 'block' : 'none'`) so the ID referenced by `aria-controls` remains valid in the DOM at all times.
