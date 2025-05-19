# 25.04.2025
## new start

```
(base) alexts14@GabanouMelissa:~$ activate conda_env

EnvironmentNameNotFound: Could not find conda environment: conda_env
You can list all discoverable environments with `conda info --envs`.


(base) alexts14@GabanouMelissa:~$ conda activate NMR_env

EnvironmentNameNotFound: Could not find conda environment: NMR_env
You can list all discoverable environments with `conda info --envs`.


(base) alexts14@GabanouMelissa:~$ conda activate NMR-env
(NMR-env) alexts14@GabanouMelissa:~$ mkdir nmr_chromosomes && cd nmr_chromosomes
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget "ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_g
laber/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz"
--2025-04-25 14:55:34--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber/dna ...
No such directory ‘pub/release-113/fasta/heterocephalus_glaber/dna’.

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 0
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ (NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget "ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_g
laber/dn-bash: syntax error near unexpected token `alexts14@GabanouMelissa:~/nmr_chromosomes$'
a/Heter(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ laber/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz"
> --2025-04-25 14:55:34--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz
>            => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz’
> Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
> Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
ging in > Logging in as anonymous ... Logged in!
> ==> SYST ... done.    ==> PWD ... done.
=> TY> ==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber/dna ...
> No such directory ‘pub/release-113/fasta/heterocephalus_glaber/dna’.
>
> (NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
 0
(NM> total 0
> ^C
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz
--2025-04-25 14:58:02--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz ... done.

==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz ...
No such file ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal_dna_sm.primary_assembly.1.fa.gz’.

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz
--2025-04-25 15:00:51--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz ... 41444776
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz ... done.
Length: 41444776 (40M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  39.52M  13.5MB/s    in 2.9s

2025-04-25 15:00:54 (13.5 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz’ saved [41444776]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ lt -lh
Command 'lt' not found, but can be installed with:
sudo apt install looptools
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 40M
-rw-r--r-- 1 alexts14 alexts14 40M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz
--2025-04-25 15:02:08--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz ... 42906844
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz ... done.
Length: 42906844 (41M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  40.92M  19.7MB/s    in 2.1s

2025-04-25 15:02:10 (19.7 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz’ saved [42906844]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 81M
-rw-r--r-- 1 alexts14 alexts14 40M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz
-rw-r--r-- 1 alexts14 alexts14 41M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz
--2025-04-25 15:02:45--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz ... 40705474
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz ... done.
Length: 40705474 (39M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  38.82M  19.5MB/s    in 2.0s

2025-04-25 15:02:47 (19.5 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz’ saved [40705474]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz
--2025-04-25 15:02:58--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz ... 39650470
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz ... done.
Length: 39650470 (38M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  37.81M  13.9MB/s    in 2.7s

2025-04-25 15:03:01 (13.9 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz’ saved [39650470]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 158M
-rw-r--r-- 1 alexts14 alexts14 40M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz
-rw-r--r-- 1 alexts14 alexts14 41M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz
-rw-r--r-- 1 alexts14 alexts14 39M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz
-rw-r--r-- 1 alexts14 alexts14 38M Apr 25 15:03 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz
--2025-04-25 15:05:55--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz ... 38969188
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz ... done.
Length: 38969188 (37M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  37.16M  10.8MB/s    in 3.6s

2025-04-25 15:05:59 (10.4 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz’ saved [38969188]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz
--2025-04-25 15:06:11--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz ... 38639569
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz ... done.
Length: 38639569 (37M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  36.85M  11.1MB/s    in 3.7s

2025-04-25 15:06:15 (10.1 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz’ saved [38639569]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz
--2025-04-25 15:06:25--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz ... 33239894
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz ... done.
Length: 33239894 (32M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  31.70M  10.7MB/s    in 3.0s

2025-04-25 15:06:28 (10.7 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz’ saved [33239894]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz
--2025-04-25 15:06:39--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz ... 32824502
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz ... done.
Length: 32824502 (31M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  31.30M  16.7MB/s    in 1.9s

2025-04-25 15:06:42 (16.7 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz’ saved [32824502]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 295M
-rw-r--r-- 1 alexts14 alexts14 40M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz
-rw-r--r-- 1 alexts14 alexts14 41M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz
-rw-r--r-- 1 alexts14 alexts14 39M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz
-rw-r--r-- 1 alexts14 alexts14 38M Apr 25 15:03 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz
-rw-r--r-- 1 alexts14 alexts14 38M Apr 25 15:05 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz
-rw-r--r-- 1 alexts14 alexts14 37M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz
-rw-r--r-- 1 alexts14 alexts14 32M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz
-rw-r--r-- 1 alexts14 alexts14 32M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa.gz
--2025-04-25 15:07:00--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa.gz ... 32075594
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa.gz ... done.
Length: 32075594 (31M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  30.59M  10.2MB/s    in 3.0s

2025-04-25 15:07:04 (10.2 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa.gz’ saved [32075594]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa.gz
--2025-04-25 15:07:16--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa.gz ... 31046836
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa.gz ... done.
Length: 31046836 (30M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  29.61M  11.6MB/s    in 2.6s

2025-04-25 15:07:19 (11.6 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa.gz’ saved [31046836]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa.gz
--2025-04-25 15:07:37--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa.gz ... 28813707
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa.gz ... done.
Length: 28813707 (27M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  27.48M  10.9MB/s    in 2.5s

2025-04-25 15:07:40 (10.9 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa.gz’ saved [28813707]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa.gz
--2025-04-25 15:07:46--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa.gz ... 28752055
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa.gz ... done.
Length: 28752055 (27M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  27.42M  11.1MB/s    in 2.5s

2025-04-25 15:07:50 (11.1 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa.gz’ saved [28752055]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa.gz
--2025-04-25 15:07:55--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa.gz ... 26995904
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa.gz ... done.
Length: 26995904 (26M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  25.75M  11.5MB/s    in 2.2s

2025-04-25 15:07:57 (11.5 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa.gz’ saved [26995904]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa.gz
--2025-04-25 15:08:05--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa.gz ... 25141686
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa.gz ... done.
Length: 25141686 (24M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  23.98M  17.2MB/s    in 1.4s

2025-04-25 15:08:07 (17.2 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa.gz’ saved [25141686]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa.gz
--2025-04-25 15:08:17--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa.gz ... 25058224
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa.gz ... done.
Length: 25058224 (24M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  23.90M  10.7MB/s    in 2.2s

2025-04-25 15:08:20 (10.7 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa.gz’ saved [25058224]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa.gz
--2025-04-25 15:08:28--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa.gz ... 24989441
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa.gz ... done.
Length: 24989441 (24M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  23.83M  10.8MB/s    in 2.2s

2025-04-25 15:08:31 (10.8 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa.gz’ saved [24989441]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa.gz
--2025-04-25 15:08:41--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa.gz ... 23426669
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa.gz ... done.
Length: 23426669 (22M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  22.34M  10.2MB/s    in 2.2s

2025-04-25 15:08:44 (10.2 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa.gz’ saved [23426669]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa.gz
--2025-04-25 15:08:52--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa.gz ... 22081786
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa.gz ... done.
Length: 22081786 (21M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  21.06M  9.45MB/s    in 2.2s

2025-04-25 15:08:56 (9.45 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa.gz’ saved [22081786]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa.gz
--2025-04-25 15:09:01--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa.gz ... 19956643
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa.gz ... done.
Length: 19956643 (19M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  19.03M  9.52MB/s    in 2.0s

2025-04-25 15:09:04 (9.52 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa.gz’ saved [19956643]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa.gz
--2025-04-25 15:09:12--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa.gz ... 19958070
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa.gz ... done.
Length: 19958070 (19M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  19.03M  9.18MB/s    in 2.1s

2025-04-25 15:09:15 (9.18 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa.gz’ saved [19958070]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa.gz
--2025-04-25 15:09:20--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa.gz ... 18475006
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa.gz ... done.
Length: 18475006 (18M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  17.62M  11.8MB/s    in 1.5s

2025-04-25 15:09:22 (11.8 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa.gz’ saved [18475006]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly22.fa.gz
--2025-04-25 15:09:30--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly22.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly22.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly22.fa.gz ... done.

==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly22.fa.gz ...
No such file ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly22.fa.gz’.

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa.gz
--2025-04-25 15:09:41--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa.gz ... 19512284
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa.gz ... done.
Length: 19512284 (19M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  18.61M  14.9MB/s    in 1.3s

2025-04-25 15:09:42 (14.9 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa.gz’ saved [19512284]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa.gz
--2025-04-25 15:09:50--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa.gz ... 17632607
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa.gz ... done.
Length: 17632607 (17M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  16.82M  8.52MB/s    in 2.0s

2025-04-25 15:09:52 (8.52 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa.gz’ saved [17632607]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 642M
-rw-r--r-- 1 alexts14 alexts14 40M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz
-rw-r--r-- 1 alexts14 alexts14 30M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa.gz
-rw-r--r-- 1 alexts14 alexts14 28M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa.gz
-rw-r--r-- 1 alexts14 alexts14 28M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa.gz
-rw-r--r-- 1 alexts14 alexts14 26M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa.gz
-rw-r--r-- 1 alexts14 alexts14 24M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa.gz
-rw-r--r-- 1 alexts14 alexts14 24M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa.gz
-rw-r--r-- 1 alexts14 alexts14 24M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa.gz
-rw-r--r-- 1 alexts14 alexts14 23M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa.gz
-rw-r--r-- 1 alexts14 alexts14 22M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa.gz
-rw-r--r-- 1 alexts14 alexts14 20M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa.gz
-rw-r--r-- 1 alexts14 alexts14 41M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz
-rw-r--r-- 1 alexts14 alexts14 20M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa.gz
-rw-r--r-- 1 alexts14 alexts14 18M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa.gz
-rw-r--r-- 1 alexts14 alexts14 19M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa.gz
-rw-r--r-- 1 alexts14 alexts14 17M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa.gz
-rw-r--r-- 1 alexts14 alexts14 39M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz
-rw-r--r-- 1 alexts14 alexts14 38M Apr 25 15:03 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz
-rw-r--r-- 1 alexts14 alexts14 38M Apr 25 15:05 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz
-rw-r--r-- 1 alexts14 alexts14 37M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz
-rw-r--r-- 1 alexts14 alexts14 32M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz
-rw-r--r-- 1 alexts14 alexts14 32M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz
-rw-r--r-- 1 alexts14 alexts14 31M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa.gz
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa.gz
--2025-04-25 15:10:30--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa.gz ... 17287174
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa.gz ... done.
Length: 17287174 (16M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  16.49M  9.01MB/s    in 1.8s

2025-04-25 15:10:32 (9.01 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa.gz’ saved [17287174]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa.gz
--2025-04-25 15:10:52--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa.gz ... 15278285
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa.gz ... done.
Length: 15278285 (15M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  14.57M  19.6MB/s    in 0.7s

2025-04-25 15:10:53 (19.6 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa.gz’ saved [15278285]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa.gz
--2025-04-25 15:11:01--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa.gz ... 14556514
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa.gz ... done.
Length: 14556514 (14M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  13.88M  8.97MB/s    in 1.5s

2025-04-25 15:11:03 (8.97 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa.gz’ saved [14556514]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa.gz
--2025-04-25 15:11:09--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa.gz ... 12639028
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa.gz ... done.
Length: 12639028 (12M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  12.05M  12.0MB/s    in 1.0s

2025-04-25 15:11:11 (12.0 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa.gz’ saved [12639028]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa.gz
--2025-04-25 15:11:16--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa.gz ... 10687275
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa.gz ... done.
Length: 10687275 (10M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  10.19M  8.96MB/s    in 1.1s

2025-04-25 15:11:18 (8.96 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa.gz’ saved [10687275]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa.gz
--2025-04-25 15:11:22--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa.gz ... 7580101
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa.gz ... done.
Length: 7580101 (7.2M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]   7.23M  7.17MB/s    in 1.0s

2025-04-25 15:11:24 (7.17 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa.gz’ saved [7580101]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa.gz
--2025-04-25 15:11:44--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa.gz ... 5401
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa.gz ... done.
Length: 5401 (5.3K) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]   5.27K  --.-KB/s    in 0.003s

2025-04-25 15:11:45 (1.77 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa.gz’ saved [5401]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  wget ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa.gz
--2025-04-25 15:12:18--  ftp://ftp.ensembl.org/pub/release-113/fasta/heterocephalus_glaber_male/dna/Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/fasta/heterocephalus_glaber_male/dna ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa.gz ... 47499681
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa.gz ... done.
Length: 47499681 (45M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  45.30M  15.1MB/s    in 3.0s

2025-04-25 15:12:21 (15.1 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa.gz’ saved [47499681]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 761M
-rw-r--r-- 1 alexts14 alexts14  40M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa.gz
-rw-r--r-- 1 alexts14 alexts14  30M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa.gz
-rw-r--r-- 1 alexts14 alexts14  28M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa.gz
-rw-r--r-- 1 alexts14 alexts14  28M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa.gz
-rw-r--r-- 1 alexts14 alexts14  26M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa.gz
-rw-r--r-- 1 alexts14 alexts14  24M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa.gz
-rw-r--r-- 1 alexts14 alexts14  24M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa.gz
-rw-r--r-- 1 alexts14 alexts14  24M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa.gz
-rw-r--r-- 1 alexts14 alexts14  23M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa.gz
-rw-r--r-- 1 alexts14 alexts14  22M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa.gz
-rw-r--r-- 1 alexts14 alexts14  20M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa.gz
-rw-r--r-- 1 alexts14 alexts14  41M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa.gz
-rw-r--r-- 1 alexts14 alexts14  20M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa.gz
-rw-r--r-- 1 alexts14 alexts14  18M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa.gz
-rw-r--r-- 1 alexts14 alexts14  19M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa.gz
-rw-r--r-- 1 alexts14 alexts14  17M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa.gz
-rw-r--r-- 1 alexts14 alexts14  17M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa.gz
-rw-r--r-- 1 alexts14 alexts14  15M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa.gz
-rw-r--r-- 1 alexts14 alexts14  14M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa.gz
-rw-r--r-- 1 alexts14 alexts14  13M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa.gz
-rw-r--r-- 1 alexts14 alexts14  11M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa.gz
-rw-r--r-- 1 alexts14 alexts14 7.3M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa.gz
-rw-r--r-- 1 alexts14 alexts14  39M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa.gz
-rw-r--r-- 1 alexts14 alexts14  38M Apr 25 15:03 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa.gz
-rw-r--r-- 1 alexts14 alexts14  38M Apr 25 15:05 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa.gz
-rw-r--r-- 1 alexts14 alexts14  37M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa.gz
-rw-r--r-- 1 alexts14 alexts14  32M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa.gz
-rw-r--r-- 1 alexts14 alexts14  32M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa.gz
-rw-r--r-- 1 alexts14 alexts14  31M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa.gz
-rw-r--r-- 1 alexts14 alexts14 5.3K Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa.gz
-rw-r--r-- 1 alexts14 alexts14  46M Apr 25 15:12 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa.gz
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ gunzip *.fa.gz
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 2.4G
-rw-r--r-- 1 alexts14 alexts14 123M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa
-rw-r--r-- 1 alexts14 alexts14  92M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa
-rw-r--r-- 1 alexts14 alexts14  86M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa
-rw-r--r-- 1 alexts14 alexts14  86M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa
-rw-r--r-- 1 alexts14 alexts14  80M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa
-rw-r--r-- 1 alexts14 alexts14  70M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa
-rw-r--r-- 1 alexts14 alexts14  66M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa
-rw-r--r-- 1 alexts14 alexts14  60M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa
-rw-r--r-- 1 alexts14 alexts14 128M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa
-rw-r--r-- 1 alexts14 alexts14  60M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa
-rw-r--r-- 1 alexts14 alexts14  55M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa
-rw-r--r-- 1 alexts14 alexts14  58M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa
-rw-r--r-- 1 alexts14 alexts14  53M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa
-rw-r--r-- 1 alexts14 alexts14  52M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa
-rw-r--r-- 1 alexts14 alexts14  46M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa
-rw-r--r-- 1 alexts14 alexts14  44M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa
-rw-r--r-- 1 alexts14 alexts14  38M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa
-rw-r--r-- 1 alexts14 alexts14  32M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa
-rw-r--r-- 1 alexts14 alexts14  23M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa
-rw-r--r-- 1 alexts14 alexts14 121M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa
-rw-r--r-- 1 alexts14 alexts14 118M Apr 25 15:03 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa
-rw-r--r-- 1 alexts14 alexts14 116M Apr 25 15:05 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa
-rw-r--r-- 1 alexts14 alexts14 115M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa
-rw-r--r-- 1 alexts14 alexts14  99M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa
-rw-r--r-- 1 alexts14 alexts14  98M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa
-rw-r--r-- 1 alexts14 alexts14  95M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa
-rw-r--r-- 1 alexts14 alexts14  17K Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa
-rw-r--r-- 1 alexts14 alexts14 142M Apr 25 15:12 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ cat *.fa > Hglaber_combined_genome.fa
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 4.7G
-rw-r--r-- 1 alexts14 alexts14 123M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa
-rw-r--r-- 1 alexts14 alexts14  92M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa
-rw-r--r-- 1 alexts14 alexts14  86M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa
-rw-r--r-- 1 alexts14 alexts14  86M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa
-rw-r--r-- 1 alexts14 alexts14  80M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa
-rw-r--r-- 1 alexts14 alexts14  70M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa
-rw-r--r-- 1 alexts14 alexts14  66M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa
-rw-r--r-- 1 alexts14 alexts14  60M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa
-rw-r--r-- 1 alexts14 alexts14 128M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa
-rw-r--r-- 1 alexts14 alexts14  60M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa
-rw-r--r-- 1 alexts14 alexts14  55M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa
-rw-r--r-- 1 alexts14 alexts14  58M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa
-rw-r--r-- 1 alexts14 alexts14  53M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa
-rw-r--r-- 1 alexts14 alexts14  52M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa
-rw-r--r-- 1 alexts14 alexts14  46M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa
-rw-r--r-- 1 alexts14 alexts14  44M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa
-rw-r--r-- 1 alexts14 alexts14  38M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa
-rw-r--r-- 1 alexts14 alexts14  32M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa
-rw-r--r-- 1 alexts14 alexts14  23M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa
-rw-r--r-- 1 alexts14 alexts14 121M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa
-rw-r--r-- 1 alexts14 alexts14 118M Apr 25 15:03 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa
-rw-r--r-- 1 alexts14 alexts14 116M Apr 25 15:05 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa
-rw-r--r-- 1 alexts14 alexts14 115M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa
-rw-r--r-- 1 alexts14 alexts14  99M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa
-rw-r--r-- 1 alexts14 alexts14  98M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa
-rw-r--r-- 1 alexts14 alexts14  95M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa
-rw-r--r-- 1 alexts14 alexts14  17K Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa
-rw-r--r-- 1 alexts14 alexts14 142M Apr 25 15:12 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa
-rw-r--r-- 1 alexts14 alexts14 2.4G Apr 25 15:58 Hglaber_combined_genome.fa
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head Hglaber_combined_genome.fa
>1 dna_sm:primary_assembly primary_assembly:Naked_mole-rat_paternal:1:1:126681680:1 REF
ACAGCCGCGCCCACAGCCGTCTCACCACCTCAGGCCACCTCCTGAGGCCCGAGCCCCTAG
GGGTCCCCTCCCCACGGCTCCTGCGCCATCCGTGTGCTCCTCTGGCGGGGCTCCACACAC
GGCAGGACACGACAAGGAATTATTCACTTCTCTCCAGTACGTGGAAATTCTCAACAGTAC
TGCAAGACGCCCTATTTTATTTAAATAGTTATAAGAACATAAGATCCCCAAATTTTTaaa
aaaaGAATAAACAATGTACAACGGTTTTTGAAATATGAAAGTGAAGTTTCAGATATGGAT
TTCCAGGCATGAATGATAAGTCAACTCAAGTGTATCAAACTGGGGTTTCCTTAAACCCTA
CATGTTATATACCTTTTGCGTAGGTCGGACTATCTCATCACCATTATGACCTATGCACTG
TTCCCAAGGTAAGGACACAGAAAATTTGCAGGGGGGTAGTGGGAAGGGGAGAATAGAGAG
GGAGACAAAAAGGTATTGAAAATGATCAAAATACAATATATATATACCAGTTTCTCAAAA
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ # Extract only the chromosome/scaffold name before the first space
 's/ .*(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ sed 's/ .*$//' Hglaber_combined_genome.fa > Hglaber_combined_genome_clean.fa
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head Hglaber_combined_genome_clean.fa
>1
ACAGCCGCGCCCACAGCCGTCTCACCACCTCAGGCCACCTCCTGAGGCCCGAGCCCCTAG
GGGTCCCCTCCCCACGGCTCCTGCGCCATCCGTGTGCTCCTCTGGCGGGGCTCCACACAC
GGCAGGACACGACAAGGAATTATTCACTTCTCTCCAGTACGTGGAAATTCTCAACAGTAC
TGCAAGACGCCCTATTTTATTTAAATAGTTATAAGAACATAAGATCCCCAAATTTTTaaa
aaaaGAATAAACAATGTACAACGGTTTTTGAAATATGAAAGTGAAGTTTCAGATATGGAT
TTCCAGGCATGAATGATAAGTCAACTCAAGTGTATCAAACTGGGGTTTCCTTAAACCCTA
CATGTTATATACCTTTTGCGTAGGTCGGACTATCTCATCACCATTATGACCTATGCACTG
TTCCCAAGGTAAGGACACAGAAAATTTGCAGGGGGGTAGTGGGAAGGGGAGAATAGAGAG
GGAGACAAAAAGGTATTGAAAATGATCAAAATACAATATATATATACCAGTTTCTCAAAA
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ wget ftp://ftp.ensembl.org/pub/release-113/gff3/heterocephalus_glaber_male/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3.gz
p Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3.gz
--2025-04-25 16:16:57--  ftp://ftp.ensembl.org/pub/release-113/gff3/heterocephalus_glaber_male/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3.gz
           => ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3.gz’
Resolving ftp.ensembl.org (ftp.ensembl.org)... 193.62.193.169
Connecting to ftp.ensembl.org (ftp.ensembl.org)|193.62.193.169|:21... connected.
Logging in as anonymous ... Logged in!
==> SYST ... done.    ==> PWD ... done.
==> TYPE I ... done.  ==> CWD (1) /pub/release-113/gff3/heterocephalus_glaber_male ... done.
==> SIZE Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3.gz ... 16724289
==> PASV ... done.    ==> RETR Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3.gz ... done.
Length: 16724289 (16M) (unauthoritative)

Heterocephalus_glaber_male.Na 100%[=================================================>]  15.95M  5.01MB/s    in 3.3s

2025-04-25 16:17:01 (4.88 MB/s) - ‘Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3.gz’ saved [16724289]

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ gunzip Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3.gz
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ samtools faidx Hglaber_combined_genome_clean.fa
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ picard CreateSequenceDictionary \
 R=Hgl>     R=Hglaber_combined_genome_clean.fa \
>     O=Hglaber_combined_genome_clean.dict
/home/alexts14/miniconda3/envs/NMR-env/bin/picard: line 5: warning: setlocale: LC_ALL: cannot change locale (en_US.UTF-8): No such file or directory
INFO    2025-04-25 16:54:37     CreateSequenceDictionary

********** NOTE: Picard's command line syntax is changing.
**********
********** For more information, please see:
********** https://github.com/broadinstitute/picard/wiki/Command-Line-Syntax-Transition-For-Users-(Pre-Transition)
**********
********** The command line looks like this in the new syntax:
**********
**********    CreateSequenceDictionary -R Hglaber_combined_genome_clean.fa -O Hglaber_combined_genome_clean.dict
**********


16:54:38.458 INFO  NativeLibraryLoader - Loading libgkl_compression.so from jar:file:/home/alexts14/miniconda3/envs/NMR-env/share/picard-2.20.4-0/picard.jar!/com/intel/gkl/native/libgkl_compression.so
[Fri Apr 25 16:54:38 CEST 2025] CreateSequenceDictionary OUTPUT=Hglaber_combined_genome_clean.dict REFERENCE=Hglaber_combined_genome_clean.fa    TRUNCATE_NAMES_AT_WHITESPACE=true NUM_SEQUENCES=2147483647 VERBOSITY=INFO QUIET=false VALIDATION_STRINGENCY=STRICT COMPRESSION_LEVEL=5 MAX_RECORDS_IN_RAM=500000 CREATE_INDEX=false CREATE_MD5_FILE=false GA4GH_CLIENT_SECRETS=client_secrets.json USE_JDK_DEFLATER=false USE_JDK_INFLATER=false
[Fri Apr 25 16:54:38 CEST 2025] Executing as alexts14@GabanouMelissa on Linux 5.15.167.4-microsoft-standard-WSL2 amd64; OpenJDK 64-Bit Server VM 11.0.13+7-b1751.21; Deflater: Intel; Inflater: Intel; Provider GCS is not available; Picard version: 2.20.4-SNAPSHOT
[Fri Apr 25 16:54:58 CEST 2025] picard.sam.CreateSequenceDictionary done. Elapsed time: 0.33 minutes.
Runtime.totalMemory()=536870912
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 7.2G
-rw-r--r-- 1 alexts14 alexts14 209M Apr 25 16:17 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3
-rw-r--r-- 1 alexts14 alexts14 123M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa
-rw-r--r-- 1 alexts14 alexts14  92M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa
-rw-r--r-- 1 alexts14 alexts14  86M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa
-rw-r--r-- 1 alexts14 alexts14  86M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa
-rw-r--r-- 1 alexts14 alexts14  80M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa
-rw-r--r-- 1 alexts14 alexts14  70M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa
-rw-r--r-- 1 alexts14 alexts14  66M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa
-rw-r--r-- 1 alexts14 alexts14  60M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa
-rw-r--r-- 1 alexts14 alexts14 128M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa
-rw-r--r-- 1 alexts14 alexts14  60M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa
-rw-r--r-- 1 alexts14 alexts14  55M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa
-rw-r--r-- 1 alexts14 alexts14  58M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa
-rw-r--r-- 1 alexts14 alexts14  53M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa
-rw-r--r-- 1 alexts14 alexts14  52M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa
-rw-r--r-- 1 alexts14 alexts14  46M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa
-rw-r--r-- 1 alexts14 alexts14  44M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa
-rw-r--r-- 1 alexts14 alexts14  38M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa
-rw-r--r-- 1 alexts14 alexts14  32M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa
-rw-r--r-- 1 alexts14 alexts14  23M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa
-rw-r--r-- 1 alexts14 alexts14 121M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa
-rw-r--r-- 1 alexts14 alexts14 118M Apr 25 15:03 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa
-rw-r--r-- 1 alexts14 alexts14 116M Apr 25 15:05 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa
-rw-r--r-- 1 alexts14 alexts14 115M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa
-rw-r--r-- 1 alexts14 alexts14  99M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa
-rw-r--r-- 1 alexts14 alexts14  98M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa
-rw-r--r-- 1 alexts14 alexts14  95M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa
-rw-r--r-- 1 alexts14 alexts14  17K Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa
-rw-r--r-- 1 alexts14 alexts14 142M Apr 25 15:12 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa
-rw-r--r-- 1 alexts14 alexts14 2.4G Apr 25 15:58 Hglaber_combined_genome.fa
-rw-r--r-- 1 alexts14 alexts14 4.0K Apr 25 16:54 Hglaber_combined_genome_clean.dict
-rw-r--r-- 1 alexts14 alexts14 2.4G Apr 25 16:08 Hglaber_combined_genome_clean.fa
-rw-r--r-- 1 alexts14 alexts14  875 Apr 25 16:53 Hglaber_combined_genome_clean.fa.fai
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$
```
So I downloaded all the chromosome seperatly, combine them and created the fai and dict files for IGV and also downloaded the gff3 file for the annotations.
```
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ sort -k1,1 -k4,4n Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 > Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.sorted.gff3
```
also the igv needed the sorted gff3

# 28.04.2025
## TSS and five_prime_UTR

```
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ awk '$3 == "gene" { if ($7 == "+") print $1, $4-1, $4, $9; else print $1, $5-1, $5, $9 }' Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.sorted.gff3 > all_genes_TSS.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ ls -lh
total 7.4G
-rw-r--r-- 1 alexts14 alexts14 209M Apr 25 16:17 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3
-rw-r--r-- 1 alexts14 alexts14 209M Apr 28 10:45 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.sorted.gff3
-rw-r--r-- 1 alexts14 alexts14 123M Apr 25 15:00 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.1.fa
-rw-r--r-- 1 alexts14 alexts14  92M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.10.fa
-rw-r--r-- 1 alexts14 alexts14  86M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.11.fa
-rw-r--r-- 1 alexts14 alexts14  86M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.12.fa
-rw-r--r-- 1 alexts14 alexts14  80M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.13.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.14.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.15.fa
-rw-r--r-- 1 alexts14 alexts14  75M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.16.fa
-rw-r--r-- 1 alexts14 alexts14  70M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.17.fa
-rw-r--r-- 1 alexts14 alexts14  66M Apr 25 15:08 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.18.fa
-rw-r--r-- 1 alexts14 alexts14  60M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.19.fa
-rw-r--r-- 1 alexts14 alexts14 128M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.2.fa
-rw-r--r-- 1 alexts14 alexts14  60M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.20.fa
-rw-r--r-- 1 alexts14 alexts14  55M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.21.fa
-rw-r--r-- 1 alexts14 alexts14  58M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.22.fa
-rw-r--r-- 1 alexts14 alexts14  53M Apr 25 15:09 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.23.fa
-rw-r--r-- 1 alexts14 alexts14  52M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.24.fa
-rw-r--r-- 1 alexts14 alexts14  46M Apr 25 15:10 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.25.fa
-rw-r--r-- 1 alexts14 alexts14  44M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.26.fa
-rw-r--r-- 1 alexts14 alexts14  38M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.27.fa
-rw-r--r-- 1 alexts14 alexts14  32M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.28.fa
-rw-r--r-- 1 alexts14 alexts14  23M Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.29.fa
-rw-r--r-- 1 alexts14 alexts14 121M Apr 25 15:02 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.3.fa
-rw-r--r-- 1 alexts14 alexts14 118M Apr 25 15:03 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.4.fa
-rw-r--r-- 1 alexts14 alexts14 116M Apr 25 15:05 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.5.fa
-rw-r--r-- 1 alexts14 alexts14 115M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.6.fa
-rw-r--r-- 1 alexts14 alexts14  99M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.7.fa
-rw-r--r-- 1 alexts14 alexts14  98M Apr 25 15:06 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.8.fa
-rw-r--r-- 1 alexts14 alexts14  95M Apr 25 15:07 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.9.fa
-rw-r--r-- 1 alexts14 alexts14  17K Apr 25 15:11 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.MT.fa
-rw-r--r-- 1 alexts14 alexts14 142M Apr 25 15:12 Heterocephalus_glaber_male.Naked_mole-rat_paternal.dna_sm.primary_assembly.X.fa
-rw-r--r-- 1 alexts14 alexts14 3.8K Apr 28 10:32 Hglaber_combined_genome.dict
-rw-r--r-- 1 alexts14 alexts14 2.4G Apr 25 15:58 Hglaber_combined_genome.fa
-rw-r--r-- 1 alexts14 alexts14  876 Apr 28 10:31 Hglaber_combined_genome.fa.fai
-rw-r--r-- 1 alexts14 alexts14 4.0K Apr 25 16:54 Hglaber_combined_genome_clean.dict
-rw-r--r-- 1 alexts14 alexts14 2.4G Apr 25 16:08 Hglaber_combined_genome_clean.fa
-rw-r--r-- 1 alexts14 alexts14  875 Apr 25 16:53 Hglaber_combined_genome_clean.fa.fai
-rw-r--r-- 1 alexts14 alexts14 2.9M Apr 28 11:16 all_genes_TSS.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head all_genes_TSS.bed
1 79208 79209 ID=gene:ENSHGLG00100011751;biotype=protein_coding;gene_id=ENSHGLG00100011751;logic_name=ensembl;version=2
1 99469 99470 ID=gene:ENSHGLG00100049051;biotype=protein_coding;gene_id=ENSHGLG00100049051;logic_name=ensembl;version=1
1 155111 155112 ID=gene:ENSHGLG00100047534;biotype=protein_coding;gene_id=ENSHGLG00100047534;logic_name=ensembl;version=1
1 210342 210343 ID=gene:ENSHGLG00100007061;biotype=protein_coding;gene_id=ENSHGLG00100007061;logic_name=ensembl;version=2
1 303332 303333 ID=gene:ENSHGLG00100050874;biotype=protein_coding;gene_id=ENSHGLG00100050874;logic_name=ensembl;version=1
1 471996 471997 ID=gene:ENSHGLG00100009882;biotype=protein_coding;gene_id=ENSHGLG00100009882;logic_name=ensembl;version=2
1 577761 577762 ID=gene:ENSHGLG00100040381;biotype=protein_coding;gene_id=ENSHGLG00100040381;logic_name=ensembl;version=1
1 578257 578258 ID=gene:ENSHGLG00100007103;biotype=protein_coding;gene_id=ENSHGLG00100007103;logic_name=ensembl;version=2
1 717826 717827 ID=gene:ENSHGLG00100050535;biotype=protein_coding;gene_id=ENSHGLG00100050535;logic_name=ensembl;version=1
1 717754 717755 ID=gene:ENSHGLG00100006540;biotype=protein_coding;gene_id=ENSHGLG00100006540;logic_name=ensembl;version=2
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ tail all_genes_TSS.bed
X 143758228 143758229 ID=gene:ENSHGLG00100035787;biotype=protein_coding;gene_id=ENSHGLG00100035787;logic_name=ensembl;version=1
X 143885931 143885932 ID=gene:ENSHGLG00100042383;biotype=protein_coding;gene_id=ENSHGLG00100042383;logic_name=ensembl;version=1
X 144141762 144141763 ID=gene:ENSHGLG00100012734;biotype=protein_coding;gene_id=ENSHGLG00100012734;logic_name=ensembl;version=2
X 144141387 144141388 ID=gene:ENSHGLG00100045952;biotype=protein_coding;gene_id=ENSHGLG00100045952;logic_name=ensembl;version=1
X 144216158 144216159 ID=gene:ENSHGLG00100020782;biotype=protein_coding;gene_id=ENSHGLG00100020782;logic_name=ensembl;version=2
X 144855810 144855811 ID=gene:ENSHGLG00100002557;biotype=protein_coding;gene_id=ENSHGLG00100002557;logic_name=ensembl;version=2
X 145028277 145028278 ID=gene:ENSHGLG00100020139;biotype=protein_coding;gene_id=ENSHGLG00100020139;logic_name=ensembl;version=2
X 145608004 145608005 ID=gene:ENSHGLG00100041293;biotype=protein_coding;gene_id=ENSHGLG00100041293;logic_name=ensembl;version=1
X 145655946 145655947 ID=gene:ENSHGLG00100012745;biotype=protein_coding;gene_id=ENSHGLG00100012745;logic_name=ensembl;version=2
X 145681433 145681434 ID=gene:ENSHGLG00100035039;biotype=protein_coding;gene_id=ENSHGLG00100035039;logic_name=ensembl;version=1
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ awk '$3 == "five_prime_UTR" {print $1, $4, $5, $9}' Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.sorted.gff3 > all_five_prime_UTRs.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ awk '{print $0, $3-$2}' all_five_prime_UTRs.bed | sort -k5,5nr | head -n 50 > top50_five_prime_UTRs.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head top50_five_prime_UTRs.bed
9 73916974 73936875 Parent=transcript:ENSHGLT00100067400 19901
18 24075644 24095202 Parent=transcript:ENSHGLT00100058256 19558
1 58707437 58726905 Parent=transcript:ENSHGLT00100057063 19468
9 73916974 73935347 Parent=transcript:ENSHGLT00100084698 18373
25 24360387 24378636 Parent=transcript:ENSHGLT00100078466 18249
10 5660108 5677118 Parent=transcript:ENSHGLT00100058596 17010
11 74086303 74101943 Parent=transcript:ENSHGLT00100081430 15640
24 11613210 11628809 Parent=transcript:ENSHGLT00100051176 15599
11 2687544 2702797 Parent=transcript:ENSHGLT00100076222 15253
8 12777006 12792152 Parent=transcript:ENSHGLT00100062038 15146
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head all_five_prime_UTRs.bed
1 76844 76904 Parent=transcript:ENSHGLT00100016094
1 76844 76904 Parent=transcript:ENSHGLT00100016095
1 76844 76904 Parent=transcript:ENSHGLT00100041989
1 76844 76904 Parent=transcript:ENSHGLT00100092820
1 78262 78607 Parent=transcript:ENSHGLT00100041989
1 78262 78607 Parent=transcript:ENSHGLT00100092820
1 79045 79193 Parent=transcript:ENSHGLT00100016094
1 79045 79209 Parent=transcript:ENSHGLT00100016095
1 99470 99695 Parent=transcript:ENSHGLT00100047040
1 99485 99695 Parent=transcript:ENSHGLT00100080349
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ tail all_five_prime_UTRs.bed
X 144854480 144854501 Parent=transcript:ENSHGLT00100003415
X 144854480 144854501 Parent=transcript:ENSHGLT00100048643
X 144854480 144854501 Parent=transcript:ENSHGLT00100065317
X 144855635 144855811 Parent=transcript:ENSHGLT00100003415
X 144855635 144855811 Parent=transcript:ENSHGLT00100048643
X 144855635 144855811 Parent=transcript:ENSHGLT00100065317
X 145607195 145607393 Parent=transcript:ENSHGLT00100044447
X 145607195 145607393 Parent=transcript:ENSHGLT00100067466
X 145607913 145608005 Parent=transcript:ENSHGLT00100052989
X 145681434 145681818 Parent=transcript:ENSHGLT00100051184
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$
```
In summary i created files of the TSS ( all_genes_TSS.bed), the five_prime_UTR (all_five_prime_UTRs.bed) and the top50 UTRs by lenght (top50_five_prime_UTRs.bed)

![image](https://github.com/user-attachments/assets/13b1bfde-06a0-4e28-9fe3-c4e148b17063)

Here is a visual of one of the top50 five_prive_UTR using IGV. 

# 29.04.2025
## New indexing we the latest ref genome assembly 

```
(base) alexts14@GabanouMelissa:~$ conda activate NMR-env
(NMR-env) alexts14@GabanouMelissa:~$ cd nmr_chromosomes
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ gffread Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 -T -o Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf
Command 'gffread' not found, but can be installed with:
sudo apt install gffread
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ sudo apt install gffread
[sudo] password for alexts14:
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following package was automatically installed and is no longer required:
  libllvm17t64
Use 'sudo apt autoremove' to remove it.
The following additional packages will be installed:
  libgclib3t64
The following NEW packages will be installed:
  gffread libgclib3t64
0 upgraded, 2 newly installed, 0 to remove and 26 not upgraded.
Need to get 229 kB of archives.
After this operation, 689 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu noble/universe amd64 libgclib3t64 amd64 0.12.7+ds-5ubuntu3 [162 kB]
Get:2 http://archive.ubuntu.com/ubuntu noble/universe amd64 gffread amd64 0.12.7-4build1 [66.2 kB]
Fetched 229 kB in 0s (843 kB/s)
Selecting previously unselected package libgclib3t64:amd64.
(Reading database ... 40775 files and directories currently installed.)
Preparing to unpack .../libgclib3t64_0.12.7+ds-5ubuntu3_amd64.deb ...
Unpacking libgclib3t64:amd64 (0.12.7+ds-5ubuntu3) ...
Selecting previously unselected package gffread.
Preparing to unpack .../gffread_0.12.7-4build1_amd64.deb ...
Unpacking gffread (0.12.7-4build1) ...
Setting up libgclib3t64:amd64 (0.12.7+ds-5ubuntu3) ...
Setting up gffread (0.12.7-4build1) ...
Processing triggers for man-db (2.12.0-4build2) ...
Processing triggers for libc-bin (2.39-0ubuntu8.4) ...
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ gffread Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 -T -o Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ mkdir ~/nmr_chromosomes/STAR_index
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ cd ~STAR_index
-bash: cd: ~STAR_index: No such file or directory
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$  cd STAR_index
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       570Mi       7.3Gi       3.1Mi       138Mi       7.2Gi
Swap:          4.0Gi          0B       4.0Gi
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ sudo fallocate -l 50G /swapfile
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ sudo chmod 600 /swapfile
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ sudo mkswap /swapfile
mkswap: /swapfile: warning: wiping old swap signature.
Setting up swapspace version 1, size = 50 GiB (53687087104 bytes)
no label, UUID=5c1f84bf-f719-4e6b-acd2-9f210f772392
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ sudo swapon /swapfile
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       624Mi       7.2Gi       3.1Mi       171Mi       7.1Gi
Swap:           53Gi          0B        53Gi
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ nproc
12
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ STAR --runThreadN 8 \
>      --runMode genomeGenerate \
>      --genomeDir ~/nmr_chromosomes/STAR_index/ \
>      --genomeFastaFiles ~/nmr_chromosomes/Hglaber_combined_genome.fa \
>      --sjdbGTFfile ~/nmr_chromosomes/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
-sjdbOv>      --sjdbOverhang 99
        /home/alexts14/miniconda3/envs/NMR-env/bin/STAR-avx2 --runThreadN 8 --runMode genomeGenerate --genomeDir /home/alexts14/nmr_chromosomes/STAR_index/ --genomeFastaFiles /home/alexts14/nmr_chromosomes/Hglaber_combined_genome.fa --sjdbGTFfile /home/alexts14/nmr_chromosomes/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf --sjdbOverhang 99
        STAR version: 2.7.11a   compiled: 2023-09-15T02:58:53+0000 :/opt/conda/conda-bld/star_1694746407721/work/source
Apr 29 16:48:52 ..... started STAR run
Apr 29 16:48:52 ... starting to generate Genome files
Apr 29 16:50:24 ..... processing annotations GTF
Apr 29 16:50:56 ... starting to sort Suffix Array. This may take a long time...
Apr 29 16:51:19 ... sorting Suffix Array chunks and saving them to disk...
STAR --runThreadN 8 \
     --runMode genomeGenerate \
     --genomeDir ~/nmr_chromosomes/STAR_index/ \
     --genomeFastaFiles ~/nmr_chromosomes/Hglaber_combined_genome.fa \
     --sjdbGTFfile ~/nmr_chromosomes/Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gtf \
     --sjdbOverhang 99
```

Indexing the ref genome again with the gtf from the gff3 to start alignments again!

# 02.05.2025
## Index still running

```
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ ls -lh
total 30G
-rw-r--r-- 1 alexts14 alexts14 6.4M May  2 04:19 Log.out
-rw-r--r-- 1 alexts14 alexts14 1.8G Apr 30 16:41 SA_0
-rw-r--r-- 1 alexts14 alexts14 1.7G Apr 30 23:35 SA_1
-rw-r--r-- 1 alexts14 alexts14 1.8G May  2 02:38 SA_10
-rw-r--r-- 1 alexts14 alexts14 1.9G May  2 02:25 SA_11
-rw-r--r-- 1 alexts14 alexts14 1.8G May  2 02:24 SA_12
-rw-r--r-- 1 alexts14 alexts14 1.8G May  2 02:36 SA_13
-rw-r--r-- 1 alexts14 alexts14 1.7G May  2 02:39 SA_14
-rw-r--r-- 1 alexts14 alexts14 1.7G May  2 02:38 SA_15
-rw-r--r-- 1 alexts14 alexts14 1.8G May  2 02:37 SA_16
-rw-r--r-- 1 alexts14 alexts14 1.8G Apr 30 16:45 SA_2
-rw-r--r-- 1 alexts14 alexts14 1.7G Apr 30 16:42 SA_3
-rw-r--r-- 1 alexts14 alexts14 1.8G Apr 30 16:35 SA_4
-rw-r--r-- 1 alexts14 alexts14 1.9G Apr 30 16:46 SA_5
-rw-r--r-- 1 alexts14 alexts14 1.8G Apr 30 16:47 SA_6
-rw-r--r-- 1 alexts14 alexts14 1.7G Apr 30 16:44 SA_7
-rw-r--r-- 1 alexts14 alexts14 1.9G Apr 30 23:22 SA_8
-rw-r--r-- 1 alexts14 alexts14 1.8G May  2 02:36 SA_9
drwx------ 2 alexts14 alexts14 4.0K Apr 29 16:48 _STARtmp
-rw-r--r-- 1 alexts14 alexts14  285 Apr 29 16:50 chrLength.txt
-rw-r--r-- 1 alexts14 alexts14   83 Apr 29 16:50 chrName.txt
-rw-r--r-- 1 alexts14 alexts14  368 Apr 29 16:50 chrNameLength.txt
-rw-r--r-- 1 alexts14 alexts14  332 Apr 29 16:50 chrStart.txt
-rw-r--r-- 1 alexts14 alexts14  19M Apr 29 16:50 exonGeTrInfo.tab
-rw-r--r-- 1 alexts14 alexts14 8.3M Apr 29 16:50 exonInfo.tab
-rw-r--r-- 1 alexts14 alexts14 2.1M Apr 29 16:50 geneInfo.tab
-rw-r--r-- 1 alexts14 alexts14 6.5M Apr 29 16:50 sjdbList.fromGTF.out.tab
-rw-r--r-- 1 alexts14 alexts14 5.2M Apr 29 16:50 transcriptInfo.tab
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/STAR_index$ top
top - 14:11:29 up 3 days,  4:01,  1 user,  load average: 4.13, 4.07, 4.06
Tasks:  29 total,   1 running,  28 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.1 sy,  0.0 ni, 64.8 id, 35.1 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :   7945.2 total,    125.0 free,   7884.9 used,    128.4 buff/cache
MiB Swap:  55296.0 total,  42956.6 free,  12339.4 used.     60.2 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
   1307 alexts14  20   0   18.7g   6.9g    208 D   1.5  89.0 305:16.00 STAR-avx2
      1 root      20   0   21852   2808   1328 S   0.0   0.0   0:24.86 systemd
      2 root      20   0    2776    180    180 S   0.0   0.0   0:00.02 init-systemd(Ub
      7 root      20   0    2804      4      4 S   0.0   0.0   0:01.14 init
    139 root      20   0   24124   1984   1528 S   0.0   0.0   0:00.96 systemd-udevd
    235 systemd+  20   0   21452    264    124 S   0.0   0.0   0:02.61 systemd-resolve
    236 systemd+  20   0   91020     60      8 S   0.0   0.0   0:08.11 systemd-timesyn
    256 root      20   0    4236     92      0 S   0.0   0.0   0:00.90 cron
    257 message+  20   0    9600    304      0 S   0.0   0.0   0:19.59 dbus-daemon
    266 root      20   0   17976    884    756 S   0.0   0.0   0:07.40 systemd-logind
    269 root      20   0 2421668   2636      0 S   0.0   0.0   3:13.65 wsl-pro-service
    275 root      20   0    3160      0      0 S   0.0   0.0   0:00.01 agetty
    279 root      20   0    3116      0      0 S   0.0   0.0   0:00.01 agetty
    282 syslog    20   0  222508    340      0 S   0.0   0.0   0:05.36 rsyslogd
    289 root      20   0  107016      0      0 S   0.0   0.0   0:00.21 unattended-upgr
    330 root      20   0    2780      0      0 S   0.0   0.0   0:00.00 SessionLeader
    331 root      20   0    2780      0      0 S   0.0   0.0   0:00.03 Relay(332)
    332 alexts14  20   0    7556      4      4 S   0.0   0.0   0:00.13 bash
    333 root      20   0    6660      0      0 S   0.0   0.0   0:00.02 login
    493 alexts14  20   0   20260    704    232 S   0.0   0.0   0:01.74 systemd
    494 alexts14  20   0   21144      0      0 S   0.0   0.0   0:00.00 (sd-pam)
    509 alexts14  20   0    6072      0      0 S   0.0   0.0   0:00.04 bash
    794 polkitd   20   0  308164      0      0 S   0.0   0.0   0:07.49 polkitd
```

# 16/05/2025

Indexing failed.

Extraction of five prime UTRS start and +- 150 bases 

```
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ cut -f3 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 | sort | uniq -c
      1 #!genebuild-last-updated 2022-09
      1 #!genome-build  Naked_mole-rat_paternal
      1 #!genome-build-accession GCA_944319725.1
      1 #!genome-date 2022-07
      1 #!genome-version Naked_mole-rat_paternal
  35146 ###
      1 ##gff-version 3
      1 ##sequence-region   1 1 126681680
      1 ##sequence-region   10 1 94825129
      1 ##sequence-region   11 1 88157664
      1 ##sequence-region   12 1 87863200
      1 ##sequence-region   13 1 82497129
      1 ##sequence-region   14 1 76838549
      1 ##sequence-region   15 1 76365940
      1 ##sequence-region   16 1 76437676
      1 ##sequence-region   17 1 71606942
      1 ##sequence-region   18 1 67431141
      1 ##sequence-region   19 1 60928233
      1 ##sequence-region   2 1 131346783
      1 ##sequence-region   20 1 61068310
      1 ##sequence-region   21 1 56435557
      1 ##sequence-region   22 1 59689252
      1 ##sequence-region   23 1 53761172
      1 ##sequence-region   24 1 52691189
      1 ##sequence-region   25 1 46678892
      1 ##sequence-region   26 1 44400560
      1 ##sequence-region   27 1 38566542
      1 ##sequence-region   28 1 32538853
      1 ##sequence-region   29 1 23277160
      1 ##sequence-region   3 1 124509033
      1 ##sequence-region   4 1 121083042
      1 ##sequence-region   5 1 119101870
      1 ##sequence-region   6 1 118199489
      1 ##sequence-region   7 1 101507220
      1 ##sequence-region   8 1 100330867
      1 ##sequence-region   9 1 97794639
      1 ##sequence-region   MT 1 16386
      1 ##sequence-region   OX090940.1 1 61021973
      1 ##sequence-region   X 1 145805425
 501232 CDS
      1 C_gene_segment
      3 J_gene_segment
     19 V_gene_segment
     19 Y_RNA
 104755 biological_region
 591691 exon
  67025 five_prime_UTR
  23343 gene
  16904 lnc_RNA
  51089 mRNA
     85 miRNA
  10427 ncRNA_gene
   1344 pseudogene
   1344 pseudogenic_transcript
      9 rRNA
     32 region
     33 scRNA
   1691 snRNA
    689 snoRNA
     22 tRNA
  44558 three_prime_UTR
     37 transcript
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ awk '$3 == "five_prime_UTR" && $1 !~ /^#/ {
chrom = >     chrom = $1;
>     strand = $7;
>     start = (strand == "+") ? $4 : $5;
>     win_start = start - 150;
>     win_end = start + 150;
>     if (win_start < 0) win_start = 0;
>
  # ext>     # extract transcript_id or gene_id from column 9
>     match($9, /ID=([^;]+)/, arr);
>     name = (arr[1] != "") ? arr[1] : ".";
>
 print c>     print chrom, win_start, win_end, name, ".", strand;
S="\t> }' OFS="\t" Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 \
> > five_prime_UTR_plusminus150_fromGFF3.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head five_prime_UTR_plusminus150_fromGFF3.bed
1       76754   77054   .       .       -
1       78457   78757   .       .       -
1       76754   77054   .       .       -
1       78457   78757   .       .       -
1       76754   77054   .       .       -
1       79043   79343   .       .       -
1       76754   77054   .       .       -
1       79059   79359   .       .       -
1       99320   99620   .       .       +
1       99335   99635   .       .       +
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ awk '$3 == "five_prime_UTR" && $1 !~ /^#/ {
chrom = >     chrom = $1;
>     strand = $7;
>     start = (strand == "+") ? $4 : $5;
>     win_start = start - 150;
>     win_end = start + 150;
>     if (win_start < 0) win_start = 0;
>
  match(>     match($9, /ID=([^;]+)/, arr);
>     id = (arr[1] != "") ? arr[1] : ".";
>
>     print chrom, win_start, win_end, id, ".", strand;
> }' OFS="\t" Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 \
> > five_prime_UTR_plusminus150_withID.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head five_prime_UTR_plusminus150_withID.bed
1       76754   77054   .       .       -
1       78457   78757   .       .       -
1       76754   77054   .       .       -
1       78457   78757   .       .       -
1       76754   77054   .       .       -
1       79043   79343   .       .       -
1       76754   77054   .       .       -
1       79059   79359   .       .       -
1       99320   99620   .       .       +
1       99335   99635   .       .       +
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ grep "five_prime_UTR" Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 | head -n 1
1       ensembl five_prime_UTR  76844   76904   .       -       .       Parent=transcript:ENSHGLT00100092820
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ awk '$3 == "five_prime_UTR" && $1 !~ /^#/ {
chrom = >     chrom = $1;
>     strand = $7;
>     start = (strand == "+") ? $4 : $5;
>     win_start = start - 150;
>     win_end = start + 150;
>     if (win_start < 0) win_start = 0;
>
  match(>     match($9, /Parent=transcript:([^;]+)/, arr);
>     transcript_id = (arr[1] != "") ? arr[1] : ".";
>
>     print chrom, win_start, win_end, transcript_id, ".", strand;
> }' OFS="\t" Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 \
> > five_prime_UTR_plusminus150_withTranscriptID.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head five_prime_UTR_plusminus150_withTranscriptID.bed
1       76754   77054   ENSHGLT00100092820      .       -
1       78457   78757   ENSHGLT00100092820      .       -
1       76754   77054   ENSHGLT00100041989      .       -
1       78457   78757   ENSHGLT00100041989      .       -
1       76754   77054   ENSHGLT00100016094      .       -
1       79043   79343   ENSHGLT00100016094      .       -
1       76754   77054   ENSHGLT00100016095      .       -
1       79059   79359   ENSHGLT00100016095      .       -
1       99320   99620   ENSHGLT00100047040      .       +
1       99335   99635   ENSHGLT00100080349      .       +
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ awk '$3 == "five_prime_UTR" && $1 !~ /^#/ {
om = $1>     chrom = $1;
>     strand = $7;
>
>     # 1-base position depends on strand
>     pos = (strand == "+") ? $4 : $5;
>     start = pos - 1;
>     end = pos;
>     if (start < 0) start = 0;
>
>     # extract transcript ID
>     match($9, /Parent=transcript:([^;]+)/, arr);
   trans>     transcript_id = (arr[1] != "") ? arr[1] : ".";>
hrom, st>     print chrom, start, end, transcript_id, ".", strand;
> }' OFS="\t" Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3 \
> > five_prime_UTR_first_base.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes$ head five_prime_UTR_first_base.bed
1       76903   76904   ENSHGLT00100092820      .       -
1       78606   78607   ENSHGLT00100092820      .       -
1       76903   76904   ENSHGLT00100041989      .       -
1       78606   78607   ENSHGLT00100041989      .       -
1       76903   76904   ENSHGLT00100016094      .       -
1       79192   79193   ENSHGLT00100016094      .       -
1       76903   76904   ENSHGLT00100016095      .       -
1       79208   79209   ENSHGLT00100016095      .       -
1       99469   99470   ENSHGLT00100047040      .       +
1       99484   99485   ENSHGLT00100080349      .       +
```

![image](https://github.com/user-attachments/assets/81391047-63a7-4bf1-9d6f-ffa8b49209cc)

# 19.05.2025
Exctract the -150/+150 sequence 
 ```
) alexts14@GabanouMelissa:~/nmr_chromosomes$ cd  5utr_analysis
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ ls -lh
total 2.9G
-rw-r--r-- 1 alexts14 alexts14 209M May 12 14:58 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3
-rw-r--r-- 1 alexts14 alexts14 209M May 12 14:59 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.sorted.gff3
-rw-r--r-- 1 alexts14 alexts14 2.4G May 12 14:59 Hglaber_combined_genome.fa
-rw-r--r-- 1 alexts14 alexts14  876 May 16 13:58 Hglaber_combined_genome.fa.fai
-rw-r--r-- 1 alexts14 alexts14  22M May 16 15:18 five_prime_UTR_plusminus150_sequences.fa
-rw-r--r-- 1 alexts14 alexts14    0 May 15 14:29 five_prime_UTR_plusminus150_with_geneid.bed
-rw-r--r-- 1 alexts14 alexts14 135M May 15 14:20 working_5utr.gtf
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ cut -f1 ../Hglaber_combined_genome.fa.fai | sort > valid_chroms.txt
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ awk 'NR==FNR {ok[$1]; next} $1 in ok' valid_chroms.txt ../five_prime_UTR_plusminus150_withTranscriptID.bed > clean_utr.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ ls -lh
total 2.9G
-rw-r--r-- 1 alexts14 alexts14 209M May 12 14:58 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.gff3
-rw-r--r-- 1 alexts14 alexts14 209M May 12 14:59 Heterocephalus_glaber_male.Naked_mole-rat_paternal.113.sorted.gff3
-rw-r--r-- 1 alexts14 alexts14 2.4G May 12 14:59 Hglaber_combined_genome.fa
-rw-r--r-- 1 alexts14 alexts14  876 May 16 13:58 Hglaber_combined_genome.fa.fai
-rw-r--r-- 1 alexts14 alexts14 2.7M May 19 15:26 clean_utr.bed
-rw-r--r-- 1 alexts14 alexts14  22M May 16 15:18 five_prime_UTR_plusminus150_sequences.fa
-rw-r--r-- 1 alexts14 alexts14    0 May 15 14:29 five_prime_UTR_plusminus150_with_geneid.bed
-rw-r--r-- 1 alexts14 alexts14   83 May 19 15:26 valid_chroms.txt
-rw-r--r-- 1 alexts14 alexts14 135M May 15 14:20 working_5utr.gtf
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ head valid_chroms.txt
1
10
11
12
13
14
15
16
17
18
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ wc -l valid_chroms.txt
31 valid_chroms.txt
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ head clean_utr.bed
1       76754   77054   ENSHGLT00100092820      .       -
1       78457   78757   ENSHGLT00100092820      .       -
1       76754   77054   ENSHGLT00100041989      .       -
1       78457   78757   ENSHGLT00100041989      .       -
1       76754   77054   ENSHGLT00100016094      .       -
1       79043   79343   ENSHGLT00100016094      .       -
1       76754   77054   ENSHGLT00100016095      .       -
1       79059   79359   ENSHGLT00100016095      .       -
1       99320   99620   ENSHGLT00100047040      .       +
1       99335   99635   ENSHGLT00100080349      .       +
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ wc -l clean_utr.bed
64580 clean_utr.bed
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ cut -f1 clean_utr.bed | sort | uniq -c
   2756 1
   1695 10
   1221 11
   2340 12
   2248 13
   1495 14
   2357 15
   1183 16
   2036 17
   1053 18
   2079 19
   2881 2
   3327 20
    998 21
   1833 22
   2865 23
   1389 24
   1373 25
   1398 26
   1145 27
   1405 28
   2909 29
   2032 3
   3147 4
   4002 5
   2171 6
   3220 7
   2921 8
   2041 9
   3060 X
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ bedtools getfasta \
>   -fi ../Hglaber_combined_genome.fa \
>   -bed clean_utr.bed \
>   -s \
ame \
  >   -name \
>   -fo five_prime_UTR_plusminus150_sequences_clean.fa


Feature (20:61068160-61068460) beyond the length of 20 size (61068310 bp).  Skipping.
Feature (20:61068160-61068460) beyond the length of 20 size (61068310 bp).  Skipping.

(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ grep -c "^>" five_prime_UTR_plusminus150_sequences_clean.fa
64578
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ awk 'BEGIN{OFS="\t"} /^>/ {header=substr($0,2); next} {print header, $0}' five_prime_UTR_plusminus150_sequences_clean.fa > utr_sequences_table.tsv
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$ head utr_sequences_table.tsv
ENSHGLT00100092820::1:76754-77054(-)    GAGTAAATTTTATATTaaaaaaaaTAGAATAGTTTTATTCTGGATTAATGCAGAAGTCTTTAGATTAGTACAGGGATTTAGGTAAGATTTTTTACAAGTTTTGAACTTGTGCCCTTGATAAATTGGCTAACCTTATGTTTCTTTTCACAGGCTGGGTGAACTCATGGACCTGGTGTTTTTCTTCTGAGAAAGAAACCTGCTCAAAAGAAAAATGGCCTTTGTTGCAACACAAGGGGCCACAGTGGTTGACCAAACCACTCTTATGAAAAAATACCTTCAGTTTGTGGCAGCTCTCACAGA
ENSHGLT00100092820::1:78457-78757(-)    GGAGAGAGCCTGGGGGCCGTTTGGGACCGGAGGGCTCGGGCTTGGGTTGGGGTCGCACATACAAGAGGTGCCTCCCGCCTAGCTGGGCACCTCTCGGCCTCCGTGCAAGCACTTGGCTCGTCGGGCCGAACGCGAACGCGGAGAGCGAAGGTGCTGTAGCGGTGCCTACAGCGCCCTCTCGGGTCCGGCGGTGCAGCCTCCGGCCGGGCTCGGCGCAGTCGGGGCGGAGCCGTTGACCCTGGGCGCCGGCTGGATGCCGGCCCTCCCGTCCCCACCTGGCAGGACGAGGTGGGATTGGCG
ENSHGLT00100041989::1:76754-77054(-)    GAGTAAATTTTATATTaaaaaaaaTAGAATAGTTTTATTCTGGATTAATGCAGAAGTCTTTAGATTAGTACAGGGATTTAGGTAAGATTTTTTACAAGTTTTGAACTTGTGCCCTTGATAAATTGGCTAACCTTATGTTTCTTTTCACAGGCTGGGTGAACTCATGGACCTGGTGTTTTTCTTCTGAGAAAGAAACCTGCTCAAAAGAAAAATGGCCTTTGTTGCAACACAAGGGGCCACAGTGGTTGACCAAACCACTCTTATGAAAAAATACCTTCAGTTTGTGGCAGCTCTCACAGA
ENSHGLT00100041989::1:78457-78757(-)    GGAGAGAGCCTGGGGGCCGTTTGGGACCGGAGGGCTCGGGCTTGGGTTGGGGTCGCACATACAAGAGGTGCCTCCCGCCTAGCTGGGCACCTCTCGGCCTCCGTGCAAGCACTTGGCTCGTCGGGCCGAACGCGAACGCGGAGAGCGAAGGTGCTGTAGCGGTGCCTACAGCGCCCTCTCGGGTCCGGCGGTGCAGCCTCCGGCCGGGCTCGGCGCAGTCGGGGCGGAGCCGTTGACCCTGGGCGCCGGCTGGATGCCGGCCCTCCCGTCCCCACCTGGCAGGACGAGGTGGGATTGGCG
ENSHGLT00100016094::1:76754-77054(-)    GAGTAAATTTTATATTaaaaaaaaTAGAATAGTTTTATTCTGGATTAATGCAGAAGTCTTTAGATTAGTACAGGGATTTAGGTAAGATTTTTTACAAGTTTTGAACTTGTGCCCTTGATAAATTGGCTAACCTTATGTTTCTTTTCACAGGCTGGGTGAACTCATGGACCTGGTGTTTTTCTTCTGAGAAAGAAACCTGCTCAAAAGAAAAATGGCCTTTGTTGCAACACAAGGGGCCACAGTGGTTGACCAAACCACTCTTATGAAAAAATACCTTCAGTTTGTGGCAGCTCTCACAGA
ENSHGLT00100016094::1:79043-79343(-)    GAAACTTCACTTGCCGGCCTGCAGcccccccTGCAGCGGGGGTTTTAAAGGGCCACGGGCCCGGCCTGCTTCTGGCTGCAGCTACCCCGCCCCTCCCGCCACGCCCTGCCGCCCGCCCAAGGCCGCTCCCACTCGGGGGCGGCGCGTCGGGGCCTAGTTCTCGGTGGGCAGGCGCAGCCGCTTTAAgcggaggcgggactgcgcgcggcggaggagctaccgcggcggtggcggggcgggaggcgaggcCTTCgggggggCGCTGGCCAGACTGCGGGCGGCCGGCCGCTGAGCTCCCGG
ENSHGLT00100016095::1:76754-77054(-)    GAGTAAATTTTATATTaaaaaaaaTAGAATAGTTTTATTCTGGATTAATGCAGAAGTCTTTAGATTAGTACAGGGATTTAGGTAAGATTTTTTACAAGTTTTGAACTTGTGCCCTTGATAAATTGGCTAACCTTATGTTTCTTTTCACAGGCTGGGTGAACTCATGGACCTGGTGTTTTTCTTCTGAGAAAGAAACCTGCTCAAAAGAAAAATGGCCTTTGTTGCAACACAAGGGGCCACAGTGGTTGACCAAACCACTCTTATGAAAAAATACCTTCAGTTTGTGGCAGCTCTCACAGA
ENSHGLT00100016095::1:79059-79359(-)    GGACCCGAGGTACGGGGAAACTTCACTTGCCGGCCTGCAGcccccccTGCAGCGGGGGTTTTAAAGGGCCACGGGCCCGGCCTGCTTCTGGCTGCAGCTACCCCGCCCCTCCCGCCACGCCCTGCCGCCCGCCCAAGGCCGCTCCCACTCGGGGGCGGCGCGTCGGGGCCTAGTTCTCGGTGGGCAGGCGCAGCCGCTTTAAgcggaggcgggactgcgcgcggcggaggagctaccgcggcggtggcggggcgggaggcgaggcCTTCgggggggCGCTGGCCAGACTGCGGGCGGCCG
ENSHGLT00100047040::1:99320-99620(+)    TTTGTTGAATGAAAAGCTGCGAGCTGGAGGTCTGAACACACCTGGAAAGGCCCAGGTGTCCGGCGCCGCCGCTGTGCGGCCCAGCATGCGCCTCTGGGGACGCTGAGTCACAACGCGCGGGCACAGACCTGGTCGGGACAAGGATGCgggggggtggggcagggaggcgacgcagatccgaggagggagggacgcggggagggggcgcgcACGGCACCGCAGACCCGCTGATGGGGCAAGGGTcgcgcgcgcggcagactgtgggcgggggcggcgcctggggaggacgagcgagcgcgg
ENSHGLT00100080349::1:99335-99635(+)    GCTGCGAGCTGGAGGTCTGAACACACCTGGAAAGGCCCAGGTGTCCGGCGCCGCCGCTGTGCGGCCCAGCATGCGCCTCTGGGGACGCTGAGTCACAACGCGCGGGCACAGACCTGGTCGGGACAAGGATGCgggggggtggggcagggaggcgacgcagatccgaggagggagggacgcggggagggggcgcgcACGGCACCGCAGACCCGCTGATGGGGCAAGGGTcgcgcgcgcggcagactgtgggcgggggcggcgcctggggaggacgagcgagcgcggcgcCCGCACCTCCGC
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$  wc -l utr_sequences_table.tsv
64578 utr_sequences_table.tsv
(NMR-env) alexts14@GabanouMelissa:~/nmr_chromosomes/5utr_analysis$
```
No we have the sequence for the -150/+150 of the 5'utrs with only 2 entries skipped due to being beyond chromosome 20’s end.
