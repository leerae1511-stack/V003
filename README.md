Tool Pocket Generator — V001
Release status: User validation build (not yet approved/locked)

Source / provenance
- Built directly from Tool_Pocket_Generator_V000.zip.
- V000 is the byte-for-byte baseline replica of the user-provided V104 ZIP.
- No later build was used as a source.

Targeted change (one issue only)
- New Tool photo outline detection: lowered the fallback dark-foreground threshold from grayscale <80 to <45.
- Reason: the V000 screenshot showed detected points split into separate clusters. The fallback threshold could include dark printed grid strokes along with the black tool, joining unrelated image regions and interfering with continuous silhouette tracing.
- Existing opening/closing morphology, contour tracing, simplification, physical-grid calibration, workspace logic, point editing, curves, geometry checks, and export code were not changed.

What was not changed
- No curve/straight point behaviour or point editing controls.
- No imported JSON geometry logic.
- No export JSON/STL naming or version strings.
- No workspace rectangle behaviour or physical ruler scale algorithm.

Verification performed
- Source comparison: V001 was unpacked from V000 and only the two visible app branding strings and the fallback silhouette threshold/comment were edited.
- JavaScript syntax check: see release handoff; runtime browser testing was not available in this build session.
- ZIP integrity/listing check performed after packaging.

Required user validation (not yet performed)
1. New Tool workflow: set workspace rectangle to 200 × 50 mm, load the supplied tool-on-grid photo, confirm physical grid, detect exact tool outline. Check that the points trace one continuous complete silhouette and are not split into two clusters. Confirm the orange workspace rectangle remains independent.
2. Import JSON workflow: import an existing project, inspect/edit points and confirm imported geometry, straight/curve settings, and dimensions remain intact.

Important
- This is a test build for the user to validate on iPad/Safari. It is not claimed to have passed either full workflow or to be an approved release. If the detector still fails, report the on-screen status and share a screenshot before any further change.
