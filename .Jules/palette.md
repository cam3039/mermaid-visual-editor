## 2024-05-24 - Modal Accessibility and Focus Management
**Learning:** Import modal was missing screen reader context (`role="dialog"`, `aria-labelledby`, `aria-describedby`) and live regions for asynchronous parsing feedback. Keyboard focus states on buttons were also missing.
**Action:** When building modals, always include proper ARIA roles and labels, ensure focus visible states on all interactive elements, and use `aria-live` regions for any dynamic status updates (like the parser feedback) so screen readers can announce them.

## 2024-05-25 - Custom Accordion Accessibility
**Learning:** Custom interactive elements like the `AccordionSection` in `InspectorPanel.tsx` lacked proper structural ARIA attributes to inform screen readers of their state (`aria-expanded`) and what they control (`aria-controls`). Additionally, keyboard focus indicators were absent, making it difficult for keyboard users to track their position.
**Action:** When building or modifying collapsible UI components, always ensure accessibility by including `aria-expanded={isOpen}`, `aria-controls` linked to a unique ID (e.g., via React's `useId()`), and clear, visible focus states (e.g., Tailwind's `focus-visible:ring-2 focus-visible:ring-indigo-500`).
