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
I now re-run it with the option to work also in the backgroud so that even if the window will close it will still work. 
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
