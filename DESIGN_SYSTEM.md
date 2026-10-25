# NEXUS Expressive Design System

NEXUS Playground is an original, single-file web experience informed by Material 3 Expressive design principles. It is **not** Google's official Material component library, and it does not claim pixel-for-pixel parity with Android system UI.

## Design intent

The interface uses five connected levers rather than treating expression as decoration:

1. **Color and roles** — primary, primary-container, secondary, tertiary-like accents, surface, and on-surface colors are expressed as shared CSS custom properties. Dark mode remaps those roles instead of applying a generic invert.
2. **Shape and containment** — navigation, cards, game surfaces, actions, and the quick-action dock have related but intentionally distinct silhouettes. Active, hover, and pressed states can morph corner geometry.
3. **Scale and hierarchy** — the home hero, action dock, statistics, and feature cards use different visual weights so the primary next step is easy to spot.
4. **Motion** — transitions use a consistent easing vocabulary; shape and position changes respond to interaction instead of running only as decoration.
5. **Responsive composition** — the desktop navigation rail becomes a compact bottom navigation on narrow screens, and the quick-action dock adapts to an icon-and-label arrangement.

## Implementation map

| Principle | Implementation |
| --- | --- |
| Shared color roles | `:root` and `[data-theme="dark"]` custom properties in `index.html` |
| Variable typography | Google Sans Flex for expressive display/body variation; Noto Sans JP for Japanese glyph coverage |
| Shape language | `.hero`, `.nav button`, `.stat`, `.feature`, `.expressive-dock`, game controls |
| Expressive quick actions | `.expressive-dock` with three real navigation actions |
| Motion | `--motion-fast`, `--motion-spring`, state transitions and `@keyframes` |
| Responsive layouts | Existing `@media` breakpoints at 1100px and 740px |
| Accessibility | Visible keyboard focus, navigation `aria-current`, reduced-motion support, labelled controls |
| Privacy | Demo assistant and user data stay in the browser; no AI API key or backend secret is embedded |

## Important product truth

The AI Lab is a rule-based browser demo, not a connected large language model. Scores, settings, and saved items use browser-local storage. The design language is inspired by M3 Expressive; the web implementation uses CSS and vanilla JavaScript rather than Google's Android/Compose component implementations.

## Validation checklist

- [x] Single HTML file remains the app entry point.
- [x] Seven page sections and existing IDs are preserved.
- [x] Existing JavaScript parses successfully.
- [x] CSS block braces are balanced.
- [x] No duplicate HTML IDs were found in static inspection.
- [x] Reduced-motion stylesheet and keyboard focus styles are present.
- [ ] Visual browser review at desktop and mobile widths.
- [ ] Full interaction regression pass in a real browser.

The unchecked items are intentionally not represented as completed: static source checks do not replace screenshot comparison or hands-on browser testing.