## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-05-25 - Focus Visible Rings and ARIA Labels
**Learning:** Found multiple custom button components (`NeuBtn`, `NeuIconBtn`, `ZoomBtn`) missing visible focus rings for keyboard navigation and `aria-label` attributes for screen readers. Using `:focus-visible` with Tailwind (`focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-indigo-500`) provides clear keyboard focus without disrupting mouse users.
**Action:** When building custom interactive elements, always ensure they have an `aria-label` (falling back to `title` if icon-only) and a visible focus state for keyboard accessibility.
