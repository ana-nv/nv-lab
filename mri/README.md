Information about MRI and fMRI, processing and analysis steps.



Topics:

# BIDS

Brain Imaging Data Structure (more information [here](https://bids-standard.github.io/bids-starter-kit/)).

## Validating BIDS dataset

With docker, you can run this line in the terminal:

`docker run -ti --rm -v [path_to_your_toplevel_bids_directory]:/data:ro bids/validator /data`


Common issues:

- files don't follow BIDS naming conventions (more info about filenames [here](https://bids-standard.github.io/bids-starter-kit/folders_and_files/files.html))
- events.tsv files are missing
- 
- ..
