# QSS-20-Final-Project

**Group members:** Justin Paré, Justin Lee, Malachai Ah Yo, Rohan Kommuri

## Description

Corporate tax avoidance through offshore structures and secrecy jurisdictions has become a defining issue in today’s economic and political landscape. Multinational corporations and high-net-worth individuals routinely establish shell companies, trusts, and complex ownership networks to shift profits, obscure beneficial ownership, and minimize tax liabilities. Although these arrangements often operate within the bounds of legality, they erode domestic tax bases, depress public revenues, and exacerbate global inequality. High-profile leaks, such as the Panama Papers and Pandora Papers, have laid bare the scale and sophistication of these offshore networks, galvanizing calls from policymakers, economists, and civil-society advocates for greater transparency, coordinated regulatory reforms, and stronger enforcement mechanisms.

In this project, we draw on the International Consortium of Investigative Journalists’ comprehensive Offshore Leaks dataset to explore the architecture and dynamics of offshore finance. By mapping connections between entities and their appointed officers, we examine which jurisdictions host the largest concentrations of shell companies and the legal or regulatory mechanisms, such as nominee-director requirements and citizenship-by-investment programs, that underpin these patterns. We further consider how offshore incorporation trends evolved around the OECD’s 2000 blacklist, comparing periods before and after its implementation to assess the effectiveness and unintended consequences of international sanctions. Through a blend of network analysis, temporal comparison, and concentration metrics, we hope to gain an understanding of how global oversight and local incentives interact to shape the ever-changing landscape of offshore finance.

## Data

We initially used the raw datasets from the ICIJ Offshore Leaks Database which can be downloaded [here](https://offshoreleaks-data.icij.org/offshoreleaks/csv/full-oldb.LATEST.zip)

Our merged and cleaned version of these datasets is stored in the cloud via Google Drive and can be accessed [here](https://drive.google.com/file/d/1Z9M-1Y1Pn37JZcPvXb2bPylqt_4_Cf7u/view?usp=sharing)

## Code

**[00_data_merging_cleaning.ipynb](https://github.com/malachaiahyo/QSS-20-Final-Project/blob/main/code/00_data_merging_cleaning.ipynb)**

**Inputs used:**
- Raw ICIJ datasets

**Actions performed:**
- Merges the raw ICIJ datasets into a single dataset based on the relationships between nodes as outlined in the relationships dataset.

**Outputs generated:**
- Most importantly produces: **ICIJ_Merged.csv** which is the merged and cleaned version of the raw data. 
- Also produces a sample of this merged and cleaned data. Along with this a merged dataset with no cleaning as well as a sample of that dataset are produced. 

**[01_top_10_graphs.ipynb](https://github.com/malachaiahyo/QSS-20-Final-Project/blob/main/code/01_top_10_graphs.ipynb)**

**Inputs used:**
- ICIJ_Merged and Entities datasets 

**Actions performed:**
Groups and counts entities by their physical‐address country and by their legal jurisdiction and plots top 10 charts for these. 

**Outputs generated:**
- [Figure 2.png](https://github.com/malachaiahyo/QSS-20-Final-Project/blob/main/output/Figure%202.png), a Bar chart of Top 10 Countries where entities are physically based
- [output/Figure 3.png](https://github.com/malachaiahyo/QSS-20-Final-Project/blob/main/output/Figure%203.png), a Bar chart of Top 10 Jurisdictions for entities

**[02_sankey_officer_and_jurisdiction_countries.ipynb](https://github.com/malachaiahyo/QSS-20-Final-Project/blob/main/code/02_sankey_officer_and_jurisdiction_countries.ipynb)**

**Inputs used:**
- ICIJ_Merged Dataset

**Actions performed:**
- Filters to officer→entity links
- Counts relationships by officer’s country (countries_start) and entity’s jurisdiction (jurisdiction_description_end).
- Selects the top officer countries and shows the relationships between them and the top 5 jurisdictions (Bahamas, British Virgin Islands, Malta, Bermuda, Barbados).

**Outputs generated:**
- [Figure 4.png](https://github.com/malachaiahyo/QSS-20-Final-Project/blob/main/output/Figure%204.png), a Sankey diagram showing officer to entity jurisdiction flows, complete with self-loops

**[03_officers_samejurisdiction.ipynb](https://github.com/malachaiahyo/QSS-20-Final-Project/blob/main/code/03_officers_samejurisdiction.ipynb)**

**Inputs used:**

**Actions performed:**

**Outputs generated:**

**[code/04_OECD_2000_investigations.ipynb](https://github.com/malachaiahyo/QSS-20-Final-Project/blob/main/code/04_OECD_2000_investigations.ipynb)**

**Inputs used:**

**Actions performed:**

**Outputs generated:**

