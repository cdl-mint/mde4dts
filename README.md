This repository contains all data created for our systematic mapping study entitled "Model-Driven Engineering for Digital Twins: A Systematic Mapping Study", which is currently under review.
In the following, we describe the individual steps of the procedure performed to obtain the results for this study, and provide links to the relevant files for each step.

# Step 1: Keyword-based search
First, we performed a keyword-based search in different literature databases using the conceptual search string 
```"Digital Twin*" AND (Model-Driven) OR "MODEL DRIVEN"```
Details on the specifics of executing this search query in the different search engines of the selected literature databases are given in the file [01 Documentation of Search.md](./01%20Documentation%20of%20Search.md). The resulting publications for each individual database are available in the folder [01 raw data](./01%20raw%20data/).

The results of this keyword-based search (paper titles and metadata) are available in the file [01 Search Results.csv](./01%20Search%20Results.csv)
We already excluded duplicates and papers that were not written in english in this initial step. The papers that remained after exclusion were forwarded to Step 2.

# Step 2: Screening of papers
Each paper in this initial corpus of search results was screened by at least two authors. This screening included reading of the title, abstract, and further metadata collected in Step 1. If both authors agreed on a reason for exclusion, the paper was excluded. Otherwise, it was forwarded to the next step. The results of this screening step are collected in the file [02 screening results.xlsx](./02%20screening%20results.xlsx).
**Description of file contents:** In this file, the sheet "Exclusion Results" summarizes the screening results. 
- The first column "Document Title" contains the paper title
- This column is followed by 5 columns that incidate for each inclusion criterium stated in our survey whether the respective paper satisfies this inclusion criterium ("yes" in the respective column) or not ("not" in the respective column). If one inclusion criterium is not satisfied, the others are not considered any more (marked with "N/A), as the paper already has to be excluded. 
- In Column F, we also specify whether an exclusion criterium applies to a given paper. In this case, the name of this exclusion criterion is stated in the respective cell. If no exclusion criterium applies, the respective cell for a paper contains the text "no". If a paper does not satisfy all inclusion criteria, the respective cell in Column F states "N/A", as the paper is already excluded before the exclusion criteria are checked. 
- In Column G, we specify whether a paper is forwarded to Step 3 because all inclusion criteria apply, and no exclusion criterium applies (marked with "OK" in the respective cell), or the paper has to be excluded in Step 2 (marked with "NOK" in the respective cell).

The further sheets of this file "Review 1" and "Review 2" detail results of the independently executed reviews for each paper. Review 1 was performed by the first author of this survey, Daniel Lehner. For review 2, the papers were split across multiple other authros. The author that performed a review for a particular paper is thereby indicated in column A of the sheet "Review 2" (JZ = Jingxi Zhang, JP = Jérôme Pfeiffer, AS = Ann-Kathrin Splettstößer, S = Sabine Sint)

# Step 3: Detailed reviewing of papers
In a next step, each of the remaining papers was read in detail by three authors to identify whether one of the exclusion criteria applied after reading the full paper. Afterwards, a multi-layer discussion process was performed to reach an agreement among all authors on which papers to exclude in this step. This process is documented in detail in the paper. The results of this detailed reviewing step are collected in the file [03 detailed reviewing results.xlsx](./03%20detailed%20reviewing%20results.xlsx).
**Description of file contents:** This file contains the sheet "Reviewing Results", with the information for each paper summarized in a dedicated row. 
- To identify a paper, the first column of each row provides the paper title. 
- In the following 4 columns, the Decision on this paper for each Reviewer (JP = Jérôme Pfeiffer, DL = Daniel Lehner, JZ = Jingxi Zhang, AS = Ann-Kathrin Splettstößer) is collected ("OK" if paper should be considered for the next step, or a reason for exclusion, according to the exclusion criteria described in the paper). If a reviewer was not assigned for a particular paper, the respective field is empty.
- The consolidated decision that was reached after executing the agreement procedure described in the paper is collected Columns F-J. Columns F-I indicate for all inclusion criteria whether they are met (marked with "yes" in the respective cell) or not (marked with "no" in the respective cell). If an exclusion criterium applies to a given paper, the name of this criterium is explicitly stated in Column J. If no exclusion criterium applies, this is marked with a "no" in Column J. 
- Column K specifies the initial decision for a paper reached based on the data collected In Columns F-J. If a paper satisfies all inclusion criteria, and no exclusion criterium applies, the respective cell is marked as "OK". If at least one inclusion criterium is not met, or at least one exclusion criterium applies, the paper is marked as "NOK" in the respective column.
- This initial decision was reviewed by all authors that were not involved in the initial detailed reviewing process. If one of the authors gave a veto on the initial decision of a paper, this veto is marked with "X" in Column L.
- If at least one author gave an initial decision of a paper, this paper was discussed in detail among all authors to reach a mutual decision. The final decision after this additional discussion process is collected in Column M. 
- For all papers that are included in our study (marked with "OK" in Column M), a unique ID was assigned in Column N.



# Step 4: Data extraction
Each paper included in our study was read by three authors to extract all relevant data. The results for individual authors for each paper are collected, discussed and finally consolidated, which was used to present the results of our study in the paper, is available in the file [04 extraction consolidation results.xlsx](./04%20extraction%20consolidation%20results.xlsx)
**Description of file contents:** The file contains the sheet "extraction consolidation result" with the information on the individual papers, whereby the first three columns include id, reference paper (correlates to MDE4DT-Papers Section) and title to identify the papers. Then, the information such as automation technique, model category, and system life cycle phase is listed according to the RQs of our paper. **Papers that contain more details regarding one column are described in several rows  (e.g., if one paper contains applications of several automation techniques, we create a dedicated row for each automation technique), which led to a total of 134 data points for the 66 included papers**

# Step 5: Snowballing
We performed forward and backward snowballing on the remaining papers to obtain the full set of relevant papers. The used code + extracted data is available in the folder [Snowballing](./snowballing/). A detailed description of the procedure followed for this snowballing step is also available in the [respective readme.md file of this folder](./snowballing/readme.md).
One paper that was included in our full set of relevant papers based on this snowballing procedure. We extracted all relevant data from this paper, as described in Setp 4. The collected data is available in the file [05 snowballing extraction results.xlsx](./05%20snowballing%20extraction%20results.xlsx).


# Data preparation and visualization
All automation scripts scripts that were used to create the visualizations shown in the paper based on the extracted data are collected in the folder [/scripts](./scripts).
To merge the consolidated extraction data with the paper metadata collected in step 1, we used the code in the file [extraction_data_preparation.ipynb](./scripts/extraction_data_preparation.ipynb), which stored the merged data in json format in the folder [/scripts/data](./scripts/data/).
This json file was then used by the code collected in the file [scatterplots.ipynb](./scripts/scatterplots.ipynb) to create the scatterplots. The barcharts were created directly based on the extracted data, using the code available in the file [barcharts.ipynb](./scripts/barcharts.ipynb). Both barcharts and scatterplots are available in the folder [./scripts/target/img](./scripts/target/img/) and its sub-folders. The folder [./scripts/data](./scripts/data/) contains temporary files that are consumed or produced by these automation scripts.
