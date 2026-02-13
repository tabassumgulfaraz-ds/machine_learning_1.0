## UNIT 5_II

## PREPROCESSING | DATA CLEANING → DATA INCONSISTENCIES/ANOMALIES

### 1. Data Inconsistency

**Data inconsistencies** are errors or contradictions in a dataset, where the same data is represented in different, conflicting, mismatched, or illogical ways across a dataset. In machine learning, inconsistent data can **mislead the model**, reduce accuracy, and increase preprocessing complexity.

In **data cleaning**, handling data inconsistencies means identifying and correcting these mismatches so the data becomes **accurate, uniform, and reliable** for training machine learning models.

### 1.1. Data Inconsistency by Data Type / Format

#### 1.1.1. Numerical Data

- **Example:** Age recorded as 25 (year) in one row and 250 (months) in another for the same person. If Age is greater than 100 consider as months.

- **Issues:** Outliers, wrong units, conflicting measurements.

- **Cleaning Approach:** Apply validation rules, detect outliers, cross-check with reference ranges.

#### 1.1.2. Categorical / Text Data

- **Example:** Gender recorded as M, Male, male, or m in different rows.

- **Issues:** Different spellings, synonyms, inconsistent abbreviations.

- **Cleaning Approach:** Standardization, mapping to a canonical form, case normalization.

#### 1.1.3. Date / Time Data

- **Example:** 01/02/2025 in one row, 2025-02-01 in another (DD/MM/YYYY vs YYYY-MM-DD).

- **Issues:** Different formats, wrong time zones, impossible dates (like 30 Feb).

- **Cleaning Approach:** Convert to a unified format (ISO standard), detect invalid dates.

#### 1.1.4. Boolean / Binary Data

- **Example:** True/False vs 1/0 vs Yes/No in the same column.

- **Issues:** Mixed representations can confuse algorithms.

- **Cleaning Approach:** Map all values to a single consistent representation.

#### 1.1.5. Multi-format / Mixed-type Columns

- **Example:** Column Price having values "$100", 100, USD 100.

- **Issues:** Numeric algorithms can't directly process strings.

- **Cleaning Approach:** Strip non-numeric symbols, convert to float or integer.

#### 1.1.6. Missing / Null Values

- **Example:** One system records missing salary as NaN, another as 0, and another as Unknown.

- **Issues:** Can create misinterpretation during analysis.

- **Cleaning Approach:** Replace with a consistent placeholder, impute, or remove rows.

#### 1.1.7. Duplicated / Redundant Records

- **Example:** Two entries for the same customer with slight differences in spelling or address.

- **Issues:** Biases statistical distributions, misleads ML models.

- **Cleaning Approach:** Deduplication using fuzzy matching, key-based merging.

#### 1.1.8. Logical Conflicts

- **Example:** A person's Date of Birth is 2010-05-10 but Age column shows 30.

- **Issues:** Internal inconsistencies can break model assumptions.

- **Cleaning Approach:** Recalculate dependent fields or flag errors for manual review.

#### 1.1.9. Naming Conversion

- U.S.A, USA, United State, United State of America

#### 1.1.10. Typographical Mistake

- James Taylor, james taylor

#### 1.1.11. Contradictory Data

- Son age < father age (truth)

- Son age > father age (not truth remove this contradictory inconsistency)

<p align="center">
  <a href="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/pdf_notes/Unit_5_II_Preprocessing%20I%20Data%20Cleaning%2C%20Data%20Inconsistencies%20or%20Anomalies.pdf" target="_blank">
    <img src="https://cdn-icons-png.flaticon.com/512/337/337946.png" 
         alt="PDF Logo" 
         width="100"/>
  </a>
</p>

<p align="center">
  <a href="https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/pdf_notes/Unit_5_II_Preprocessing%20I%20Data%20Cleaning%2C%20Data%20Inconsistencies%20or%20Anomalies.pdf" target="_blank">
    <b>Preprocessing | Data Cleaning → Data Inconsistencies/ Anomalies</b>
  </a>
</p>







https://github.com/tabassumgulfaraz-ds/machine_learning_1.0/blob/main/files_and_datasets/f_ds5_II/preprocessing_datacleaning_datainconsistancies.ipynb
