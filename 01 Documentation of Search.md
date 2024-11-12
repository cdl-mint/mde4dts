# IEEE Xplore

73 Search Results by performing the following procedure on September 1st 2024 (available in file [/01 raw data/IEEE.csv](/01%20raw%20data/IEEE.csv)):

1. Go to https://ieeexplore.ieee.org/Xplore/home.jsp
2. Enter the following String in the search field and press enter:
```
(("Document Title": "Digital Twin" OR "Abstract": "Digital Twin" OR "Author Keywords": "Digital Twin" OR "Publication Title": "Digital Twin") 
OR
("Document Title": "Digital Twins" OR "Abstract": "Digital Twins" OR "Author Keywords": "Digital Twins" OR "Publication Title": "Digital Twins") 
)
AND
(("Document Title": "Model-Driven" OR "Abstract": "Model-Driven" OR "Author Keywords": "Model-Driven" OR "Publication Title": "Model-Driven") 
OR
("Document Title": "Model Driven" OR "Abstract": "Model Driven" OR "Author Keywords": "Model Driven" OR "Publication Title": "Model Driven") )
```
3. In the following window, select "Conferences, Journals, Magazines" and click "Apply"
![Screenshot of the publication type selection in IEEE Xplore](./pics/search_ieee_types.PNG)
4. In the left menu bar, select the "Range" option in the "Year" area and enter "empty" to "2023" as range (the website will automatically replace the empty value with "2018"). Also select search for "Documents" and "Show All Results" perform no other selections in this menubar.
![Screenshot of the year selection in IEEE Xplore](./pics/search_ieee_config.PNG)

# ACM
50 Search Results by performing the following procedure on September 1st 2024 (available in file [/01 raw data/acm.csv](/01%20raw%20data/acm.csv)):

> [!CAUTION]
> **Note:** When executing this search for ACM again on November 12th 2024, we realized that the results changed due to a very recent update of the database, from 50 to 64. However, when crosschecking these new results with our initial search from September 1st, we found that the additional papers were already included in our corpus through IEEE and Web of Science.

1. Go to https://dl.acm.org/
2. Enter the following String in the search field and press "Enter":
```
(
Title:("digital twin" OR "digital twins") 
OR ContentGroupTitle:("digital twin" OR "digital twins") 
OR Abstract: ("digital twin" OR "digital twins")
OR Keyword:("digital twin" OR "digital twins")
)
AND
(
Title:("model driven" OR "model-driven") 
OR ContentGroupTitle:("model driven" OR "model-driven") 
OR Abstract:("model driven" OR "model-driven") 
OR Keyword:("model driven" OR "model-driven")
)
```
3. Make sure that the selected database is "The ACM Guide to Computing Literature", as indicated in the screenshot below
4. In the Sidebar to the left, reduce the years to "2018-2023"

**The following screenshot shows the final configuration:**

![Screenshot of ACM search configuration](./pics/search_acm.PNG)

# Web of Science
*Note: the selected databases for web of science are based on the subscription of the author's universities. Unfortunately, search results also depend on the specific subscription to the WoS Core Collection database, which is different for individual universities. For example, for the subscription provided by the "Consortium of Austrian University Libraries" provided by the Johannes Kepler University, we retrieved 118 search results. For the Subscription provided by the "University of Stuttgart", we retrieved 122 publications.*

122 Search Results by performing the following procedure on September 1st 2024 (available in file [/01 raw data/WoS.xls](/01%20raw%20data/WoS.xls)): 
1. go to https://www.webofscience.com/wos/woscc/advanced-search
2. login if required
3. Select "All Databases" for the "Search in" option and "All" for the "Collections" option. Based on the subscriptions of the authors' universities, this includes the following databases: Web of Science Core Collection, Grants Index, KCI-Korean Journal Database, MEDLINE, Preprint Citation Index, ProQuest Dissertations & Theses Citation Index, SciELO Citation Index
![Screenshot of available Web of Science databases](./pics/search_wos_dbs.PNG)
4. In the textfield that says "Enter or edit your query here.", enter the following string:
```
(
    (TS=("Digital Twin") OR TI=("Digital Twin") OR SO=("Digital Twin") OR AB=("Digital Twin") OR CF=("Digital Twin") OR AK=("Digital Twin"))
    OR
    (TS=("Digital Twins") OR TI=("Digital Twins") OR SO=("Digital Twins") OR AB=("Digital Twins") OR CF=("Digital Twins") OR AK=("Digital Twins"))
)AND (
    (TS=("Model Driven") OR TI=("Model Driven") OR SO=("Model Driven") OR AB=("Model Driven") OR CF=("Model Driven") OR AK=("Model Driven"))
    OR
    (TS=("Model-Driven") OR TI=("Model-Driven") OR SO=("Model-Driven") OR AB=("Model-Driven") OR CF=("Model-Driven") OR AK=("Model-Driven"))
)
```
5. Click the "Add Date Range" option, and select "Custom" in the "Publication Date" dropdown.
6. Enter 1900-01-01 and 2023-12-31 as date range.

**The following screenshot shows the final configuration:**

![Screenshot of Web of Science search configuration](./pics/search_wos.PNG)

# Scopus
182 Search Results by performing the following procedure on September 1st 2024 (available in file [/01 raw data/scopus.csv](/01%20raw%20data/SCOPUS.csv)): 
1. Go to https://www.scopus.com/search/form.uri?display=advanced
2. Enter the following String in the "Enter Search String" field:
```
( SRCTITLE ( "Digital Twin" ) OR TITLE-ABS-KEY ( "Digital Twin" ) OR SRCTITLE ( "Digital Twins" ) OR TITLE-ABS-KEY ( "Digital Twins" ) ) 
AND ( SRCTITLE ( "Model Driven" ) OR TITLE-ABS-KEY ( "Model Driven" ) OR SRCTITLE ( Model-Driven ) OR TITLE-ABS-KEY ( Model-Driven ) ) 
AND PUBYEAR < 2024
```
