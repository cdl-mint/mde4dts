This folder contains relevant data for the snowballing step (step 4) performed as part of the systematic mapping study described in this repository. In the following, each sub-step performed for executing the snowballing is described in more detail:

# 4.1: Get Titles
We performed backward and forward snowballing for all identified papers, extracting the title of each found paper. We only included papers, and disregarded other types of references, such as hyperlinks to specific websites. The resulting list of papers can be found in the file [41_snowballing_titles.csv](./41_snowballing_titles.csv)

# 4.2: Get Metadata for Titles
To extract metadata for all identified titles, we used a python API provided by Scopus. In the Jupyter Notebook provided in this repository ([file 42_get_metadata](./42_get_metadata.ipynb)), we provide the code that we used to (i) retrieve the scopus ID for each title, (ii) persist the id as part of the file [42_scopus_ids.csv](./42_scopus_ids.csv), and (iii) query for the metadata of all papers using these IDs in the scopus API, and persisting the results in the file [42_snowballing_metadata_all.csv](./42_snowballing_metadata_all.csv). Note: The resulting list of papers with metadata ([42_snowballing_metadata_all.csv](./42_snowballing_metadata_all.csv)) is smaller than the initial set of snowballing titles ([41_snowballing_titles.csv](./41_snowballing_titles.csv)), as this initial set contained multiple duplicate entries (e.g., papers that were referenced by multiple papers from our data set retrieved in Step 3 of the seach procedure).

# 4.3: Apply Search Criteria
In the set of papers + metadata retrieved in Step 4.2, we automatically applied the search string from our initial search, as described in the paper. We also try to automatically eliminate papers that are already available in the initial set of papers retrieved from the keywords-based search. The respective code is available in the [file 43_apply_search_criteria](./43_apply_search_criteria.ipynb), and the resulting set of papers is found in [43_snowballindg_metadata_reduced.csv](./43_snowballing_metadata_reduced.csv)

# 4.4: Manually reduce papers