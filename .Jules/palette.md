## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.
## 2025-04-03 - Aria-labels on Custom Buttons
**Learning:** Reusable custom button components (like `NeuBtn`, `ZoomBtn`, `NeuIconBtn`) in this application often rely solely on the `title` attribute for tooltips, which may not reliably serve as an accessible name for screen readers, especially if they contain only icons or visually hidden text.
**Action:** When creating or modifying generic UI button wrappers, always ensure that `aria-label` is mapped explicitly or falls back to `title` (e.g., `aria-label={title}`) to maintain accessibility for icon-only buttons.
