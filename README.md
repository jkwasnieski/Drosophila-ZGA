# Drosophila-ZGA
Supplemental Code for Kwasnieski et al. (2019), Genome Research

These scripts were originally written by Yarden Katz, https://github.com/yarden/rnaseqlib
/events/parseTables.py and /events/SpliceGraph.py were modified for the intron analysis in Kwasnieski et al. (2019)
gff_make_annotation.py was used but without modification

To make annotations:
1) Clone and install rnaseqlib from  https://github.com/yarden/rnaseqlib
2) Replace /events/parseTables.py and /events/SpliceGraph.py with modified versions
3) Navigate to ./rnaseqlib/gff/
4) Copy your genePred file to this directory and re-name it “refGene.txt”. The rnaseqlib code will only load genePred tables if they are named ensGene.txt, refGene.txt or knownGene.txt. Will only need to be done once per genome.
5) Execute “python gff_make_annotation.py ./ $outdir --flanking-rule commonshortest --genome-label xxx” where xxx is what you want your annotations to be named