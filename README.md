This repository includes the dataset, and the data analysis code accompanying the submitted paper, titled:
**Characterizing Usability Issue Discussions in Open Source Software Projects.**


**The dataset**

The purpose of these artifacts is to identify the impacts of usability and its heuristics for user interface design (10 Nielsen Heuristics) in issue discussions of five popular OSS projects hosted on GitHub: three data science notebook projects (Jupyter Lab, Google Colab, and CoCalc) and two code editor projects (VSCode and Atom) GitHub repositories.

First, we manually labeled sampled data and identified usability issues from non-usability issues. Then, we investigated the type of usability aspect targeted in each usability issue based on ten well-known Nielsen heuristics. In this regard, we have following main dataset:

- The "AllSampledProjectLabeldeddata_English_Feature_Agreed.csv" file contains information (including  Agree usability, Agree Nielsen heuristic, reporting issues with visual support, number of reactions to the report, sentiment, tone (Dominant tone), discussion length, number of participants, time to first comment, time to last comment, time to close the issue, and the metadata) of all the sampled labelled data of the five mentioned repositories.

To answer RQ1, we focus on Topic modeling on all issue data collected from the five open source projects. We gathered the following datasets to answer RQ1:
 
- The "NotebookProjectsdata_English.csv" file contains filtered English data points of data science notebook projects (including detected language for title and body with the help of Google translator API preprocessed title and body as issue content, and the metadata) 
- The "CodeEditorProjectsdata_English.csv" file contains filtered English data points of code editor projects (including detected language for title and body with the help of Google translator API preprocessed title and body as issue content, and the metadata)

To answer RQ3, we did research to characterize usability issues with the help of different features such as 1) reporting issues with visual support, 2) number of reactions to the report, 3) sentiment of issue post, 4) tone of issue post, 5) discussion length, 6) the number of participants in each discussion, 7) the time to the first comment, 8) the time to the last comment, and 9) the time to close an issue. We gathered the following datasets to answer RQ3:

- The "All_Data_RQ3.csv" file contains prepared data after calculating timestamps, tone and sentiment aggregation for statistic analysis to answer RQ3 (including  Agree usability, Agree Nielsen heuristic, reporting issues with visual support, number of reactions to the report, sentiment, tone (Dominant tone), discussion length, number of participants, time to the first comment, time to last comment, and time to close issue, and the metadata) of all the sampled labeled data of the five mentioned repositories.
- The "NotebookProjects_Data_RQ3.csv" file contains prepared data science notebooks labeled data for statistic analysis to address RQ3.
- The "CodeEditorProjects_Data_RQ3.csv" file contains prepared code editor labeled data for statistic analysis to address RQ3.

To address RQ4, we need to unify users and find the role of issue posters (if the issue poster only posted usability issues, none usability, or both). We gathered the following datasets to answer RQ4:

- The "All_Data_RQ4.csv" file contains prepared data science notebooks labeled data for statistic analysis to address RQ4 (including a number of posted issues, number of posted comments, number of years on GitHub, number of repositories owned, user’s role in the project, and the metadata).
- The "NotebookProjects_Data_RQ4.csv" file contains prepared data science notebooks labeled data for statistic analysis to address RQ4.
- The "CodeEditorProjects_Data_RQ4.csv" file contains prepared code editor projects labeled data for statistic analysis to address RQ4.

**The analysis code**
- The "Topic_Modeling_RQ1_NotebookProjects.ipynb" and "Topic_Modeling_RQ1_CodeEditorProjects.ipynb" files are the Python code to investigate Topic Modeling (LDA) to cluster and distinguish the list of topics in the entire dataset of the selected projects in two different categories (three data science notebook projects and two code editor projects)
- The "Statistical Analysis-RQ3.ipynb" file is the Python code for analyzing the gathered data to indicate the impact of usability and Nielsen heuristics on characteristics of usability issues.
- The "Statistical Analysis-RQ4.ipynb" file is the Python code for analyzing the gathered data to indicate the impact of usability issue posters.
- The "Statistical Analysis-RQ3-RQ4_Chi-Squared-and-Post-hoc-test.r" file is the R code for running Chi-squared and Post hoc test to address RQ3 and RQ4.
