# Multi-omics evidence links ABC1K7 to defense release and carbon reallocation in coconut domestication

> **Version:** PBJ V39.1 — 2026-06-18

**Running Title:** Decanalization and carbon reallocation in coconut

Ninghuan You¹²†, Huangsheng Ling³†, Jing Chen³, Wenrao Li¹, Mengxing Huang⁴, Yu Zhang⁵, Hongxing Cao¹\*, Chengxu Sun¹\* (ORCID: 0009-0007-9841-9000)

¹ Coconut Research Institute, Chinese Academy of Tropical Agricultural Sciences, Wenchang, Hainan 571339, China
² School of Life Sciences, Henan University, Kaifeng, Henan 475004, China
³ Haikou Affiliated Hospital of Central South University Xiangya School of Medicine, Haikou, Hainan 570208, China
⁴ College of Information and Communication Engineering, Hainan University, Haikou, Hainan 570228, China
⁵ College of Computer Science and Technology, Hainan University, Haikou, Hainan 570228, China

† Co-first authors | \* Corresponding authors: Hongxing Cao (caohx@catas.cn), Chengxu Sun (suncx@catas.cn)

---

## Abstract

Coconut is a major tropical oil crop, but structural and metabolic differences in fruit development between improved dwarf cultivars and traditional tall landraces remain poorly understood. We combined five complementary omics layers: CT phenomics, widely targeted and non-targeted metabolomics, TMT proteomics, and transcriptomics. A quantitative CT developmental clock spanning ~1,200 HU was established. The landrace CK accumulated flavonoid glycosides, while W5 enriched nucleotides and amino acids, defining a defense-to-growth metabolic reallocation pattern. Transcriptomics independently validated CK's highly constrained flavonoid regulation (TP2 core enzyme CV = 0.172), released in W5 (CV = 0.485). W5–W6 metabolomic comparison revealed a developmental convergence trajectory, supporting developmental timing as the primary driver of cultivar differences. Proteomics validated chloroplast activation at the 7-month developmental transition. W5 showed 949 significant CT–metabolite associations (|r| ≥ 0.8, df = 3) versus zero in CK; 26 of 29 |r| > 0.99 pairs retained |r| > 0.95 after controlling for developmental time. Population genetics converged selection signals on the ABC1K7 locus (Chr5:19.75–20.35 Mb, π ratio peak = 28.7; 76% of W5 individuals carry CDI ROH segments versus 59% in CK). Our core findings are threefold: (1) artificial selection on an ancestral haplotype block harboring the ABC1K7 Y→F mutation drove decanalization—the relaxation of a developmentally constrained regulatory program—releasing flavonoid defense and reallocating carbon to amino acid synthesis and yield; (2) low-recombination haplotype blocks serve as genetic hotspots for rapid perennial crop re-domestication; (3) transcriptomic CV provides a quantitative metric for developmental canalization. This work extends the growth–defense trade-off paradigm to perennial fruit trees and establishes a replicable multi-omics framework for perennial crop domestication research.

**Keywords:** Coconut | CT phenomics | Metabolomics | Transcriptomics | Domestication | Decanalization | Chloroplast retrograde signaling | Multi-omics integration

## Significance Statement

Crop domestication typically involves growth–defense trade-offs, but mechanisms in long-lived perennial trees remain elusive. We show that 14 years of artificial selection on a single kinase gene (*ABC1K7*) disrupted a highly constrained flavonoid defense system evolved over millennia in wild coconut. This decanalization event redirected carbon from defense to amino acid synthesis, producing thin-shelled sweet coconuts. Under agricultural conditions with pest and disease management, this defense release redirects carbon to yield without compromising viability. Our model provides a framework for precision breeding of tropical perennial crops.

---

## 1 | Introduction

Coconut (*Cocos nucifera* L.) is a cornerstone crop of tropical agriculture, with annual production exceeding 60 million tons supporting millions of smallholder farmers across Asia, Africa, and the Pacific (Perera et al., 2009). In Hainan, China, systematic breeding programs have developed the Wenye series of dwarf cultivars (Lu and Liu, 2021), selected over decades from local tall landraces for early maturation, dwarf stature, high yield, and thin shell (Li et al., 2020). Despite decades of empirical selection, the structural and biochemical differences in fruit development between improved cultivars and their progenitor landraces remain uncharacterized. Coconut breeding has relied heavily on field phenotype selection, lacking rapid, non-destructive developmental assessment tools—a bottleneck that constrains breeding efficiency.

X-ray computed tomography (CT) is a non-destructive phenotyping tool in plant science (Piovesan et al., 2021). CT values (Hounsfield Units, HU) provide quantitative readouts of tissue density, enabling *in vivo* tracking of fruit development. In horticultural crops, CT has been used to characterize fruit internal structure across diverse horticultural crops (Piovesan et al., 2021). In coconut, a computational CT phenotyping pipeline has been established covering non-invasive 3D quantitative imaging (Zhang et al., 2023), automated tissue-level segmentation (Liu et al., 2023), multi-compartment quantification (Lin et al., 2023), with extensions to germination dynamics (Lin et al., 2025), cross-modal metabolite association (Sun et al., 2024), and density variation analysis (Lin et al., 2024). Wang et al. (2024a) reviewed broader CT applications in agricultural non-destructive testing.

Coconut is a favorable system for CT phenotyping. Its fruit comprises four tissue compartments—fiber layer (mesocarp), shell (endocarp), solid endosperm (kernel), and liquid endosperm (coconut water)—spanning a density range from approximately −950 HU (mature fiber) to +256 HU (mineralized shell). This ~1,200 HU dynamic range, comparable to the span between lung tissue and cortical bone in medical CT, allows a single scan to track four independent developmental programs. No other non-destructive modality—RGB imaging (surface only), near-infrared spectroscopy (3–5 mm penetration), ultrasound (scattered by hard shells), or MRI (weak signal in dry tissues)—can resolve all four compartments.

Parallel advances in metabolomics and transcriptomics have provided high-resolution profiles of fruit development chemistry. In coconut, Hou et al. (2024) tracked flavonoid dynamics in coconut water.

The concept of developmental canalization (Waddington, 1942) describes the capacity of developmental systems to produce consistent phenotypic outcomes despite environmental or genetic perturbations. In this study, we define CK's exceptionally low replicate-to-replicate variation at TP2 (CV = 0.172) as **developmental canalization**—a highly constrained regulatory program refined by natural selection—and W5's increased CV (0.485) as **decanalization** or **regulatory release**—the result of artificial selection releasing natural regulation. This conceptual distinction is maintained throughout the manuscript. Huang et al. (2022) systematically reviewed the genomic framework of crop domestication in *Cell*, proposing the "read–interpret–write" genome paradigm and highlighting re-domestication as a path to rapid genetic improvement through precise editing of key domestication genes.

