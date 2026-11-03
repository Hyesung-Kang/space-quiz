# Project Rules

## Scope and Structure
- Keep the quiz self-contained in [index.html](index.html), including CSS, JavaScript, question data, and artwork.
- Preserve direct `file://` usage. Do not introduce a server, build tooling, dependencies, CDN assets, or network requests.
- Keep changes limited to the requested behavior or styling; preserve unrelated content and existing user edits.
- For visual-only requests, change the relevant CSS without altering quiz data or JavaScript behavior.

## Behavior and Accessibility
- Keep 10 questions with four answers each. Each question uses `category`, `question`, `answers`, a zero-based `correct` index, and `fact`.
- Preserve answer locking and the duplicate-scoring guard in `selectAnswer()`. Keep the score, progress, results review, and restart state consistent.
- Preserve semantic buttons, keyboard operation, visible focus rings, focus management, live feedback, and `prefers-reduced-motion` support.
- Communicate correctness through text or symbols as well as color, and preserve the responsive layouts.

## Validation
- Open the HTML directly in the VS Code integrated browser; no installation or build command is needed. There is no configured automated test suite.
- For behavior changes, check correct and incorrect answers, repeat-selection protection, all 10 questions, results review, and restart.
- For style changes, check the affected pointer and keyboard states at desktop and narrow mobile widths, plus reduced-motion behavior when animations change.
- Report checks actually performed and any verification gaps; do not claim unrun tests passed.