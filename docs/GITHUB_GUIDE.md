# Put your Lamb-wave project on GitHub

A repository is a project folder with change history. Its README introduces the project below the file list. A commit saves a change with a short message. This guide uses GitHub's website; no terminal or Git installation is required.

## 1. Download and prepare

Download and extract `Lamb_Wave_GitHub_Package.zip`. Open its `lamb-wave-defect-detection-abaqus` folder. You will find the English PDF, LaTeX source, figures, original videos, a written README, and documentation folders. `code/` and `models/` contain instructions because the uploaded archive did not include native Abaqus models or scripts.

## 2. Create an account and repository

1. Open https://github.com and select Sign up if you do not have an account.
2. Complete account verification and sign in.
3. Open https://github.com/new.
4. Fill the fields below.

| Field | What to enter |
| --- | --- |
| Owner | Your personal GitHub account |
| Repository name | `lamb-wave-defect-detection-abaqus` |
| Description | `Abaqus/Explicit simulation of Lamb-wave propagation and hole-induced scattering in aluminum plates for nondestructive testing.` |
| Visibility | Public for your portfolio; Private while preparing |
| Add README | On; replace the starter with the supplied file |
| Add .gitignore | None; one is supplied |
| License | None until the group decides which reuse permissions to grant |

5. Click Create repository.

For an existing repository dedicated to this project, use the upload steps below without creating another one. For an existing multi-project repository, upload the complete named project folder as a subfolder and link its README from your root README. Avoid replacing an unrelated root README.

## 3. Upload your project

1. On the Code page, select Add file → Upload files.
2. Drag the extracted project's **contents** into the upload area: `README.md`, `.gitignore`, `report/`, `videos/`, `docs/`, `models/`, `code/`, and `data/`.
3. Keep the README at the repository root for a standalone repository. Check paths such as `report/main.tex`, `report/figures/rId55.jpeg`, and `videos/Fullplate.mp4`.
4. Do not upload only the outer ZIP; extracted files make the report and documentation easy to browse.
5. Enter this commit message:

```text
Add Lamb-wave report, figures, and simulation videos
```

6. For the initial upload to your own new repository, commit directly to main if offered and select Commit changes. If GitHub offers a proposal workflow instead, follow its displayed steps.
7. Return to the repository homepage. Confirm that the supplied README replaces the starter and its comparison image displays.

GitHub supports 100 files per browser upload and 25 MiB per individual file. The prepared package fits those limits. If `.gitignore` is hidden, enable hidden items in your file manager, or use Add file → Create new file and paste its contents. Browser uploads do not automatically filter chosen files using ignore rules.

## 4. Fill About and Topics

Click the gear beside About on the Code page. Paste this description:

```text
Abaqus/Explicit simulation of Lamb-wave propagation and hole-induced scattering in aluminum plates for nondestructive testing.
```

Leave Website blank. Add these Topics individually, then save:

```text
abaqus
finite-element-analysis
lamb-waves
wave-propagation
nondestructive-testing
structural-health-monitoring
ultrasonics
mechanical-engineering
```

## 5. What to write in each README section

The supplied root README is ready to upload. Its sections contain:

| Section | Content already written |
| --- | --- |
| Title and introduction | Software, plate-wave study, and purpose |
| Team | All three original authors, instructor, and date |
| Objective | Intact, large-hole, and smaller-hole comparisons |
| Model overview | Dimensions, source/sensor locations, boundaries, pulse, and step |
| Methods | Explicit finite elements, U3 histories, and animation comparisons |
| Results and scope | Qualitative observations and limits of available evidence |
| Files | Links to report, source, videos, data, and documentation |
| Software and reproduction | Abaqus release visible in videos and missing native files |
| Build the English report | LaTeX and Overleaf instructions |
| Attribution and translation | Team credit and conversion details |
| License | Current reuse-permission status |

Do not claim numerical detection accuracy, experimental validation, or a verified specific Lamb mode. Native models and raw histories are not yet included. Preserve the group attribution; describe your own contribution separately only when you can state it accurately.

## 6. Other repository tabs

| Tab or feature | What to do |
| --- | --- |
| Code | Store the project files and display the README |
| Issues | Optional tasks: add CAE/INP files, confirm small-hole radius, audit units |
| Pull requests | Optional review of future changes |
| Actions | Leave unused initially; automated builds are optional |
| Projects | Optional task board |
| Wiki | Optional; README and docs already explain the project |
| Security | No project summary to write here |
| Insights | GitHub-generated activity information |
| Settings | Keep defaults unless changing visibility or enabled features |
| Releases | Optional milestone downloads after the model files are added |

These are features, not mandatory written sections. You do not need to fill every tab.

## 7. Add the code and model files stored elsewhere

1. Add original `.cae` and `.inp` files under `models/`.
2. Add Abaqus Python scripts or other original analysis code under `code/`.
3. Add compact exported time/displacement tables under `data/`, with explicit units.
4. Update `docs/REPRODUCING.md` with exact software requirements, commands, job names, inputs, and output paths. Record the small-hole radius and exact element type.
5. Update the README file table and availability statement once those files are actually present.
6. Upload and commit with `Add original Abaqus models and analysis scripts`.

Large ODB files may exceed browser-upload limits; do not include them in an ordinary upload batch without checking size. The supplied `.gitignore` excludes generated ODB and scratch files for future Git use, but it does not prevent you manually selecting them in a browser upload.

## 8. Compile the English report

For Overleaf, use `Lamb_Wave_English_LaTeX.zip`:

1. Sign in to Overleaf.
2. Choose New Project → Upload Project and select the ZIP.
3. Set `main.tex` as the main document and choose pdfLaTeX.
4. Compile. Keep `figures/` beside the source.

No custom font or bibliography file is required; references are embedded in the LaTeX source. Abaqus is not needed to compile the report. The full GitHub package also contains these files under `report/`; select the nested `report/main.tex` if uploading that package instead.

## 9. Edit and check the repository

Open a text file, choose the pencil, edit, preview, and commit. Upload a revised file at the same path to save another version.

Check that the README renders, the comparison image displays, the English PDF opens, and all three videos download. GitHub may not preview native CAE or INP content in a useful form; use Abaqus for native models. Confirm collaborators' preferred English name spellings before publication.

Your project link will be:

```text
https://github.com/YOUR-USERNAME/lamb-wave-defect-detection-abaqus
```

Replace `YOUR-USERNAME` with your actual username. You can pin the repository from your profile using Customize your pins. Add the project link beside its title in your CV.

## 10. CV wording

Title: **Lamb Wave Simulation for Defect Detection**

Description: **Simulated Lamb-wave propagation in aluminum plates using Abaqus/Explicit to analyze defect-induced scattering.**

The description avoids assigning you sole authorship of the group project or claiming unverified detection performance.

Official GitHub references:

- https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository
- https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
