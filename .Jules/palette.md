## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-10-24 - Icon-only Buttons Accessibility
**Learning:** Many custom `NeuBtn` and standard `button` elements that rely on icons or visual cues for context were missing explicit `aria-label`s. Passing a `title` prop isn't fully sufficient for screen reader accessibility, leading to poor UX for visually impaired users.
**Action:** Always map the `title` prop (or a descriptive string) to the `aria-label` attribute on generic UI button wrappers (e.g., `NeuBtn`) and raw `<button>` elements to maintain high accessibility standards.