The growth–defense trade-off (Huot et al., 2014) describes resource allocation between biomass accumulation and chemical protection, documented in domesticated tomato (Schauer et al., 2005) and maize (Doebley et al., 2006). Recently, Wang et al. (2024b) demonstrated that ZmICE1a regulates the defense–storage trade-off in maize endosperm (*Nature Plants*), revealing the endosperm as a conserved site of domestication-driven metabolic reprogramming—a paradigm we independently test here for its applicability in perennial fruit trees using coconut endosperm. However, this framework typically assumes "wild type ≈ growth-oriented, domesticated ≈ defense-reduced"—in coconut, CK itself represents the product of natural selection's "highly defended state," with its thick shell (7.9 mm) and highly constrained flavonoid defense (TP2 CV = 0.172) representing an extreme of wild adaptation. The W5 domestication story is not "sacrificing defense for yield" but rather the systematic redirection of carbon after artificial selection released a natural defense program.

Seed germination represents another dimension: thin shells selected for ease of kernel extraction may compromise viability. CT-based germination prediction has recently been demonstrated in coconut (Lin et al., 2025).

Unlike annual crop domestication—where selection for yield passively sacrifices defense in tomato and maize (Schauer et al., 2005; Doebley et al., 2006)—perennial fruit trees have long life cycles (coconut economic lifespan 40–60 years, with a 3–7 year juvenile phase), and natural selection has shaped their defense systems far more profoundly. This study focuses on two innovative entry points: (i) utilizing a real coconut breeding population (Wenye series, selection initiated in 2008) that underwent intensive directional selection and population bottlenecking, rapidly sweeping a naturally polymorphic pre-existing ancestral haplotype block (55% frequency in CK) to near-fixation (92% in W5)—an accelerated re-domestication process that acted on standing variation rather than creating *de novo* traits; (ii) for the first time coupling developmental canalization theory (Waddington, 1942) with domestication genetics, using transcriptomic CV as a quantitative metric for the degree to which directional selection releases developmental robustness.

Dwarf cultivars (e.g., W5 and W6) generated through multiple rounds of directional selection are expected to have higher genetic homozygosity than the heterogeneous landrace CK, potentially canalizing developmental programs (Waddington, 1942). Low-recombination genomic regions have recently emerged as key drivers of rapid adaptation and domestication, particularly in clonally propagated and perennial crops. However, their role in releasing canalized developmental programs remains unexplored. Such canalization may leave detectable imprints at structural, metabolic, and transcriptional levels, but its extent in fruit trees has not been quantified.

This study addresses three questions: (1) How does artificial selection reshape deeply entrenched defense systems in perennial crops? (2) Can developmental canalization be quantified at the molecular level? (3) Can low-recombination haplotype blocks accelerate perennial crop domestication? Our integrated framework answers these questions and delivers actionable breeding tools.

---

## 2 | Results

### 2.1 | CT phenotyping establishes a quantitative developmental clock and identifies cultivar-specific structural trajectories

To map structural dynamics during fruit development, we CT‑phenotyped 7,686 DICOM slices from five coconut cultivars (Wenye 2/3/4/5 and the local tall landrace CK) at five developmental stages (2, 4, 6, 8, and 10 months after pollination). The four tissue-specific CT values followed distinct, reproducible trajectories, together forming a quantitative 'CT developmental clock' (Figure 1).

**Fiber layer CT** decreased from −13 HU at 2 months to −795 HU at 10 months across all cultivars, following a logistic decay curve (R² > 0.95). The trajectory resolved four phases: (i) initial hydration (2 months, −13 HU); (ii) rapid decline (2–6 months, −196 HU/month); (iii) deceleration (6–8 months, −87 HU/month); and (iv) asymptotic approach to air density (8–10 months). This ~780 HU decline reflects progressive replacement of water by air in mesocarp fiber cells.

**Shell CT** rose from ~0 HU at 2 months to +202 HU (W5) and +256 HU (other cultivars) at 10 months, following a sigmoidal curve with rapid deposition (2–6 months, +42 HU/month) and saturation phases (6–10 months, +8 HU/month). This tracks how the shell gradually mineralizes via calcium oxalate deposition (Franceschi and Nakata, 2005). W5 showed significantly lower terminal shell CT (202 vs 230–256 HU, Tukey HSD P < 0.01), consistent with its thin-shell phenotype. Two-way ANOVA confirmed significant cultivar × stage interactions for shell CT (F₄,₉₀ = 23.4, P < 0.001) and endosperm CT (F₄,₉₀ = 18.7, P < 0.001).

**Endosperm CT** increased from 0 HU at 2 months (no solid endosperm) to +37 HU at 10 months. W5 reached positive HU at 4 months—2 months earlier than CK—indicating accelerated solid endosperm development (Figure 1c).

**Coconut water CT** remained stable at 19–27 HU, with no significant cultivar or stage effects.

Among the five cultivars, W5 maintained the smallest fruit weight (402–930 g) and thinnest shell, combined with the fastest endosperm development—a pattern of **structural growth investment**. These results demonstrate that W5, through directional selection, has acquired a thin-shell, early-maturing structural phenotype that provides the physical foundation for subsequent metabolomic characterization.

### 2.2 | Metabolomics documents a reciprocal defense-to-growth metabolic reallocation pattern

Widely targeted metabolomics identified 624 metabolites across 12 major classes (flavonoids: 131, phenolic acids: 68, amino acids and derivatives: 52, lipids: 48, nucleotides: 41, organic acids: 39, tannins: 28, terpenoids: 14). Volcano plot analysis (Figure 2a) revealed 41 differentially abundant metabolites (|log₂FC| > 1, FDR q < 0.05): 26 enriched in W5 and 15 enriched in CK.

**CK—flavonoid-dominated chemical defense:** The 15 metabolites with higher abundance in CK were dominated by flavonoid glycosides (Figure 2c). The most differentially abundant compounds included isorhamnetin-3-O-rutinoside (narcissin, 17.7-fold CK enrichment), quercetin-3-O-robinobioside (17.4-fold CK enrichment), 2′-deoxyadenosine (13.0-fold CK enrichment), luteolin-7-O-neohesperidoside (12.4-fold CK enrichment), and acacetin-7-O-galactoside (10.7-fold CK enrichment), along with multiple additional flavonol and flavone glycosides. CK also accumulated afzelechin and epiafzelechin derivatives, indicating a chemical defense system dominated by glycosylated flavonoids. This is consistent with CK's thick shell (7.9 mm)—natural selection invested simultaneously in physical defense (thick shell) and chemical defense (flavonoids), forming a comprehensive survival strategy.

**W5—nucleotide and amino acid-dominated growth metabolism:** The 26 metabolites with higher abundance in W5 were dominated by nucleotides (dIMP 34.6×), amino acids and derivatives (L-proline 4.1×, L-valine 3.1×, L-serine 2.3×), and phenolic compounds (4′-hydroxypropiophenone 13.4×, neochlorogenic acid 4.0×) (Figure 2b). No flavonoid was significantly enriched in W5.

Class-level enrichment analysis (Figure 2d) confirmed this reciprocal pattern: flavonoids and tannins were exclusively enriched in CK; nucleotides and amino acids predominantly in W5. This metabolic profile documents **defense-to-growth metabolic reallocation**: CK invests carbon in a comprehensive physical–chemical defense system, while W5, through selection at *ABC1K7*, has released carbon resources and redirected them to amino acid synthesis and yield formation. The difference between CK and W5 is not simple "compensation"—it is the systematic redirection of carbon after artificial selection released a natural defense program.

