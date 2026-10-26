# Project rules

## Structure
- Keep the quiz self-contained in `index.html`, with inline CSS and JavaScript.
- Use plain HTML, CSS, and JavaScript. Do not add dependencies, build tools,
  servers, or external assets.
- Open `index.html` directly in the integrated browser using a `file://` URL.

## Design and accessibility
- Preserve the narrow, responsive layout and mission-control styling.
- Use the existing `--cp-*` variables for colors. Preserve light and dark themes,
  system color-scheme detection, and the `scoutTheme` override.
- Keep body text at 14-16px with the existing sans-serif stack; use monospace
  for console labels.
- Use semantic buttons, visible focus indicators, keyboard controls, and
  accessible feedback. Respect `prefers-reduced-motion`.
- Show correct and incorrect states with text or symbols as well as color.

## Quiz behavior
- Keep 10 questions, one answer per question, a progress bar, and a score counter.
- Preserve green correct feedback, red shake incorrect feedback, and answer
  explanations. Prevent repeated answers from changing the score.
- Keep the results score, emoji reaction, answer review, and replay reset.

## Changes and checks
- Make focused changes and follow the existing code style.
- After behavior changes, smoke-test the quiz in the integrated browser:
  keyboard shortcuts and focus, correct and incorrect feedback, score and
  progress, results, answer review, and replay.
- Check both themes and a narrow viewport after visual changes.
- Distinguish dispatched keyboard-event checks from native keyboard testing.
  Report only checks actually performed, and state any limitations.
