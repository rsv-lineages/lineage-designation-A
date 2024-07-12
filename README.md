# Lineage designations for RSV-A
This repository contains the definitions of lineages for RSV-A following the proposal put forward in [**Standardized Phylogenetic Classification of Human Respiratory Syncytial Virus Below the Subgroup Level**](https://wwwnc.cdc.gov/eid/article/30/8/24-0209_article) by Goya et al and the RSV Genotyping Consensus Consortium.

Please refer to the preprint for an in-depth discussion of the lineages and nomenclature. You can assign your own sequence data to the different lineages using [Nextclade](https://clades.nextstrain.org) or [UShER](https://genome.ucsc.edu/cgi-bin/hgPhyloPlace).

## [Summary of designated lineages](.auto-generated/clades.md)


## Lineage maintenance

To define a new lineage, add "lineage YAML" file to the folder `lineages`. These files have the following format
```yaml
defining_mutations:
- locus: F
  position: 540
  state: L
- locus: F
  position: 547
  state: F
- locus: L
  position: 174
  state: G
name: A.2
parent: A
representatives:
- MG642040
- MG642058
- MG642032
- MG642024
- MG642079
- MG642083
unaliased_name: A.2
```

Once a new yaml file got added and merged into master, run the helper scripts to regenerate the autogenerated markdown summaries and clade-tsv files.
```shell
python ../helper-scripts/generate_markdown_summary.py --input-dir lineages --lineage A
python ../helper-scripts/construct_tsv.py --input-dir lineages --output-tsv .auto-generated/lineages.tsv
```
