## About 

Process for tidying POXC data from the plate reader and doing calculations. These files and folders are connected in a workflow. The instructions are written assuming you will download this whole folder, open the .Rproj file, and get started (as opposed to simply downloading one or the other of the scripts).

The general process is: 

- Prepare data (see below) 
- Run the `01_create_poxc_plate_templates.Rmd`, which reads from `raw_data/` and saves to `templates/` 
- Run the `02_poxc_calculation.Rmd`, which reads from `templates/` and saves to `results/`

### Before you start 

1. Save your raw data from plate reader as `.xlsx` files in the `raw_data/` directory.  
2. Have your plate maps typed up (see `plate_maps.csv`) and get your soil mass data typed up (see `poxc_soil_mass.csv`). If your data sheets do not mimic this format, you will need to update the code (or update your data sheets).  
3. Have your lab notebook handy, with any notes about pipetting errors, etc. ready (see `lab_notes/`)  
3. If required, you can add an additional file like `cig_names_master.csv` with additional metadata about your sites and samples. This is joined to the calculations at the end of `02_poxc_calculation.Rmd`.  