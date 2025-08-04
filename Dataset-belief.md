# Dataset Description

On Eedi, students answer Diagnostic Questions (DQs), which are multiple-choice questions featuring one correct answer and three incorrect answers, known as distractors. After responding with a multiple-choice selection, students were sometimes asked to provide a written explanation justifying their selected answer. These explanations are the primary focus of the MAP dataset and are to be used to identify and address potential misconceptions in students’ reasoning.

The goal of the competition is to develop a model that performs 3 steps:

Determines whether the selected answer is correct. (True or False in Category; e.g., True_Correct)
Assesses whether the explanation contains a misconception. (Correct, Misconception, or Neither in Category; e.g., True_Correct)
Identifies the specific misconception present, if any.
The Diagnostic Questions were presented in image format on the Eedi platform. All question content, including mathematical expressions, has been extracted via a human-in-the-loop OCR process to ensure accuracy.
 
 
 ---------------------
Files
[train/test].csv

QuestionId - Unique question identifier.
QuestionText - The text of the question.
MC_Answer - The multiple-choice answer the student selected.
StudentExplanation - A student's explanation for choosing a specific multiple-choice answer.
Category - [train only] A classification of the relationship between a student's multiple-choice answer and their explanation (e.g., True_Misconception, which indicates a correct multiple-choice answer selection accompanied by an explanation that reveals a misconception).
Misconception - [train only] The math misconception identified in the student's explanation for answers. Only applicable when Category contains a misconception, otherwise is 'NA'.
sample_submission.csv - A submission file in the correct format.

Category:Misconception - The predicted classification Category concatenated with the Misconception by a colon (:). Up to three predictions can be made, separated by a space.
The re-run test data contains approximately 16,000 rows.