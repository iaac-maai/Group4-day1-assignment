# Group 4 — Data Cleaning and Exploratory Data Analysis

**Repository:** `iaac-maai/Group4-day1-assignment`

## Team Members

- Fawad
- Hetashri
- Daria
- Luis

---

## 1. Use Case

This project investigates residential building energy performance and consumption using the UK's National Energy Efficiency Data-Framework (NEED).

The aim is to understand the quality of property-level energy data, explore relationships between building characteristics and energy demand, and communicate findings through descriptive statistics and visualisations.

The exploratory analysis focuses on:

- Energy Performance Certificate (EPC) distributions.
- Historical gas consumption patterns.
- Historical electricity consumption patterns.
- Energy consumption differences across property types.
- Relationships between gas and electricity consumption.

The cleaned dataset and analytical findings provide a foundation for future predictive modelling of residential building energy performance.

## 2. Project Overview

This project focuses on data cleaning, preprocessing and Exploratory Data Analysis (EDA) using Python.

The workflow includes:

1. Loading and inspecting the original dataset.
2. Identifying missing values and duplicate records.
3. Checking data types and data consistency.
4. Investigating potential outliers.
5. Preparing data for analysis.
6. Performing descriptive and statistical analysis.
7. Generating visualisations to communicate energy consumption patterns.
8. Documenting findings and limitations.

## 3. Dataset

The project uses the **National Energy Efficiency Data-Framework (NEED): Anonymised Data 2026**, published by the UK Department for Energy Security and Net Zero (DESNZ).

| Attribute | Description |
|---|---|
| Dataset name | National Energy Efficiency Data-Framework (NEED): Anonymised Data 2026 |
| Publisher | Department for Energy Security and Net Zero (DESNZ) |
| Geographic coverage | England and Wales |
| Unit of observation | Individual residential properties |
| Original sample size | 50,000 rows |
| Number of columns | 96 |
| Temporal coverage | 2005–2024 |
| Main variables | Gas consumption, electricity consumption, EPC ratings, property characteristics and energy-efficiency measures |
| File format | CSV |

**Original dataset:** National Energy Efficiency Data-Framework (NEED), 2026 release.

The dataset contains anonymised property-level information, including energy consumption, building characteristics and energy-efficiency measures.

### Dataset Licensing

The original dataset is published under the UK Open Government Licence (OGL).

Users should consult the original publication and licence terms for attribution requirements.

## 4. Dataset Access and Storage

The original dataset is not committed to this GitHub repository.

To reproduce the analysis:

1. Obtain the 50,000-row anonymised NEED 2026 dataset from its official source.
2. Place the downloaded CSV file inside the project's `data/` directory.
3. Ensure the filename is:

`anon2026_50k.csv`

The expected local structure is:

```text
data/
├── .gitkeep
└── anon2026_50k.csv
```

The original and cleaned datasets are excluded from version control to avoid committing large data files.

## 5. Research Questions

The exploratory analysis investigates the following questions:

1. How are EPC ratings distributed across the properties in the dataset, and how do they relate to energy consumption where comparable observations are available?

2. How has average annual gas consumption changed between 2005 and 2024?

3. How has average annual electricity consumption changed between 2005 and 2024?

4. What relationships exist between gas and electricity consumption across the available observation period?

5. How does energy consumption vary across different residential building types?

These questions are investigated using descriptive statistics, grouped comparisons, correlation analysis and visualisations.

## 6. Project Structure

```text
Group4-day1-assignment/
│
├── data/
│   └── .gitkeep
│
├── figures/
│   ├── average_energy_by_building_type.png
│   ├── epc_distribution.png
│   ├── average_annual_gas_consumption.png
│   ├── average_annual_electricity_consumption.png
│   └── gas_vs_electricity_consumption_trends.png
│
├── notebook/
│   └── uk_energy_consumption_eda.ipynb
│
├── LICENSE
├── README.md
├── requirements.txt
└── .gitignore
```

**Note:** The original and cleaned CSV files are stored locally and are not tracked by Git.

## 7. Installation and How to Run

### Prerequisites

- Python 3.10 or later.
- Jupyter Notebook.
- Visual Studio Code or another compatible notebook environment.

### Step 1: Clone the Repository

```bash
git clone https://github.com/iaac-maai/Group4-day1-assignment.git

cd Group4-day1-assignment
```

### Step 2: Create a Virtual Environment

```bash
python -m venv .venv
```

### Step 3: Activate the Environment

**Windows PowerShell:**

```powershell
.venv\Scripts\Activate.ps1
```

**macOS/Linux:**

```bash
source .venv/bin/activate
```

### Step 4: Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### Step 5: Add the Dataset

Download the original anonymised NEED dataset and place it inside:

```text
data/anon2026_50k.csv
```

### Step 6: Run the Notebook

Open:

`notebook/uk_energy_consumption_eda.ipynb`

in Jupyter through Visual Studio Code.

Select the `.venv` Python kernel and execute:

**Restart Kernel → Run All**

The notebook performs the data-cleaning and exploratory analysis workflow and generates the corresponding visualisations.

## 8. Data Cleaning and Preprocessing

The data-cleaning workflow focuses on improving data quality and preparing the dataset for exploratory analysis.

The following checks and operations are included:

