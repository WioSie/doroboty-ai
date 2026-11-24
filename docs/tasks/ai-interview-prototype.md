# AI interview prototype step

## Intent

Make the optional AI interview step usable as a front-end prototype without an API key or external processing. Keep the candidate's three-question sequence, separate three-minute timer per question, text entry and local voice recording. Show clear placeholders for future question generation, transcription and recruiter summary APIs.

## Acceptance criteria

- After opting into the demo, the candidate can move through questions 1, 2 and 3, each with a fresh three-minute timer and an answer field.
- The timed question screen uses concrete sample questions and clearly says they are examples awaiting a future API integration.
- Text answers and optional voice recordings remain in the current browser. The prototype makes no OpenAI requests and does not claim a real transcription or AI summary.
- An audio-only answer can be reviewed and submitted; the recruiter view shows the recording and a clearly marked transcription placeholder.
- The candidate and recruiter views clearly state that the application is a same-browser demonstration and is not delivered to an employer.
- The changed application dialog follows the supplied dark AI moodboard: deep navy panels, cyan focus/interaction accents, pale-cyan text, yellow primary action and restrained glow, with responsive wrapping and keyboard-visible focus.
- Update FEATURES.md and security/task documentation to describe the simulated behavior.

## Design and integration notes

Use the local dark AI moodboard already applied to the static role page and `ai-interview.css`. Keep the existing static flow controller and browser-local application/audio stores. Do not add an API key, endpoint, provider call or remote dependency.

## Verification

Run `./scripts/verify`, inspect the final diff, and report which browser checks actually execute in this environment.
