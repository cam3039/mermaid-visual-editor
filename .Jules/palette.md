## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.
## 2025-02-14 - Accessible Accordions
**Learning:** Accordion components using conditional rendering (`{open && <div>}`) break screen reader accessibility because the target of `aria-controls` is completely removed from the DOM when collapsed, causing validation tools and assistive tech to fail to find the associated region.
**Action:** Always maintain the content wrapper in the DOM using a unique `id` (via `useId()`) and toggle its visibility with CSS (e.g., `display: open ? 'block' : 'none'`) while updating `aria-expanded` on the controlling button.
