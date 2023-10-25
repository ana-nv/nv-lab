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
- participants.tsv is missing
- participants.json file is missing or does not describe all variables from the tsv file
- datasset_description is missing or there is no name of the dataset or author names in it.
- readme file is missing or too short
- ...


# OSF

Upload your dataset to osf using osfclient

Installation:
`pip3 install osfclient`

### upload a file in an OSF project
`osf -p <projectid> -u yourOSFacount@example.com upload local/file.txt remote/path.txt`
### upload a folder (recursively) in an OSF project
`osf -p <projectid> -u yourOSFacount@example.com upload local/file.txt remote/path`
