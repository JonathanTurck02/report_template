A brief description of the methods can be found below.

Disclaimer: Please do not copy directly for publication purposes for assistance in drafting a final methods section please contact [jonathanturck@tamu.edu](mailto:jonathanturck@tamu.edu)

### DNA Isolation, Sequencing, and Bioinformatics

An aliquot of 100 mg (wet weight) of each faecal sample DNA was extracted with a DNA isolation kit (MoBio Power soil, MoBio Laboratoroies, USA) following the manufacturer’s instructions.

A single‐step 30-cycle PCR using the HotStarTaq Plus Master Mix Kit (Qiagen) was performed under the following conditions: 94°C for 3 minutes, followed by 28 cycles (5 cycles used on PCR products) of 94°C for 30 seconds, 53°C for 40 seconds and 72°C for 1 minute, after which a final elongation step at 72°C for 5 minutes was performed. Illumina sequencing of V4 region of the bacterial 16S rRNA genes was performed using primers 515F (5′‐GTGCCAGCMGCCGCGGTAA‐3′) to 806R (5′‐ GGACTACVSGGGTATCTAAT‐3″) at the MR DNA laboratory (www.mrdnalab.com, Shallowater, Texas).

The demultiplexed sequences were imported into QIIME2 (v. 2024.10) for analysis. The DADA2 denoising procedure was used to remove chimeric sequences and identify amplicon sequence variants (ASVs). To assign taxonomy SILVA release 138 was used with the VSEARCH algorithm. To determine phylogenetic relationships sequences were aligned using MAFFT and a phylogenetic tree was constructed with FastTree. The samples were rarefied at the lowest per sample number of identified ASVs, 100000, for even depth of analysis.

Alpha diversity was calculated using Chao1, observed features, and Shannon metrics to estimate community richness and evenness. To test for differences in alpha diversity between groups a Krukal-Wallis test was used for both Omnibus and pairwise comparisons. A mixed-effects model used to assess the effects of time point, group, and their interaction on the outcome variable.

Beta diversity was calculated using Bray-Curtis, unweighted UniFrac, and weighted UniFrac dissimilarity to estimate overall differences in community structure. An Analysis of Similarities (ANOSIM), with 999 permutations, was used to assess the compositional chages across metrics.

To identify differentially abundant microbial phyla, ANCOMBC (v3.21) was used. The fixed effects were modeled by Group, Day, and their interaction. Entity was included as a random effect to control for individual variation. The Holm-Bonferroni method was used to correct for multiple comparisons.

Visualizations were created using QIIME2. Statistics were run withing QIIME2 (v2024.10), GraphPad Prism (v10.0.2), and R (v4.5.0).

- Bolyen E, Rideout JR, Dillon MR, Bokulich NA, Abnet CC, Al-Ghalith GA, Alexander H, Alm EJ, Arumugam M, Asnicar F, Bai Y, Bisanz JE, Bittinger K, Brejnrod A, Brislawn CJ, Brown CT, Callahan BJ, Caraballo-Rodríguez AM, Chase J, Cope EK, Da Silva R, Diener C, Dorrestein PC, Douglas GM, Durall DM, Duvallet C, Edwardson CF, Ernst M, Estaki M, Fouquier J, Gauglitz JM, Gibbons SM, Gibson DL, Gonzalez A, Gorlick K, Guo J, Hillmann B, Holmes S, Holste H, Huttenhower C, Huttley GA, Janssen S, Jarmusch AK, Jiang L, Kaehler BD, Kang KB, Keefe CR, Keim P, Kelley ST, Knights D, Koester I, Kosciolek T, Kreps J, Langille MGI, Lee J, Ley R, Liu YX, Loftfield E, Lozupone C, Maher M, Marotz C, Martin BD, McDonald D, McIver LJ, Melnik AV, Metcalf JL, Morgan SC, Morton JT, Naimey AT, Navas-Molina JA, Nothias LF, Orchanian SB, Pearson T, Peoples SL, Petras D, Preuss ML, Pruesse E, Rasmussen LB, Rivers A, Robeson MS, Rosenthal P, Segata N, Shaffer M, Shiffer A, Sinha R, Song SJ, Spear JR, Swafford AD, Thompson LR, Torres PJ, Trinh P, Tripathi A, Turnbaugh PJ, Ul-Hasan S, van der Hooft JJJ, Vargas F, Vázquez-Baeza Y, Vogtmann E, von Hippel M, Walters W, Wan Y, Wang M, Warren J, Weber KC, Williamson CHD, Willis AD, Xu ZZ, Zaneveld JR, Zhang Y, Zhu Q, Knight R, and Caporaso JG. 2019. Reproducible, interactive, scalable and extensible microbiome data science using QIIME 2. Nature Biotechnology 37: 852–857. https://doi.org/10.1038/s41587-019-0209-9
- Clarke KR (1993) Non-parametric multivariate analyses of changes in community structure. Aust J Ecol 18:117-43.
- Benjamin J Callahan, Paul J McMurdie, Michael J Rosen, Andrew W Han, Amy Jo A Johnson, and Susan P Holmes. *Dada2: high-resolution sample inference from illumina amplicon data.* Nature Methods, 13(7):581, 2016. doi:[10.1038/nmeth.3869](https://doi.org/10.1038/nmeth.3869).
- Torbjørn Rognes, Tomáš Flouri, Ben Nichols, Christopher Quince, and Frédéric Mahé. *Vsearch: a versatile open source tool for metagenomics.* PeerJ, 4:e2584, 2016. doi:[10.7717/peerj.2584](https://doi.org/10.7717/peerj.2584).
- Price, M.N., Dehal, P.S., and Arkin, A.P. (2010) *FastTree 2 -- Approximately Maximum-Likelihood Trees for Large Alignments.* PLoS ONE, 5(3):e9490. doi:[10.1371/journal.pone.0009490](https://doi.org/10.1371/journal.pone.0009490).
- Martinez Arbizu, P. (2020). pairwiseAdonis: Pairwise multilevel comparison using adonis. R package version 0.4
- Wickham H (2016). ggplot2: Elegant Graphics for Data Analysis. Springer-Verlag New York. ISBN 978-3-319-24277-4, https://ggplot2.tidyverse.org.


