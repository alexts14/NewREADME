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
```
