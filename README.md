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
legend("topright",c('ARVM-g1','ARVM-g2','K562'),col=c('blue','red','darkgreen'),lty=1,lwd=2)
```
## divide_bam

## FPKM_count

## geneBody_coverage

## geneBody_coverage2

## infer_experiment

## inner_distance

## insertion_profile

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
