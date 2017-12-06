# htseq-count-cluster
A cli wrapper for running [htseq](https://github.com/simon-anders/htseq)'s `htseq-count` on a cluster.

## Install
`pip install git+https://github.com/datasnakes/htseq-analysis-scripts.git`

## Features
- For use with large datasets (we've previously used a dataset of 120 different human samples)
- For use with SGE/SGI cluster systems
- Submits multiple jobs
- Command line interface/script
- Merges counts files into one counts table/csv file


### Command-line options
```
usage: htseq_count_cluster.py [-h] [-p INPATH] [-f INFILE] [-g GTF]
                              [-o OUTPATH] [-e EMAIL]

This is a command line wrapper around htseq-count.

optional arguments:
  -h, --help            show this help message and exit
  -p INPATH, --inpath INPATH
                        Path of your samples/sample folders.
  -f INFILE, --infile INFILE
                        Name or path to your input csv file.
  -g GTF, --gtf GTF     Name or path to your gtf/gff file.
  -o OUTPATH, --outpath OUTPATH
                        Directory of your output counts file. The counts file
                        will be named.
  -e EMAIL, --email EMAIL
                        Email address to send script completion to.

*Ensure that htseq-count is in your path.

```

### Examples

```bash
python htseq_count_cluster.py -p path/to/samples/ -f samples.csv -g genes.gtf -o path/to/cluster-output/
```
This script uses logzero so there will be color coded logging information to your shell.

A common linux practice is to use `screen` to create a new shell and run a program
so that if it does produce output to the stdout/shell, the user can exit that particular
shell without the program ending and utilize another shell.


## ToDo
- [ ] Monitor Jobs
- [ ] Enhance wrapper input for other use cases.


## Maintainers
Shaurita Hutchins | [@sdhutchins](https://github.com/sdhutchins) | [✉](mailto:sdhutchins@outlook.com)

Rob Gilmore | [@grabear](https://github.com/grabear) | [✉](mailto:robgilmore127@gmail.com)


## Help
Please feel free to [open an issue](https://github.com/datasnakes/htseq-count-cluster/issues/new) if you have a question/feedback/problem
or [submit a pull request](https://github.com/datasnakes/htseq-count-cluster/compare) to add a feature/refactor/etc. to this project.