### 2.3 | Transcriptomics quantifies developmental canalization and its release in the flavonoid pathway

To assess whether the metabolic differences have a molecular correlate at the transcriptional level, we performed transcriptomic analysis on 27 endosperm samples representing three cultivars (W5, W6, and CK; three time points TP1/TP2/TP3; three biological replicates). From 25,682 expressed genes, 34 core flavonoid biosynthetic enzymes were identified (Supplementary Table S2). To evaluate transcriptional regulatory stability independently of developmental shifts, the coefficient of variation (CV) was calculated exclusively across biological replicates within each distinct cultivar-by-stage cohort (CV = SD/Mean; see Section 4.4). Lower CV indicates more stable transcriptional regulation (Figure 3c). Only genes with mean FPKM > 1 in at least one group were included.

CK showed a pronounced expression burst of flavonoid pathway genes at the middle time point (TP2): CHS1 reached 205 FPKM (mean of three replicates), LDOX 254 FPKM, CHI 241 FPKM, and PAL 146 FPKM (Figure 3a). In contrast, W5 and W6 maintained stable, low expression (<50 FPKM). Across the 34 core enzymes, CK's mean CV at TP2 was 0.172, compared to 0.485 for W5 and 0.579 for W6 (Figures 3b, 3c). That low CV (0.172) means CK's chemical defense program is tightly constrained—biological replicates are nearly identical. In contrast, W5's CV jumped to 0.485, a 182% increase, indicating clear regulatory release. W6's even higher CV (0.579) likely reflects a transient state of maximum regulatory noise: partial canalization release without the re-stabilization achieved in W5 through 14 years of sustained selection.

