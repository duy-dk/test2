
samtools calmd - calculates MD and NM tags
http://www.htslib.org/doc/samtools-calmd.html
### Synopsis
'''
samtools calmd [-Eeubr][-C capQcoef] aln.bam ref.fasta
'''

output sam file

hg19
/media/bio06/portable_drive/genome_ref/hg19/hg19.fa.gz
### index hg19
### index bam file

samtools calmd -b /media/bio06/portable_drive/pd_bam/BSAn_PD89_R1_val_1_bismark_bt2_pe.bam \
/media/bio06/portable_drive/genome_ref/hg19/hg19.fa.gz \
1> calmd.bam \
2> /dev/null

./revelio.py calmd.bam masked.bam

./revelio.py -T 10 -f /media/bio06/portable_drive/genome_ref/hg19/hg19.fa /media/bio06/portable_drive/pd_bam/BSAn_PD89_R1_val_1_bismark_bt2_pe.bam masked.bam

