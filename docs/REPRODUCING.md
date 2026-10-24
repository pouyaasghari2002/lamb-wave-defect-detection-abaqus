# Reproduction workflow

The archive supplies a report and videos, not a runnable Abaqus model. These steps describe the reported workflow; they were not executed during translation.

## Geometry and coordinate convention

Use a 100 × 100 × 1 mm plate. For a convenient convention with x rightward and y upward from the lower-left corner, the source lies at (10, 90) mm, the sensor at (90, 10) mm, and the large-hole center at (70, 30) mm with radius 25 mm. These coordinates are derived from the report's stated edge distances. The smaller hole is central; its exact radius must come from the original model or project team.

Create a 3D plate and partition it so the source and sensor locations can be selected consistently. The screenshots show 3D Stress elements in the Explicit library, but the exact element code and thickness discretization are not established.

## Material and units

The shown numerical entries are Young's modulus 62000, Poisson's ratio 0.33, and density 2.7e-9. A consistent N–mm–s–tonne interpretation gives E = 62000 MPa and density = 2700 kg/m³. Confirm this against the native model rather than treating the inferred units as original declarations. Under this system displacements are in mm and forces in N.

## Step, boundaries, and excitation

1. Create a Dynamic, Explicit step lasting 1e-4 s.
2. The screenshot caps the increment at 1e-7 s. Verify stability and temporal resolution for the actual mesh.
3. Constrain U1, U2, and U3 on the perimeter side faces.
4. Apply the concentrated out-of-plane load at the source, CF3 = 1 and the other components zero.
5. Define the tabular Pulse using `data/pulse_from_report.csv`. It transcribes the visible screenshot; it is not a validated Hanning-windowed analytic excitation. Verify interpolation, post-pulse behavior, and units in the native input.

## Mesh and outputs

The Global Seeds dialog shows approximate global size 1. Verify local refinement around holes, element formulation, elements through thickness, wavelength resolution, and convergence; a seed value alone does not establish accuracy.

Request out-of-plane sensor U3 history every increment. Field output uses 100 evenly spaced intervals. The original job uses Double – analysis only. Recreate the intact, large-hole, and smaller-hole cases using consistent sensor locations, output settings, and loading.

## Compare results

Overlay U3 histories and examine time windows that separate direct arrivals from hole scattering and outer-edge reflections. Confirm length units before converting amplitudes. Export raw time/displacement tables, label axes, and retain physical time separately from video playback duration. No raw output values were digitized or generated during translation.

## Add your native files

Place CAE and INP files under `models/`, Abaqus Python or post-processing scripts under `code/`, and compact exported histories under `data/`. Explain each file, the required Abaqus release, exact run commands, job names, units, and expected outputs. Do not replace the original report or videos when adding a revised model.

Large ODB output databases can exceed GitHub upload limits. Keep them outside the ordinary browser upload or use a suitable large-file distribution method; compact CSV exports are easier to review. No ODB file is included in this package.
