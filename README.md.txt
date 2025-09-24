# CirrhoMetrix: A Cirrhosis Prognostic Score Calculator

## Project Overview

**CirrhoMetrix** is a simple, web-based tool developed to assist medical professionals and students in calculating key prognostic scores for patients with cirrhosis. It provides a quick and accurate summary of a patient's liver disease status based on clinical and laboratory parameters, supporting clinical decision-making and academic research.

This tool was created as part of a medical gastroenterology residency thesis project by Dr R Sriman Narayan Reddy to compare the prognostic value of MELD-Na and MELD 3.0 scores in a clinical setting.

## How to Use the Tool

1.  **Open the file:** Simply open the `cirrhosis_calculator.html` file in any modern web browser (Chrome, Firefox, Safari, etc.).
2.  **Enter data:** Fill in the required clinical and lab parameters in the respective input fields.
3.  **Calculate:** Click the **"Calculate Scores"** button to generate the prognostic summary.
4.  **View results:** The **"Clinical Impression"** box will appear at the bottom of the page, displaying the calculated scores and a summary of the patient's condition.

## Prognostic Scores & Formulas

This tool uses the following validated scoring models and their corresponding formulas, calibrated to match widely used clinical calculators like MDCalc.

### 1. Child-Pugh Score

The Child-Pugh score assesses the severity of liver disease. It uses five parameters, with each assigned 1, 2, or 3 points.

* **Total Bilirubin:** <2.0 mg/dL (1 pt), 2.0-3.0 mg/dL (2 pts), >3.0 mg/dL (3 pts)
* **Serum Albumin:** >3.5 g/dL (1 pt), 2.8-3.5 g/dL (2 pts), <2.8 g/dL (3 pts)
* **INR:** <1.7 (1 pt), 1.7-2.3 (2 pts), >2.3 (3 pts)
* **Ascites:** None (1 pt), Mild (2 pts), Moderate to Severe (3 pts)
* **Hepatic Encephalopathy:** None (1 pt), Grade I-II (2 pts), Grade III-IV (3 pts)

### 2. MELD-Na Score (UNOS/OPTN)

The MELD-Na score is a crucial tool for predicting short-term mortality in cirrhosis. The calculation is a two-step process:

* **MELD (Original, Pre-2016):** `MELD = 10 * [0.957*ln(Creatinine) + 0.378*ln(Bilirubin) + 1.120*ln(INR) + 0.643]` (Parameters are capped, and values less than 1 are treated as 1).
* **MELD-Na Adjustment:** If MELD > 11, the score is adjusted using the sodium value: `MELD-Na = MELD + 1.32*(137 – Na) – [0.033*MELD*(137 – Na)]`

### 3. MELD 3.0 Score

The MELD 3.0 score is a modern update that provides a more accurate prognosis by incorporating Albumin and Gender.

* **MELD 3.0:** A complex formula involving multiple coefficients for creatinine, INR, bilirubin, sodium, albumin, age, and a gender-based correction factor.

## Developer

Developed by **Dr R Sriman Narayan Reddy**.

## Disclaimer

This tool is for educational and research purposes only and should not be used as a substitute for professional medical advice. Always consult a qualified healthcare professional for medical diagnoses and treatment.