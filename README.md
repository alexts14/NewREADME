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
