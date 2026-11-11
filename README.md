# Vruntime Ink Theme

A dependency-free light/dark theme switch where the new theme **bleeds outward like ink**
from the button you click. Uses the View Transitions API with an animated organic mask;
falls back to an instant switch in unsupported browsers and when `prefers-reduced-motion` is on.

## Use

```html
<button id="toggle">Switch theme</button>
<script type="module">
  import { createInkTheme, bindToggle } from './src/inkbleed.js';
  const theme = createInkTheme();            // sets data-theme="light|dark" on <html>
  bindToggle(document.getElementById('toggle'), theme);
</script>
```

Style with `[data-theme='dark'] { ... }`. API: `theme.get()`, `theme.set('dark', elementOrPoint)`, `theme.toggle(origin)`.
Options: `attribute, storageKey, duration, roughness, scale, edge, easing, onChange`.

## License — free, but credit required

Free for personal and commercial use under the **Vruntime Labs Attribution License v1.0**.
You must credit **Vruntime Labs** visibly (UI, docs, or acknowledgements) — see `LICENSE` and `NOTICE.md`.

Original work by Vruntime Labs; contains no code from third-party theme-toggle projects.
