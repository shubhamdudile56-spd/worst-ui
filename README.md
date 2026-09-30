# worst-ui

A collection of deliberately bad web design, published for educational and comedic purposes.

Every page in this repo is an intentional anti-pattern showcase. The goal is to demonstrate
which design decisions make an interface unusable, so they can be recognised and avoided in
real projects. None of this is a recommendation.

## Pages

| File | What it is |
| --- | --- |
| [`index.html`](index.html) | Entry point. Animated rainbow background, Comic Sans, text strokes, cursor-follower emoji, sticky stickers that flee from the pointer, two interrupting modals, and a form that validates five ways per field. |
| [`annoying.html`](annoying.html) | The same page served as a standalone file. |
| [`worst-ui.html`](worst-ui.html) | Neon dark-pattern storefront: fake urgency counters, preselected checkboxes, confirmshaming, and a fake countdown that resets. |
| [`worst-ui-3.html`](worst-ui-3.html) | Third iteration of the same exercise, with a different set of anti-patterns. |
| [`dark-pattern-store.html`](dark-pattern-store.html) | Dark-pattern storefront focused on subscription traps and consent manipulation. |
| [`aether-core.html`](aether-core.html) | The calm, well-designed counterpart. This is the "before" screenshot, so to speak — the same product brief executed properly. |
| [`landing.html`](landing.html) | The polished landing page for the fictional Cadence product, written before the anti-pattern version. |

## How to view

Open any file directly in a browser, no build step or dependencies:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Why the calm version is here too

`aether-core.html` and `landing.html` are included as the reference implementation. The contrast
between them and the rest of the repo is the entire point: the same feature set, the same data,
the same interactions — one is calm and usable, the other is hostile. Comparing the two is the
fastest way to build intuition for which choices carry real usability cost.

## Accessibility notes

The anti-pattern pages fail accessibility in specific, intentional ways:

- Colour-only status communication and text/background contrast ratios below WCAG AA
- Continuous decorative motion with no way to pause it (`index.html` does honour
  `prefers-reduced-motion`, which is the one concession it makes)
- Auto-playing interruptions that steal focus and cannot be dismissed without engaging
- Uppercase body copy, dense multi-weight outlines, and near-unreadable letterforms
- Layouts that do not reflow usably on small viewports

Do not copy any of it into a real product.
