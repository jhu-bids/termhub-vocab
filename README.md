# TermHub Vocabularies

## Datasets
As of the time of this writing (May 11th, 2022), 100% of the datasets in this 
folder pertain to work related to the N3C grant, and have been downloaded 
directly from the N3C data enclave.

**Structure**  
(Not sure yet, but might be something like this:)

`datasets/registry.json`:
This is a file which is used to orchestrate which datasets will be downloaded 
and kept up-to-date within this repository. The JSON file is simply a flat list
of key-value pairs, where the keys are dataset names, and the values are RIDs (
Reference IDs), which is how they are identified within the N3C data enclave.

When downloaded, datasets are stored as such:
`datasets/<dataset-name>/<ref>/<transaction-id>`

## How to update datasets
From the [ValueSet-Tools repository](https://github.com/HOT-Ecosystem/ValueSet-Tools/), 
run_single the dataset download CLI using this command: 
`python enclave_wrangler/dataset_download.py --download-all-registered-datasets`
