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
# 26.03.2025
# Indexing correctly running
```
 System information as of Wed Mar 26 09:49:11 CET 2025

  System load:  1.4                  Processes:             33
  Usage of /:   11.4% of 1006.85GB   Users logged in:       1
  Memory usage: 96%                  IPv4 address for eth0: 172.28.149.249
  Swap usage:   17%

 * Strictly confined Kubernetes makes edge and IoT secure. Learn how MicroK8s
   just raised the bar for easy, resilient and secure K8s cluster deployment.

   https://ubuntu.com/engage/secure-kubernetes-at-the-edge

This message is shown once a day. To disable it please create the
/home/alexts14/.hushlogin file.
conda activate NMR-env(base) alexts14@GabanouMelissa:~$ conda activate NMR-env
(NMR-env) alexts14@GabanouMelissa:~$ cd ~/NMR_project
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ top
top - 09:51:51 up 1 day, 23:40,  1 user,  load average: 1.13, 1.15, 1.06
Tasks:  29 total,   1 running,  28 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.1 sy,  0.0 ni, 91.6 id,  8.3 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :   7945.2 total,    230.4 free,   7814.7 used,     57.8 buff/cache
MiB Swap:  36864.0 total,  30379.7 free,   6484.3 used.    130.5 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
   2953 alexts14  20   0   11.5g   7.1g    164 D   0.6  91.9 156:34.56 STAR-avx2
      1 root      20   0   21832   1644    180 S   0.0   0.0   0:14.40 systemd
      2 root      20   0    2776     52     52 S   0.0   0.0   0:00.11 init-systemd(Ub
      7 root      20   0    2812      4      4 S   0.0   0.0   0:08.14 init
     91 root      19  -1   66752   3764   3304 S   0.0   0.0   0:28.71 systemd-journal
    139 root      20   0   24124   2148   1692 S   0.0   0.0   0:01.46 systemd-udevd
    229 systemd+  20   0   21452    556    412 S   0.0   0.0   0:01.61 systemd-resolve
    230 systemd+  20   0   91020    236    172 S   0.0   0.0   0:05.21 systemd-timesyn
    247 root      20   0    4236     92      0 S   0.0   0.0   0:00.62 cron
    248 message+  20   0    9592    356      0 S   0.0   0.0   0:10.18 dbus-daemon
    261 root      20   0   17976    176      0 S   0.0   0.0   0:04.02 systemd-logind
    265 root      20   0 2052432   2840      0 S   0.0   0.0   0:37.92 wsl-pro-service
    271 root      20   0    3160      0      0 S   0.0   0.0   0:00.01 agetty
    278 root      20   0    3116      0      0 S   0.0   0.0   0:00.01 agetty
    281 syslog    20   0  222508    404      0 S   0.0   0.0   0:03.55 rsyslogd
    290 root      20   0  107012      0      0 S   0.0   0.0   0:00.20 unattended-upgr
    334 root      20   0    2780      0      0 S   0.0   0.0   0:00.00 SessionLeader
    335 root      20   0    2780      0      0 S   0.0   0.0   0:00.06 Relay(336)
    336 alexts14  20   0    6204     24     24 S   0.0   0.0   0:00.19 bash
    337 root      20   0    6656      0      0 S   0.0   0.0   0:00.02 login
    489 alexts14  20   0   20264   1020    504 S   0.0   0.0   0:01.08 systemd
    490 alexts14  20   0   21144      0      0 S   0.0   0.0   0:00.00 (sd-pam)
    503 alexts14  20   0    6072      4      4 S   0.0   0.0   0:00.05 bash
    984 polkitd   20   0  308160    176      0 S   0.0   0.0   0:04.47 polkitd
   2948 alexts14  20   0    4756      0      0 S   0.0   0.0   0:00.00 STAR
   4186 root      20   0    2780     64      8 S   0.0   0.0   0:00.00 SessionLeader
   4187 root      20   0    2780     72      8 S   0.0   0.0   0:00.02 Relay(4188)
   4188 alexts14  20   0    6204   5220   3448 S   0.0   0.1   0:00.11 bash
   4255 alexts14  20   0    9336   5148   3000 R   0.0   0.1   0:00.07 top
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -f ~/NMR_project/star_index_full/Log.out
Mar 25 12:42:17 ... starting to sort Suffix Array. This may take a long time...
Number of chunks: 11;   chunks size limit: 3898642832 bytes
Mar 25 12:42:40 ... sorting Suffix Array chunks and saving them to disk...
Writing 3730453064 bytes into /home/alexts14/NMR_project/star_index_full//SA_0 ; empty space on disk = 910014525440 bytes ... done
Writing 3759292744 bytes into /home/alexts14/NMR_project/star_index_full//SA_1 ; empty space on disk = 910043119616 bytes ... done
Writing 3894598048 bytes into /home/alexts14/NMR_project/star_index_full//SA_2 ; empty space on disk = 910178263040 bytes ... done
Writing 3809661048 bytes into /home/alexts14/NMR_project/star_index_full//SA_3 ; empty space on disk = 910093176832 bytes ... done
Writing 3732790344 bytes into /home/alexts14/NMR_project/star_index_full//SA_4 ; empty space on disk = 910015086592 bytes ... done
Writing 3895950056 bytes into /home/alexts14/NMR_project/star_index_full//SA_5 ; empty space on disk = 910177398784 bytes ... done
Writing 3860360648 bytes into /home/alexts14/NMR_project/star_index_full//SA_6 ; empty space on disk = 906281103360 bytes ... done
```
That means STAR has successfully written 7 of the 11 total Suffix Array chunks. 
## Ubuntu crashed again and the index was incomplete. 
I now re-run it with the option to work also in the backgroud so that even if the window will close it will still work (nohup). 
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -f ~/NMR_project/star_index_full/Log.out
Mar 25 12:42:17 ... starting to sort Suffix Array. This may take a long time...
Number of chunks: 11;   chunks size limit: 3898642832 bytes
Mar 25 12:42:40 ... sorting Suffix Array chunks and saving them to disk...
Writing 3730453064 bytes into /home/alexts14/NMR_project/star_index_full//SA_0 ; empty space on disk = 910014525440 bytes ... done
Writing 3759292744 bytes into /home/alexts14/NMR_project/star_index_full//SA_1 ; empty space on disk = 910043119616 bytes ... done
Writing 3894598048 bytes into /home/alexts14/NMR_project/star_index_full//SA_2 ; empty space on disk = 910178263040 bytes ... done
Writing 3809661048 bytes into /home/alexts14/NMR_project/star_index_full//SA_3 ; empty space on disk = 910093176832 bytes ... done
Writing 3732790344 bytes into /home/alexts14/NMR_project/star_index_full//SA_4 ; empty space on disk = 910015086592 bytes ... done
Writing 3895950056 bytes into /home/alexts14/NMR_project/star_index_full//SA_5 ; empty space on disk = 910177398784 bytes ... done
Writing 3860360648 bytes into /home/alexts14/NMR_project/star_index_full//SA_6 ; empty space on disk = 906281103360 bytes ... done


^C
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ^C
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ps aux | grep STAR
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
alexts14     527  0.0  0.0   4092  1984 pts/0    S+   10:38   0:00 grep --color=auto STAR
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -n 30 ~/NMR_project/star_index_full/Log.out
WARNING: while processing sjdbGTFfile=/home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf: chromosome 'MT' not found in Genome fasta files for line:
MT      RefSeq  exon    13548   14078   .       -       .       gene_id "ENSHGLG00100000033"; gene_version "1"; transcript_id "ENSHGLT00100000033"; transcript_version "1"; exon_number "1"; gene_name "ND6"; gene_source "RefSeq"; gene_biotype "protein_coding"; transcript_name "ND6-201"; transcript_source "RefSeq"; transcript_biotype "protein_coding"; exon_id "ENSHGLE00100000033"; exon_version "1"; tag "Ensembl_canonical";
WARNING: while processing sjdbGTFfile=/home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf: chromosome 'MT' not found in Genome fasta files for line:
MT      RefSeq  exon    14079   14146   .       -       .       gene_id "ENSHGLG00100000034"; gene_version "1"; transcript_id "ENSHGLT00100000034"; transcript_version "1"; exon_number "1"; gene_source "RefSeq"; gene_biotype "Mt_tRNA"; transcript_source "RefSeq"; transcript_biotype "Mt_tRNA"; exon_id "ENSHGLE00100000034"; exon_version "1"; tag "Ensembl_canonical";
WARNING: while processing sjdbGTFfile=/home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf: chromosome 'MT' not found in Genome fasta files for line:
MT      RefSeq  exon    14149   15283   .       +       .       gene_id "ENSHGLG00100000035"; gene_version "1"; transcript_id "ENSHGLT00100000035"; transcript_version "1"; exon_number "1"; gene_name "CYTB"; gene_source "RefSeq"; gene_biotype "protein_coding"; transcript_name "CYTB-201"; transcript_source "RefSeq"; transcript_biotype "protein_coding"; exon_id "ENSHGLE00100000035"; exon_version "1"; tag "Ensembl_canonical";
WARNING: while processing sjdbGTFfile=/home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf: chromosome 'MT' not found in Genome fasta files for line:
MT      RefSeq  exon    15289   15357   .       +       .       gene_id "ENSHGLG00100000036"; gene_version "1"; transcript_id "ENSHGLT00100000036"; transcript_version "1"; exon_number "1"; gene_source "RefSeq"; gene_biotype "Mt_tRNA"; transcript_source "RefSeq"; transcript_biotype "Mt_tRNA"; exon_id "ENSHGLE00100000036"; exon_version "1"; tag "Ensembl_canonical";
WARNING: while processing sjdbGTFfile=/home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf: chromosome 'MT' not found in Genome fasta files for line:
MT      RefSeq  exon    15360   15425   .       -       .       gene_id "ENSHGLG00100000037"; gene_version "1"; transcript_id "ENSHGLT00100000037"; transcript_version "1"; exon_number "1"; gene_source "RefSeq"; gene_biotype "Mt_tRNA"; transcript_source "RefSeq"; transcript_biotype "Mt_tRNA"; exon_id "ENSHGLE00100000037"; exon_version "1"; tag "Ensembl_canonical";
Processing pGe.sjdbGTFfile=/home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf, found:
                2768 transcripts
                20594 exons (non-collapsed)
                8928 collapsed junctions
