A brief description of the methods can be found below.

### DNA Isolation, Sequencing, and Bioinformatics

An aliquot of 100 mg (wet weight) of each fecal sample DNA was extracted with a DNA isolation kit (MoBio Power soil, MoBio Laboratories, USA) following the manufacturer’s instructions.

Isolated DNA was then sent to CosmosID (Germantown, MD, USA) for library preparation and sequencing. Isolated DNA was quantified using Qubit Flex fluorometer and Qubit™ dsDNA BR Assay Kit (Thermofisher Scientific). DNA libraries were prepared using the Watchmaker DNA Library Prep Kit (7K0019-1K). Genomic DNA was fragmented using a mastermix of Watchmaker Frag/AT Buffer and Frag/AT Enzyme Mix. IDT xGen UDI Primers and IDT Stubby Adapters were added to each sample followed by 7 cycles of PCR to construct the DNA libraries. The final DNA libraries were purified using CleanNGS magnetic beads (CleanNA) and eluted in nuclease-free water. Following elution, the libraries were quantified using the Qubit™ fluorometer dsDNA HS Assay Kit. Libraries were circularized and sequenced on the Element AVITI platform using the 2x150 Cloudbreak FreeStyle sequencing kit to a target depth of 20M reads.

Sequences were quality controlled and trimmed using fastp [1]. Next quality controlled reads were aligned with Bowtie2 to the CanFam3.1 [8] reference genome for depletion of host reads [2]. These high quality reads were then taxonomically profiled using MetaPhlAn (4.2) based on an updated database curated in January 2025 [3]. MetaPhlAn was run with the 'very-sensitive-local' Bowtie2 parameter to increase sensitivity and reduce proportion of unclassified metagenome reads. To account for possible false positive species that did not meet 10% prevalence at a relative abundance of 0.01% were removed prior to downstream analysis.

Alpha and beta diversity metrics were calculated in QIIME2 (v2024.10) [4]. For alpha diversity the observed features and Shannon index were calculated. A pairwise Kruskal-Wallis test was applied to test differences in alpha diversity between groups 1 and 2. For beta diversity the Bray-Curtis distance metrics was calculated and principal coordinate analysis (PCoA) was performed to quantify community composition. The `beta-group-significance` function was used with QIIME2 to calculate a PERMANOVA with 999 permutations. Finally, differential abundance of individual taxa was tested using the `ANCOMBC` method [7].

Visualizations were created using QIIME2 (v2024.10), Phyloseq (v3.21),and ggplot2 (v3.5.2).

**References:**

[1] Shifu Chen. 2023. Ultrafast one-pass FASTQ data preprocessing, quality control, and deduplication using fastp. iMeta 2: e107. https://doi.org/10.1002/imt2.107

[2] Langmead B, Salzberg S. Fast gapped-read alignment with Bowtie 2. Nature Methods. 2012, 9:357-359.

[3] Blanco-Miguez, A., Beghini, F., Cumbo, F., McIver, L. J., Thompson, K. N., Zolfo, M., Manghi, P., Dubois, L., Huang, K. D., Thomas, A. M., Piccinno, G., Piperni, E., Punčochář, M., Valles-Colomer, M., Tett, A., Giordano, F., Davies, R., Wolf, J., Berry, S. E., Spector, T. D., Franzosa, E. A., Pasolli, E., Asnicar, F., Huttenhower, C., & Segata, N. (2023). Extending and improving metagenomic taxonomic profiling with uncharacterized species with MetaPhlAn 4. *Nature Biotechnology*, 41(11), 1633-1644.

[4] Bolyen E, Rideout JR, Dillon MR, Bokulich NA, Abnet CC, Al-Ghalith GA, Alexander H, Alm EJ, Arumugam M, Asnicar F, Bai Y, Bisanz JE, Bittinger K, Brejnrod A, Brislawn CJ, Brown CT, Callahan BJ, Caraballo-Rodríguez AM, Chase J, Cope EK, Da Silva R, Diener C, Dorrestein PC, Douglas GM, Durall DM, Duvallet C, Edwardson CF, Ernst M, Estaki M, Fouquier J, Gauglitz JM, Gibbons SM, Gibson DL, Gonzalez A, Gorlick K, Guo J, Hillmann B, Holmes S, Holste H, Huttenhower C, Huttley GA, Janssen S, Jarmusch AK, Jiang L, Kaehler BD, Kang KB, Keefe CR, Keim P, Kelley ST, Knights D, Koester I, Kosciolek T, Kreps J, Langille MGI, Lee J, Ley R, Liu YX, Loftfield E, Lozupone C, Maher M, Marotz C, Martin BD, McDonald D, McIver LJ, Melnik AV, Metcalf JL, Morgan SC, Morton JT, Naimey AT, Navas-Molina JA, Nothias LF, Orchanian SB, Pearson T, Peoples SL, Petras D, Preuss ML, Pruesse E, Rasmussen LB, Rivers A, Robeson MS, Rosenthal P, Segata N, Shaffer M, Shiffer A, Sinha R, Song SJ, Spear JR, Swafford AD, Thompson LR, Torres PJ, Trinh P, Tripathi A, Turnbaugh PJ, Ul-Hasan S, van der Hooft JJJ, Vargas F, Vázquez-Baeza Y, Vogtmann E, von Hippel M, Walters W, Wan Y, Wang M, Warren J, Weber KC, Williamson CHD, Willis AD, Xu ZZ, Zaneveld JR, Zhang Y, Zhu Q, Knight R, and Caporaso JG. 2019. Reproducible, interactive, scalable and extensible microbiome data science using QIIME 2. Nature Biotechnology 37: 852–857. https://doi.org/10.1038/s41587-019-0209-9

[5] McMurdie and Holmes (2013) phyloseq: An R Package for Reproducible Interactive Analysis and Graphics of Microbiome Census Data. PLoS ONE. 8(4):e61217

[6] Lin H, Peddada SD (2020). “Analysis of compositions of microbiomes with bias correction.” Nature Communications, 11(1), 1-11. https://www.nature.com/articles/s41467-020-17041-7. 

[7] National Center for Biotechnology Information. (2020). Canis lupus familiaris genome assembly, CanFam3.1 (GCF_000002285.3). NCBI Datasets. https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_000002285.3/
