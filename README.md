# hcc_u_soon
Preprocessing and Modeling Pipelines for the research project "Machine learning predicts liver cancer risk from routine clinical data: a large population-based multicentric study"

## Repository Structure
The repository is structured into three main parts:

1. **Data Preprocessing in the UKBiobank Dataset**:
    - This section contains scripts and notebooks for cleaning, concatenating, and scaling the raw data derived from the UKBiobank.
    - The user may provide a `Mastertable.xlsx` specifying the covariates and comorbidities to be included.
    - See **preprocessing_ukb**.
2. **Modeling**:
    - This section contains the code to train, evaluate, compress, and deploy machine learning models trained on the UKBiobank. The condensed, lightweight models can be deployed and externally validated.
3. **External Validation in the AllOfUs Cohort from the USA**:
    - We externally validated our lightweight, feature-reduced model by obtaining and combining the necessary information from the AllOfUs Cohort. The model performance was then evaluated against the primary training and testing data from the UKB.

As a tool for demonstration, we built a graphical user interface which can be found on [Hugging Face](https://huggingface.co/spaces/schneiderlab/ML-HCC) under this [link](https://huggingface.co/spaces/schneiderlab/ML-HCC). This is no medical device and should not influence any clinical decision.


**References**
Machine learning predicts liver cancer risk from routine clinical data: a large population-based multicentric study
Jan Clusmann, Paul-Henry Koop, David Y. Zhang, Felix van Haag, Omar S. M. El Nahhas, Tobias Seibel, Laura Žigutytė, Apichat Kaewdech, Julien Calderaro, Frank Tacke, Tom Luedde, Daniel Truhn, Tony Bruns, Kai Markus Schneider, Jakob N. Kather, Carolin V. Schneider
medRxiv 2024.11.03.24316662; doi: https://doi.org/10.1101/2024.11.03.24316662

**Figure 1 from [Clusmann et al. (2024)](https://doi.org/10.1101/2024.11.03.24316662)**
a The task of predicting HCC occurrence was divided into prediction from a healthy cohort (“All”) and prediction among patients-at-risk (“PAR”). Multimodal data from UKB was extracted and scenarios set up according to availability of data on a patient's trajectory in the healthcare system. b ML architecture with an inner-layer five-fold crossvalidation, with a grouped-split approach, where each split (indicated by small squares) combines 4-5 assessment centers together,, with each split serving four times as training and once as validation set. Training data solely generated from UKB centers within England as indicated on the schematic map of Great Britain. The final model is a majority vote (M) built from the five generated ML models. M was then applied to the with-held test set built from UKB centers in Scotland/Wales (+Newcastle, for 80:20 balance between train/test) with numerical prediction output. c Evaluation and independent external testing of the model, including classification, time-to-event analysis and sub-group analysis. Thresholds are applied to rule-in for screening (when > “High”-threshold) or to rule-out for screening (when < “Low”-threshold).
