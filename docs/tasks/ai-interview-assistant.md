# AI interview assistant — prototype scope

## Current behavior

The separate static candidate demo contains an optional, same-browser interview mockup. It presents three sample questions one at a time, each with a fresh three-minute timer, a text field and optional local audio recording. Questions, transcription and the recruiter summary are example content or placeholders. The current implementation does not call OpenAI or expose an AI API route.

The attached PDF is not read. Application text is stored in localStorage and recordings in IndexedDB. The recruiter inbox is a demonstration view in the same browser, not authentication, access control or delivery to an employer. Use synthetic data only.

## Scope change

The earlier implementation plan described a working OpenAI integration. The current assignment is a visual and interaction prototype only, so no API key, provider request, transcription service or generated summary is required. See [the current task intent](ai-interview-prototype.md).

## Verification

Run `./scripts/verify` and report what ran. Browser journeys require a provisioned Playwright Chromium; do not install browser or OS dependencies automatically.
