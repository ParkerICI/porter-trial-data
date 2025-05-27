# porter-trial-data
Summary datasets from the PORTER clinical trial in metastatic castration-resistant prostate cancer (mCRPC), as reported in the following manuscript. 

Galsky MD, Autio KA, Cabanski CR, Wentzel K, Graff JN, Friedlander TW, Howes TR, Shotts KM, Densmore J, Spasic M, Da Silva DM, Chen RO, Lata J, Skolnik J, Keler T, Yellin MJ, LaVallee TM, Fairchild J, Boffo S, O'Donnell-Tormey J, Dugan U, Bhardwaj N, Subudhi SK, Fong L. Clinical and Translational Results from PORTER, a Multi-cohort Phase 1 Platform Trial of Combination Immunotherapy in Metastatic Castration-Resistant Prostate Cancer. Clinical Cancer Research. 2025. https://doi.org/10.1158/1078-0432.CCR-24-3693

## DATA DICTIONARY
### clinical-data
#### Subject-Level Data: PORTER_SuppTableS6_AllPatients.xlsx
An extended version of Supplementary Table S6 from the manuscript, which contains data on all 43 patients.


#### Subject-Level Data: PORTER_clinical_data_public.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* measurable.disease = Indicates whether the patient had measurable or non-measurable disease per PCWG3-modified RECIST criteria
* age	= Age
* sex	= Sex
* race = Race
* ethnicity	= Ethnicity
* treatment.duration.months = Time in months from first dose of study drug to last dose
* CTC.baseline = Circulating Tumor Cells (cells / 7.5 mL blood) at Baseline. NA indicates no baseline CTC measurement was obtained.
* CTC.percent.change.from.baseline =  Best (lowest) percentage change in CTC from baseline across all post-baseline timepoints. NA indicates the patient had no baseline and/or post-baseline measurements.
* CTC.responder = "Y" indicates a patient had baseline CTC >= 5 cells / 7.5 mL of blood and at least one post-baseline CTC <= 4 cells / 7.5 mL of blood. "N" indicates a patient had baseline CTC >= 5 cells / 7.5 mL of blood and either no post-baseline CTC measurements or all post-treatment CTC measurements were >= 5 cells / 7.5 mL of blood. "NE" indicates a patient had baseline CTC <= 4 cells / 7.5 mL of blood or no baseline CTC measurement.
* PSA.baseline = PSA (ng/mL) at Baseline. 
* PSA.percent.change.from.baseline =  Best (lowest) percentage change in PSA from baseline across all post-baseline timepoints. NA indicates the patient had no post-baseline measurements.
* PSA.responder = "Y" indicates a patient had a decrease in PSA > 50% from baseline at 2 post-baseline timepoints at least 3 weeks apart. "N" indicates this criteria was not met.
* target.lesions.percent.change.from.baseline = Best (lowest) percentage change in the sum of target lesions from baseline across all post-baseline tumor scans. NA indicates a patient had non-measurable disease (no target lesions) or no post-baseline scans.
* best.overall.response = Best Overall Response by PCWG3-modified RECIST version 1.1.
* rPFS.months = Radiographic progression free survival (months)
* rPFS.event.flag = "0" represents a censored value, "1" represents an rPFS event was observed
* os.months = Overall Survival (months)
* os.event.flag = "0" represents a censored value, "1" represents an OS event (death) was observed
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months


#### Adverse Events: PORTER_ae_public.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* ae.coded.preferred.term = AE Preferred Term, coded using dictionary MedDRA v25.0
* ae.coded.soc = AE System Organ Class, coded using dictionary MedDRA v25.0
* study.day.start = Study Day of AE Start
* study.day.end = Study Day of AE End. "NA" represents an event that was ongoing at time of study discontinuation.
* ae.severity = AE Severity Grade
* ae.serious = "Y" represents the AE was a Serious Adverse Event (SAE)
* ae.related.treatments = Which study treatments the AE was attributed to by the investigator. A blank field indicates the AE was deemed unrelated to all study treatments. 
* ae.outcome = AE Outcome
* coding.dictionary = Dictionary that AE Terms were Coded to (MedDRA v25.0)
  

#### Clinical Labs, including CTC and PSA: PORTER_labs_public.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* lab.category = Lab Test Type (Chemistry, Hematology, Thyroid Function Testing)
* lab.test = Lab Test Name
* visit = Visit Name when Lab Test was Performed
* study.day = Study Day of Lab Test
* lab.value = Value of Lab Test
* lower.limit.normal = Lower Limit of Normal Range
* upper.limit.normal = Upper Limit of Normal Range
* baseline flag = "Y" indicates the measurement was considered a patient's baseline value
* baseline.value = baseline test value for the patient
* change from baseline = absolute change from baseline
* percent.change.from.baseline = percentage change from baseline


#### Prior Systemic Cancer Therapies: PORTER_priortherapy_public.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* study.day.start = Study Day Prior Therapy Started. NA indicates the start date was unknown.
* study.day.end = Study Day Prior Therapy Ended. NA indicates the end date was unknown.
* therapy.verbatim.name = Verbatim (site-reported) Name of Therapy
* therapy.coded.preferred.name = Therapy Preferred Name, coded using dictionary WHODrug
* coding.dictionary = Dictionary that Prior Therapies were Coded to (WHODrug-Global-B3 September 2021)
* therapy.best.response = Best Response to the Therapy


### translational-data
#### Mass Cytometry (CyTOF): PORTER_cytof_public.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* timepoint.id = Timepoint of Sample Collection
* cell.population.name = Cell Population
* percent.of.leukocytes = Abundance Value, measured as the Percentage of Leukocytes
* percent.of.parent = Abundance Value, measured as the Percentage of the Parent Population
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months


#### Olink Serum Proteomics: AMADEUS_primarycohort_olink.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* timepoint.id = Timepoint of Sample Collection
* protein.name = Name of Protein
* npx = Protein Expression, measured as NPX Units
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months


#### RNAseq, Baseline Samples: AMADEUS_primarycohort_rnaseq_baseline.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* timepoint.id = Timepoint of Biopsy Collection
* gene.name = Gene Name
* raw.count = Raw Counts
* TPM.transcript.per.million = Transcripts per Million (TPM) Value
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months


#### Whole Exome Sequencing - MSI and Tumor Mutational Burden: PORTER_msi_tmb_public.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* msi = MSI Classification
* tmb = Tumor Mutational Burden, measured as Number of Mutations per Megabase


#### Whole Exome Sequencing - Mutation Calls: PORTER_mutations_public.csv
* manuscript.id = Deidentified Subject ID reported in the manuscript
* cohort = Treatment Cohort (A, B, C)
* treatment = Treatment Regimen
* composite.endpoint.responder = "Y" indicates a patient met at least one of the following criteria: CTC.responder = "Y", PSA.responder = "Y", or best.overall.response = "Partial Response"
* disease.control.6month = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* timepoint.id = Timepoint of sample collection (BL [baseline] or Archival)
* chromosome = Chromosome of mutation
* position = Sequence position of mutation
* gene.symbol = Gene symbol where mutation occurs
* variant.type = type of mutation
* variant.effect = Effect of mutation
* variant.effect.impact = predicted effect of mutation
* functional.class = functional class of mutation