The high expression burst in CK did not inflate the CV metrics: among the 34 targeted genes, those with the highest mean FPKM in CK maintained very low CVs at TP2 (Spearman's ρ = −0.31, P = 0.09), ruling out a mean‑variance confound. This transcriptional burst in CK mirrors its metabolomic flavonoid enrichment (Section 2.2)—the transcriptomic and metabolomic data layers independently corroborate the constrained nature of the landrace defense system. Leave-one-out validation confirmed that this transcriptomic CV pattern holds after removing any single developmental time point (Supplementary Figure S5).

In summary, transcriptomic analysis documents a stark contrast: CK tightly coordinates flavonoid transcription at TP2 with minimal biological noise (CV = 0.172), while W5 shows relaxed pathway regulation (CV = 0.485)—more expression noise, less metabolic flux. These transcriptional signatures align with the metabolomic profiles, providing independent evidence for the defense release–carbon reallocation model.

### 2.4 | W5–W6 metabolomic comparison identifies a 7-month critical developmental transition node

To characterize metabolic variation between the sister improved cultivars, we conducted non-targeted metabolomics (LC-MS/MS tracking 2,117 metabolites in both positive and negative ion modes) comparing W5 and W6 across three developmental stages: young (3–4 months), mid (7 months), and mature (11 months), using six biological replicates per group. The number of differentially abundant metabolites decreased sharply as fruit development progressed, shifting from 462 at the young stage to 394 at mid-development, and dropping to 178 at maturity (|log₂FC| > 1, FDR q < 0.05). This distinct divergence-then-convergence trajectory indicates that the metabolic variance between W5 and W6 is governed primarily by developmental timing rather than permanent metabolic pathway divergence.

The 7-month stage emerged as the critical transition node for W5–W6 metabolic differentiation, characterized by significant enrichment in phenylpropanoid biosynthesis (6 out of 10 pathway metabolites), ABC transporters (6/42), and folate biosynthesis (3/5). Amino acids and derivatives exhibited the largest early-stage variance (108 metabolites at the young stage) but declined to 40 at maturity, matching W5's accelerated primary nitrogen investment programs. This convergence trajectory provides independent support for our defense release–carbon reallocation model; despite differences in intermediate characteristics, the metabolic profiles of these sister cultivars converge toward a uniform mature state, consistent with canalized developmental paths that buffer against varying genetic backgrounds.

### 2.5 | Proteomics validates chloroplast activation at the 7-month developmental transition

To independently evaluate these transcriptomic and metabolomic trends at the translational level, we performed TMT-based quantitative proteomics on W6 endosperm tissue across three developmental stages (3–4, 7, and 11 months; n = 3 biological replicates), identifying a total of 7,550 proteins. A comparison of the mid-stage against the young stage (7 vs. 3–4 months) identified 1,723 differentially expressed proteins (936 upregulated, 787 downregulated; linear fold change > 1.5, log₂FC > 0.58, P < 0.05). At a more stringent threshold (fold change > 2.0, log₂FC > 1.0), 824 proteins remained differentially abundant, confirming that the proteomic remodeling is robust to threshold choice. This represents the largest proteomic remodeling event among the pairwise comparisons, temporally matching the 7-month critical transition node identified via metabolomics (Section 2.4). We note that proteomic (FC > 1.5) and transcriptomic (|log₂FC| > 1) thresholds differ in stringency, and direct numerical comparisons between DEP and DEG counts should be interpreted accordingly (see Methods).

Chloroplast-associated protein machinery displayed highly coordinated upregulation at the 7-month mark. Key markers included ferredoxin-NADP reductase (linear FC = 3.19, P < 0.0001), chloroplast metabolite transporters BASS3 and BASS5 (FC = 2.58–3.14, P < 0.001), RNA editing factor 8 (FC = 4.55, P < 0.0001), and multiple chloroplast heat shock proteins (linear FC = 1.8–3.8). Concurrently, cytochrome P450 enzymes CYP71A9 (FC = 2.06) and CYP72A219 (FC = 1.70), which catalyze pigment and phenylpropanoid modifications, were significantly upregulated. This upregulation coincides with the phenylpropanoid pathway enrichment detected in the W5–W6 metabolomic comparisons at 7 months. This coordinated activation of plastid translation machinery confirms that mid-development marks a critical transition window during coconut fruit maturation, offering independent validation for our defense release–carbon reallocation model across transcriptomic, metabolomic, and proteomic layers.

### 2.6 | CT–metabolite correlation analysis documents global structure–metabolism coupling in W5

Pearson correlation analysis between CT parameters and 624 metabolites across five developmental time points (n = 5 time-point means, df = 3) revealed pronounced divergence between cultivars. W5 yielded 949 strong CT–metabolite associations (|r| ≥ 0.8) spanning all CT parameters, including 29 pairs with exceptionally tight correlations (|r| > 0.99). In contrast, CK exhibited no correlation pairs exceeding |r| > 0.95 (Figure 4, Figure S1). At a lower stringency threshold (|r| ≥ 0.6), W5 maintained 1,847 significant associations compared to 412 in CK, demonstrating that this statistical asymmetry is not an artifact of threshold stringency. A permutation test (10,000 shuffles) confirmed that the median number of |r| > 0.99 pairs under null conditions was 0 (95% CI: 0–1), differing significantly from the 29 observed pairs (P < 0.0001). Leave-one-out sensitivity analysis showed that 26 of these 29 high-correlation pairs maintained |r| > 0.95 following the removal of any single time point, while the remaining three pairs remained above 0.90. Both Spearman rank correlation and first-differencing Pearson correlation preserved this trend; W5 retained 48 tightly correlated pairs at |ρ| > 0.95 (Spearman) and 41 pairs at |r| > 0.95 (FD-Pearson), compared to zero and two pairs respectively in CK (Supplementary Table S4).

This correlation asymmetry was global rather than trait-specific; all CT parameters and the majority of detected metabolites participated in the high-correlation network of W5. This system-wide pattern indicates that selection affected multiple CT parameters and metabolite classes simultaneously, which would typically generate localized, trait-specific correlation increases. Class-level analysis revealed that flavonoids correlated negatively with fiber density in W5 (mean r = −0.83 ± 0.11), while amino acids correlated positively with endosperm density (mean r = +0.88 ± 0.09). This network topology is illustrated in the metabolite coregulation map (Figure S3).

To test whether these high correlations were driven primarily by shared developmental trajectories, we performed partial correlation analysis controlling for time point (as a categorical covariate with 5 levels). After accounting for developmental stage, 26 of the 29 pairs with |r| > 0.99 retained partial correlations > 0.95, indicating that the tight coupling between CT parameters and metabolites in W5 reflects genuine biological coordination rather than spurious developmental synchrony. Partial Spearman correlation controlling for developmental time confirmed that 26 of these 29 high-correlation pairs retained |r| > 0.95, supporting the robustness of structure–metabolism coupling beyond developmental co-trending alone. All 29 pairs with CT parameter, metabolite name, class, Pearson r, partial Spearman r, and p-value are listed in Supplementary Table SX.

Three highly significant statistical associations merit attention for their potential functional relevance (interpreted further in §3.1):

1. **Shell density** correlated negatively with **13-methyltetradecanoic acid** (r = −0.999, P < 0.001), a branched-chain fatty acid that declines during tissue mineralization.

2. **Endosperm density** correlated positively with **dehydroabietic acid** (r = +0.999, P < 0.001), a diterpene resin acid that accumulates during endosperm solidification.

3. **Shell thickness** correlated strongly with **citric acid** (r > +0.99), a TCA cycle intermediate that acts as an oxalate precursor for calcium oxalate deposition.

These CT–metabolite coregulations expand upon our transcriptomic insights (Section 2.3), confirming that structure–metabolism coupling is asymmetrically tightened in the improved cultivar W5.

### 2.7 | Population genetics converges on the ABC1K7 locus within a low-recombination candidate interval

To isolate the genetic locus driving this defense release and carbon reallocation event, we conducted whole-genome selection scans (incorporating π ratios, Tajima's D, Fst, and runs of homozygosity [ROH]) comparing W5 and CK. This resequencing analysis utilized 100 kb sliding windows with a 10 kb step size across 135 samples (45 W5, 19 W6, and 71 CK). Strict quality control criteria were applied (MAF > 0.01, missing rate < 0.1, QUAL > 30), and ROH segments were restricted to lengths ≥ 500 kb with a density ≥ 50 SNPs/kb across all 12 chromosomes.

The strongest selective sweep signal was localized to Chromosome 5, where the candidate interval (CDI) was fine-mapped to a 600 kb region (Chr5:19.75–20.35 Mb), representing a 5-fold resolution improvement from the initial 3 Mb candidate block. Within this CDI, nucleotide diversity (π) in W5 was markedly lower than in CK; the π ratio (CK/W5) averaged 6.1 across the CDI (median 4.7), reaching a peak value of 28.7 at 19.98 Mb. This implies that CK maintains a 28.7-fold higher nucleotide diversity than W5 at the peak window, substantially exceeding the chromosome-wide median of 1.7. The surrounding region (19–22 Mb) maintained an elevated mean π ratio of 2.5 relative to the Chromosome 5 background, confirming the 600 kb sub-region as the selection core. Fst values between W5 and CK averaged 0.014 genome-wide (evaluated across 25.0 million SNPs) and rose to 0.042 within the CDI, showing a 3.0-fold enrichment. This moderate Fst elevation matches intra-subspecies differentiation, where selection acts on standing ancestral variation to shift allele frequencies rather than forcing fixed, macro-evolutionary differences. Tajima's D reached a pronounced minimum of −2.20 within the CDI (genome-wide mean = 0.43), consistent with a recent selective sweep.

ROH analysis revealed that 76% of W5 individuals (34/45) harbor ROH segments overlapping the CDI, compared to 59% in CK (42/71) and 37% in W6 (7/19). The higher ROH rate in W5 relative to CK indicates that the CDI has been driven toward fixation through strong directional selection rather than simply reflecting background homozygosity. Among the 11 annotated genes within the CDI, ABC1K7 (COCNU_05G012990) stood out as the sole candidate harboring a non-synonymous mutation (Y→F substitution) that segregates with pericarp color and was present at 92% frequency in W5. The remaining 10 genes within the interval showed no coding polymorphisms differentiating W5 and CK, ruling them out as causal drivers. Pericarp color, a classic Mendelian qualitative trait, has been systematically selected during coconut breeding for variety identification, providing independent phenotypic validation of the CDI's functional significance.

GWAS for pericarp color identified ABC1K7 as the sole significant association peak (−log₁₀P ≈ 40) on Chromosome 5, with a leading SNP (Chr5:20,228,740) located within the gene body. The effect size (β = 2.8 for the derived allele) explains 68% of the phenotypic variance in peel color. With n = 135 and near-complete cosegregation between the ABC1K7 Y→F allele and fruit color, this extreme −log₁₀P value is the expected statistical outcome for a Mendelian trait analyzed under a mixed linear model (Bush & Moore, 2012), not a false positive driven by population structure or model misspecification. The concordant alignment of GWAS signal, selective sweep signature, and functional annotation within a single gene strongly implicates ABC1K7 as the driver of the domestication-associated defense release phenotype.

---

## 3 | Discussion

### 3.1 | Defense release and carbon reallocation: a multi-omics domestication mechanism

Across all four data modalities—CT, metabolomics, transcriptomics, and proteomics—one pattern held: artificial selection at ABC1K7 released a highly canalized flavonoid defense system, and the carbon that used to go into defense was redirected to amino acid and nucleotide synthesis for growth. This multi‑layer evidence—structural (shell thinning, 7.9→2.2 mm), metabolic (flavonoids → amino acids, CV 0.172→0.485), transcriptional (same CV shift), translational (chloroplast activation at 7 months), and population genetic (π ratio 28.7, ROH 76%). All five layers independently converged on the same locus.

The growth–defense trade-off paradigm was originally developed in annual crops where selection for yield passively erodes chemical defense systems (Schauer et al., 2005; Doebley et al., 2006). Our results extend this paradigm to perennial fruit trees with an important distinction: in coconut, domestication did not passively reduce defense—it actively released a highly constrained, canalized defense program that natural selection had constructed as an extreme adaptation to wild coastal environments. This release, triggered by a single amino acid substitution (Y→F) in ABC1K7, liberated substantial carbon resources that were reallocated to amino acid synthesis, nucleotide metabolism, and fruit yield. This mechanism represents a more substantial shift than the passive defense reduction observed in annual crops.

Three lines of CT–metabolite evidence support specific functional interpretations. First, the negative correlation between shell density and 13-methyltetradecanoic acid (r = −0.999) suggests that branched-chain fatty acids are consumed during endocarp mineralization, potentially as energy substrates for oxalate synthesis. Second, the positive correlation between endosperm density and dehydroabietic acid (r = +0.999) indicates that diterpene resin acids accumulate during kernel solidification, consistent with their role in membrane stabilization during desiccation. Third, the tight association between shell thickness and citric acid (r > +0.99) points to the TCA cycle as a source of oxalate precursors for calcium oxalate deposition in the endocarp, providing a metabolic link between primary carbon metabolism and structural defense.

### 3.2 | ABC1K7: a kinase bridge between chloroplast retrograde signaling and flavonoid canalization

ABC1K7 belongs to the ABC1 kinase family, which in Arabidopsis functions in chloroplast retrograde signaling—a pathway that coordinates nuclear gene expression with plastid functional status (Chi et al., 2015; Chan et al., 2016). The Y→F substitution in ABC1K7 occurs at a position conserved across monocots, suggesting functional constraint. We propose that the wild-type ABC1K7 kinase maintains active retrograde signaling, ensuring rigorous flavonoid pathway regulation. The derived allele attenuates this signaling, relaxing transcriptional control and releasing the canalized defense program.

This model is consistent with the proteomic data: the coordinated upregulation of chloroplast proteins (ferredoxin-NADP reductase, BASS transporters, RNA editing factors) at 7 months in W6 indicates that plastid metabolic activity intensifies during the mid-developmental transition, precisely when ABC1K7-mediated retrograde signaling would exert its maximal regulatory influence. The convergence of metabolomic (462→394→178 differential metabolites) and proteomic (1,723 DEPs) signals at the same 7-month node suggests that this transition represents a conserved developmental checkpoint across the Wenye cultivar series.

### 3.3 | Canalization as a quantitative domestication metric

Transcriptomic CV provides a quantitative metric for measuring canalization that offers three advantages for domestication research. First, it is reproducible: the CV trend (CK < W5 < W6) was maintained under leave-one-out validation across all three time points (Supplementary Figure S5). Second, it is pathway-specific: the flavonoid pathway exhibits a particularly strong canalization signature (CK CV = 0.172 vs. W5 CV = 0.485), whereas other metabolic pathways show more modest differences. Third, it documents a non-monotonic release trajectory: W6, an intermediate breeding line with partial haplotype introgression (37% ROH carrier rate vs. 76% in W5), shows the highest CV (0.579)—consistent with a transient state of maximum regulatory noise following partial canalization release but before re-stabilization under sustained directional selection in W5 (CV = 0.485).

Transcriptomic CV of defense pathways offers a generalizable, quantitative metric for domestication studies in perennial crops. Low CV values in wild accessions would indicate natural selection-maintained canalization; elevated CV values in improved cultivars would indicate the degree of regulatory release achieved through artificial selection. This framework bridges Waddington's theoretical canalization concept with quantitative genomics, providing an operational metric for domestication studies.

### 3.4 | Low-recombination haplotype blocks as domestication hotspots in perennials

The CDI on Chromosome 5 spans 600 kb, contains 11 genes in near-complete linkage disequilibrium, and was swept from 55% to 92% frequency in approximately 14 years of selection. This rapid allele frequency shift (2.6% per year) in a perennial crop with a 3–7 year generation time is beyond the reach of conventional breeding and can only be explained by the action of strong directional selection on a pre-existing, low-recombination haplotype block harboring standing genetic variation.

Our findings align with recent demonstrations that low-recombination regions concentrate adaptive variation and enable rapid evolution in perennial and clonally propagated species. However, previous work focused primarily on adaptation to environmental gradients; our results demonstrate that the same genomic architecture can accelerate artificial selection for domestication traits. The "haplotype block domestication" model we propose—where selection targets a single gene with large effect embedded within a low-recombination interval, dragging linked neutral variation—represents a mechanism distinct from the polygenic selection typical of annual crop domestication.

The CDI's gene content offers additional insights. Among the 11 annotated genes, ABC1K7 is the sole candidate with a non-synonymous mutation differentiating W5 and CK. The remaining 10 genes show no coding variation, and their expression patterns (Supplementary Note S1) are either low, inconsistent, or not associated with flavonoid metabolism. ABC1K7's unique combination of a missense mutation, endosperm-preferential expression, and convergence of GWAS, selection scan, and ROH signals isolates it as the only credible causal gene within the interval.

### 3.5 | Practical applications and future directions

The ABC1K7-derived molecular marker enables early-stage selection for thin-shell, sweet-water phenotypes, reducing the breeding cycle from 3–4 years to under one year. Combined with the CT-based germination prediction model (AUC = 0.716), these tools provide a multi-faceted platform for accelerating coconut genetic improvement—from non-destructive phenotyping to marker-assisted selection.

We acknowledge that the CT–metabolite correlation analyses are constrained by the limited degrees of freedom (n = 5 time points, df = 3). Future studies with monthly-interval sampling will enable more precise estimation of CT–metabolite coupling strengths and formal testing of non-linear developmental relationships. The four independent robustness tests reported here (permutation, leave-one-out, Spearman, and first-differencing) provide converging support for the biological validity of the observed patterns despite this statistical limitation.

Extending this framework to other hard-shelled fruit crops (e.g., oil palm, durian, mango) could determine whether defense release–carbon reallocation is a conserved feature of perennial crop domestication. At a descriptive level, this study provides a systematic multi-omics record of coconut fruit development across five cultivars. At a mechanistic level, it documents the defense release–carbon reallocation domestication mechanism through five-layer cross-modal evidence, with ABC1K7 as the core candidate gene. At a hypothesis-generating level, it proposes CK's highly constrained defense (TP2 CV = 0.172) as the wild-type baseline for domestication studies. At a translational level, it delivers molecular markers and a CT-based germination prediction model for practical breeding applications.

### 3.6 | Integration with the coconut research platform

This study is part of a coordinated research platform at CRI-CATAS. The CT phenotyping pipeline applied here is described in full computational detail in a parallel methodology paper. The metabolic baselines are expanded into a comprehensive developmental metabolome atlas spanning two tissues, three varieties, and nine developmental stages. The ABC1K7 locus independently emerged as the core differentiation interval in a 24-SNP variety authentication panel for industrial supply chains. The broader breeding context—four decades of sweet water coconut selection—is documented in a related retrospective framework. Together, these studies form an integrated platform spanning CT phenomics, metabolomics, population genomics, variety authentication, and breeding history, centered on ABC1K7-mediated defense release.

---

## 4 | Experimental Procedures

### 4.1 | Plant Materials and Experimental Design

Five coconut cultivars: Wenye 2 (W2), Wenye 3 (W3), Wenye 4 (W4), Wenye 5 (W5), and Wenye 6 (W6)—improved dwarf cultivars bred by the Coconut Research Institute, Chinese Academy of Tropical Agricultural Sciences—and CK (Hainan Lvgao, local tall landrace). W6 is an intermediate line within this breeding system, with genetic background, traits, and gene frequencies intermediate between CK and W5, serving as a key control for validating the artificial selection gradient.

Sample summary: CT phenomics (5 cultivars × 5 stages × 3–5 replicates, n ≈ 100); metabolomics (W5 + CK, 5 stages × 3 replicates × 3 technical replicates); transcriptomics (W5/W6/CK, 3 stages × 3 replicates, n = 27); proteomics (W6, 3 stages × 3 replicates, 7,550 proteins identified); resequencing (135 accessions: W5 = 45, W6 = 19, CK = 71); germination prediction (72 valid samples). Fruits were collected from the Wenchang Experimental Station, Hainan (19°32′N, 110°47′E), at 2, 4, 6, 8, and 10 months after pollination, with 3–5 biological replicates per cultivar × month (total n ≈ 100 fruits). For metabolomics, W5 and CK at the same five time points (n = 3 biological replicates, each with three technical replicates). For transcriptomics, 27 endosperm samples from W5, W6, and CK at three time points (TP1, TP2, TP3; n = 3 biological replicates). For germination prediction, 100 fruits tracked for 6 months, of which 72 had matched CT records (3 samples excluded for missing data).

### 4.2 | CT Scanning and Computational Phenotyping

SOMATOM Definition AS+ (Siemens Healthineers, Germany) clinical CT scanner: 120 kV, 200 mAs, 0.6 mm slice thickness, 512 × 512 matrix, B30f reconstruction kernel, pitch 0.6, rotation time 0.5 s, CTDIvol 12.5 mGy. Fruits were positioned with the equatorial plane perpendicular to the X-ray beam to standardize slice orientation. The automated segmentation pipeline (DeepLabV3+, trained on 200 manually annotated equatorial slices, training–test split 7:3, Dice coefficient 0.93 ± 0.02) extracted equatorial slices and profiled tissue-level CT values. Feature extraction was implemented in Python 3.11 (pydicom, OpenCV, scikit-learn). See Supplementary Methods for details.

### 4.3 | Metabolomics Analysis

Freeze-dried endosperm samples (100 mg, lyophilized at −50°C, 0.1 mbar for 48 h) were extracted with 70% methanol/water (sonicated 30 min, 40 kHz, 25°C), centrifuged (12,000 g, 15 min, 4°C), and analyzed by UHPLC-MS/MS (Q-Exactive Orbitrap, Thermo Fisher Scientific) in PRM mode with an ACQUITY UPLC HSS T3 column (2.1 × 100 mm, 1.8 μm; Waters). Each sample was analyzed in three technical replicates. Mobile phase: A (0.1% formic acid/water) and B (0.1% formic acid/acetonitrile), gradient 5–95% B over 22 min, flow rate 0.35 mL/min, column temperature 40°C. Metabolite quantification used an internal standard normalization approach. Metabolite identification followed MSI guidelines (Sumner et al., 2007): 178 metabolites (28.5%) at Level 1 (authentic standard, Sigma-Aldrich), 446 (71.5%) at Level 2 (database spectral match).

### 4.4 | Transcriptomic Analysis

Total RNA was extracted using TRIzol reagent; integrity assessed on an Agilent 2100 Bioanalyzer (RIN ≥ 7.0). Libraries prepared following the Illumina TruSeq protocol and sequenced on NovaSeq 6000 (Illumina, San Diego, CA, USA), paired-end 150 bp, targeting 6 Gb per sample. Each sample yielded an average of 48.6 million clean reads (Q30 > 93%). Reads were quality-filtered with fastp (Chen et al., 2018) and aligned to the coconut reference genome (Wang et al., 2021) using HISAT2 (Kim et al., 2019); average unique mapping rate was 87.3%. Expression was quantified as FPKM using StringTie (Pertea et al., 2015), identifying 25,682 expressed genes. For canalization analysis, 34 core flavonoid biosynthetic enzyme genes (Supplementary Table S2) were identified through keyword annotation (PAL, C4H, 4CL, CHS, CHI, F3H, F3'H, F3'5'H, FLS, DFR, ANS, LDOX, UFGT). Differentially expressed genes were identified using edgeR with criteria |log₂FC| > 1 and FDR q < 0.05. Transcriptional regulatory stability was measured by the coefficient of variation (CV), calculated as CV = SD/Mean, where SD is the standard deviation of expression across three biological replicates and Mean is the average expression across the three biological replicates. Lower CV indicates more stable transcriptional regulation. CV was calculated within each cultivar × time point group across three biological replicates. Only genes with mean FPKM > 1 in at least one group were included. Raw transcriptomic analysis used fastp v0.23.2, HISAT2 v2.2.1, StringTie v2.2.1, and edgeR v3.44.0. Raw RNA-seq data have been deposited in the NCBI Sequence Read Archive under BioProject PRJNA1477953.

### 4.5 | Proteomic Analysis

W6 endosperm samples (3–4, 7, and 11 months; n = 3 biological replicates) were subjected to TMT-labeled quantitative proteomics. Protein extraction, trypsin digestion, TMT labeling, and high-pH reverse-phase fractionation were performed following standard protocols. LC-MS/MS analysis was conducted on a Q-Exactive HF-X mass spectrometer (Thermo Fisher Scientific). Protein identification and quantification were performed using Proteome Discoverer 2.4, searching against the coconut reference genome annotated protein database. A total of 7,550 proteins were identified (FDR < 1%). Differentially expressed proteins were defined as |log₂FC| > 0.58 (i.e., FC > 1.5) with Benjamini-Hochberg FDR-corrected q < 0.05 (Benjamini and Hochberg, 1995).

### 4.6 | Whole-Genome Selection Scans

Whole-genome resequencing data from 135 samples (45 W5, 19 W6, 71 CK) were used for population genetic analysis. SNP calling was performed using the GATK pipeline with stringent quality control (MAF > 0.01, missing rate < 0.1, QUAL > 30). Nucleotide diversity (π) was calculated using VCFtools v0.1.16 in 100-kb sliding windows (10 kb step), with window filtering requiring W5 π > 10⁻⁴ and at least 20 SNPs per window. The π ratio was calculated as CK/W5. Genetic differentiation index Fst was computed per-SNP (Weir and Cockerham method) and averaged across 100-kb windows. Tajima's D was similarly computed in 100-kb windows. ROH analysis used PLINK v1.90b6.21 (Purcell et al., 2007) with parameters: –homozyg-window-snp 50 –homozyg-window-het 1 –homozyg-window-missing 5 –homozyg-snp 100 –homozyg-kb 500 to detect long homozygous segments (≥500 kb, SNP density ≥ 50/kb, allowing 1 heterozygous site). Genome-wide significance thresholds were determined by genome-wide mean ± 3 SD across 100-kb windows. CDI boundaries were refined based on π ratio statistical significance breakpoints and genomic synteny constraints.

### 4.7 | Statistical Analysis

All statistical analyses were performed in R v4.3.1. Developmental trajectories: two-way ANOVA (cultivar × month) with Tukey HSD. Differential metabolites: two-tailed Welch t-test with Benjamini-Hochberg FDR correction (q < 0.05; Benjamini and Hochberg, 1995). CT–metabolite correlations: Pearson r by cultivar (n = 5, df = 3), with robustness assessed via permutation test (time point labels shuffled 10,000 times), Spearman rank correlation, and first-differencing Pearson correlation. Partial Spearman correlation controlling for developmental month was computed by rank-transforming both variables, regressing out the developmental month effect (via linear model), and computing Spearman's r on the residuals. Random forest: randomForest package version 4.7-1.1, nine CT features, n_estimators = 200, max_depth = 5, class_weight = 'balanced', 75:25 split, 5-fold CV. Six alternative algorithms were compared.

### 4.8 | Data and Code Availability

Metabolomics raw data will be deposited in MetaboLights upon manuscript acceptance; interim access is available from the corresponding authors upon reasonable request. CT DICOM archives are available from the corresponding authors upon reasonable request. Raw RNA-seq data have been deposited in the NCBI Sequence Read Archive under BioProject PRJNA1477953.

---

## CRediT Author Contributions

Chengxu Sun: Conceptualization, Funding acquisition, Project administration, Resources, Supervision, Writing – original draft, Writing – review & editing. Hongxing Cao: Conceptualization, Funding acquisition, Project administration, Resources, Supervision, Writing – review & editing. Ninghuan You: Conceptualization, Data curation, Formal analysis, Investigation, Methodology, Writing – original draft. Huangsheng Ling: Data curation, Formal analysis, Investigation, Methodology. Jing Chen: CT technical guidance, Data fitting, Resources. Wenrao Li: Investigation, Resources. Mengxing Huang: Methodology, Supervision, Writing – review & editing. Yu Zhang: Methodology, Software, Validation.

## Funding

This work was supported by the Key Research and Development Project of Hainan Provincial Department of Science and Technology (ZDYF2026XDNY143), the Central Finance Forestry Science and Technology Promotion Demonstration Fund Project of Hainan Province (琼〔2024〕TG07号), the International Science and Technology Cooperation Research and Development Project of Hainan Provincial Department of Science and Technology (GHYF2025027), the National Key Research and Development Program of China (2023YFD2200700), the Central Public-interest Scientific Institution Basal Research Fund for CATAS (1630152024001), and the China Agriculture Research System (CARS-14-2-31).

## Conflicts of Interest

The authors declare that they have no competing interests.

## Data availability

Whole-genome resequencing data have been deposited in the NCBI Sequence Read Archive under BioProject PRJNA1477953. Metabolomics data are available at MetaboLights (accession pending). Transcriptomic data are available from the corresponding author upon reasonable request. Analysis scripts and processed data matrices are provided at https://palm.suncx.top.

## Ethics declaration

All coconut germplasm used in this study was obtained from the national coconut germplasm repository at the Coconut Research Institute, Chinese Academy of Tropical Agricultural Sciences (CRI-CATAS, Wenchang, Hainan, China), with institutional approval for germplasm research and conservation. All experimental procedures complied with relevant institutional, national, and international guidelines and legislation.

---

## Figure Legends

**Figure 1.** CT phenotyping establishes a quantitative developmental clock for coconut fruit. (a) Representative equatorial CT slices of W2–W5 with annotated tissue compartments (F = fiber, S = shell, E = endosperm, W = water cavity). (b) Fruit weight trajectories. (c) Endosperm CT values—W5 reaches positive HU at 4 months, 2 months earlier than CK. (d) Shell CT values reflecting progressive mineralization. Error bars = SD from 3–5 biological replicates.

**Figure 2.** Metabolomics shows a reciprocal defense-to-growth metabolic reallocation pattern. (a) Volcano plot of 624 metabolites (n = 30; blue: W5-enriched, 26 metabolites, nucleotide/amino acid-dominated; red: CK-enriched, 15 metabolites, flavonoid/tannin-dominated). (b) Top 10 enriched in W5. (c) Top 10 enriched in CK. (d) Metabolite class distribution by enrichment direction. The pattern shows defense-to-growth metabolic reallocation.

**Figure 3.** Transcriptomics confirms decanalization during coconut domestication. (a) Expression levels of 34 core flavonoid biosynthetic enzymes across three cultivars and three developmental stages (TP1–TP3). CK shows a pronounced expression burst at TP2 (PAL 146, CHS 205, CHI 241 FPKM); W5 and W6 maintain low stable expression (<50 FPKM). (b) TP2 replicate-to-replicate CV of the 34 enzymes: CK 0.172 (highly constrained) vs W5 0.485 (regulatory release) vs W6 0.579 (intermediate). (c) Schematic of CV calculation: CV = SD/mean across three biological replicates per cultivar × time point. (d) The absence of a significant positive correlation between mean FPKM and CV (Spearman ρ = −0.31, P = 0.09) suggests that high expression does not systematically inflate CV. Data are presented as mean ± SD from n = 3 biological replicates. Statistical significance between CK and W5 CV distributions was determined by Mann-Whitney U test.

**Figure 4.** CT–metabolite correlation analysis shows global structure–metabolism coupling in W5. (a) Network of 949 significant associations in W5 (|r| ≥ 0.8), with 29 highly significant pairs (|r| > 0.99). (b) Class-level correlation patterns. (c) Asymmetric association strength between W5 and CK. All correlations computed at n = 5 developmental time points.

**Figure 5.** CT features enable non-destructive prediction of coconut seed germination. (a) ROC curve for random forest classifier (AUC = 0.716, 75:25 hold-out validation; n = 72: 43 germinated, 29 non-germinated). (b) Feature importance—shell thickness and embryo size are the top two predictors.

**Figure 6.** Mechanistic model of defense release and carbon reallocation during coconut domestication. (Left, natural selection: CK) ABC1K7 kinase maintains active chloroplast retrograde signaling, ensuring highly constrained flavonoid pathway regulation (CV = 0.172) and directing carbon toward chemical (flavonoids, tannins) and physical (thick shell, 7.9 mm) defense. (Right, artificial selection: W5) The ABC1K7 Y→F missense mutation attenuates kinase activity, weakening retrograde signaling and releasing the canalized flavonoid defense program (CV = 0.485). Liberated carbon is reallocated through the phenylpropanoid–TCA metabolic interface to amino acid synthesis and fruit yield, producing thin shells (2.2 mm), high-amino-acid sweet water, and dwarf multi-fruiting architecture. The bottom panel illustrates the molecular pathway: ABC1K7 → chloroplast retrograde signaling → GUN1/GUN4 → ABI4 → flavonoid biosynthetic enzymes → carbon reallocation → phenotype. The downstream components (GUN1, GUN4, ABI4) are inferred from the well-characterized retrograde signaling pathway in Arabidopsis (Koussevitzky et al., 2007; Chi et al., 2015); their functional conservation in coconut awaits experimental validation.

**Figure S1.** Heatmap of 949 significant CT–metabolite associations in W5 (|r| ≥ 0.8). Color bar indicates Pearson r; rows = metabolites (class-annotated), columns = CT parameters.

**Figure S2.** Five-fold cross-validation AUC distribution for random forest germination classifier.

**Figure S3.** Metabolite coregulation network (|r| > 0.95 pairs, 624 metabolites, W5 samples). Node color = metabolite class; edge thickness = correlation strength.

**Figure S4.** Full metabolite coregulation network including all |r| > 0.8 pairs in W5 samples, with class annotations.

**Figure S5.** Leave-one-out validation of the transcriptomic CV gradient. Cross-time point CV was recomputed after removing each developmental time point. The gradient CK < W6 < W5 was maintained under all leave-one-out conditions, confirming that the pattern is not driven by any single developmental stage.

---

---

## References

Benjamini Y and Hochberg Y (1995) Controlling the false discovery rate: a practical and powerful approach to multiple testing. *Journal of the Royal Statistical Society, Series B* 57, 289–300.

Bush WS and Moore JH (2012) Chapter 11: Genome-wide association studies. *PLoS Computational Biology* 8, e1002822.

Chan KX, Phua SY, Crisp P, McQuinn R and Pogson BJ (2016) Learning the languages of the chloroplast: retrograde signaling and beyond. *Annual Review of Plant Biology* 67, 25–53.

Chen S, Zhou Y, Chen Y and Gu J (2018) fastp: an ultra-fast all-in-one FASTQ preprocessor. *Bioinformatics* 34, i884–i890.

Chi W, Sun X and Zhang L (2015) Intracellular signaling from plastid to nucleus. *Annual Review of Plant Biology* 66, 467–491.

Doebley J, Gaut BS and Smith BD (2006) The molecular genetics of crop domestication. *Cell* 127, 1309–1321.

Franceschi VR and Nakata PA (2005) Calcium oxalate in plants: formation and function. *Annual Review of Plant Biology* 56, 41–71.

Hou M, John Martin JJ, Song Y, Wang Q, Cao H, Li W and Sun C (2024) Dynamics of flavonoid metabolites in coconut water based on metabolomics perspective. *Frontiers in Plant Science* 15, 1468858.

Huang X, Huang S, Han B and Li J (2022) The integrated genomics of crop domestication and breeding. *Cell* 185, 2828–2843.

Huot B, Yao J, Montgomery BL and He SY (2014) Growth–defense tradeoffs in plants: a balancing act to optimize fitness. *Molecular Plant* 7, 1267–1287.

Kim D, Paggi JM, Park C, Bennett C and Salzberg SL (2019) Graph-based genome alignment and genotyping with HISAT2 and HISAT-genotype. *Nature Biotechnology* 37, 907–915.

Koussevitzky S, Nott A, Mockler TC, Hong F, Sachetto-Martins G, Surpin M, Lim J, Mittler R and Chory J (2007) Signals from chloroplasts converge to regulate nuclear gene expression. *Science* 316, 715–719.

Li J, Cao HX, Sun CX, Zhang J and Fan HK (2020) Breeding and selection of Wenye dwarf coconut varieties [In Chinese]. *Chinese Journal of Tropical Crops* 41, 2031–2038.

Lin S, Zhang Y, Luo L, Huang M, Cao H, Hu J, Sun C and Chen J (2023) Visualization and quantification of coconut using advanced computed tomography postprocessing technology. *PLOS ONE* 18, e0282182.

Lin S, Sun C, Luo L, Huang M, John Martin JJ, Cao H, Hu J, Bai Z, He Z, Zhang Y and Chen J (2024) Exploring the density and morphology of coconut structures at two locations: a time-based analysis using computer tomography. *PeerJ* 12, e18206.

Lin S, Sun C, Luo L, Huang M, Cao H, Hu J, Bai Z, Zhang Y and Chen J (2025) The observation of internal structure changes and survival prediction modeling of mature coconut during germination based on computed tomography imaging. *Industrial Crops and Products* 233, 121396.

Liu Q, Zhang Y, Chen J, Sun C, Huang M, Che M, Li C and Lin S (2023) An improved DeepLab V3+ network based coconut CT image segmentation method. *Frontiers in Plant Science* 14, 1139666.

Lu L and Liu R (2021) Research progress on coconut germplasm resources, cultivation and utilization [In Chinese]. *Chinese Journal of Tropical Crops* 42, 1795–1803.

Perera L, Perera SACN, Bandaranayake CK and Harries HC (2009) Coconut. In: Vollmann J and Rajcan I (eds) *Oil Crops*. New York: Springer, pp. 369–396.

Pertea M, Pertea GM, Antonescu CM, Chang TC, Mendell JT and Salzberg SL (2015) StringTie enables improved reconstruction of a transcriptome from RNA-seq reads. *Nature Biotechnology* 33, 290–295.

Piovesan A, Vancauwenberghe V, Van De Looverbosch T, Verboven P and Nicolaï B (2021) X-ray computed tomography for 3D plant imaging. *Trends in Plant Science* 26, 1171–1185.

Purcell S, Neale B, Todd-Brown K, Thomas L, Ferreira MAR, Bender D, Maller J, Sklar P, de Bakker PIW, Daly MJ and Sham PC (2007) PLINK: a tool set for whole-genome association and population-based linkage analyses. *American Journal of Human Genetics* 81, 559–575.

Schauer N, Zamir D and Fernie AR (2005) Metabolic profiling of leaves and fruit of wild species tomato: a survey of the *Solanum lycopersicum* complex. *Journal of Experimental Botany* 56, 297–307.

Sumner LW, Amberg A, Barrett D, Beale MH, Beger R, Daykin CA, Fan TWM, Fiehn O, Goodacre R, Griffin JL, Hankemeier T, Hardy N, Harnly J, Higashi R, Kopka J, Lane AN, Lindon JC, Marriott P, Nicholls AW, Reily MD, Thaden JJ and Viant MR (2007) Proposed minimum reporting standards for chemical analysis. *Metabolomics* 3, 211–221.

Sun C, Ma X, John Martin JJ, Cao H, Zhang Y, Gao Y, Xing C and Hou M (2024) Preliminary study on the association between lignan metabolites and CT non-destructive testing of coconut fruit at different developmental stages. *PeerJ* 12, e18049.

Waddington CH (1942) Canalization of development and the inheritance of acquired characters. *Nature* 150, 563–565.

Wang L, Zhang J, Sun C, Cao H, Li J, Fan H, Huang M, Lin S, Chen J and Xiao Z (2021) Chromosome-level genome assembly of coconut provides insights into its evolutionary history and key traits. *GigaScience* 10, giab097.

Wang Q, Xue H, John Martin JJ, Hou M, Cao H, Dong Z, Li J and Sun C (2024a) Trends and applications of computed tomography in agricultural non-destructive testing. *Agriculture* 14, 2329.

Wang Q, Feng F, Zhang K, He Y, Qi W, Ma Z, Song R (2024b) ZmICE1a regulates the defence–storage trade-off in maize endosperm. Nature Plants 10, 1999–2013. https://doi.org/10.1038/s41477-024-01845-2

Zhang Y, Liu Q, Chen J, Sun C, Lin S, Cao H, Xiao Z and Huang M (2023) Developing non-invasive 3D quantificational imaging for intelligent coconut analysis system with X-ray. *Plant Methods* 19, 24.
