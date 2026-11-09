# Crowdcress 1.0 TEST
Native Android Kuralin majority-loop puzzle. Android 8+ (min26), target35. Package com.gg007.crowdcress. Twelve original unique boards on a compact 4x4 grid.

## Rules
Kuralin loop puzzle on a 4x4 grid. Tap between two side-neighbor cell centers to toggle a road. Make exactly one closed loop with no crossings, branches or repeated cells. All unused cells darken automatically, including inside the loop; dark cells may touch. Each fixed circle compares only the cells touching that circle: two at a shared cell side, four at an interior grid corner. White W means more light loop cells, black B means more dark unused cells, gray G means equal counts. Clues do not count roads and the loop need not pass through circles. Undo/reset, next and level selection; saved palette and optional clue letters. No timer, score, dragging or separate shade control.

## Download and status
https://mega.co.nz/#!pRUSBbaK!UMtL293xnChXFUvtFhMCz5T-jTgyuyfXtlFmX4Npj9Q
APK SHA256 16208a759f125faef91f9e9eb70534f54a189bb0f3bf137be1e8e07475fdf33d; 20974 bytes. Original signing certificate SHA256 1651d9e269ece8a76f36ed4bba24ebc50f9de1e5f856e0567e0e8169fcb25597. Anonymous downloaded bytes match. No requested permissions. Original icon unchanged.

## Checks
Independent incidence-bitcount and closed walk versus production degree counting and bit flood agree on all 16,777,216 edge masks of the 4x4 grid, identifying 213 simple cycles. Independent explicit two/four-cell lists versus production doubled-coordinate touch tests agree on all 786,432 board/shading states. Each of twelve distinct clue boards admits exactly one loop, and all twelve loops differ. Tests cover toggles, bounds, undo, reset, solved lock, malformed masks and two/four-cell majority/equality cases. Portable generator seed 570909 reproduces the twelve boards; every board includes all three circle types. Actual drawing-adapter taps solve all twelve, with undo/replay, next, levels, menu, privacy and saved palette/clue letters checked. Six drawing previews inspected, not phone screenshots. Initial adapter compilation had a local variable name collision with MotionEvent, fixed before build/tests; oracle rules and expectations unchanged. Phone runtime/performance/external-browser QA and full Git source commit remain incomplete. Signed TEST, not final or Play published.

## Functional difference
Reviewed all 188 prior studio descriptions and current 803 web registry records using functional terms. Mastermind candidate rejected because web entry36 already implements it. Brookmere uses exact vertex counts with connected white cells, Nearwillow uses cell-neighbor dark counts with separated darks, and Nearcress uses nearest-edge direction clues. Crowdcress instead couples a single cell-center loop with majority/equality tests over two/four touching cells and unrestricted dark adjacency. No Kuralin/Kurarin functional match found in reviewed corpus; corpus is partial. Known Kuralin adaptation with original boards, code and visuals, no copied layouts/code/art and no origin claim. Nikoli Japanese/English and independent puzzle-author rules agree; Morass clarifies two/four-cell circles and touching darks. Edgepedia derivative wording about orthogonal neighbors is less precise than the primary touching-cells rule, and its complexity/history claims are not relied on.
Rules https://www.nikoli.co.jp/en/puzzles/kuralin/ ; independent rules https://dj-puzzles.blogspot.com/2025/06/genre-spotlight-46-kurarin-puzzles-350.html .

## Build
JDK17, Android SDK35/build-tools35.0.0. python generate-levels.py reproduces levels.json. javac -d /tmp/blue-test src/com/gg007/crowdcress/Board.java BoardTest.java then java -cp /tmp/blue-test com.gg007.crowdcress.BoardTest. bash build.sh makes an unsigned aligned APK unless KEYSTORE_PATH and KEYSTORE_PASSWORD_FILE point to your own private signing material. No signing secret is included.

## Privacy and branding
Crowdcress runs offline without accounts, ads, analytics, third-party SDKs or requested permissions. Palette, clue letters and solved-board marks stay in this app on your device. Clear app data or uninstall to remove them. The studio link opens your external browser.
GG007 original icon, menu studio https://ilanis-agent.github.io/gg-007-gaming/ and privacy.

## Preservation and publishing
Complete source/APK, exact cumulative 189-card studio and published catalog/studio sources and updater privately preserved at https://files.instinct.com/n4bsju3krwbk-crowdcress-source-archive . Repository https://github.com/iLanis-agent/crowdcress holds README only; full Git source commit pending. Existing Jekyll static includes retained without changes; no Pages settings changes or client loader. Both site publications verified separately.
