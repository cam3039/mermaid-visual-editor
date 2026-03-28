## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2026-03-28 - Consistent Keyboard Focus States
**Learning:** Many interactive components like the toolbars, inspector elements, and zoom controls lacked explicit keyboard focus indicators, making the interface difficult to navigate via keyboard. While standard elements have native outlines, custom interactive elements and wrapper containers require intentional styling.
**Action:** When creating or modifying interactive elements (buttons, inputs, select dropdowns), ensure they always include visible keyboard focus states (e.g., `focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-indigo-500`). For grouped or nested components where the focusable element is visually hidden, use `focus-within:ring-2` on the visible wrapper container (like the `ColorSwatch` label).
