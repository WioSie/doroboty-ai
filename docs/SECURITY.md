# Prototype data boundary

This teaching prototype has no production server or real authentication. Role-specific UI and local transition checks organize the scenario; anyone using the browser can inspect browser-local data. Use synthetic data only.

The React scenario exposes one recruiter account in the employer entry flow and keeps role selection browser-local; the separate static DoRobory.AI demo also includes one passwordless recruiter identity. Neither selector is authentication, access control or a private recruiter workspace. Anyone using the browser can select a role or edit stored data. Recruiter-created offers, application stages and decisions remain in that browser and are not sent to employers or other devices. Do not enter real candidate data or use the demo for employment decisions.

Never put API keys, credentials, real CVs or private material in frontend source, JSON, localStorage or exports. Exports include recruiter notes. The optional static candidate interview is a mockup: it uses sample questions and makes no external requests or AI-provider calls.

After opting into the mock interview, the browser displays three fixed example questions. Text answers are stored in localStorage and audio recordings in IndexedDB. Transcription and summary are visibly marked placeholders; neither answers nor recordings leave the browser. The attached PDF is not read. This same-browser demo has no authentication or role confidentiality. Do not use real applicant material in this feature.

Vite does not expose AI interview routes. The static build and development server both use the same local mockup. No CV audio or answer content is sent to a server.

Render imported text through React text nodes, validate imports with shared Zod schemas, reject unsupported versions, duplicate IDs, broken references and oversized files. Never overwrite an unreadable save automatically.