| Quality Check | Description |
|---|---|
| Duplicate records | Identification and examination of duplicate observations. |
| Missing values | Inspection of missing values across relevant variables. |
| Data types | Verification and correction of inconsistent data types where necessary. |
| Outliers | Investigation of unusually high or low energy consumption values. |
| Data consistency | Checking the consistency of property characteristics and energy consumption variables. |
| Feature preparation | Selection and preparation of relevant variables for exploratory analysis. |

Cleaning decisions are documented in the Jupyter notebook, including the reasoning behind data transformations and exclusions.

### Cleaned Dataset

The processed dataset is exported locally as:

`data/anon2026_50k_cleaned.csv`

The cleaned dataset is not committed to the repository.

## 9. Exploratory Data Analysis

The exploratory analysis uses descriptive statistics, distributions, grouped comparisons, historical trends and correlation analysis.

The following visualisations are generated and included in the repository.

### 9.1 Annual Electricity Consumption Trends (2005–2024)

This visualisation examines changes in average annual electricity consumption across the available observation period.

![Annual Electricity Consumption Trends](figures/average_annual_electricity_consumption.png)

### 9.2 Annual Gas Consumption Trends (2005–2024)

This visualisation examines changes in average annual gas consumption and provides insight into historical residential gas demand.

![Annual Gas Consumption Trends](figures/average_annual_gas_consumption.png)

### 9.3 Energy Consumption by Building Type

This comparison explores differences in energy consumption across residential building types.

![Average Energy Consumption by Building Type](figures/average_energy_by_building_type.png)

### 9.4 EPC Rating Distribution

This visualisation examines the distribution of Energy Performance Certificate ratings across the properties in the dataset.

![EPC Distribution](figures/epc_distribution.png)

### 9.5 Gas vs Electricity Consumption Trends

This visualisation compares historical gas and electricity consumption trends using an indexed baseline of 2005 = 100, where the required observations are available.

![Gas vs Electricity Consumption Trends](figures/gas_vs_electricity_consumption_trends.png)

## 10. Key Findings

The notebook presents the quantitative results of the exploratory analysis.

The main areas investigated include:

- **EPC performance:** Distribution of energy performance ratings across residential properties.
- **Gas consumption:** Changes in average annual gas consumption over the observation period.
- **Electricity consumption:** Changes in average annual electricity consumption.
- **Building characteristics:** Differences in energy consumption across property types.
- **Energy relationships:** Associations between gas and electricity consumption.

Numerical findings and supporting interpretations should be taken from the executed notebook and its corresponding analytical outputs.

## 11. Limitations and Potential Biases

The analysis has several limitations that should be considered when interpreting the results:

- The anonymised dataset represents a sample rather than the complete population of residential properties.
- Geographic coverage is limited to England and Wales.
- Missing values and differences in data availability may affect the results of individual analyses.
- EPC ratings and measured energy consumption represent related but different aspects of building energy performance.
- Changes in energy consumption may also be influenced by weather conditions, energy prices, occupancy patterns and household behaviour.
- Observed correlations and historical trends do not establish causal relationships.
- Historical consumption patterns should not automatically be interpreted as indicators of future energy demand.

## 12. Licence

### Source Code and Documentation

The original source code and documentation developed by Group 4 for this project are licensed under the **MIT License**.

See the [LICENSE](LICENSE) file for the complete licence terms.

### Dataset

The National Energy Efficiency Data-Framework (NEED) anonymised dataset is published by the UK Department for Energy Security and Net Zero.

The dataset is distributed under the **Open Government Licence v3.0 (OGL v3.0)**.

Users should follow the original publisher's attribution requirements and applicable licence conditions.

**Dataset source:** National Energy Efficiency Data-Framework (NEED), 2026.

**Dataset licence:** Open Government Licence v3.0.

## 13. AI Usage Disclosure

| Category | Disclosure |
|---|---|
| **Tools** | ChatGPT (conversational AI assistant). Used through chat interactions. No autonomous AI agents were used to edit repository files or execute the project workflow. |
| **Why** | To support learning Python data analysis, troubleshoot programming issues, understand Pandas operations, improve data visualisation and assist with Git/GitHub workflows and project documentation. |
| **Where** | Data-cleaning and preprocessing workflow, exploratory data analysis, visualisation development, notebook documentation, README preparation and Git/GitHub troubleshooting. |
| **How** | Conversational prompts were used to request explanations, code examples and debugging suggestions. For example: "How can I identify missing values, duplicate records and inconsistent data types in this dataset using Pandas?" Suggestions were reviewed, adapted and tested against the actual dataset. Generated code was checked through execution, inspection of outputs and verification of visualisations. Suggestions that did not fit the dataset structure or project requirements were modified or rejected. |

### Lessons Learned

ChatGPT was useful for understanding unfamiliar Python operations, troubleshooting programming errors and exploring alternative approaches to data analysis.

However, some suggestions required modification to match the actual dataset structure, available variables and project requirements.

We learned that AI-generated code and explanations should not be accepted without verification. In future projects, we would provide more precise dataset context in our prompts, validate intermediate outputs systematically and document important analytical decisions.

The team remains responsible for understanding, validating and defending all code, data-cleaning decisions and analytical interpretations included in this submission.