# MAP - Charting Student Math Misunderstandings
### Predict the affinity between misconceptions and student open-ended respons


link: <https://www.kaggle.com/competitions/map-charting-student-math-misunderstandings/overview>

# Overview

Overview
In this competition, you’ll develop an NLP model driven by ML to accurately predict students’ potential math misconceptions based on student explanations in open-ended responses. This solution will suggest candidate misconceptions for these explanations, making it easier for teachers to identify and address students’ incorrect thinking, which is critical to improving student math learning.

Start

24 days ago
Close
2 months to go
Merger & Entry
Description
Students are often asked to explain their mathematical reasoning. These explanations provide rich insight into student thinking and often reveal underlying misconceptions (systematic incorrect ways of thinking).

For example, students often think 0.355 is larger than 0.8 because they incorrectly apply their knowledge of whole numbers to decimals, reasoning that 355 is greater than 8. Students develop a range of misconceptions in math, sometimes because they incorrectly apply prior knowledge to new content and sometimes because they are trying to make sense of new information but misunderstand it. To read more about these definitions and framework, please see the linked report here.This competition aims to explore such possibilities by encouraging participants to develop models that can distinguish between these types of conceptual errors in students’ responses, paving the way for improved feedback and better learning outcomes.

Tagging students’ explanations as containing potential misconceptions is valuable for diagnostic feedback but is time-consuming and challenging to scale. Misconceptions can be subtle, vary in specificity, and evolve as new patterns in student reasoning emerge.
Initial efforts to use pre-trained language models have not been successful, likely due to the complexity of the mathematical content in the questions. Therefore, a more efficient and consistent approach is needed to streamline the tagging process and enhance the overall quality.

The MAP (Misconception Annotation Project) competition challenges you to develop a Natural Language Processing (NLP) model driven by Machine Learning (ML) that predicts students’ potential math misconceptions based on student explanations. The goal is to create a model that identifies potential math misconceptions that generalize across different problems.
Your work could help improve the understanding and management of misconceptions, enhancing the educational experience for both students and teachers.

Vanderbilt University and The Learning Agency have partnered with Kaggle to host this competition.

Acknowledgments
Vanderbilt University and The Learning Agency would like to thank the Gates Foundation and the Walton Family Foundation for their support in making this work possible, as well as Eedi for providing the data. Eedi is an edtech platform that helps students ages 9 to 16 master math by identifying and resolving misconceptions using diagnostic questions, AI-powered insights, and access to live one-on-one tutoring to boost understanding and confidence.

Walton Logo

Evaluation
Submissions are evaluated according to the Mean Average Precision @ 3 (MAP@3):


where 
 is the number of observations, 
 is the precision at cutoff 
, 
 is the number predictions submitted per observation, and 
 is an indicator function equaling 1 if the item at rank 
 is a relevant (correct) label, zero otherwise.

Once a correct label has been scored for an observation, that label is no longer considered relevant for that observation, and additional predictions of that label are skipped in the calculation. For example, if the correct label is A for an observation, the following predictions all score an average precision of 1.0.

[A, B, C, D, E]
[A, A, A, A, A]
[A, B, A, C, A]
There is only one correct label per observation (hence no divisor term in front of the inner summation.)

Submission File
For each row_id in the test set, you must predict the corresponding Category and Misconception, concatenated with a colon (:). You can predict up to 3 Category:Misconception values per row (any predictions beyond the third are ignored), and the predictions should be space-delimited. The file should contain a header and have the following format:

row_id,Category:Misconception
36696,True_Correct:NA False_Neither:NA False_Misconception:Incomplete
36697,True_Correct:NA False_Neither:NA False_Misconception:Incomplete
36698,True_Correct:NA False_Neither:NA False_Misconception:Incomplete
etc.
...
Timeline
July 10, 2025 - Start Date.

October 8, 2025 - Entry Deadline. You must accept the competition rules before this date in order to compete.

October 8, 2025 - Team Merger Deadline. This is the last day participants may join or merge teams.

October 15, 2025 - Final Submission Deadline.

All deadlines are at 11:59 PM UTC on the corresponding day unless otherwise noted. The competition organizers reserve the right to update the contest timeline if they deem it necessary.

Prizes
Leaderboard Prizes
1st Place - $ 20,000
2nd Place - $ 12,000
3rd Place - $ 8,000
4th Place - $ 5,000
5th Place - $ 5,000
6th Place - $ 5,000
Code Requirements

---------------------------------------------
This is a Code Competition
Submissions to this competition must be made through Notebooks. In order for the "Submit" button to be active after a commit, the following conditions must be met:

CPU Notebook <= 9 hours run-time
GPU Notebook <= 9 hours run-time
Internet access disabled
Freely & publicly available external data is allowed, including pre-trained models
Submission file must be named submission.csv
Please see the Code Competition FAQ for more information on how to submit. And review the code debugging doc if you are encountering submission errors.

----------------------
Citation
Jules King, Kennedy Smith, L Burleigh, Scott Crossley, Maggie Demkin, and Walter Reade. MAP - Charting Student Math Misunderstandings. https://kaggle.com/competitions/map-charting-student-math-misunderstandings, 2025. Kaggle.