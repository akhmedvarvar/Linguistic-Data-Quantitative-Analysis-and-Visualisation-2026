# Preposition Corrections in Heritage and Foreign Language Russian

## General information

**Project goal.** I will compare preposition corrections in texts written by heritage learners (HL) and foreign-language learners (FL) of Russian. The main question is whether the two groups differ in the distribution of preposition insertions, deletions and substitutions within an existing sample of annotated government errors. I will also examine which prepositions are most often involved and whether the descriptive patterns vary across proficiency levels.

**Data.** The project will use an existing manually annotated sample from the English-background RULEC component of RLC-GEC. The sample is documented as containing 485 observations: 175 HL and 310 FL observations. The analysis will use the existing fields `quote_preposition`, `correction_preposition`, `language_background` and `level`, together with annotation and sentence identifiers. No new data collection or manual linguistic annotation is planned.

**Hypotheses.** My primary hypothesis is that the distribution of preposition-edit categories differs between HL and FL in this sample. A secondary, exploratory expectation is that a small number of prepositions and substitution pairs account for a large share of preposition edits. I will also examine whether an overall HL–FL contrast remains visible within the available proficiency levels, without treating this comparison as evidence of individual development.

**Linguistic relevance.** This project develops my interest in Russian case government and differences between heritage and foreign-language learner profiles. It shifts the focus from previously examined case substitutions to operations involving prepositions. The existing annotation will be reused as input; the proposed contribution is a new set of calculations, visualisations and interpretations based on those fields.

The dataset contains selected government-error annotations rather than all uses of prepositions. Therefore, the project will compare the composition of recorded corrections, not overall error rates or the accuracy of either learner group.

## Planned steps

### 1. Check the existing data

I will load the CSV with pandas and inspect the relevant columns, group sizes, proficiency labels and identifiers. I will distinguish an explicitly absent preposition from an unknown or missing value using the existing annotation conventions. Rows whose preposition status cannot be established from the available fields will be excluded from the relevant comparison, with their number reported. This step will establish a transparent analysis sample without adding new annotation.

### 2. Derive preposition-edit categories

I will classify each usable observation by comparing the original and corrected preposition fields. The five categories will be: absent in both versions; the same preposition retained; a preposition inserted in the correction; a preposition deleted in the correction; and one preposition replaced by another. Insertion in the correction corresponds to an omission in the learner text, while deletion corresponds to an extra preposition in that text. I will keep these directions explicit throughout the report. The categories will be derived automatically from the existing values, after removing only technical differences such as surrounding whitespace.

### 3. Describe the distribution in HL and FL

I will calculate counts and within-group percentages for all five categories and visualise them using stacked bar charts. I will then describe the three edit categories separately, using only observations with a preposition change as their denominator. This distinction will show both how often preposition changes occur within the selected government-error sample and how the types of change are distributed. Counts will accompany percentages because the groups differ in size.

### 4. Identify frequent prepositions and substitution pairs

I will tabulate which prepositions are inserted, which are deleted and which original-to-corrected pairs occur in substitutions. Ranked bar charts will display frequent insertions and deletions, while a heatmap will display substitution pairs. I will quantify concentration by reporting the share of edits accounted for by the most frequent prepositions or pairs. Rare categories will remain available in the output tables even when a figure displays only the most frequent items. This step will identify the lexical patterns behind the overall category counts.

### 5. Compare the learner groups statistically

I will use a contingency table to examine the association between learner profile and the five correction categories, omitting any category with a zero total. I will report Cramér’s V alongside the table. If expected counts are sufficiently large, I will use a chi-square test; otherwise, I will use a Monte Carlo test with fixed margins rather than relying on the asymptotic approximation. A secondary comparison will examine insertion, deletion and substitution among preposition edits only. If both tests are performed, their p-values will be adjusted using the Holm procedure.

These tests will be exploratory: multiple observations can originate from the same sentence or writer. I will report repeated sentence identifiers and, where existing mappings permit, repeat the comparison using one observation per original sentence to assess sensitivity to within-sentence repetition. This does not remove dependence between sentences by the same writer; participant-level inference is not possible from the current table alone.

### 6. Examine proficiency and sample limitations

I will cross-tabulate correction categories by learner profile and the existing proficiency levels, reporting the size of every subgroup. Faceted bar charts will show whether the overall contrast is also visible within levels. Small subgroups will be described cautiously rather than subjected to numerous separate tests. I will discuss missing values, unequal group sizes, repeated observations and the restriction to government-error annotations. This step will help distinguish a broad descriptive pattern from one driven by a particular part of the sample.

### 7. Prepare a reproducible report

I will organise the analysis in a Jupyter notebook using pandas, NumPy, SciPy, matplotlib and seaborn. The notebook will include the research questions, category definitions, sample counts, calculations, figures and conclusions. A README and requirements file will explain how to reproduce the results, and any simulation will use a fixed random seed. The final outputs will include summary tables, group-comparison charts and a preposition-substitution heatmap. If the annotated input cannot be redistributed, the repository will explain how to supply it locally rather than publish the data without permission.

## Anticipated results

The project will establish whether HL and FL show different distributions of preposition corrections in the selected sample and identify the prepositions responsible for the most frequent edits. I expect some concentration around a limited set of prepositions, but the direction and size of group differences remain empirical questions. Similar distributions would also be informative, suggesting shared patterns within this particular error sample. The results will complement the existing case-substitution analysis by showing how corrections to prepositions contribute to the broader picture of Russian government errors.
