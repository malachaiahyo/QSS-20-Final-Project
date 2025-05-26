# QSS-20-Final-Project

Group members: Rohan Kommuri, Justin Lee, Justin Pare, Malachai Ah Yo

**Goal:**

Using the ICIJ Offshore Leaks dataset, our goal is to uncover patterns and drivers of offshore wealth flows and movement. We want to undestand how entity type (LLC, LTD, foundations, charities, etc.) varies across jurisdiction, analyze the changes in popularity of specific jurisdictions over time and assess how these shifts may be influenced by laws and/or enforcement trends, and map regional concentrations of offshore leaks activity to better understand how certain countries or territories facilitate financial secrecy. 

We then will visualize these trends using a heat map time series that tracks the physical locations of entities and their jurisdictions over time. This visualization will use incorporation_date_start and inactivation_date_start to animate the rise and decline of offshore registrations in different regions, with each category shown in distinct colors

**Data:**

Our cleaned and merged dataset is stored in the cloud and can be accessed here: https://drive.google.com/drive/folders/1nqny_5WbX_T3PfL-px_pQ9luz-3PQCUN?usp=drive_link

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

Identify the Top 10 countries where entities are physically located (based on the address country).

Identify the Top 10 jurisdictions where entities are incorporated.

Visualize these using a bar chart with a gradient color scheme:

Blue: Top 10 physical locations

Orange: Top 10 jurisdictions

**Planned Visualization**

A heat map time series visualization that maps:

The physical locations of entities (country_end)

The jurisdictions of incorporation (jurisdiction_start)

Using incorporation_date_start and inactivation_date_start to animate the temporal dynamics of offshore activity

We will supplement this analysis with external research to better understand the legal and political reasons why certain jurisdictions dominate offshore registrations, all the data is stored in a Google Drive folder 

