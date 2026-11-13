# Verification record — 2026-11-13

## Reference-image revisions and Singapore

-26 countries and78 learning images. Verified29 supplied reference slots were changed/new, plus1 Spain correction;30 revised/new assets total. Comparison and selected licensed source URLs are listed in REPLACEMENTS.md.
- Actual candidate subjects were inspected; the Italy Sagrada reference was assigned to Spain and Italy retained the Colosseum. Italy house changed to a Florence palazzo courtyard with aligned facts. China house was broadened to northernChina for the Shanxi aerial source.
- Brazil now uses a labelled Amazon-basin MAP, not a photograph or a currentforest-cover map; its topic/source no longer falsely refers to the smaller UNESCO conservation area. Singapore Merlion links to the tourism board and is not labelled UNESCO.
- Automated checks passed3640 randomized questions,26 unique country records,78 image/license/creator entries, both previous-format and full182-topic backups, map kind/country classification checks, entry assets and script syntax.
- Browser: Singapore full7-step journey completed, photo enlargement/Escape restored the quiz state, stamp saved. All3 newSingapore images loaded; officialculturelink correct; Brazil enlargement labelled map with clearbasin caption. Portrait800×1280 had790px client/scroll width and766px dialog width. No captured consoleerrors.
- All117 service-worker precache URLs returnedHTTP200 with correct JPEG MIME. PhysicalGalaxy device and network-disconnected playback remain untested. Screenshot:qa/preview-26-countries.jpg.


## Real-photo update

- Replaced illustrations/food emoji with75 real photographs:25 foods,25 homes/community spaces and25 heritage sites. Source descriptions and photo subjects were matched, and all75 were decoded and visually inspected on three contact sheets; drawings, mismatched examples and weak candidates were replaced.
- Each photo has creator, Commons file, license, modification statement and retrieval date in photos.js and PHOTO-CREDITS.html. House captions state specific regional/community examples. Hangi is labelled a cooking process; the salmon buffet is labelled a preparation example. Brazil's stilt-house source is688×457, so enlargement cannot add detail absent from that original. Photos are resized/recompressed without generated content or composites.
- Updated automated checks passed:75 local JPEG paths, author/license/source fields, per-photo credit anchors, registry script loading order, plus the existing3500 randomized question and progress/backup tests.
- All112 offline precache URLs returned HTTP200;75 JPEG responses had correct image/jpeg MIME types. Browser displayed offline-ready after installation. Network-disconnected execution on a physical tablet remains untested.
- Browser checks: house, food and heritage enlargements; full image uses object-fit:contain; creator/original/license visible; Escape/close and focus return to original photo button; opening a photo during house/heritage missions preserves the current question and subsequent answer behavior. Quiz caption avoids printing the answer's Korean name before solving.
- Full updated Indonesia seven-step journey completed and saved its stamp. Portrait800×1280 and narrow390×844 layouts had no document overflow; photo dialogs stayed within viewport (766px/356px widths respectively). No captured browser errors in the tested flow. Final screenshot:qa/preview-photos.jpg.
- Final GitHub package is produced by tools/package.py. It includes all75 final JPEGs and credits, but excludes acquisition originals, candidate files and the local-path audit report. Archive integrity, entry-file location and all photo paths are checked.

## Passed

- `node tools/check.mjs`: 25 distinct countries including Indonesia; 3,500 randomized question generations with 2/4 choices and exactly one answer; country data fields; included SVG flags; map paths and coordinate projection; review date arithmetic; retry resets; profile separation; backup round-trip and malformed/prototype-key rejection; JS syntax and entry assets.
- All 35 service-worker precache URLs returned HTTP 200 through the local static server.
- Browser: Indonesia's full seven-mission journey; deliberately wrong flag choice followed by hint and correction; completion stamp persisted; only the wrong topic was due for same-day review; the other profile showed zero stamps and due cards.
- Browser: parent difficulty change led to four flag choices; empty search message; source dialog and Escape; supplied flags displayed without broken images; local persistence survived reload.
- Browser: 1280×800 landscape, 800×1280 portrait and 390×844 narrow layout. Portrait and narrow layouts stacked panels; document scroll width equaled client width. Menu scroll is intentionally internal on narrow screens. Final preview saved as qa/preview.jpg.
- Browser displayed ‘오프라인 준비 완료’ after worker activation. Actual network-disconnected navigation was not tested. Offline cache URL completeness was verified separately.
- Browser console check showed no captured errors during the tested flow.

## Static audit scope

The premium static auditor was run. Native select ownership is recorded in premium-ui.json and UX-CONTRACT.md. Its actionless-button regex only recognizes inline onclick/framework handlers, and does not follow the document click delegation or JS-assigned handlers used here. Remaining findings of this type are recorded in premium-audit.json and assessed as false positives, not a runtime pass from the auditor. The real UI flows above supplied runtime evidence. The @google/design.md CLI was unavailable in this bundled Node runtime; its lint command was not run.

## Not verified

- A physical Galaxy tablet, Samsung Internet and device-specific Korean/foreign-language voice availability.
- Network-disconnected playback, cache eviction and an installed home-screen shortcut on Android.
- Live GitHub Pages deployment; no repository/account destination was supplied.
- Independent expert review of every cultural phrase. Content references, regional caveats and source limitations are recorded in SOURCES.md.
- Browser UI import/export file chooser round-trip; the parser/validation round-trip and rejection paths passed automated checks.
