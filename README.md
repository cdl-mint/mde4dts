This repository contains all data created for our systematic mapping study entitled "Model-Driven Engineering for Digital Twins: A Systematic Mapping Study", which is currently under review.
In the following, we describe the individual steps of the procedure performed to obtain the results for this study, and provide links to the relevant files for each step.

# 1. Keyword-based search
First, we performed a keyword-based search in different literature databases using the conceptual search string 
"Digital Twin*" AND (Model-Driven) OR "MODEL DRIVEN
Details on the specifics of executing this search query in the different search engines of the selected literature databases are given in the file [00 Documentation of Search.md](./00%20Search%20Results.csv)

The results of this keyword-based search (paper titles and metadata) are available in the file [00 Search Results.csv](./00%20Search%20Results.csv)
This file contains xx duplicates, as well as yy papers which were not written in English or not peer-reviewed. We already excluded these papers in this initial step. The papers that remained after exclusion were forwarded to Step 2.

# 2. Screening of papers
Each paper in this initial corpus of search results was screened by at least two authors. This screening included reading of the title, abstract, and further metadata collected in step 1. If both authors agreed on a reason for exclusion, the paper was excluded. Otherwise, it was forwarded to the next step. The results of this screening step are collected in the file [01 screening results.xlsx](./01%20screening%20results.xlsx).
**Description of file contents:** In this file, the sheet "Exclusion Results" summarizes the screening results. The first column "Document Title" contains the paper title, followed by the column "Decision" indicating the result for this paper after the screening process ("OK" for inclusion of the paper in the next step, or a reason for exclusion according to the exclusion criteria described in the paper). The following columns detail the screening results + comments of the individual reviewers, followed by meta-data of the paper. Whereas the first author who reviewed all papers directly put his notes into this sheet, other authors used a dedicated sheet ("Review 2") to ensure double-blind reviewing, also detailing the person who actually performed the review (DL = Daniel Lehner, JZ = Jingxi Zhang, JP = Jérôme Pfeiffer, AS = Ann-Kathrin Splettstößer, S = Sabine Sint). The reviewing result of reviewer 2 in the sheet "Exclusion Results" contains a forward reference to this information.

# 3. Detailed reviewing of papers
In a next step, each of the remaining papers was read in detail by three authors to identify whether one of the exclusion criteria applied after reading the full paper. Afterwards, a multi-layer discussion process was performed to reach an agreement among all authors on which papers to exclude in this step. This process is documented in detail in the paper. The results of this detailed reviewing step are collected in the file [02 detailed reviewing results.xlsx](./02%20detailed%20reviewing%20results.xlsx).
**Description of file contents:** This file contains the sheet "Reviewing Results", with the information for each paper summarized in a dedicated row. To identify a paper, the first column of each row provides the paper title. In the following columns, the Decision on this paper for each Reviewer (JP = Jérôme Pfeiffer, DL = Daniel Lehner, JZ = Jingxi Zhang, AS = Ann-Kathrin Splettstößer) is collected ("OK" if paper should be considered for the next step, or a reason for exclusion, according to the exclusion criteria described in the paper). If a reviewer was not assigned for a particular paper, the respective field is empty. The distribution of papers among reviewers is found in the sheet "Paper Assignment". The consolidated decision that was reached after executing the agreement procedure described in the paper is collected in the column "Decision". All these decisions were then again reviewed by the authors of this paper who were not part of the preceding exclusion process. Each author had the option to give a Veto on any decision, which triggered another round of discussion among all authors for this particular paper. Each veto is marked with an "X" in the column "Veto?", followed by the final decision that was agreed on among all authors after another round of discussion, in the column "Decision after Veto".

# 4. Snowballing
We performed forward and backward snowballing on the remaining papers to obtain the full set of relevant papers. The used code + extracted data is available in the folder [Snowballing](./snowballing/). A detailed description of the procedure followed for this snowballing step is also available in the [respective readme.md file of this folder](-/snowballing/readme.md)


# 5. Data extraction
Each paper in this full set of relevant papers was read by three authors to extract all relevant data. The results for individual authors for each paper are collected in the file [03 extraction results.xlsx](./03%20extraction%20results.xlsx). The collected data was afterwards consolidated among the authors for each paper. The consolidated data, which was used to present the results of our study in the paper, is available in the file [04 extraction consolidation results.xlsx](./04%20extraction%20consolidation%20results.xlsx)
**Description of file contents: TODO Sabine - bitte hier beschreiben, nachdem du das file angepasst hast!** 

# Data preparation and visualization
To merge the consolidated extraction data with the paper metadata collected in step 1, we used the code in the file [extraction_data_preparation.ipynb](./extraction_data_preparation.ipynb), which stored the merged data in json format in the folder [/target/json](./target/json/).
This json file was then used by the code collected in the file [visualizations.ipynb](./visualizations_Jingxi_2.ipynb) to create the visualizations of the raw data which are available in the folder [/target/img](./target/img/) and its sub-folders. The folder [/data](./data/) contains temporary files that are consumed or produced by these automation scripts.
