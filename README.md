# caust prototype: causal gene intervention for robust spatial domain identification

a minimal working prototype developed for the osre 2026 project proposal under mentor lijinghua zhang.

### project goal
current spatial transcriptomics tools rely heavily on correlation. this makes them brittle because they get tricked by lazy genes that are only accidentally co located with tissue structures. models often fail to generalize across different tissue slices or donors.

caust aims to solve this by using causal gene interventions (mathematical knockouts). the main question is:

if i mathematically knock out this gene (set its expression to zero everywhere), does the spatial domain pattern actually break down?

genes that cause large changes are likely real causal boss genes driving the tissue structure. genes with little impact are likely spurious correlations.

### what this prototype does
this colab notebook demonstrates a minimal but concrete prototype as requested by the mentor:

1. loads dlpfc 151676 (standard benchmark dataset)
2. runs a basic stagate style pipeline to identify spatial domains (baseline)
3. performs simple gene knockouts for several candidate genes (mobp, pcp4, hopx, nrgn, snap25, gfap)
4. quantifies the effect of each knockout using embedding shift and ari stability
5. generates visualizations including side by side spatial plots and a bar plot of gene impact

### why we built this prototype
the mentor specifically asked for preliminary results instead of just more text in the proposal. she suggested:

run a basic stagate pipeline on dlpfc sections and perform a simple gene perturbation knockout experiment. report some quantitative effect (changes in ari or embedding distance).

this notebook delivers exactly that a small but working setup with clear quantitative signals and plots.

it serves as proof of feasibility for the full caust project (a pytorch causal intervention module).


### how to run
1. open the notebook in google colab
2. run cells sequentially (installations → data loading → preprocessing → baseline → knockouts → plots)
3. the notebook runs on free colab (gpu recommended but cpu is fine)


### acknowledgments
mentor lijinghua zhang for clear guidance on building a minimal prototype.
stagate authors and the spatial transcriptomics community for public datasets.

### end visualisation

<img width="863" height="505" alt="download" src="https://github.com/user-attachments/assets/1b15400e-22c4-4280-8a39-d8d39e587828" />
 

this prototype shows that the core idea of caust is feasible and can produce measurable causal signals.

ready for full implementation during the project 

shaurya
osre 2026 applicant
april 2026
