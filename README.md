# CancerSEEK
Cancer detection through the multi-analyte blood test CancerSEEK

The only widely used blood test for earlier cancer detection is based on measurement of prostate-specific antigen, and the proper use of this test is still being debated. The approved tests for cancer detection are not blood-based and include colonoscopy, mammography, and cervical cytology. New blood tests for cancer must have very high specificity; otherwise, too many healthy individuals will receive positive test results, leading to unnecessary follow-up procedures and anxiety.

Earlier detection is key to reducing cancer deaths. CancerSEEK is a new type of blood test being tested out with the aim of improving cancer detection. It can detect eight common cancer types through the assessment of the levels of circulating proteins and mutations in cell-free DNA. The test was applied on 1005 patients with nonmetastatic, clinically detected cancers of ovary, liver, stomach, pancreas, esophagus, colorectum, lung or breast. The median sensitivity was 0.70 for the eight cancer types. The top sensitivities ranged from 0.69 to 0.98 for the detection of five cancer types (ovary, liver, stomach, pancreas, and esophagus). Additionally, 812 healthy control patients were included in the study.


The complete dataset can be found through this link, which is related to this research paper. The research team has already worked on the dataset through a PCA-based sequencing of each sample to detect low-prevelance mutations and proteins.


Earlier research has been done on this very same dataset, nevertheless, let's see if we can improve the results! Both in terms of Sensitivity and Specificity. The project will focus on maximising Sensitivity as I consider it being more important to find as many of the patients with cancer as possible rather than incorrectly classifying healthy patients as sick. The former might lead to a patient's death, while the latter "only" puts them through more tests.



# Conclusions

First we successfully managed to identify every single cancer patient in our data. Both Specificity and Sensitivity were calculated to a perfect 1.0; meaning that none of the healthy patients were classified as having cancer, nor was any of the cancer patients classified as healthy. The subsequent AUC score was an equally perfect 1.0. That's really good! On top of that, we indentified the protein AFP (pg/ml) as being the most important in making these predictions. In fact, our Gradient Boosting model was able to make perfect predictions solely on this protein.


We suspected that the AFP (pg/ml) protein was too well correlated with the output variable and made predictions using a Random Forest model as well. This model attributed an importance of around 49 percent to this protein, allowing us to abandon the idea of discarding the AFP (pg/ml) protein from the input feature set. (This is a slightly alternative approach to reaching this conclusion, but which is later validated with this paper about biomarkers.) More work should be done on a larger scale with thousands, or even tens of thousands, of cancer patients to validate this, but the results are nevertheless promising.
Making predictions for each Cancer Type was more cumbersome. We still managed to achieve a perfect Specificity of 1.0 by classifying all healthy patients as healthy. Sensitivity was more tricky, ranging between 0.14 and 0.93 for the eight cancer types with a median of 0.75. Considering the top five cancer Sensitivities, as they did in the published paper, range varied between 0.75 and 0.93 (Colorectum, Breast, Lung, Pancreas and Ovary). It's in line with, or slightly higher, than the range of 0.69 to 0.98 and median of 0.70 achieved in the paper. I've used 20% of the data as test set.


What is surprising though is the types of cancer that experienced the highest scorings. In the published paper Ovary, Liver, Stomach, Pancreas, and Esophagus cancer reached highest specificities while we scored highest on Colorectum, Breast, Lung, Pancreas and Ovary. Only Ovary and Pancreas overlap. In general for Machine Learning, more data mean better results. It makes therefore sense that we achieve the highest specificities where there are more cancer type samples to train our model on (i.e. Colorectum, Breast, Lung and Pancreas). See above printout. The published paper's results are completely opposite on this point.


We can conclude that the project has been a success by reaching, and in some sense also beating, the scores achieved in the research paper. There are still several things I would like to try out such as finetuning the model even more, adding the mutations we discarded in the beginning as input feature; it might also be worth to train a model for each one of the eight cancer types. Another approach might be to train a Deep Learning model on the data using Keras/Tensorflow (rather than doing it in sklearn since we would be able to tune it better). Lastly, the models would likely benefit from more data and it should thus be a priority if production at scale is a long term objective.

