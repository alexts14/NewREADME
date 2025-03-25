# 24.03.2025
## Ref genome indexing with the GTF file
To do this we have to encrease the swap to around 35-40 GB because the indexing needs that size of RAM and it cannot be completed in any other way in my computer.
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       601Mi       7.2Gi       3.1Mi       224Mi       7.2Gi
Swap:          4.0Gi          0B       4.0Gi
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ sudo swapoff -a
sudo rm -f /swapfile
[sudo] password for alexts14:
Sorry, try again.
[sudo] password for alexts14:
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ sudo fallocate -l 36G /swapfile
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ls -lh /swapfile
-rw------- 1 root root 36G Mar 24 14:14 /swapfile
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ sudo chmod 600 /swapfile
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ sudo mkswap /swapfile
mkswap: /swapfile: warning: wiping old swap signature.
Setting up swapspace version 1, size = 36 GiB (38654701568 bytes)
no label, UUID=fedb0de3-9dae-4276-a90f-fdb482ba4a5c
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ sudo swapon /swapfile
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       625Mi       7.2Gi       3.1Mi       237Mi       7.1Gi
Swap:           35Gi          0B        35Gi
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$
```
Swap-supercharged 🔋 — STAR will now have \~43–44 GB total memory (RAM + swap), which is more than enough to build the full index with the GTF file included.
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ mkdir -p ~/NMR_project/star_index_full
TAR --runThreadN 4 \
     --runMode genomeGenerate \
     --genomeDir ~/NMR_project/star_index_full \
     --genomeFastaFiles ~/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna \
     --sjdbGTFfile ~/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
     --sjdbOverhang 99
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ STAR --runThreadN 4 \
>      --runMode genomeGenerate \
>      --genomeDir ~/NMR_project/star_index_full \
>      --genomeFastaFiles ~/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna \
>      --sjdbGTFfile ~/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
>      --sjdbOverhang 99
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --runMode genomeGenerate --genomeDir /home/alexts14/NMR_project/star_index_full --genomeFastaFiles /home/alexts14/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna --sjdbGTFfile /home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99
        STAR version: 2.7.11b   compiled: 2024-11-25T09:14:51+0000 :/opt/conda/conda-bld/star_1732525954305/work/source
Mar 24 14:18:59 ..... started STAR run
Mar 24 14:18:59 ... starting to generate Genome files
Mar 24 14:20:23 ..... processing annotations GTF
Mar 24 14:21:07 ... starting to sort Suffix Array. This may take a long time...
Mar 24 14:21:29 ... sorting Suffix Array chunks and saving them to disk...
```
Started the indexing that will probably take a long time ( time need)

# 25.03.2025
## STAR indexing is still running
Unfortunately i did a ^C in the indexing by accident and I killed it and now i am running it again.
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ mkdir -p ~/NMR_project/star_index_full
TAR --runThreadN 4 \
     --runMode genomeGenerate \
     --genomeDir ~/NMR_project/star_index_full \
     --genomeFastaFiles ~/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna \
     --sjdbGTFfile ~/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
     --sjdbOverhang 99
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ STAR --runThreadN 4 \
>      --runMode genomeGenerate \
>      --genomeDir ~/NMR_project/star_index_full \
>      --genomeFastaFiles ~/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna \
>      --sjdbGTFfile ~/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
>      --sjdbOverhang 99
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --runMode genomeGenerate --genomeDir /home/alexts14/NMR_project/star_index_full --genomeFastaFiles /home/alexts14/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna --sjdbGTFfile /home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99
        STAR version: 2.7.11b   compiled: 2024-11-25T09:14:51+0000 :/opt/conda/conda-bld/star_1732525954305/work/source
Mar 24 14:18:59 ..... started STAR run
Mar 24 14:18:59 ... starting to generate Genome files
Mar 24 14:20:23 ..... processing annotations GTF
Mar 24 14:21:07 ... starting to sort Suffix Array. This may take a long time...
Mar 24 14:21:29 ... sorting Suffix Array chunks and saving them to disk...
^C
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -n 20 ~/NMR_project/star_index_full/Log.out
MT      RefSeq  exon    15360   15425   .       -       .       gene_id "ENSHGLG00100000037"; gene_version "1"; transcript_id "ENSHGLT00100000037"; transcript_version "1"; exon_number "1"; gene_source "RefSeq"; gene_biotype "Mt_tRNA"; transcript_source "RefSeq"; transcript_biotype "Mt_tRNA"; exon_id "ENSHGLE00100000037"; exon_version "1"; tag "Ensembl_canonical";
Processing pGe.sjdbGTFfile=/home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf, found:
                2768 transcripts
                20594 exons (non-collapsed)
                8928 collapsed junctions
Total junctions: 8928
Mar 24 14:20:37 ..... finished GTF processing

Estimated genome size with padding and SJs: total=genome+SJ=2703523776 = 2504523776 + 199000000
GstrandBit=32
Number of SA indices: 4996924032
Mar 24 14:21:07 ... starting to sort Suffix Array. This may take a long time...
Number of chunks: 11;   chunks size limit: 3898642832 bytes
Mar 24 14:21:29 ... sorting Suffix Array chunks and saving them to disk...
Writing 3730453064 bytes into /home/alexts14/NMR_project/star_index_full//SA_0 ; empty space on disk = 929073672192 bytes ... done
Writing 3759292744 bytes into /home/alexts14/NMR_project/star_index_full//SA_1 ; empty space on disk = 925362700288 bytes ... done
Writing 3894598048 bytes into /home/alexts14/NMR_project/star_index_full//SA_2 ; empty space on disk = 921608896512 bytes ... done
Writing 3809661048 bytes into /home/alexts14/NMR_project/star_index_full//SA_3 ; empty space on disk = 917714034688 bytes ... done
Writing 3732790344 bytes into /home/alexts14/NMR_project/star_index_full//SA_4 ; empty space on disk = 913913569280 bytes ... done
Writing 3895950056 bytes into /home/alexts14/NMR_project/star_index_full//SA_5 ; empty space on disk = 910180274176 bytes ... done
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ STAR --runThreadN 4 \
>      --runMode genomeGenerate \
   --gen>      --genomeDir ~/NMR_project/star_index_full \
>      --genomeFastaFiles ~/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna \
--sjdbGTFfile ~/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
     --sjdbOverhang 99
>      --sjdbGTFfile ~/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
>      --sjdbOverhang 99
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --runMode genomeGenerate --genomeDir /home/alexts14/NMR_project/star_index_full --genomeFastaFiles /home/alexts14/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna --sjdbGTFfile /home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99
        STAR version: 2.7.11b   compiled: 2024-11-25T09:14:51+0000 :/opt/conda/conda-bld/star_1732525954305/work/source
Mar 25 12:40:06 ..... started STAR run
Mar 25 12:40:06 ... starting to generate Genome files
Mar 25 12:41:27 ..... processing annotations GTF
Mar 25 12:42:17 ... starting to sort Suffix Array. This may take a long time...
Mar 25 12:42:40 ... sorting Suffix Array chunks and saving them to disk...
```
