IWHMB
================
YuHong Huang

<!-- README.md is generated from README.Rmd. Please edit that file -->

# IWHMB

The goal of IWHMB is to calculate Individual Weighted Hallmark Gene Set
Mutation burden,Details of algorithm principles will be further
published after the article is published

## Installation

You can install the development version of IWHMB thrugh Through github
or source code

## Example

### color table set

``` r
library(ggsci)
my_pal = c(pal_npg()(12), pal_aaas()(12), pal_futurama()(12))
my_pal = my_pal[!is.na(my_pal)]
my_pal = my_pal[!duplicated(my_pal)]
```

### Creat a PathObject

``` r
library(IWHMB)
TCGA_PathObj = CreatePathObject(gmt_path="test/data/h.all.v7.4.symbols.gmt",
                                gene_exp_counts='test/data/TCGA_HNSC_gene_exp_count.csv',
                                gene_map='test/data/Homo_sapiens.GRCh38.99.chr.gtf',
                                gene_exp_TPM="test/data/TCGA_HNSC_gene_exp_TPM_tumor.csv",
                                ppi_data_path="test/data/ppi_dataset_all.txt",
                                cor_method=1,
                                mut_exp="test/data/TCGA-HNSC_UCSC.varscan2_snv.tsv.gz",
                                count_log=FALSE,
                                TPM_log=FALSE,
                                GeneSetCollect=FALSE,
                                sep = "\t")
```
