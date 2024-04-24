# BIDS for behavioral studies
## Resources
[Behavioral experiments (with no neural recordings) - Brain Imaging Data Structure v1.9.0](https://bids-specification.readthedocs.io/en/stable/modality-specific-files/behavioral-experiments.html)
## Software: 
[bids-matlab](https://github.com/bids-standard/bids-matlab) | 
[bids-starter-kit on GitHub](https://github.com/bids-standard/bids-starter-kit) | 
[JSONio on GitHub](https://github.com/gllmflndn/JSONio)
## How to implement
You may use the template in the BIDS starter kit (bids-starter-kit/general). Simply copy the corresponding mat file and modify the variables for your project.
### After preprocessing:
create_events_tsv_json_full.m
### Before finalizing everything:
createBIDS_participants_tsv.m    
createBIDS_dataset_description_json.m

See the example for transriv project:
- Add ‘transriv-bids’ to matlab path
- Go to the root_dir or use the full path of root_dir as input to the functions
- Preprocess data from a subject: 
`createBIDS_beh_after_preprocessing(root_dir, ‘transriv’, ‘S001’, ‘Rivalry’, ‘GG’)`
- Create dataset files by running `transriv_finalizeBIDS.m`

The folder structure based on BIDS:
```
root_dir
  └─ ‘transriv’
        ├─ sourcedata
        │     └─ sub-S001
        │         └─ ses-Rivalry
        │               └─ beh
        │                   └─ sub-S001_ses-Rivalry_run-GG_beh.mat
        └─ rawdata
             └─ sub-S001
                 └─ ses-Rivalry
                     └─ beh
                         ├─ sub-S001_ses-Rivalry_run-GG_beh.json
                         └─ sub-S001_ses-Rivalry_run-GG_beh.tsv
```
