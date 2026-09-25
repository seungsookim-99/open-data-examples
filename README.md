# open-data-examples

Example notebooks for datasets published by the Choi Lab, Korea University College of
Medicine, on the [Registry of Open Data on AWS](https://registry.opendata.aws/).

Maintained by Seungsoo Kim on behalf of the Choi Lab.

| Directory | Dataset | Notebook |
| --- | --- | --- |
| `kova3/` | Korean Variant Archive 3 (KOVA3) | [`get-to-know-a-dataset.ipynb`](kova3/get-to-know-a-dataset.ipynb) |

Dataset documentation lives with each dataset:

- KOVA3: https://github.com/ku-choi-lab/kova3

## Running the notebooks

The notebooks read the open tier from Amazon S3 without credentials. Install the
dependencies and start Jupyter:

```bash
python3 -m pip install boto3 botocore numpy polars pyarrow matplotlib jupyterlab
jupyter lab
```

`bcftools` is needed for the VCF streaming cells:

```bash
conda install -c bioconda bcftools   # or: brew install bcftools
```

The gnomAD comparison cell also needs a local GRCh38 analysis-set FASTA, used to
left-align indels on both sides of the comparison. Set `REF_FASTA` in that cell
to its path.

## License

Notebook code in this repository is released under the MIT License; see
[LICENSE](LICENSE). The datasets themselves carry their own licenses; see each
dataset's documentation repository.
