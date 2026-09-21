# open-data-examples

Example notebooks for datasets published by the Choi Lab, Korea University College of
Medicine, on the [Registry of Open Data on AWS](https://registry.opendata.aws/).

Maintained by Seungsoo Kim on behalf of the Choi Laboratory.

| Directory | Dataset | Notebook |
| --- | --- | --- |
| `kova3/` | Korean Variant Archive 3 (KOVA3) | [`get-to-know-a-dataset.ipynb`](kova3/get-to-know-a-dataset.ipynb) |

Dataset documentation lives with each dataset:

- KOVA3: https://github.com/KuChoiLab/kova3

## Running the notebooks

The notebooks read the open tier from Amazon S3 without credentials. Install the
dependencies and start Jupyter:

```bash
python3 -m pip install boto3 botocore polars pyarrow matplotlib jupyterlab
jupyter lab
```

`bcftools` is needed for the VCF streaming cells:

```bash
conda install -c bioconda bcftools   # or: brew install bcftools
```

## Licence

Notebook code in this repository is released under the MIT Licence. The datasets
themselves carry their own licences; see each dataset's documentation repository.
