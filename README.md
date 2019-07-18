# ad hoc analyses of three RSeQC runs

## bam_stat

## clipping_profile
```sh
for f in clipping_profile/*.r; do sed -n '2,4 p' $f; done
```
## deletion_profile
```sh
for f in deletion_profile/*.r; do sed -n '2,4 p' $f; done |tr '\n' ';'| sed 's/plot/lines/2g;s/blue/red/2;s/blue/darkgreen/2' > p.r
```
```r
source('p.r')
legend("topright",c('K562','ARVM-g1','ARVM-g2'),col=c('blue','red','darkgreen'),lty=1,lwd=2)
```
## divide_bam

## FPKM_count

## geneBody_coverage

## geneBody_coverage2

## infer_experiment

## inner_distance
```sh
grep 'fragsize=' inner_distance/*.r|sed 's/inner_distance\//data.frame(sample="/;s/\.inner_distance.*:/",/' > p.r
```
```r
ggplot(df, aes(x=fragsize, color=sample)) + geom_density()
```
## insertion_profile
```sh
for f in insertion_profile/*.r; do sed -n '2,5 p' $f; done |tr '\n' ';'| sed 's/plot/lines/2g;s/blue/red/2;s/blue/darkgreen/2' > p.r
for f in insertion_profile/*.r; do sed -n '8,11 p' $f; done |tr '\n' ';'| sed 's/plot/lines/2g;s/blue/red/2;s/blue/darkgreen/2' > p1.r
```
## junction_annotation

## junction_saturation

## mismatch_profile

## normalize_bigwig

## overlay_bigwig

## read_distribution

## read_duplication

## read_GC

## read_hexamer

## read_NVC

## read_quality

## RNA_fragment_size

## RPKM_count

## RPKM_saturation

## spilt_bam

## split_paired_bam

## tin
