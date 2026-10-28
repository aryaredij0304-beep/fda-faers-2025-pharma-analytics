# fda-faers-2025-pharma-analytics
Business Analyst project — FDA FAERS 2025 fatal adverse event analysis using Excel and Power BI
# Pharmacovigilance Risk Intelligence — FDA FAERS 2025

## Problem Statement

Pharmaceutical companies face increasing regulatory scrutiny around 
adverse event monitoring. Yet most pharmacovigilance reviews are 
reactive — triggered by incidents rather than driven by patterns 
in reporting data. This project analyses the complete census of 
97,251 fatal adverse event reports submitted to the US FDA in 2025 
to answer one question:

**Where is fatal adverse event risk concentrated, and what does 
that tell us about gaps in the current pharmacovigilance system?**

---

## Dataset

- **Source:** FDA Adverse Event Reporting System (FAERS) via openFDA API
- **Coverage:** January 1 – December 31, 2025 (complete census, no sampling)
- **Records:** 97,251 fatal adverse event reports after deduplication 
  and quality filtering
- **Key fields:** Drug name, patient age/sex/weight, reporter type, 
  country of occurrence, fatal reactions, drug indication

---

## Analytical Framework

Rather than treating this as a data exercise, the analysis was 
structured around stakeholder needs — each question mapped to a 
specific decision-maker in a pharmaceutical quality and regulatory 
function:

| Stakeholder | Business Question |
|---|---|
| QA Manager | Which drugs warrant priority pharmacovigilance review? |
| Regulatory Affairs Head | Are there temporal anomalies that signal systemic issues? |
| Medical Safety Officer | Which patient populations are most at risk? |
| Regional Manager | Where are pharmacovigilance infrastructure gaps? |
| Compliance Head | Is the reporting system functioning as intended? |

---

## Key Findings

### 1. Drug Risk Concentration
The top 5 drugs by fatal report frequency — Dapagliflozin (2,402), 
Nuplazid (1,983), Carbidopa/Levodopa (1,163), Osimertinib (1,015), 
and Budesonide/Formoterol/Glycopyrronium (969) — collectively account 
for 7.75% of all fatal reports. All five treat serious chronic 
conditions in elderly or critically ill populations. This demands 
careful interpretation: high report volume may reflect disease 
severity rather than direct drug causality, and conflating the two 
leads to misinformed pharmacovigilance prioritisation.

### 2. Systemic Reporting Anomaly — January Surge
January 2025 recorded 12,058 reports — 48.8% above the monthly 
average of 8,104 and well beyond any other month. The remaining 
11 months showed stable volume between 7,044 and 8,941. This 
pattern is consistent with periodic reporting cycles and year-end 
backlog submission rather than a genuine January safety event — 
a distinction that matters when regulators interpret trend data.

### 3. Pharmacovigilance Compliance Gap — Reporter Type
Consumers/Non-Health Professionals are the single largest reporting 
group at 33.36% — exceeding physician reporting at 28.80%. 
Pharmacists, despite being the last clinical touchpoint before 
patient medication, represent only 6.23% of reporters. In a 
well-functioning pharmacovigilance system, healthcare professionals 
should dominate reporting. This disparity points to a structural 
under-reporting problem by clinical staff — a compliance risk that 
regulatory bodies increasingly scrutinise.

### 4. Geographic Concentration and Infrastructure Gaps
The US accounts for 38.76% of all reports — a reflection of 
mandatory MedWatch reporting requirements rather than inherently 
higher US drug risk. Markets like Brazil (0.90%) and China (2.14%) 
are likely under-represented relative to their pharmaceutical market 
size, suggesting weaker FDA-aligned pharmacovigilance infrastructure. 
India at 2.46% (rank 6) reflects its growing role as a global 
pharmaceutical manufacturing hub with increasing regulatory 
accountability to FDA and EU-GMP standards.

### 5. Elderly Patient Vulnerability
Patients aged 61-80 represent the single largest age cohort at 
28.59%. Combined elderly patients (61+) account for 39.52% of 
all fatal reports — nearly 4 in 10. Fatal adverse events follow 
a clear age progression rising sharply from middle age. This 
concentration in elderly populations has direct implications for 
pharmacovigilance monitoring design: risk stratification by age 
cohort, not just by drug, is essential for accurate safety signals.

---

## Deliverables

- `data_quality_report.xlsx` — Null analysis, outlier checks, 
  categorical validation across all 10 columns
- `faers_analysis.xlsx` — Full Pivot Table analysis for all 5 
  stakeholder questions
- `faers_dashboard.pbix` — Interactive Power BI dashboard with 
  slicers for country, reporter type, and patient gender

---

## Tools
Excel | Power BI | FDA openFDA API

---

## Data Source
Kulkarni, A. (2025). *FDA FAERS 2025: Fatal Drug Adverse Events 
(Complete Census)*. Kaggle.
