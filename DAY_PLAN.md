# Nilearn crash course: one-day plan

Upload the `.ipynb` files to Google Drive (or drag them into colab.research.google.com via File > Upload notebook). Each notebook installs nilearn in its first code cell. Checked against the nilearn `main` branch examples folder on 2026-10-16.

| Time | Notebook | Core idea | Read afterwards (nilearn `examples/`) |
|---|---|---|---|
| 09:00-09:30 | 00 Setup & mental model | Brain image = array + affine | `00_tutorials/plot_nilearn_101`, `plot_3d_and_4d_niimg` |
| 09:30-10:30 | 01 Images & plotting | Resampling, smoothing, stat-map plotting | `01_plotting/plot_atlas`, `plot_overlay`; `06_manipulating_images/plot_smooth_mean_image` |
| 10:30-10:45 | Break | Move. Water. | |
| 10:45-12:00 | 02 Maskers | 4D image -> 2D table (the key concept) | `06_manipulating_images/plot_nifti_simple`, `plot_mask_computation`; `03_connectivity/plot_signal_extraction` |
| 12:00-12:45 | Lunch | | |
| 12:45-14:00 | 03 Connectivity | Region-by-region signal relationships | `03_connectivity/plot_group_level_connectivity`, `plot_seed_to_voxel_correlation` |
| 14:00-14:15 | Break | | |
| 14:15-15:30 | 04 Decoding | ML on brain data, leakage-safe CV | `00_tutorials/plot_decoding_tutorial`; `02_decoding/plot_haxby_anova_svm`, `plot_haxby_understand_decoder` |
| 15:30-15:45 | Break | | |
| 15:45-17:15 | 05 GLM | Design matrix, contrasts, thresholding, group level | `00_tutorials/plot_single_subject_single_run`; `05_glm_second_level/plot_second_level_one_sample_test` |
| 17:15-18:00 | 06 Capstone | One mini-project + 5-sentence write-up | `07_advanced/*` for next steps |

## How to use each notebook
1. Read the concept cell. 2. Write a **prediction** as a comment before running. 3. Try the exercise yourself; the notebooks give function names and hints in the exercise text, not solutions. 4. Open the matching gallery example *after* your own attempt and compare approaches.

## Running a gallery example yourself
The gallery files are `.py` scripts with `# %%` cell markers. Fastest route: open the example on the nilearn documentation site and use its download-notebook link, then upload that to Colab. Or copy the script into a Colab cell block and run it (add `!pip install -q nilearn` first).

## If you're short on time
Do 00, 02, then either 03 or 04 or 05 depending on your goal (connectivity / ML / classic task fMRI). Skip stretch exercises.

## If something breaks
Nilearn's API evolves (e.g. `nilearn.input_data` no longer exists, use `nilearn.maskers`; surface plotting now centres on `SurfaceImage`). Use `function?` for the docstring of your installed version, and compare with the matching gallery example.
