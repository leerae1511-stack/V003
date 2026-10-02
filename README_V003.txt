Tool Pocket Generator — V003
Release status: Validation build; not yet approved.

Provenance
- Built directly from the uploaded Tool_Pocket_Generator_V001(1).zip.
- Source archive: index.html, manifest.webmanifest, sw.js, README.md.
- V002 was not used.

One authorised change
- Import JSON only: Detect Rectangle in Workspace converts existing imported points to workspace-relative millimetres before resizing, then maps them into the resized frame.
- Point UIDs are retained.
- The original non-imported/New Tool branch of detectWorkspaceRectangle() is retained verbatim.

Not changed
- New Tool photo upload, physical-grid confirmation, photo outline detection and scale calculation.
- Point editing, numbering, straight/curve controls, Geometry Check, JSON/STL geometry generation and other workflows.
- Existing JSON/STL export filename version strings.

Checks performed
- Source ZIP opened and contents inspected.
- Target function found uniquely before replacement.
- Original non-imported branch retained verbatim in the replacement.
- V003 branding updated in index.html.
- ZIP integrity and release-label checks performed after packaging.
- Browser execution, complete workflows, and iPad/Safari testing have NOT been performed here.

User validation required
A. Import JSON
1. Import a project and note its dimensions and point positions.
2. Increase workspace dimensions and press Detect Rectangle in Workspace.
3. Confirm the outline retains the same physical size and shape.
4. Reduce workspace dimensions below the outline size and repeat; confirm it is not scaled down.
5. Edit a point, run Geometry Check, export and reimport JSON.

B. New Tool regression
1. Start New Tool using the previously working tool-on-grid photo.
2. Confirm the physical grid and detect the exact outline.
3. Compare profile dimensions and shape with V001; run Geometry Check.

V003 is not an approved baseline until user validation is complete and accepted.
