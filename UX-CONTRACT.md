# Interaction contract

| Capability | Canonical owner | Source of truth | Allowed variants | Verification |
|---|---|---|---|---|
| Select/Listbox | Native HTML select | app.js and index.html | Profile / difficulty | Browser profile switch and 4-choice mission |
| Scrollbar | Global app.css baseline | DESIGN.md | Component geometry only | 390px / 800px / 1280px layout checks |
| Toast | notice() in app.js | This contract | Timed status / persistent storage error | Browser status and unit storage schema checks |

- Action ownership: app.js document-level click delegation handles data-view, data-start, data-answer, data-review, data-hint and other data attributes. Controls with fixed IDs have JS-assigned onclick listeners. Static regex checks looking only for inline onclick will report false actionless-button findings; do not introduce duplicate inline event handlers to satisfy that regex.
- Views: explore, passport, review, parent. Navigation cancels no saved progress; a trip may be left and restarted without awarding a stamp.
- Two fixed local profiles, each with independent stamps and spaced-review records. Profile switching returns to explore and ends the active unsaved trip. No account, PII, analytics or external runtime requests.
- Explore: filter by continent or name, select country via list or map pin, read six topic cards, start seven-step mission. Every step gives hint, retry and explanation; no timer/lives. Easy has 2 choices, challenge 4. A corrected answer still advances but remains due for review.
- Native select owns profile and difficulty. Native input owns search. All actions are native buttons. All map pins have native country-button alternatives.
- Feedback owner: shared inline feedback + persistent global role=status. Scrollbar owner: global CSS. Modal owner: native dialog with close button, Escape and focus restoration. No alert/confirm/prompt.
- Audio: explicit speech request only. Korean reading uses available device voices. Native greeting uses a matching language voice or reports unavailability instead of reading in an incorrect voice. Audio off cancels speech. Effects are brief opt-in Web Audio tones.
- Persistence: one versioned localStorage object; write failures are visible. Backups have strict validation, preview, user-triggered replace and native dialog confirmation. No silent reset. Export includes both profiles and preferences. Import size <=1MB. Prototype-pollution keys and unknown IDs rejected through reconstruction of known fields.
- Review due dates use local calendar days and attempt-based intervals. Wrong answers remain due; first-try right answers increase interval. All profiles stay separate. Review falls back to previously learned material when nothing is due; zero records shows an explanation.
- Passport stamp awarded only when all seven stages are completed. Parent view distinguishes completed countries, topic mastery and due cards, and shows per-country provenance.
- Runtime: bundled scripts, map and flags; direct index.html opening works without fetch. Optional service worker caches the local app on HTTPS/localhost. Never claim offline ready before successful worker activation and asset precache. Updates are notified on next visit; browser storage can be cleared, backups are recommended. On deployment under a project subpath all asset URLs are relative.
- QA: test schema, 25 country coverage, question choices, coordinate projection, retry/interval logic and backup rejection with node tools/check.mjs; browser check explore, all seven mission steps, passport, review, modal and narrow layout.

- Photo owner: photo() in app.js uses the78 bundled images and photos.js provenance. Native dialog enlargement shows the full image, educational caption, creator, original Commons file and license. Escape and close restore focus to the photo button, including while a quiz is active. No navigation or answer state changes on photo open/close. All photo credits also appear in PHOTO-CREDITS.html.
