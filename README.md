# exfi_validation: A Snakemake workflow to validate exfi's performance

[![Build Status](https://travis-ci.org/jlanga/exfi_validation.svg?branch=master)](https://travis-ci.org/jlanga/exfi_validation)

## 1. Description

Workflow to:

<!---- Trim genomic reads (trimmomatic) -->
- Find putative exons (exfi, abyss-bloom)
<!---- Map agaist different exonic, transcriptomic and genomic references (bwa + samtools) -->
- Make reports

## 2. First steps

Follow the contents of the `.travis.yml` file:

0. Install (ana|mini)conda

- [Anaconda](https://www.continuum.io/downloads)

- [miniconda](http://conda.pydata.org/miniconda.html)

1. Install snakemake
    ```sh
    conda install snakemake
    ```

2. Execute the pipeline. Snakemake will take care of the dependencies:

    ```sh
    snakemake --use-conda -j 20
    ```

Once you know it works, edit the `config.yaml` with paths to your data


## 3. File organization

The hierarchy of the folder is the one described in [A Quick Guide to Organizing Computational Biology Projects](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424):

```
smsk
├── bin: your binaries, scripts, installation and virtualenv related files.
├── data: raw data, hopefully links to backup data.
├── README.md
├── results: processed data.
└── src: additional source code, tarballs, etc.
```


## Bibliography

- [A Quick Guide to Organizing Computational Biology Projects](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424)

- [Snakemake—a scalable bioinformatics workflow engine](http://bioinformatics.oxfordjournals.org/content/28/19/2520)

- [biobloomtools]()

- [abyss]()

- [bedtools]()
