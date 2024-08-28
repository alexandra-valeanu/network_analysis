## Network analysis

This repository serves as solution for the Systems Biology task.

| Input  | Text file with a list of genetic variants (rs-numbers) [`data/variant_list.txt`](data/variant_list.txt) |
|--------|---------------------------------------------------------------------------------------------------------|
| Output | Network in Cytoscape linking variant to gene to pathway [`results`](results)                            |

## Steps

- [x] Use [`BioMart`](https://pypi.org/project/pybiomart/) to retrieve the associated gene for each of the variants in
  the [`data/variant_list.txt`](data/variant_list.txt)
- [x] Create a network in [`Cytoscape`](https://cytoscape.org/) linking the SNPs to the genes
- [x] Use the [`CyTargetLinker`](https://cytargetlinker.github.io/) app for [`Cytoscape`](https://cytoscape.org/) to add
  known pathways from [`WikiPathways`](https://www.wikipathways.org/) in which the genes are involved
- [x] Save an image of the final network and the session in [`results`](results)

## Results

- Initial results [`results`](results): Network analysis output with custom styling applied, but no manual adjustments.
- Arranged network [`results/arranged_network`](results/arranged_network): Enhanced network visualization, featuring:
    - Layout optimization: Different Cytoscape layouts applied for better organization.
    - Manual adjustments: Nodes and edges repositioned for improved clarity.

The code is located in [`notebooks/task_network.ipynb`](notebooks/task_network.ipynb)

To run the code a [conda](https://docs.anaconda.com/miniconda/) environment needs to be set up using [
`environment.yml`](environment.yml)

```bash
conda env create -f environment.yml
```

