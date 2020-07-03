# Cancer detection CancerSEEK


Earlier detection is key to reducing cancer deaths. CancerSEEK is a new type of blood test being tested out with the aim of improving cancer detection. It can detect eight common cancer types through the assessment of the levels of circulating proteins and mutations in cell-free DNA. The test was applied on 1005 patients with nonmetastatic, clinically detected cancers of ovary, liver, stomach, pancreas, esophagus, colorectum, lung or breast. __The median sensitivity was 0.70 for the eight cancer types.__ The top sensitivities ranged from 0.69 to 0.98 for the detection of five cancer types (ovary, liver, stomach, pancreas, and esophagus). Additionally, 812 healthy control patients were included in the study. With only 7 of those scoring positive, the paper reported a specificity of above 99%. 


The dataset can be found through [this](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6080308/#SD2) link, which is related to [this](https://science.sciencemag.org/content/359/6378/926.long) research paper. 

Earlier research has been done on this very same dataset, nevertheless, let's see if I can improve the results! Both in terms of Sensitivity and Specificity. **The project will focus on maximising Sensitivity as it can be considered being more important to find as many of the patients with cancer as possible rather than incorrectly classifying healthy patients as sick.** The former might lead to a patient's death, while the latter "only" puts them through more tests. 



## Results

Considerable improvements have been achieved on some key cancer types. **Specificity reached roughly the same levels as in the study at above 99% while sensitivity has been boosted for Breast cancer with 100% (to 69%), Colorectum with 31% (to 85%) and Pancreas 21% (to 85%).**



### Future work

Experimenting with other pre-processing steps, data cleaning, data transformation, feature engineering, feature selection, model parameter tuning as well as with more complex models migth improve the results even more. Feature selection might be the first step to try out as decreasing the number of features might decrease the price of the test, meaning more patients can be screened. 

**NOTE:** After consulting with the company they are now focusing on other approaches to detect the location of the tumor. 






