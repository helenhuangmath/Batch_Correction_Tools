# Batch Correction Tools

### Several ways to remove batch correction:

#### 1. SVA package, ComBat method

Ref: 

https://bioconductor.org/packages/release/bioc/vignettes/sva/inst/doc/sva.pdf

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3307112/

```
sva::ComBat()
```


#### 2. Limma package, removeBatchEffect method 

Ref (usage in DESeq2): 
http://bioconductor.org/packages/devel/bioc/vignettes/DESeq2/inst/doc/DESeq2.html

```
limma::removeBatchEffect()
```


#### 3. RUVSeq package, RUVs() 

Ref: 
http://bioconductor.org/packages/release/bioc/vignettes/RUVSeq/inst/doc/RUVSeq.pdf

```
RUVs()
RUVr()
```


#### 4. Regress out batch in DESeq2 with design formula:

```
dds <- DESeqDataSetFromMatrix(countData = cts,
                              colData = coldata,
                              design= ~ batch + condition)
dds <- DESeq(dds)
```


#### Other Ref: 

https://journals.plos.org/plosone/article/file?id=10.1371/journal.pone.0159921&type=printable