Total junctions: 8928
Mar 25 12:41:41 ..... finished GTF processing

Estimated genome size with padding and SJs: total=genome+SJ=2703523776 = 2504523776 + 199000000
GstrandBit=32
Number of SA indices: 4996924032
Mar 25 12:42:17 ... starting to sort Suffix Array. This may take a long time...
Number of chunks: 11;   chunks size limit: 3898642832 bytes
Mar 25 12:42:40 ... sorting Suffix Array chunks and saving them to disk...
Writing 3730453064 bytes into /home/alexts14/NMR_project/star_index_full//SA_0 ; empty space on disk = 910014525440 bytes ... done
Writing 3759292744 bytes into /home/alexts14/NMR_project/star_index_full//SA_1 ; empty space on disk = 910043119616 bytes ... done
Writing 3894598048 bytes into /home/alexts14/NMR_project/star_index_full//SA_2 ; empty space on disk = 910178263040 bytes ... done
Writing 3809661048 bytes into /home/alexts14/NMR_project/star_index_full//SA_3 ; empty space on disk = 910093176832 bytes ... done
Writing 3732790344 bytes into /home/alexts14/NMR_project/star_index_full//SA_4 ; empty space on disk = 910015086592 bytes ... done
Writing 3895950056 bytes into /home/alexts14/NMR_project/star_index_full//SA_5 ; empty space on disk = 910177398784 bytes ... done
Writing 3860360648 bytes into /home/alexts14/NMR_project/star_index_full//SA_6 ; empty space on disk = 906281103360 bytes ... done
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       585Mi       6.7Gi       3.1Mi       682Mi       7.2Gi
Swap:          4.0Gi          0B       4.0Gi
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ sudo swapon /swapfile
[sudo] password for alexts14:
Sorry, try again.
[sudo] password for alexts14:
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       612Mi       6.7Gi       3.1Mi       683Mi       7.2Gi
Swap:           39Gi          0B        39Gi
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ rm -r ~/NMR_project/star_index_full/*
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ nohup STAR --runThreadN 4 \
>      --runMode genomeGenerate \
>      --genomeDir ~/NMR_project/star_index_full \
>      --genomeFastaFiles ~/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna \
>      --sjdbGTFfile ~/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
>      --sjdbOverhang 99 > star_log.txt 2>&1 &
[1] 537
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -f star_log.txt
nohup: ignoring input
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --runMode genomeGenerate --genomeDir /home/alexts14/NMR_project/star_index_full --genomeFastaFiles /home/alexts14/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna --sjdbGTFfile /home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99
        STAR version: 2.7.11b   compiled: 2024-11-25T09:14:51+0000 :/opt/conda/conda-bld/star_1732525954305/work/source
Mar 26 10:43:04 ..... started STAR run
Mar 26 10:43:04 ... starting to generate Genome files
^C
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ps aux | grep STAR
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
alexts14     537  0.0  0.0   4756  1884 pts/0    S    10:43   0:00 /bin/bash /home/alexts14/miniconda3/envs/NMR-env/bin/STAR --runThreadN 4 --runMode genomeGenerate --genomeDir /home/alexts14/NMR_project/star_index_full --genomeFastaFiles /home/alexts14/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna --sjdbGTFfile /home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99
alexts14     542 77.3 59.8 4901592 4873376 pts/0 R    10:43   0:58 /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --runMode genomeGenerate --genomeDir /home/alexts14/NMR_project/star_index_full --genomeFastaFiles /home/alexts14/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna --sjdbGTFfile /home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99
alexts14     545  0.0  0.0   4092  1924 pts/0    S+   10:44   0:00 grep --color=auto STAR
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ top
top - 10:44:39 up 10 min,  1 user,  load average: 0.81, 0.37, 0.20
Tasks:  25 total,   2 running,  23 sleeping,   0 stopped,   0 zombie
%Cpu(s):  5.6 us,  0.4 sy,  0.0 ni, 91.4 id,  2.6 wa,  0.0 hi,  0.1 si,  0.0 st
MiB Mem :   7945.2 total,    123.7 free,   5361.8 used,   2695.6 buff/cache
MiB Swap:  40960.0 total,  40920.4 free,     39.6 used.   2583.4 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
    542 alexts14  20   0 4901592   4.6g   5092 R  67.8  59.8   1:12.70 STAR-avx2
      1 root      20   0   21676  12304   9412 S   0.0   0.2   0:00.87 systemd
      2 root      20   0    2776   1836   1796 S   0.0   0.0   0:00.01 init-systemd(Ub
      7 root      20   0    2776    132    132 S   0.0   0.0   0:00.00 init
     79 root      19  -1   50436  14576  13400 S   0.0   0.2   0:00.27 systemd-journal
    126 root      20   0   24124   5032   3712 S   0.0   0.1   0:00.22 systemd-udevd
    214 systemd+  20   0   21452  11836   9644 S   0.0   0.1   0:00.19 systemd-resolve
    215 systemd+  20   0   91020   6512   5664 S   0.0   0.1   0:00.12 systemd-timesyn
    231 root      20   0    4236   2628   2388 S   0.0   0.0   0:00.01 cron
    232 message+  20   0    9588   4932   4376 S   0.0   0.1   0:00.10 dbus-daemon
    239 root      20   0   17976   8184   7164 S   0.0   0.1   0:00.12 systemd-logind
    244 root      20   0 1756096  17588  10960 S   0.0   0.2   0:00.16 wsl-pro-service
    250 root      20   0    3160   1136   1048 S   0.0   0.0   0:00.01 agetty
    254 root      20   0    3116   1140   1056 S   0.0   0.0   0:00.01 agetty
    256 syslog    20   0  222508   9296   4408 S   0.0   0.1   0:00.10 rsyslogd
    265 root      20   0  107012  19240   9912 S   0.0   0.2   0:00.21 unattended-upgr
    328 root      20   0    2780    140     80 S   0.0   0.0   0:00.00 SessionLeader
    329 root      20   0    2780    136     80 S   0.0   0.0   0:00.02 Relay(330)
    330 alexts14  20   0    6204   3352   2840 S   0.0   0.0   0:00.12 bash
    331 root      20   0    6660   4016   3764 S   0.0   0.0   0:00.02 login
    444 alexts14  20   0   20260  11364   9288 S   0.0   0.1   0:00.21 systemd
    445 alexts14  20   0   21148    508      0 S   0.0   0.0   0:00.00 (sd-pam)
    458 alexts14  20   0    6072   3744   2148 S   0.0   0.0   0:00.05 bash
    537 alexts14  20   0    4756   1884   1884 S   0.0   0.0   0:00.00 STAR
    546 alexts14  20   0    9336   5160   3004 R   0.0   0.1   0:00.01 top
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -f star_log.txt
nohup: ignoring input
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --runMode genomeGenerate --genomeDir /home/alexts14/NMR_project/star_index_full --genomeFastaFiles /home/alexts14/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna --sjdbGTFfile /home/alexts14/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99
        STAR version: 2.7.11b   compiled: 2024-11-25T09:14:51+0000 :/opt/conda/conda-bld/star_1732525954305/work/source
Mar 26 10:43:04 ..... started STAR run
Mar 26 10:43:04 ... starting to generate Genome files
Mar 26 10:44:52 ..... processing annotations GTF
Mar 26 10:45:32 ... starting to sort Suffix Array. This may take a long time...
Mar 26 10:45:55 ... sorting Suffix Array chunks and saving them to disk...
```
# 27.03.2025
# Final steps of indexing
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ls -lh ~/NMR_project/star_index_full
total 29G
-rw-r--r-- 1 alexts14 alexts14 284M Mar 27 08:48 Log.out
-rw-r--r-- 1 alexts14 alexts14 3.5G Mar 26 12:36 SA_0
-rw-r--r-- 1 alexts14 alexts14 3.6G Mar 26 15:02 SA_1
-rw-r--r-- 1 alexts14 alexts14 3.7G Mar 26 18:21 SA_2
-rw-r--r-- 1 alexts14 alexts14 3.6G Mar 26 21:20 SA_3
-rw-r--r-- 1 alexts14 alexts14 3.5G Mar 27 00:07 SA_4
-rw-r--r-- 1 alexts14 alexts14 3.7G Mar 27 03:15 SA_5
-rw-r--r-- 1 alexts14 alexts14 3.6G Mar 27 06:04 SA_6
-rw-r--r-- 1 alexts14 alexts14 3.5G Mar 27 08:48 SA_7
-rw-r--r-- 1 alexts14 alexts14  294 Mar 26 10:45 chrLength.txt
-rw-r--r-- 1 alexts14 alexts14  352 Mar 26 10:45 chrName.txt
-rw-r--r-- 1 alexts14 alexts14  646 Mar 26 10:45 chrNameLength.txt
-rw-r--r-- 1 alexts14 alexts14  346 Mar 26 10:45 chrStart.txt
-rw-r--r-- 1 alexts14 alexts14 657K Mar 26 10:45 exonGeTrInfo.tab
-rw-r--r-- 1 alexts14 alexts14 298K Mar 26 10:45 exonInfo.tab
-rw-r--r-- 1 alexts14 alexts14  69K Mar 26 10:45 geneInfo.tab
-rw-r--r-- 1 alexts14 alexts14 304K Mar 26 10:45 sjdbList.fromGTF.out.tab
-rw-r--r-- 1 alexts14 alexts14 179K Mar 26 10:45 transcriptInfo.tab
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$
```
The index file is progressing. 
# 28.03.2025
## The daily report
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -f star_log.txt
Mar 26 10:43:04 ..... started STAR run
Mar 26 10:43:04 ... starting to generate Genome files
Mar 26 10:44:52 ..... processing annotations GTF
Mar 26 10:45:32 ... starting to sort Suffix Array. This may take a long time...
Mar 26 10:45:55 ... sorting Suffix Array chunks and saving them to disk...
Mar 27 15:46:39 ... loading chunks from disk, packing SA...
Mar 27 16:01:25 ... finished generating suffix array
Mar 27 16:01:25 ... generating Suffix Array index
Mar 27 16:20:13 ... completed Suffix Array index
Mar 27 16:20:13 ..... inserting junctions into the genome indices
^C
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ls -lh ~/NMR_project/star_index_full
total 287M
-rw-r--r-- 1 alexts14 alexts14 284M Mar 28 05:17 Log.out
-rw-r--r-- 1 alexts14 alexts14  294 Mar 26 10:45 chrLength.txt
-rw-r--r-- 1 alexts14 alexts14  352 Mar 26 10:45 chrName.txt
-rw-r--r-- 1 alexts14 alexts14  646 Mar 26 10:45 chrNameLength.txt
-rw-r--r-- 1 alexts14 alexts14  346 Mar 26 10:45 chrStart.txt
-rw-r--r-- 1 alexts14 alexts14 657K Mar 26 10:45 exonGeTrInfo.tab
-rw-r--r-- 1 alexts14 alexts14 298K Mar 26 10:45 exonInfo.tab
-rw-r--r-- 1 alexts14 alexts14  69K Mar 26 10:45 geneInfo.tab
-rw-r--r-- 1 alexts14 alexts14 262K Mar 27 16:20 sjdbInfo.txt
-rw-r--r-- 1 alexts14 alexts14 304K Mar 26 10:45 sjdbList.fromGTF.out.tab
-rw-r--r-- 1 alexts14 alexts14 268K Mar 27 16:20 sjdbList.out.tab
-rw-r--r-- 1 alexts14 alexts14 179K Mar 26 10:45 transcriptInfo.tab
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ top
top - 10:08:31 up 2 days,  1:17,  1 user,  load average: 1.08, 1.12, 1.10
Tasks:  26 total,   1 running,  25 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.1 sy,  0.0 ni, 90.1 id,  9.8 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :   7945.2 total,    128.6 free,   7882.9 used,    124.7 buff/cache
MiB Swap:  40960.0 total,  21304.8 free,  19655.2 used.     62.2 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
    542 alexts14  20   0   26.9g   6.4g    340 D   1.7  82.2 244:57.65 STAR-avx2
      1 root      20   0   21676   3804   1800 S   0.0   0.0   0:15.60 systemd
      2 root      20   0    2776    152    152 S   0.0   0.0   0:00.02 init-systemd(Ub
      7 root      20   0    2792      4      4 S   0.0   0.0   0:00.13 init
     79 root      19  -1   66828   3456   2932 S   0.0   0.0   0:28.08 systemd-journal
    126 root      20   0   24124     72      0 S   0.0   0.0   0:00.81 systemd-udevd
    214 systemd+  20   0   21452    744    632 S   0.0   0.0   0:01.67 systemd-resolve
    215 systemd+  20   0   91020    968    892 S   0.0   0.0   0:05.49 systemd-timesyn
    231 root      20   0    4236    508    400 S   0.0   0.0   0:00.66 cron
    232 message+  20   0    9588    368      0 S   0.0   0.0   0:10.55 dbus-daemon
    239 root      20   0   17976    388    216 S   0.0   0.0   0:04.25 systemd-logind
    244 root      20   0 2274460   2316      0 S   0.0   0.0   0:42.45 wsl-pro-service
    250 root      20   0    3160      0      0 S   0.0   0.0   0:00.01 agetty
    254 root      20   0    3116      0      0 S   0.0   0.0   0:00.01 agetty
    256 syslog    20   0  222508    284      0 S   0.0   0.0   0:03.79 rsyslogd
    265 root      20   0  107012      0      0 S   0.0   0.0   0:00.21 unattended-upgr
    328 root      20   0    2780      0      0 S   0.0   0.0   0:00.00 SessionLeader
    329 root      20   0    2780    160    156 S   0.0   0.0   0:00.12 Relay(330)
    330 alexts14  20   0    6204   2208   1704 S   0.0   0.0   0:00.36 bash
    331 root      20   0    6660      0      0 S   0.0   0.0   0:00.02 login
    444 alexts14  20   0   20260   1780   1176 S   0.0   0.0   0:01.15 systemd
    445 alexts14  20   0   21148      0      0 S   0.0   0.0   0:00.00 (sd-pam)
    458 alexts14  20   0    6072      4      4 S   0.0   0.0   0:00.05 bash
    537 alexts14  20   0    4756      0      0 S   0.0   0.0   0:00.00 STAR
   1726 polkitd   20   0  308160    248      0 S   0.0   0.0   0:03.19 polkitd
   3286 alexts14  20   0    9396   5156   3004 R   0.0   0.1   0:00.10 top
```
The new update is:
```
cannot o(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -f star_log.txt
Mar 26 10:44:52 ..... processing annotations GTF
Mar 26 10:45:32 ... starting to sort Suffix Array. This may take a long time...
Mar 26 10:45:55 ... sorting Suffix Array chunks and saving them to disk...
Mar 27 15:46:39 ... loading chunks from disk, packing SA...
Mar 27 16:01:25 ... finished generating suffix array
Mar 27 16:01:25 ... generating Suffix Array index
Mar 27 16:20:13 ... completed Suffix Array index
Mar 27 16:20:13 ..... inserting junctions into the genome indices
Mar 28 12:13:32 ... writing Genome to disk ...
Mar 28 12:35:13 ... writing Suffix Array to disk ...
```
## Indexing has just finished
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ tail -f star_log.txt
Mar 26 10:44:52 ..... processing annotations GTF
Mar 26 10:45:32 ... starting to sort Suffix Array. This may take a long time...
Mar 26 10:45:55 ... sorting Suffix Array chunks and saving them to disk...
Mar 27 15:46:39 ... loading chunks from disk, packing SA...
Mar 27 16:01:25 ... finished generating suffix array
Mar 27 16:01:25 ... generating Suffix Array index
Mar 27 16:20:13 ... completed Suffix Array index
Mar 27 16:20:13 ..... inserting junctions into the genome indices
Mar 28 12:13:32 ... writing Genome to disk ...
Mar 28 12:35:13 ... writing Suffix Array to disk ...
Mar 28 14:55:16 ... writing SAindex to disk
Mar 28 15:00:10 ..... finished successfully
^C
[1]+  Done                    nohup STAR --runThreadN 4 --runMode genomeGenerate --genomeDir ~/NMR_project/star_index_full --genomeFastaFiles ~/NMR_project/GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna --sjdbGTFfile ~/NMR_project/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99 > star_log.txt 2>&1
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ls -lh ~/NMR_project/star_index_full
total 24G
-rw-r--r-- 1 alexts14 alexts14 2.4G Mar 28 12:33 Genome
-rw-r--r-- 1 alexts14 alexts14 284M Mar 28 15:00 Log.out
-rw-r--r-- 1 alexts14 alexts14  20G Mar 28 14:48 SA
-rw-r--r-- 1 alexts14 alexts14 1.5G Mar 28 14:55 SAindex
-rw-r--r-- 1 alexts14 alexts14  294 Mar 26 10:45 chrLength.txt
-rw-r--r-- 1 alexts14 alexts14  352 Mar 26 10:45 chrName.txt
-rw-r--r-- 1 alexts14 alexts14  646 Mar 26 10:45 chrNameLength.txt
-rw-r--r-- 1 alexts14 alexts14  346 Mar 26 10:45 chrStart.txt
-rw-r--r-- 1 alexts14 alexts14 657K Mar 26 10:45 exonGeTrInfo.tab
-rw-r--r-- 1 alexts14 alexts14 298K Mar 26 10:45 exonInfo.tab
-rw-r--r-- 1 alexts14 alexts14  69K Mar 26 10:45 geneInfo.tab
-rw-r--r-- 1 alexts14 alexts14  964 Mar 28 12:13 genomeParameters.txt
-rw-r--r-- 1 alexts14 alexts14 262K Mar 27 16:20 sjdbInfo.txt
-rw-r--r-- 1 alexts14 alexts14 304K Mar 26 10:45 sjdbList.fromGTF.out.tab
-rw-r--r-- 1 alexts14 alexts14 268K Mar 27 16:20 sjdbList.out.tab
-rw-r--r-- 1 alexts14 alexts14 179K Mar 26 10:45 transcriptInfo.tab
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$
```
# 31.03.2025
Now that the indexing of the genome is complete we can continue with some alignment tests. 
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ STAR --runThreadN 4 \
 --genom>      --genomeDir ~/NMR_project/star_index_full \
>      --readFilesIn SRR21882792_1.fastq SRR21882792_2.fastq \
 --outF>      --outFileNamePrefix SRR21882792_test_ \
>      --readMapNumber 100000 \
>      --outSAMtype BAM SortedByCoordinate
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --genomeDir /home/alexts14/NMR_project/star_index_full --readFilesIn SRR21882792_1.fastq SRR21882792_2.fastq --outFileNamePrefix SRR21882792_test_ --readMapNumber 100000 --outSAMtype BAM SortedByCoordinate
        STAR version: 2.7.11b   compiled: 2024-11-25T09:14:51+0000 :/opt/conda/conda-bld/star_1732525954305/work/source
Mar 31 13:55:20 ..... started STAR run
Mar 31 13:55:20 ..... loading genome

EXITING: fatal error trying to allocate genome arrays, exception thrown: std::bad_alloc
Possible cause 1: not enough RAM. Check if you have enough RAM 26699067469 bytes
Possible cause 2: not enough virtual memory allowed with ulimit. SOLUTION: run ulimit -v 26699067469

Mar 31 13:55:20 ...... FATAL ERROR, exiting
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ulimit -v
unlimited
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       582Mi       7.1Gi       3.1Mi       322Mi       7.2Gi
Swap:          4.0Gi          0B       4.0Gi
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ls -lh /swapfile
-rw------- 1 root root 36G Mar 24 14:14 /swapfile
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ sudo swapon /swapfile
[sudo] password for alexts14:
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       609Mi       7.1Gi       3.1Mi       323Mi       7.2Gi
Swap:           39Gi          0B        39Gi
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ STAR --runThreadN 4 \
>      --genomeDir ~/NMR_project/star_index_full \
>      --readFilesIn SRR21882792_1.fastq SRR21882792_2.fastq \
>      --outFileNamePrefix SRR21882792_test_ \
>      --readMapNumber 100000 \
>      --outSAMtype BAM SortedByCoordinate
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --genomeDir /home/alexts14/NMR_project/star_index_full --readFilesIn SRR21882792_1.fastq SRR21882792_2.fastq --outFileNamePrefix SRR21882792_test_ --readMapNumber 100000 --outSAMtype BAM SortedByCoordinate
        STAR version: 2.7.11b   compiled: 2024-11-25T09:14:51+0000 :/opt/conda/conda-bld/star_1732525954305/work/source
Mar 31 13:58:15 ..... started STAR run
Mar 31 13:58:15 ..... loading genome
Mar 31 14:05:05 ..... started mapping
```
Used readMapNumber 100000 to make a small alignment to run a test before going to a full alignment. Also needed to activate the swap file of 36G, as it would not work without it.  
# 01.04.2025
## Alignment test finished
```
NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ls -lh
total 11G
-rw-r--r-- 1 alexts14 alexts14    0 Mar 19 11:42 --genomeDir
-rw-r--r-- 1 alexts14 alexts14    0 Mar 19 11:42 --genomeFastaFiles
-rw-r--r-- 1 alexts14 alexts14    0 Mar 19 11:42 --genomeSAsparseD
-rw-r--r-- 1 alexts14 alexts14    0 Mar 19 11:42 --limitGenomeGenerateRAM
-rw-r--r-- 1 alexts14 alexts14    0 Mar 19 11:42 --runMode
-rw-r--r-- 1 alexts14 alexts14 2.4G Mar 18 09:13 GCA_944319725.1_Naked_mole-rat_paternal_genomic.fna
-rw-r--r-- 1 alexts14 alexts14 439M Mar 21 16:19 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf
-rw-r--r-- 1 alexts14 alexts14  253 Mar 21 16:19 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf.gz:Zone.Identifier
drwxr-xr-x 2 alexts14 alexts14 4.0K Mar 21 10:37 SRR21882792
-rw-r--r-- 1 alexts14 alexts14 3.8M Mar 21 10:43 SRR21882792.fastq
-rw-r--r-- 1 alexts14 alexts14 3.9G Mar 21 10:49 SRR21882792_1.fastq
-rw-r--r-- 1 alexts14 alexts14 602K Mar 21 11:01 SRR21882792_1_fastqc.html
-rw-r--r-- 1 alexts14 alexts14 367K Mar 21 11:01 SRR21882792_1_fastqc.zip
-rw-r--r-- 1 alexts14 alexts14 3.9G Mar 21 10:49 SRR21882792_2.fastq
-rw-r--r-- 1 alexts14 alexts14 610K Mar 21 11:03 SRR21882792_2_fastqc.html
-rw-r--r-- 1 alexts14 alexts14 369K Mar 21 11:03 SRR21882792_2_fastqc.zip
-rw-r--r-- 1 alexts14 alexts14  11M Mar 31 21:10 SRR21882792_test_Aligned.sortedByCoord.out.bam
-rw-r--r-- 1 alexts14 alexts14 2.0K Mar 31 21:10 SRR21882792_test_Log.final.out
-rw-r--r-- 1 alexts14 alexts14 7.0K Mar 31 21:10 SRR21882792_test_Log.out
-rw-r--r-- 1 alexts14 alexts14  482 Mar 31 21:10 SRR21882792_test_Log.progress.out
-rw-r--r-- 1 alexts14 alexts14  81K Mar 31 21:10 SRR21882792_test_SJ.out.tab
drwxr-xr-x 2 alexts14 alexts14 4.0K Mar 20 14:23 fasterq.tmp.GabanouMelissa.1568
drwxr-xr-x 2 alexts14 alexts14 4.0K Mar 28 14:55 star_index_full
-rw-r--r-- 1 alexts14 alexts14 1.3K Mar 28 15:00 star_log.txt
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$
```
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ STAR --runThreadN 4 \
>      --genomeDir ~/NMR_project/star_index_full \
>      --readFilesIn SRR21882792_1.fastq SRR21882792_2.fastq \
>      --outFileNamePrefix SRR21882792_test_ \
>      --readMapNumber 100000 \
>      --outSAMtype BAM SortedByCoordinate
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 4 --genomeDir /home/alexts14/NMR_project/star_index_full --readFilesIn SRR21882792_1.fastq SRR21882792_2.fastq --outFileNamePrefix SRR21882792_test_ --readMapNumber 100000 --outSAMtype BAM SortedByCoordinate
        STAR version: 2.7.11b   compiled: 2024-11-25T09:14:51+0000 :/opt/conda/conda-bld/star_1732525954305/work/source
Mar 31 13:58:15 ..... started STAR run
Mar 31 13:58:15 ..... loading genome
Mar 31 14:05:05 ..... started mapping
Mar 31 21:10:00 ..... finished mapping
Mar 31 21:10:06 ..... started sorting BAM
Mar 31 21:10:12 ..... finished successfully
```
This was the process and the duration of the 100000 read alignment
# 02.04.2025
Next steps
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ cat SRR21882792_test_Log.final.out
                                 Started job on |       Mar 31 13:58:15
                             Started mapping on |       Mar 31 14:05:05
                                    Finished on |       Mar 31 21:10:12
       Mapping speed, Million of reads per hour |       0.01

                          Number of input reads |       100000
                      Average input read length |       238
                                    UNIQUE READS:
                   Uniquely mapped reads number |       94204
                        Uniquely mapped reads % |       94.20%
                          Average mapped length |       236.44
                       Number of splices: Total |       19810
            Number of splices: Annotated (sjdb) |       1825
                       Number of splices: GT/AG |       19328
                       Number of splices: GC/AG |       94
                       Number of splices: AT/AC |       4
               Number of splices: Non-canonical |       384
                      Mismatch rate per base, % |       0.42%
                         Deletion rate per base |       0.11%
                        Deletion average length |       1.82
                        Insertion rate per base |       0.02%
                       Insertion average length |       1.40
                             MULTI-MAPPING READS:
        Number of reads mapped to multiple loci |       2369
             % of reads mapped to multiple loci |       2.37%
        Number of reads mapped to too many loci |       904
             % of reads mapped to too many loci |       0.90%
                                  UNMAPPED READS:
  Number of reads unmapped: too many mismatches |       0
       % of reads unmapped: too many mismatches |       0.00%
            Number of reads unmapped: too short |       884
                 % of reads unmapped: too short |       0.88%
                Number of reads unmapped: other |       1639
                     % of reads unmapped: other |       1.64%
                                  CHIMERIC READS:
                       Number of chimeric reads |       0
                            % of chimeric reads |       0.00%
```
This is the alignment report. 
### Overview
Total reads: 100,000 (Exactly the test we asked for). Average read length: 238 bp (Very typical for RNA-seq PE data).
Uniquely mapped reads:      94.20%	           (Excellent (anything above ~75-80% is generally good)).
Multi-mapped reads:	        2.37%	             (Very normal for RNA-seq).
Too many loci:	              0.90%	             (Also acceptable.\).
Unmapped:	                  2.52%	             (Combined (too short + other), very low and healthy).
Chimeric reads:	            0%	               (Not a problem unless you expect structural variants).
Then first, we indexed the BAM file (required for viewing & counting)
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ samtools index SRR21882792_test_Aligned.sortedByCoord.out.bam
```
Second, check alignment content
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ samtools view SRR21882792_test_Aligned.sortedByCoord.out.bam | head -n 10
SRR21882792.88324       419     OX090941.1      2689716 0       69M     =       2689716    69      CTAAGATTTTGTTCCTATTTTTCCATTTTCTCATATTAATCCCATTCCCTTCTATCCTTTCCCCTAGCC      AAFFFJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJFJJJJJJJJJJJJJFJJJJFJF   NH:i:10    HI:i:5  AS:i:136        nM:i:0
SRR21882792.88324       339     OX090941.1      2689716 0       69M     =       2689716    -69     CTAAGATTTTGTTCCTATTTTTCCATTTTCTCATATTAATCCCATTCCCTTCTATCCTTTCCCCTAGCC      JJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJFJJJJJJJJJFFFAA   NH:i:10    HI:i:5  AS:i:136        nM:i:0
SRR21882792.35054       147     OX090941.1      9372519 255     26M1513N79M734N19M
=       9372528 -2362   CCTTTATGTTCTCAGAATAAGGGTTCTGAGGATGAAAATCAGGCCTGAAACCTTGAGGGAGCTCTACTTCTTCCATGTTCTTTGAATTCTCTGAAGAGGCAGGAATGGAAGCATTTTCTTCTTT       AAJJJJJJFF7F<JJJJJJFFJJJFJJJJAJJJJJJJF<JFJJJJFJJJJJJJJ<FJJ<JFA-AJJJJJAJFFAJFJJJJJJJJJJJJJJJFAA7<JJJJJFJJJAFJJJJJAFJJJJJFFFAA  NH:i:1  HI:i:1  AS:i:216        nM:i:10
SRR21882792.35055       147     OX090941.1      9372519 255     26M1513N79M734N19M
=       9372528 -2362   CCTTTATGTTCTCAGAATAAGGGTTCTGAGGATGAAAATCAGGCCTGAAACCTTGAGGGAGCTCTACTTCTTCCATGTTCTTTGAATTCTCTGAAGAGGCAGGAATGGAAGCATTTTCTTCTTT       AJJJJJJJJJAJJJFJJJJFJJJJJJJFFJFJJFJJF<F-AAA-FJAA<FAAFJJJJJJF<JFFJFJJJJJFAAJFJJJFJFJFJJJJJJJJJFJJJJAF-AFFJJJJFJJJJJJFFFFFFFAA  NH:i:1  HI:i:1  AS:i:216        nM:i:10
SRR21882792.35053       99      OX090941.1      9372524 255     15S21M1513N79M734N35M      =       9374057 2378    GTCAACATTTCCTTTATGTTCTCAGAATAAGGGTTCTGAGGATGAAAATCAGGCCTGAAACCTTGAGGGAGCTCTACTTCTTCCATGTTCTTTGAATTCTCTGAAGAGGCAGGAATGGAAGCATTTTCTTCTTTCCTAAGACTCTGTAAT        AAFFFJFJJJJJJFJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJFJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJFJJJJJJJJJJJJJJJJJFFJJFJFJJJJJJJF        NH:i:1  HI:i:1  AS:i:223        nM:i:10
SRR21882792.35054       99      OX090941.1      9372528 255     9S17M1513N79M734N19M       =       9372519 2362    CCTTTATGTTCTCAGAATAAGGGTTCTGAGGATGAAAATCAGGCCTGAAACCTTGAGGGAGCTCTACTTCTTCCATGTTCTTTGAATTCTCTGAAGAGGCAGGAATGGAAGCATTTTCTTCTTT       AAAF<JJJFJJJFFJJFFJAJJFAJJJJJFJJJJJJFFFJAFJJ<FAJJJJJFJJF<AA-AJFJJJJJJJJJJ<AF<FFA-FJJJJJJ<JFFJFFFAA<JJ<A<AAA<FA7A<AFF-7<AFFAF  NH:i:1  HI:i:1  AS:i:216        nM:i:10
SRR21882792.35055       99      OX090941.1      9372528 255     9S17M1513N79M734N19M       =       9372519 2362    CCTTTATGTTCTCAGAATAAGGGTTCTGAGGATGAAAATCAGGCCTGAAACCTTGAGGGAGCTCTACTTCTTCCATGTTCTTTGAATTCTCTGAAGAGGCAGGAATGGAAGCATTTTCTTCTTT       AAFFFJJFFJJJJJFJJJJJJJJJJJAJJFFJFJJJJJJFJJJJJJJJFJFFJJJJFJ<A<-FJFFJJF-AA<-JA<A----7-AF<7<F7F<FJFJF-FJA-<FF--FJAFJ777FAFFFAF<  NH:i:1  HI:i:1  AS:i:216        nM:i:10
SRR21882792.35053       147     OX090941.1      9374057 255     35S80M734N31M4S =
     9372524    -2378   GTCAACATTTCCTTTATGTTCTCAGAATAAGGGTTCTGAGGATGAAAATCAGGCCTGAAACCTTGAGGGAGCTCTACTTCTTCCATGTTCTTTGAATTCTCTGAAGAGGCAGGAATGGAAGCATTTTCTTCTTTCCTAAGACTCTGTAAT        JJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJFJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJFJJJJJJJJJJJJJJJFJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJFFFAANH:i:1  HI:i:1  AS:i:223        nM:i:10
SRR21882792.35051       99      OX090941.1      9374089 255     1S48M734N56M2S  =
     9374871    838     GGGCGCTCTACTTCTTCCATGTTCTTTGAATTCTCTGAAGAGGCAGGAATGGAAGCATTTTCTTCTTTCCTAAGACTCTGTAATGCTTTTATCTGCTGAGATATTAT        A-AAAJJJJJJJJJJJJJJJFJFAJAJJJFJJJJFAJFJJJJFJJJF<AAAFF<JJA---FFFFFFJJJAJ<7A777FFJJFJJJJJJJJAJJFFFF-FJFFJ<FFJ
     NH:i:1     HI:i:1  AS:i:146        nM:i:6
SRR21882792.35052       99      OX090941.1      9374089 255     1S48M734N56M2S  =
     9374089    838     GGGCGCTCTACTTCTTCCATGTTCTTTGAATTCTCTGAAGAGGCAGGAATGGAAGCATTTTCTTCTTTCCTAAGACTCTGTAATGCTTTTATCTGCTGAGATATTAT        AAFFFJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJFJJJJJFJJJJJJJJJJ7FFAAAFJ7AFFFFAAAAAFF7-FF-FF
     NH:i:1     HI:i:1  AS:i:190        nM:i:8
```
Third, get a summary of the BAM file
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ samtools flagstat SRR21882792_test_Aligned.sortedByCoord.out.bam
206188 + 0 in total (QC-passed reads + QC-failed reads)
193137 + 0 primary
13051 + 0 secondary
0 + 0 supplementary
0 + 0 duplicates
0 + 0 primary duplicates
206188 + 0 mapped (100.00% : N/A)
193137 + 0 primary mapped (100.00% : N/A)
193137 + 0 paired in sequencing
96571 + 0 read1
96566 + 0 read2
193128 + 0 properly paired (100.00% : N/A)
193128 + 0 with itself and mate mapped
9 + 0 singletons (0.00% : N/A)
0 + 0 with mate mapped to a different chr
0 + 0 with mate mapped to a different chr (mapQ>=5)
```
Total alignments	206,188	 (we had paired-end, so this is close to 2 x 100,000 reads).
Primary mapped	193,137	(Primary alignments, no funny secondary only junk).
Secondary alignments	13,051	(STAR reports secondaries when allowing multi-mapping (we had NH:i:10 tags in your SAM lines)).
Properly paired	193,128	(Proper pairing is almost perfect (this is gold)).
Singleton	9	(Singletons are negligible).
Duplicates	0	(STAR does not mark duplicates by default, so this is expected).
### Next step will be to use IGV to check the aligned seq.
To do that we need to find the regions with a lot of reads (high coverage) to visualize them easily in IGV. 
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ samtools idxstats SRR21882792_test_Aligned.sortedByCoord.out.bam
OX090941.1      126681680       476     0
OX090942.1      131346783       292     0
OX090943.1      124509033       266     0
OX090944.1      121083042       302     0
OX090945.1      119101870       1614    0
OX090946.1      118199489       252     0
OX090947.1      101507220       255     0
OX090948.1      100330867       278     0
OX090949.1      97794639        2226    0
OX090950.1      94825129        584     0
OX090951.1      88157664        205     0
OX090952.1      87863200        236     0
OX090953.1      82497129        168130  0
OX090954.1      76838549        256     0
OX090955.1      76365940        390     0
OX090956.1      76437676        198     0
OX090957.1      71606942        730     0
OX090958.1      67431141        644     0
OX090959.1      60928233        250     0
OX090960.1      61068310        238     0
OX090961.1      56435557        114     0
OX090962.1      59689252        162     0
OX090963.1      53761172        15072   0
OX090964.1      52691189        138     0
OX090965.1      46678892        1328    0
OX090966.1      44400560        134     0
OX090967.1      38566542        104     0
OX090968.1      32538853        86      0
OX090969.1      23277160        92      0
OX090970.1      145805425       554     0
OX090940.1      61021973        10582   0
OX090971.1      16428   0       0
```
Explanation:
- First column = chromosome
- Second = chromosome length
- Third = number of mapped reads
- Fourth = unmapped reads
### We will check chromosome OX090953.1 because it has the highest read count by far.
![image](https://github.com/user-attachments/assets/4d323cbe-dc96-4cd8-bb5f-257df27cf879)
✔ Coverage
✔ Junctions
✔ Alignments


This means:

✅ The test alignment is correctly indexed and visualized
✅ Reads are properly spliced (notice the arcs)
# 03.04.2025
##  Finding peaks or coverage plots
- Extract bigWig or bedGraph coverage files
- Visualize smoother coverage tracks in IGV (nicer than raw BAM)
- Use bedtools
```
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ bedtools genomecov -ibam SRR21882792_test_Aligned.sortedByCoord.out.bam -bg > SRR21882792_test.bedGraph
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ ls -lh SRR21882792_test.bedGraph
ad SRR21882792_test.bedGraph
-rw-r--r-- 1 alexts14 alexts14 3.6M Apr  3 11:38 SRR21882792_test.bedGraph
(NMR-env) alexts14@GabanouMelissa:~/NMR_project$ head SRR21882792_test.bedGraph
OX090941.1      2689715 2689784 2
OX090941.1      9372518 9372523 2
OX090941.1      9372523 9372527 3
OX090941.1      9372527 9374056 5
OX090941.1      9374056 9374088 6
OX090941.1      9374088 9374870 9
OX090941.1      9374870 9374889 10
OX090941.1      9374889 9374901 6
OX090941.1      9374901 9374905 5
OX090941.1      9374905 9374915 4
```
To create a .bigWig file, we created a new -env because deeptool could not be downloaded because of deferrent versions of others tools that were blocking it in the NMR-env.
```
(base) alexts14@GabanouMelissa:~$ conda create -n coverage-env -c bioconda -c conda-forge python=3.9 deeptools
Channels:
 - bioconda
 - conda-forge
 - defaults
Platform: linux-64
Collecting package metadata (repodata.json): done
Solving environment: done


==> WARNING: A newer version of conda exists. <==
    current version: 25.1.1
    latest version: 25.3.0

Please update conda by running

    $ conda update -n base -c defaults conda



## Package Plan ##

  environment location: /home/alexts14/miniconda3/envs/coverage-env

  added / updated specs:
    - deeptools
    - python=3.9


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    _libgcc_mutex-0.1          |      conda_forge           3 KB  conda-forge
    _openmp_mutex-4.5          |            2_gnu          23 KB  conda-forge
    alabaster-0.7.16           |     pyhd8ed1ab_0          18 KB  conda-forge
    babel-2.17.0               |     pyhd8ed1ab_0         6.6 MB  conda-forge
    brotli-1.1.0               |       hb9d3cd8_2          19 KB  conda-forge
    brotli-bin-1.1.0           |       hb9d3cd8_2          18 KB  conda-forge
    brotli-python-1.1.0        |   py39hf88036b_2         341 KB  conda-forge
    bzip2-1.0.8                |       h4bc722e_7         247 KB  conda-forge
    ca-certificates-2025.1.31  |       hbcca054_0         154 KB  conda-forge
    certifi-2025.1.31          |     pyhd8ed1ab_0         159 KB  conda-forge
    cffi-1.17.1                |   py39h15c3d72_0         236 KB  conda-forge
    charset-normalizer-3.4.1   |     pyhd8ed1ab_0          46 KB  conda-forge
    colorama-0.4.6             |     pyhd8ed1ab_1          26 KB  conda-forge
    contourpy-1.3.0            |   py39h74842e3_2         256 KB  conda-forge
    cycler-0.12.1              |     pyhd8ed1ab_1          13 KB  conda-forge
    deeptools-3.5.6            |     pyhdfd78af_0         143 KB  bioconda
    deeptoolsintervals-0.1.9   |  py39hcc2ff80_11          76 KB  bioconda
    docutils-0.21.2            |     pyhd8ed1ab_1         393 KB  conda-forge
    fonttools-4.56.0           |   py39h9399b63_0         2.2 MB  conda-forge
    freetype-2.13.3            |       h48d6fc4_0         625 KB  conda-forge
    h2-4.2.0                   |     pyhd8ed1ab_0          53 KB  conda-forge
    hpack-4.1.0                |     pyhd8ed1ab_0          30 KB  conda-forge
    hyperframe-6.1.0           |     pyhd8ed1ab_0          17 KB  conda-forge
    idna-3.10                  |     pyhd8ed1ab_1          49 KB  conda-forge
    imagesize-1.4.1            |     pyhd8ed1ab_0          10 KB  conda-forge
    importlib-metadata-8.6.1   |     pyha770c72_0          28 KB  conda-forge
    importlib-resources-6.5.2  |     pyhd8ed1ab_0           9 KB  conda-forge
    importlib_resources-6.5.2  |     pyhd8ed1ab_0          33 KB  conda-forge
    jinja2-3.1.6               |     pyhd8ed1ab_0         110 KB  conda-forge
    keyutils-1.6.1             |       h166bdaf_0         115 KB  conda-forge
    kiwisolver-1.4.7           |   py39h74842e3_0          70 KB  conda-forge
    krb5-1.21.3                |       h659f571_0         1.3 MB  conda-forge
    lcms2-2.17                 |       h717163a_0         242 KB  conda-forge
    ld_impl_linux-64-2.43      |       h712a8e2_4         656 KB  conda-forge
    lerc-4.0.0                 |       h27087fc_0         275 KB  conda-forge
    libblas-3.9.0              |31_h59b9bed_openblas          16 KB  conda-forge
    libbrotlicommon-1.1.0      |       hb9d3cd8_2          67 KB  conda-forge
    libbrotlidec-1.1.0         |       hb9d3cd8_2          32 KB  conda-forge
    libbrotlienc-1.1.0         |       hb9d3cd8_2         275 KB  conda-forge
    libcblas-3.9.0             |31_he106b2a_openblas          16 KB  conda-forge
    libcurl-8.13.0             |       h332b0f4_0         428 KB  conda-forge
    libdeflate-1.22            |       hb9d3cd8_0          71 KB  conda-forge
    libffi-3.4.6               |       h2dba641_1          56 KB  conda-forge
    libjpeg-turbo-3.0.0        |       hd590300_1         604 KB  conda-forge
    liblapack-3.9.0            |31_h7ac8fdf_openblas          16 KB  conda-forge
    libopenblas-0.3.29         |pthreads_h94d23a6_0         5.6 MB  conda-forge
    libpng-1.6.47              |       h943b412_0         282 KB  conda-forge
    libsqlite-3.49.1           |       hee588c1_2         897 KB  conda-forge
    libtiff-4.7.0              |       hc4654cb_2         419 KB  conda-forge
    libwebp-base-1.5.0         |       h851e524_0         420 KB  conda-forge
    libxcb-1.17.0              |       h8a09558_0         387 KB  conda-forge
    markupsafe-3.0.2           |   py39h9399b63_1          22 KB  conda-forge
    matplotlib-base-3.9.4      |   py39h16632d1_0         6.7 MB  conda-forge
    munkres-1.0.7              |             py_1          10 KB  bioconda
    narwhals-1.33.0            |     pyhd8ed1ab_0         186 KB  conda-forge
    numpy-2.0.2                |   py39h9cb892a_1         7.6 MB  conda-forge
    numpydoc-1.8.0             |     pyhd8ed1ab_1          57 KB  conda-forge
    openjpeg-2.5.3             |       h5fbd93e_0         335 KB  conda-forge
    packaging-24.2             |     pyhd8ed1ab_2          59 KB  conda-forge
    pillow-11.1.0              |   py39h15c0740_0        40.3 MB  conda-forge
    pip-25.0.1                 |     pyh8b19718_0         1.2 MB  conda-forge
    plotly-6.0.1               |     pyhd8ed1ab_0         4.8 MB  conda-forge
    pthread-stubs-0.4          |    hb9d3cd8_1002           8 KB  conda-forge
    py2bit-0.3.3               |   py39hbcbf7aa_1          29 KB  bioconda
    pybigwig-0.3.24            |   py39h616c374_0          87 KB  bioconda
    pycparser-2.22             |     pyh29332c3_1         108 KB  conda-forge
    pygments-2.19.1            |     pyhd8ed1ab_0         868 KB  conda-forge
    pyparsing-3.2.3            |     pyhd8ed1ab_1          94 KB  conda-forge
    pysam-0.23.0               |   py39hdd5828d_0         4.6 MB  bioconda
    pysocks-1.7.1              |     pyha55dd90_7          21 KB  conda-forge
    python-3.9.21              |h9c0c6dc_1_cpython        22.5 MB  conda-forge
    python-dateutil-2.9.0.post0|     pyhff2d567_1         217 KB  conda-forge
    python_abi-3.9             |           6_cp39           7 KB  conda-forge
    pytz-2025.2                |     pyhd8ed1ab_0         185 KB  conda-forge
    qhull-2020.2               |       h434a139_5         540 KB  conda-forge
    readline-8.2               |       h8c095d6_2         276 KB  conda-forge
    requests-2.32.3            |     pyhd8ed1ab_1          57 KB  conda-forge
    scipy-1.13.1               |   py39haf93ffa_0        15.8 MB  conda-forge
    setuptools-75.8.2          |     pyhff2d567_0         760 KB  conda-forge
    six-1.17.0                 |     pyhd8ed1ab_0          16 KB  conda-forge
    snowballstemmer-2.2.0      |     pyhd8ed1ab_0          57 KB  conda-forge
    sphinx-7.4.7               |     pyhd8ed1ab_0         1.3 MB  conda-forge
    sphinxcontrib-applehelp-2.0.0|     pyhd8ed1ab_1          29 KB  conda-forge
    sphinxcontrib-devhelp-2.0.0|     pyhd8ed1ab_1          24 KB  conda-forge
    sphinxcontrib-htmlhelp-2.1.0|     pyhd8ed1ab_1          32 KB  conda-forge
    sphinxcontrib-jsmath-1.0.1 |     pyhd8ed1ab_1          10 KB  conda-forge
    sphinxcontrib-qthelp-2.0.0 |     pyhd8ed1ab_1          26 KB  conda-forge
    sphinxcontrib-serializinghtml-1.1.10|     pyhd8ed1ab_1          28 KB  conda-forge
    tabulate-0.9.0             |     pyhd8ed1ab_2          37 KB  conda-forge
    tomli-2.2.1                |     pyhd8ed1ab_1          19 KB  conda-forge
    tzdata-2025b               |       h78e105d_0         120 KB  conda-forge
    unicodedata2-16.0.0        |   py39h8cd3c5a_0         395 KB  conda-forge
    urllib3-2.3.0              |     pyhd8ed1ab_0          98 KB  conda-forge
    wheel-0.45.1               |     pyhd8ed1ab_1          61 KB  conda-forge
    xorg-libxau-1.0.12         |       hb9d3cd8_0          14 KB  conda-forge
    xorg-libxdmcp-1.1.5        |       hb9d3cd8_0          19 KB  conda-forge
    zipp-3.21.0                |     pyhd8ed1ab_1          21 KB  conda-forge
    zstandard-0.23.0           |   py39h8cd3c5a_1         703 KB  conda-forge
    zstd-1.5.7                 |       hb8e6e7a_2         554 KB  conda-forge
    ------------------------------------------------------------
                                           Total:       134.9 MB

The following NEW packages will be INSTALLED:

  _libgcc_mutex      conda-forge/linux-64::_libgcc_mutex-0.1-conda_forge
  _openmp_mutex      conda-forge/linux-64::_openmp_mutex-4.5-2_gnu
  alabaster          conda-forge/noarch::alabaster-0.7.16-pyhd8ed1ab_0
  babel              conda-forge/noarch::babel-2.17.0-pyhd8ed1ab_0
  brotli             conda-forge/linux-64::brotli-1.1.0-hb9d3cd8_2
  brotli-bin         conda-forge/linux-64::brotli-bin-1.1.0-hb9d3cd8_2
  brotli-python      conda-forge/linux-64::brotli-python-1.1.0-py39hf88036b_2
  bzip2              conda-forge/linux-64::bzip2-1.0.8-h4bc722e_7
  c-ares             conda-forge/linux-64::c-ares-1.34.4-hb9d3cd8_0
  ca-certificates    conda-forge/linux-64::ca-certificates-2025.1.31-hbcca054_0
  certifi            conda-forge/noarch::certifi-2025.1.31-pyhd8ed1ab_0
  cffi               conda-forge/linux-64::cffi-1.17.1-py39h15c3d72_0
  charset-normalizer conda-forge/noarch::charset-normalizer-3.4.1-pyhd8ed1ab_0
  colorama           conda-forge/noarch::colorama-0.4.6-pyhd8ed1ab_1
  contourpy          conda-forge/linux-64::contourpy-1.3.0-py39h74842e3_2
  cycler             conda-forge/noarch::cycler-0.12.1-pyhd8ed1ab_1
  deeptools          bioconda/noarch::deeptools-3.5.6-pyhdfd78af_0
  deeptoolsintervals bioconda/linux-64::deeptoolsintervals-0.1.9-py39hcc2ff80_11
  docutils           conda-forge/noarch::docutils-0.21.2-pyhd8ed1ab_1
  fonttools          conda-forge/linux-64::fonttools-4.56.0-py39h9399b63_0
  freetype           conda-forge/linux-64::freetype-2.13.3-h48d6fc4_0
  h2                 conda-forge/noarch::h2-4.2.0-pyhd8ed1ab_0
  hpack              conda-forge/noarch::hpack-4.1.0-pyhd8ed1ab_0
  hyperframe         conda-forge/noarch::hyperframe-6.1.0-pyhd8ed1ab_0
  idna               conda-forge/noarch::idna-3.10-pyhd8ed1ab_1
  imagesize          conda-forge/noarch::imagesize-1.4.1-pyhd8ed1ab_0
  importlib-metadata conda-forge/noarch::importlib-metadata-8.6.1-pyha770c72_0
  importlib-resourc~ conda-forge/noarch::importlib-resources-6.5.2-pyhd8ed1ab_0
  importlib_resourc~ conda-forge/noarch::importlib_resources-6.5.2-pyhd8ed1ab_0
  jinja2             conda-forge/noarch::jinja2-3.1.6-pyhd8ed1ab_0
  keyutils           conda-forge/linux-64::keyutils-1.6.1-h166bdaf_0
  kiwisolver         conda-forge/linux-64::kiwisolver-1.4.7-py39h74842e3_0
  krb5               conda-forge/linux-64::krb5-1.21.3-h659f571_0
  lcms2              conda-forge/linux-64::lcms2-2.17-h717163a_0
  ld_impl_linux-64   conda-forge/linux-64::ld_impl_linux-64-2.43-h712a8e2_4
  lerc               conda-forge/linux-64::lerc-4.0.0-h27087fc_0
  libblas            conda-forge/linux-64::libblas-3.9.0-31_h59b9bed_openblas
  libbrotlicommon    conda-forge/linux-64::libbrotlicommon-1.1.0-hb9d3cd8_2
  libbrotlidec       conda-forge/linux-64::libbrotlidec-1.1.0-hb9d3cd8_2
  libbrotlienc       conda-forge/linux-64::libbrotlienc-1.1.0-hb9d3cd8_2
  libcblas           conda-forge/linux-64::libcblas-3.9.0-31_he106b2a_openblas
  libcurl            conda-forge/linux-64::libcurl-8.13.0-h332b0f4_0
  libdeflate         conda-forge/linux-64::libdeflate-1.22-hb9d3cd8_0
  libedit            conda-forge/linux-64::libedit-3.1.20250104-pl5321h7949ede_0
  libev              conda-forge/linux-64::libev-4.33-hd590300_2
  libffi             conda-forge/linux-64::libffi-3.4.6-h2dba641_1
  libgcc             conda-forge/linux-64::libgcc-14.2.0-h767d61c_2
  libgcc-ng          conda-forge/linux-64::libgcc-ng-14.2.0-h69a702a_2
  libgfortran        conda-forge/linux-64::libgfortran-14.2.0-h69a702a_2
  libgfortran-ng     conda-forge/linux-64::libgfortran-ng-14.2.0-h69a702a_2
  libgfortran5       conda-forge/linux-64::libgfortran5-14.2.0-hf1ad2bd_2
  libgomp            conda-forge/linux-64::libgomp-14.2.0-h767d61c_2
  libjpeg-turbo      conda-forge/linux-64::libjpeg-turbo-3.0.0-hd590300_1
  liblapack          conda-forge/linux-64::liblapack-3.9.0-31_h7ac8fdf_openblas
  liblzma            conda-forge/linux-64::liblzma-5.6.4-hb9d3cd8_0
  libnghttp2         conda-forge/linux-64::libnghttp2-1.64.0-h161d5f1_0
  libnsl             conda-forge/linux-64::libnsl-2.0.1-hd590300_0
  libopenblas        conda-forge/linux-64::libopenblas-0.3.29-pthreads_h94d23a6_0
  libpng             conda-forge/linux-64::libpng-1.6.47-h943b412_0
  libsqlite          conda-forge/linux-64::libsqlite-3.49.1-hee588c1_2
  libssh2            conda-forge/linux-64::libssh2-1.11.1-hf672d98_0
  libstdcxx          conda-forge/linux-64::libstdcxx-14.2.0-h8f9b012_2
  libstdcxx-ng       conda-forge/linux-64::libstdcxx-ng-14.2.0-h4852527_2
  libtiff            conda-forge/linux-64::libtiff-4.7.0-hc4654cb_2
  libuuid            conda-forge/linux-64::libuuid-2.38.1-h0b41bf4_0
  libwebp-base       conda-forge/linux-64::libwebp-base-1.5.0-h851e524_0
  libxcb             conda-forge/linux-64::libxcb-1.17.0-h8a09558_0
  libxcrypt          conda-forge/linux-64::libxcrypt-4.4.36-hd590300_1
  libzlib            conda-forge/linux-64::libzlib-1.3.1-hb9d3cd8_2
  markupsafe         conda-forge/linux-64::markupsafe-3.0.2-py39h9399b63_1
  matplotlib-base    conda-forge/linux-64::matplotlib-base-3.9.4-py39h16632d1_0
  munkres            bioconda/noarch::munkres-1.0.7-py_1
  narwhals           conda-forge/noarch::narwhals-1.33.0-pyhd8ed1ab_0
  ncurses            conda-forge/linux-64::ncurses-6.5-h2d0b736_3
  numpy              conda-forge/linux-64::numpy-2.0.2-py39h9cb892a_1
  numpydoc           conda-forge/noarch::numpydoc-1.8.0-pyhd8ed1ab_1
  openjpeg           conda-forge/linux-64::openjpeg-2.5.3-h5fbd93e_0
  openssl            conda-forge/linux-64::openssl-3.4.1-h7b32b05_0
  packaging          conda-forge/noarch::packaging-24.2-pyhd8ed1ab_2
  pillow             conda-forge/linux-64::pillow-11.1.0-py39h15c0740_0
  pip                conda-forge/noarch::pip-25.0.1-pyh8b19718_0
  plotly             conda-forge/noarch::plotly-6.0.1-pyhd8ed1ab_0
  pthread-stubs      conda-forge/linux-64::pthread-stubs-0.4-hb9d3cd8_1002
  py2bit             bioconda/linux-64::py2bit-0.3.3-py39hbcbf7aa_1
  pybigwig           bioconda/linux-64::pybigwig-0.3.24-py39h616c374_0
  pycparser          conda-forge/noarch::pycparser-2.22-pyh29332c3_1
  pygments           conda-forge/noarch::pygments-2.19.1-pyhd8ed1ab_0
  pyparsing          conda-forge/noarch::pyparsing-3.2.3-pyhd8ed1ab_1
  pysam              bioconda/linux-64::pysam-0.23.0-py39hdd5828d_0
  pysocks            conda-forge/noarch::pysocks-1.7.1-pyha55dd90_7
  python             conda-forge/linux-64::python-3.9.21-h9c0c6dc_1_cpython
  python-dateutil    conda-forge/noarch::python-dateutil-2.9.0.post0-pyhff2d567_1
  python_abi         conda-forge/linux-64::python_abi-3.9-6_cp39
  pytz               conda-forge/noarch::pytz-2025.2-pyhd8ed1ab_0
  qhull              conda-forge/linux-64::qhull-2020.2-h434a139_5
  readline           conda-forge/linux-64::readline-8.2-h8c095d6_2
  requests           conda-forge/noarch::requests-2.32.3-pyhd8ed1ab_1
  scipy              conda-forge/linux-64::scipy-1.13.1-py39haf93ffa_0
  setuptools         conda-forge/noarch::setuptools-75.8.2-pyhff2d567_0
  six                conda-forge/noarch::six-1.17.0-pyhd8ed1ab_0
  snowballstemmer    conda-forge/noarch::snowballstemmer-2.2.0-pyhd8ed1ab_0
  sphinx             conda-forge/noarch::sphinx-7.4.7-pyhd8ed1ab_0
  sphinxcontrib-app~ conda-forge/noarch::sphinxcontrib-applehelp-2.0.0-pyhd8ed1ab_1
  sphinxcontrib-dev~ conda-forge/noarch::sphinxcontrib-devhelp-2.0.0-pyhd8ed1ab_1
  sphinxcontrib-htm~ conda-forge/noarch::sphinxcontrib-htmlhelp-2.1.0-pyhd8ed1ab_1
  sphinxcontrib-jsm~ conda-forge/noarch::sphinxcontrib-jsmath-1.0.1-pyhd8ed1ab_1
  sphinxcontrib-qth~ conda-forge/noarch::sphinxcontrib-qthelp-2.0.0-pyhd8ed1ab_1
  sphinxcontrib-ser~ conda-forge/noarch::sphinxcontrib-serializinghtml-1.1.10-pyhd8ed1ab_1
  tabulate           conda-forge/noarch::tabulate-0.9.0-pyhd8ed1ab_2
  tk                 conda-forge/linux-64::tk-8.6.13-noxft_h4845f30_101
  tomli              conda-forge/noarch::tomli-2.2.1-pyhd8ed1ab_1
  tzdata             conda-forge/noarch::tzdata-2025b-h78e105d_0
  unicodedata2       conda-forge/linux-64::unicodedata2-16.0.0-py39h8cd3c5a_0
  urllib3            conda-forge/noarch::urllib3-2.3.0-pyhd8ed1ab_0
  wheel              conda-forge/noarch::wheel-0.45.1-pyhd8ed1ab_1
  xorg-libxau        conda-forge/linux-64::xorg-libxau-1.0.12-hb9d3cd8_0
  xorg-libxdmcp      conda-forge/linux-64::xorg-libxdmcp-1.1.5-hb9d3cd8_0
  zipp               conda-forge/noarch::zipp-3.21.0-pyhd8ed1ab_1
  zlib               conda-forge/linux-64::zlib-1.3.1-hb9d3cd8_2
  zstandard          conda-forge/linux-64::zstandard-0.23.0-py39h8cd3c5a_1
  zstd               conda-forge/linux-64::zstd-1.5.7-hb8e6e7a_2


Proceed ([y]/n)? y


Downloading and Extracting Packages:
pillow-11.1.0        | 40.3 MB   | #################8                          |  41%
python-3.9.21        | 22.5 MB   | ###################################4        |  82% scipy-1.13.1         | 15.8 MB   | #########################################8  |  97% numpy-2.0.2          | 7.6 MB    | ########################################### | 100%
matplotlib-base-3.9. | 6.7 MB    | ########################################### | 100%
babel-2.17.0         | 6.6 MB    | ##################################4         |  80% pillow-11.1.0        | 40.3 MB   | ########################################### | 100%
python-3.9.21        | 22.5 MB   | ########################################### | 100% scipy-1.13.1         | 15.8 MB   | ########################################### | 100%
numpy-2.0.2          | 7.6 MB    | ########################################### | 100%
matplotlib-base-3.9. | 6.7 MB    | ########################################### | 100%
babel-2.17.0         | 6.6 MB    | ########################################### | 100%
libopenblas-0.3.29   | 5.6 MB    | ########################################### | 100%
plotly-6.0.1         | 4.8 MB    | ########################################### | 100%
pysam-0.23.0         | 4.6 MB    | ########################################### | 100%
fonttools-4.56.0     | 2.2 MB    | ########################################### | 100%
krb5-1.21.3          | 1.3 MB    | ########################################### | 100%
sphinx-7.4.7         | 1.3 MB    | ########################################### | 100%
pip-25.0.1           | 1.2 MB    | ########################################### | 100%
libsqlite-3.49.1     | 897 KB    | ########################################### | 100%
pygments-2.19.1      | 868 KB    | ########################################### | 100%
setuptools-75.8.2    | 760 KB    | ########################################### | 100%
zstandard-0.23.0     | 703 KB    | ########################################### | 100%
ld_impl_linux-64-2.4 | 656 KB    | ########################################### | 100%
freetype-2.13.3      | 625 KB    | ########################################### | 100%
libjpeg-turbo-3.0.0  | 604 KB    | ########################################### | 100%
zstd-1.5.7           | 554 KB    | ########################################### | 100%
qhull-2020.2         | 540 KB    | ########################################### | 100%
libcurl-8.13.0       | 428 KB    | ########################################### | 100%
libwebp-base-1.5.0   | 420 KB    | ########################################### | 100%
libtiff-4.7.0        | 419 KB    | ########################################### | 100%
unicodedata2-16.0.0  | 395 KB    | ########################################### | 100%
docutils-0.21.2      | 393 KB    | ########################################### | 100%

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate coverage-env
#
# To deactivate an active environment, use
#
#     $ conda deactivate

(base) alexts14@GabanouMelissa:~$ conda activate coverage-env
(coverage-env) alexts14@GabanouMelissa:~$ conda install -c bioconda -c conda-forge deeptools
Channels:
 - bioconda
 - conda-forge
 - defaults
Platform: linux-64
Collecting package metadata (repodata.json): done
Solving environment: done


==> WARNING: A newer version of conda exists. <==
    current version: 25.1.1
    latest version: 25.3.0

Please update conda by running

    $ conda update -n base -c defaults conda



# All requested packages already installed.

(coverage-env) alexts14@GabanouMelissa:~$ bamCoverage -b ~/NMR_project/SRR21882792_test_Aligned.sortedByCoord.out.bam -o ~/NMR_project/SRR21882792_test.bw
bamFilesList: ['/home/alexts14/NMR_project/SRR21882792_test_Aligned.sortedByCoord.out.bam']
binLength: 50
numberOfSamples: None
blackListFileName: None
skipZeroOverZero: False
bed_and_bin: False
genomeChunkSize: None
defaultFragmentLength: read length
numberOfProcessors: 1
verbose: False
region: None
bedFile: None
minMappingQuality: None
ignoreDuplicates: False
chrsToSkip: []
stepSize: 50
center_read: False
samFlag_include: None
samFlag_exclude: None
minFragmentLength: 0
maxFragmentLength: 0
zerosToNans: False
smoothLength: None
save_data: False
out_file_for_raw_data: None
maxPairedFragmentLength: 1000
(coverage-env) alexts14@GabanouMelissa:~$ ls -lh ~/NMR_project/*.bw
-rw-r--r-- 1 alexts14 alexts14 413K Apr  3 14:17 /home/alexts14/NMR_project/SRR21882792_test.bw
(coverage-env) alexts14@GabanouMelissa:~$ cp ~/NMR_project/SRR21882792_test.bw /mnt/c/IGV_data/
(coverage-env) alexts14@GabanouMelissa:~$
```
So, we created a new env and made the .bw file here and copied it to windows so that we can visualize it in IGV
![image](https://github.com/user-attachments/assets/521db47c-04cb-4888-8093-f3c7ba387a01)
# 04.04.2025
It seems like something is wrong with the gtf file, as no gene annotations appear in IGV
