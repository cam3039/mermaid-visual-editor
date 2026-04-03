## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.
## 2024-05-25 - Focus Management for Custom Input Wrappers
**Learning:** Custom inputs enclosed in wrappers (like the invisible `<input type="color">` in `ColorSwatch`) fail to show a focus state when navigated via keyboard.
**Action:** Use `focus-within:outline-none focus-within:ring-2 focus-within:ring-indigo-500` on the visible wrapper element to ensure the focus state is shown properly when the inner invisible element receives focus. This improves keyboard navigation accessibility.
