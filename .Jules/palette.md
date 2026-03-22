## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.
## 2025-03-22 - Missing Visible Focus on Custom Neumorphic Buttons
**Learning:** Custom UI buttons designed with intricate box-shadows (Neumorphism) often lack default browser focus outlines because they use custom CSS shapes or unset default borders. This breaks keyboard accessibility because users cannot see which element is currently active.
**Action:** When creating custom styled buttons or input wrappers that deviate from standard browser styles, explicitly add `focus-visible:ring-2` (or equivalent `focus-within` for wrappers) to restore an accessible visual focus indicator that does not interfere with mouse usage.
