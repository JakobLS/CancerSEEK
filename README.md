# Cancer detection CancerSEEK


Earlier detection is key to reducing cancer deaths. CancerSEEK is a new type of blood test being tested out with the aim of improving cancer detection. It can detect eight common cancer types through the assessment of the levels of circulating proteins and mutations in cell-free DNA. The test was applied on 1005 patients with nonmetastatic, clinically detected cancers of ovary, liver, stomach, pancreas, esophagus, colorectum, lung or breast. __The median sensitivity was 0.70 for the eight cancer types.__ The top sensitivities ranged from 0.69 to 0.98 for the detection of five cancer types (ovary, liver, stomach, pancreas, and esophagus). Additionally, 812 healthy control patients were included in the study. With only 7 of those scoring positive, the paper reported a specificity of above 99%. 


The dataset can be found through [this](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6080308/#SD2) link, which is related to [this](https://science.sciencemag.org/content/359/6378/926.long) research paper. The research team has already worked on the data through PCR-based sequencing of each sample to detect low-prevelance mutations and proteins.

Earlier research has been done on this very same dataset, nevertheless, let's see if I can improve the results! Both in terms of Sensitivity and Specificity. **The project will focus on maximising Sensitivity as it can be considered to be more important to find as many of the patients with cancer as possible rather than incorrectly classifying healthy patients as sick.** The former might lead to a patient's death, while the latter "only" puts them through more tests. 



## Results

Considerable improvements have been achieved through the steps applied in the experiment. With only some basic parameter tuning the performance was boosted considerable compared with the results obtained in the study. **Specificity is reaching roughly the same levels at around 99% while sensitivity is boosted to an impressive 81%. That's an 11 percentage point increase compared to the study!** Or 16 percent! The same features that were evaluated in the study were used in this experiment as well, plus *Plasma DNA concentration*,	*Mutant allele freqeuncy*, 	*Mutant fragments/mL plasma* and *Age*. The 12 most common mutations were also extracted from the column *Mutation identified in plasma*.



### Future work

Experimenting with other pre-processing steps, data cleaning, data transformation, feature engineering, feature selection, model parameter tuning as well as with more complex models migth improve the results even more. 






