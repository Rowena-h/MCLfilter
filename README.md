# MCLfilter

A tool to filter [**MCL**](https://micans.org/mcl/) output from orthologue detection analysis into single-copy orthologous clusters ready for alignment.

## Requirements

MCLfilter is a bash script which runs in the command line. To download, simply use:

```
git clone https://github.com/Rowena-h/MCLfilter.git
```

Make the script executable with:

```
chmod +x MCLfilter
```

## Usage

Option | Description
------ | -----------
-h, --help | Display these options
-i, --input | An MCL output file containing clusters of gene names on one line, separated by tabs
-t, --taxa | A file containing a list of the taxon names used in the orthologue clustering
-m, --minimum | Minimum number of taxa required in a cluster i.e. amount of missing data allowed (must not exceed total number of genomes)
-f, --fasta | Directory of fasta files from which orthologues were clustered
-l, --length | Minimum sequence length, default 180

### Example

```
./MCLfilter -i ort.group -t taxon_list -m 4 -f fasta_files/
```

To see an example run, refer to the [sample](https://github.com/Rowena-h/MCLfilter/tree/master/sample) directory.
