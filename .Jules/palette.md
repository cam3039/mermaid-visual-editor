## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-06-15 - Accordion Accessibility and Focus Management
**Learning:** Accordion toggles were missing screen reader context (`aria-expanded`, `aria-controls`) and focus visible states. Conditionally rendering children also broke `aria-controls` references when closed.
**Action:** When building or modifying collapsible UI components, always include `aria-expanded` and `aria-controls` linked to a unique ID, ensure visible focus states, and keep the content wrapper in the DOM toggling visibility via `display: 'block' | 'none'` to maintain valid ARIA references.
