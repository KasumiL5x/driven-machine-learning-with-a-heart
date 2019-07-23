# Machine Learning with a Heart

This is my submission for the DrivenData competition [Machine Learning with a Heart](https://www.drivendata.org/competitions/54/machine-learning-with-a-heart/page/107/).

# Status
I have not yet finished this challenge.

---

## Problem Description
We must predict the binary class `heart_disease_present` where:

* `0` represents no heart disease present
* `1` represents heart disease present

## Dataset
There are 14 columns. `patient_id` is the unique and random identifier for a patient.  The rest are:

* `slope_of_peak_exercise_st_segment` (type: int): the slope of the peak exercise [ST segment](https://en.wikipedia.org/wiki/ST_segment), an electrocardiography read out indicating quality of blood flow to the heart
* `thal` (type: categorical): results of [thallium stress test](https://www.ucsfbenioffchildrens.org/tests/007201.html) measuring blood flow to the heart, with possible values `normal`, `fixed_defect`, `reversible_defect`
* `resting_blood_pressure` (type: int): resting blood pressure
* `chest_pain_type` (type: int): chest pain type (4 values)
* `num_major_vessels` (type: int): number of major vessels (0-3) colored by flourosopy
* `fasting_blood_sugar_gt_120_mg_per_dl` (type: binary): fasting blood sugar > 120 mg/dl
* `resting_ekg_results` (type: int): resting electrocardiographic results (values 0,1,2)
* `serum_cholesterol_mg_per_dl` (type: int): serum cholestoral in mg/dl
* `oldpeak_eq_st_depression` (type: float): oldpeak = [ST depression](https://en.wikipedia.org/wiki/ST_depression) induced by exercise relative to rest, a measure of abnormality in electrocardiograms
* `sex` (type: binary): `0`: female, `1`: male
* `age` (type: int): age in years
* `max_heart_rate_achieved` (type: int): maximum heart rate achieved (beats per minute)
* `exercise_induced_angina` (type: binary): exercise-induced chest pain (`0`: False, `1`: True)

## Feature Examples
| **Field**                            | **Value** |
|--------------------------------------|-----------|
| slope_of_peak_exercise_st_segment    | 2         |
| thal                                 | normal    |
| resting_blood_pressure               | 125       |
| chest_pain_type                      | 3         |
| num_major_vessels                    | 0         |
| fasting_blood_sugar_gt_120_mg_per_dl | 1         |
| resting_ekg_results                  | 2         |
| serum_cholesterol_mg_per_dl          | 245       |
| oldpeak_eq_st_depression             | 2.4       |
| sex                                  | 1         |
| age                                  | 51        |
| max_heart_rate_achieved              | 166       |
| exercise_induced_angina              | 0         |

## Performance
Performance is evaluated using the binary [log loss](https://en.wikipedia.org/wiki/Loss_functions_for_classification#Cross_entropy_loss_(Log_Loss)).

## Submission Format
Two columns are required: `patient_id` and `heart_disease_present`.  Because this competition uses a log loss evaluation metric, `heart_disease_present` should contain the **probabilities that patients have heart disease** and **not** the binary label.  For example:

| **patient_id** | **heart_disease_present** |
|----------------|---------------------------|
| olalu7         | 0.5                       |
| z9n6mx         | 0.5                       |
| ...            | ...                       |