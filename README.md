This repository contains all data created for our systematic mapping study entitled "Model-Driven Engineering for Digital Twins: A Systematic Mapping Study", which is currently under review.
In the following, we describe the individual steps of the procedure performed to obtain the results for this study, and provide links to the relevant files for each step.

# 1. Keyword-based search
First, we performed a keyword-based search in different literature databases. The results of this keyword-based search (paper titles and metadata) are available in the file [00 Search Results.csv](./00%20Search%20Results.csv)

# 2. Screening of papers
Each paper in this initial corpus of search results was screened by at least two authors. This screening included reading of the title, abstract, and further metadata collected in step 1. If both authors agreed on a reason for exclusion, the paper was excluded. Otherwise, it was forwarded to the next step. The results of this screening step are collected in the file [01 screening results.xlsx](./01%20screening%20results.xlsx)

# 3. Detailed reviewing of papers
In a next step, each of the remaining papers was read in detail by three authors to identify whether one of the exclusion criteria applied after reading the full paper. Afterwards, a multi-layer discussion process was performed to reach an agreement among all authors on which papers to exclude in this step. This process is documented in detail in the paper. The results of this detailed reviewing step are collected in the file [02 detailed reviewing results.xlsx](./02%20detailed%20reviewing%20results.xlsx).

# 4. Snowballing
We performed forward and backward snowballing on the remaining papers to obtain the full set of relevant papers. The used code + extracted data is available in the folder [Snowballing](./snowballing/).


# 5. Data extraction
Each paper in this full set of relevant papers was read by three authors to extract all relevant data. The results for individual authors for each paper are collected in the file [03 extraction results.xlsx](./03%20extraction%20results.xlsx). The collected data was afterwards consolidated among the authors for each paper. The consolidated data, which was used to present the results of our study in the paper, is available in the file [04 extraction consolidation results.xlsx](./04%20extraction%20consolidation%20results.xlsx)

# Data preparation and visualization
To merge the consolidated extraction data with the paper metadata collected in step 1, we used the code in the file [extraction_data_preparation.ipynb](./extraction_data_preparation.ipynb), which stored the merged data in json format in the folder [/target/json](./target/json/).
This json file was then used by the code collected in the file [visualizations.ipynb](./visualizations_Jingxi_2.ipynb) to create the visualizations of the raw data which are available in the folder [/target/img](./target/img/) and its sub-folders. The folder [/data](./data/) contains temporary files that are consumed or produced by these automation scripts.