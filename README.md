# QSS-20-Final-Project

Group members: Justin Lee, Justin Pare, Malachai Ah Yo, Rohan Kommuri

**Goal:**

Using the ICIJ Offshore Leaks dataset, we want to undestand how entity type (LLC, LTD, foundations, charities, etc.) varies across jurisdictions and regions, analyze the changes in popularity of specific jurisdictions over time and assess how these shifts may be influenced by laws and/or enforcement trends that happened around the same time as any shifts, and map regional concentrations of offshore leaks activity. We hope that this anlysis will help us to better understand how the movement of offshore wealth firms has changed over time and illuminate the impact of any legal, fiscal, and geographic forces which shape offshore wealth flows. 

Potential forms of analyis we hope to use on the data are listed below in **Potential Future Analyses and Visualizations**

**Data:**

For our analysis, we used the Raw Datasets from the ICIJ Offshore Leaks Database which can be downloaded [here] (https://offshoreleaks-data.icij.org/offshoreleaks/csv/full-oldb.LATEST.zip)

Our cleaned and merged dataset is stored in the cloud via google drive and can be accessed [here] (https://drive.google.com/file/d/1Z9M-1Y1Pn37JZcPvXb2bPylqt_4_Cf7u/view?usp=sharing)

This dataset represents a merged table from the ICIJ’s Entities, Addresses, and Relationships files, focused on linking each offshore entity to its registered address

**Filtering Approach:**

Each row in our final dataset represents a dyad between two nodes:

The _start suffix corresponds to the first node (typically an entity) and the _end suffix corresponds to the second node (typically an address).

Filter node_id_start to include only entities

Filter node_id_end to include only addresses.

Retain only relevant columns, including:

jurisdiction_start: the jurisdiction of the entity

incorporation_date_start: when the entity was incorporated

inactivation_date_start: when the entity was inactivated (if applicable)

These columns were removed due to irrelevancy: 
status, start_date, end_date, note_start, dorm_date_start, valid_until_start, valid_until_end, note_end

**Initial Analysis**

Identify the Top 10 countries where entities are physically located (based on the address country)

Identify the Top 10 jurisdictions where entities are incorporated

Visualize these using a bar chart with a gradient color scheme:

Blue: Top 10 physical locations

Orange: Top 10 jurisdictions

**Potential Issues to Look At**
Some potential issues that we could review would be how the datasets were merged together as well as the filtering and cleaning of the data. Specifically, we want to ensure that the integrity of our merged dataset is not compromised with inconsistencies that make it different from the individual datasets (ie, the entity type associated with a specific node_id in the merged data set is different than the entity type for that node id in the original datasets). We also want to prevent and or handle missing and null values in the merged dataset for our analysis. 

**Potential Future Analyses and Visualizations**

A heat map time series visualization that maps:

The physical locations of entities (country_end)

The jurisdictions of incorporation (jurisdiction_start)

Using incorporation_date_start and inactivation_date_start to animate the temporal dynamics of offshore activity

We will supplement this analysis with external research to better understand the legal and political reasons why certain jurisdictions dominate offshore registrations, all the data is stored in a Google Drive folder 

