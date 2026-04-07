## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-04-07 - Generic UI button wrapper ARIA mapping
**Learning:** Reusable UI button wrappers (`NeuBtn`, `NeuIconBtn`, `ZoomBtn`) often accept a `title` prop for native tooltips but fail to map it to `aria-label`, resulting in inaccessible icon-only buttons across multiple features (e.g., Object Settings, Diagram Settings, Expand Modal).
**Action:** When creating or modifying generic UI button wrappers, always ensure that `aria-label` is mapped explicitly or falls back to `title` (`aria-label={title}`) to maintain accessibility for screen reader users.
