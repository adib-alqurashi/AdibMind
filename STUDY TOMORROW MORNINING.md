# Topic 7 Practice Exam: Basic Classification Methods

DATA 211. **Part A:** 24 MCQ on concepts. **Part B:** written questions on one dataset, from easy to hard, with the decision tree last.

Each answer is folded under its question. Click it to open.

---

## Part A: MCQ

**1.** How does this course place machine learning (ML), AI and data science?
- (a) AI is a subset of ML
- (b) ML is a subset of AI, used here as an application of data-science skills
- (c) Data science is a subset of ML
- (d) All three mean the same thing

> [!success]- Answer
> **(b)** ML is a subset of AI, and the course treats ML as an application of data-science skills.

**2.** In a classification dataset, the column you want to predict is called the…
- (a) feature
- (b) predictor
- (c) label (target)
- (d) attribute

> [!success]- Answer
> **(c)** The label, also called the target or class, is what you predict.

**3.** Which group contains only other names for features?
- (a) attributes, predictors, independent variables
- (b) target, class, output
- (c) predictors, target, input
- (d) class, attribute, dependent variable

> [!success]- Answer
> **(a)** Target, class and output are names for the label.

**4.** A bank has past loan records marked "repaid" or "defaulted" and wants to predict this for new applicants. What kind of task is this?
- (a) Supervised classification
- (b) Supervised regression
- (c) Unsupervised clustering
- (d) Reinforcement learning

> [!success]- Answer
> **(a)** The past outcomes are known (supervised), and the outcome is a category (classification).

**5.** Which of these is a regression task?
- (a) Predicting tomorrow's temperature in °C
- (b) Deciding whether an email is spam
- (c) Predicting the iris species
- (d) Grouping customers with no labels

> [!success]- Answer
> **(a)** A temperature is a number, so this is regression.

**6.** A factory only has data from machines working normally and wants to flag unusual behaviour. What type of problem is this?
- (a) Binary
- (b) Multi-class
- (c) One-class
- (d) Regression

> [!success]- Answer
> **(c)** Only the normal class is known, so this is one-class classification.

**7.** Which of these is a multi-class problem?
- (a) Balloon inflated: T / F
- (b) Student result: pass / fail
- (c) Letter grade: A / B / C / D
- (d) Transaction: fraud / normal

> [!success]- Answer
> **(c)** It has 4 classes. The others have only 2.

**8.** Labels are stored as 1 = setosa, 2 = versicolor, 3 = virginica. Which statement is valid?
- (a) Class 2 is twice class 1
- (b) An average label of 2.1 means "mostly versicolor"
- (c) Renaming them A / B / C changes no information
- (d) The task becomes regression because the labels are numbers

> [!success]- Answer
> **(c)** Numbers used as labels are names, not quantities.

**9.** In model construction, the classification algorithm takes ___ and produces ___.
- (a) testing data, training data
- (b) training data, a classifier (model)
- (c) unseen data, a label column
- (d) a classifier, training data

> [!success]- Answer
> **(b)** Training data goes into the algorithm, and the result is the classifier.

**10.** Why is the testing data kept separate from the training data?
- (a) To make training faster
- (b) Because testing data has no labels
- (c) To estimate how the model will do on data it has not seen
- (d) To raise the training accuracy

> [!success]- Answer
> **(c)** Testing data estimates how the model performs on unseen data.

**11.** What is a false negative (FN)?
- (a) Predicted positive, actually negative
- (b) Predicted negative, actually positive: a miss
- (c) Predicted negative, actually negative
- (d) Predicted positive, actually positive

> [!success]- Answer
> **(b)** An FN is a miss. A false alarm (predicted positive, actually negative) is an FP.

**12.** In a dataset where 95% of records are negative, a model that always predicts "negative" will have…
- (a) low accuracy and high recall
- (b) high accuracy but zero recall
- (c) high precision and high recall
- (d) accuracy equal to recall

> [!success]- Answer
> **(b)** TN dominates accuracy, but $TP = 0$, so recall $= 0$.

**13.** Which question does precision answer?
- (a) Of all the actual positives, how many were found?
- (b) Of the cases predicted positive, how many really are positive?
- (c) What fraction of all predictions were correct?
- (d) How many negatives were predicted correctly?

> [!success]- Answer
> **(b)** $p = \frac{TP}{TP + FP}$. Option (a) describes recall.

**14.** A cancer screening test must miss as few sick patients as possible. Which measure matters most?
- (a) Precision
- (b) Recall
- (c) Accuracy
- (d) Error rate

> [!success]- Answer
> **(b)** Recall measures how many of the actually sick patients were caught.

**15.** Why does F1 use the harmonic mean instead of the ordinary average?
- (a) It is easier to calculate
- (b) It ignores false negatives
- (c) A low value pulls it down, so F1 is high only when both p and r are high
- (d) It always equals accuracy

> [!success]- Answer
> **(c)** The harmonic mean stays close to the smaller of the two values.

**16.** In a multi-class confusion matrix, how do you get precision for one class?
- (a) Divide the diagonal by the total
- (b) Treat that class as positive and all the others as negative (one-vs-rest)
- (c) Average all the rows
- (d) It can't be computed for more than 2 classes

> [!success]- Answer
> **(b)** One-vs-rest gives each class its own TP, FP and FN. Option (a) is accuracy.

**17.** The lecture's matrix has rows = predicted and columns = actual. What is different in scikit-learn's `confusion_matrix(y_true, y_pred)`?
- (a) Nothing, it is the same
- (b) Rows and columns are swapped: rows = actual, columns = predicted
- (c) It shows percentages instead of counts
- (d) It hides the diagonal

> [!success]- Answer
> **(b)** scikit-learn prints the transpose of the lecture's table.

**18.** With an unbalanced dataset, why use stratified sampling in the holdout method?
- (a) So the minority class appears in both the training and test sets
- (b) To make the test set larger
- (c) To remove outliers
- (d) So no test set is needed

> [!success]- Answer
> **(a)** Each class is sampled separately, so the minority class isn't lost.

**19.** What is the main advantage of k-fold cross-validation over random subsampling?
- (a) It trains only one model
- (b) Every record is tested exactly once, so the test sets never overlap
- (c) It does not need labels
- (d) It always uses 50% of the data for testing

> [!success]- Answer
> **(b)** In random subsampling the test sets can overlap. In k-fold they can't.

**20.** When does the basic decision-tree algorithm stop splitting?
- (a) After 3 levels
- (b) When there are no more attributes or no more instances
- (c) When the root's entropy equals 1
- (d) When accuracy reaches 100%

> [!success]- Answer
> **(b)** These are the two stopping rules from the lecture.

**21.** ID3 (Ross Quinlan) chooses as the split the attribute with the…
- (a) most distinct values
- (b) highest entropy after the split
- (c) highest information gain
- (d) first column in the table

> [!success]- Answer
> **(c)** The highest gain means the biggest drop in entropy.

**22.** A node where every record is "Yes" has entropy…
- (a) 0, and it becomes a leaf
- (b) 1, and it must be split
- (c) 0.5, and it must be split
- (d) undefined

> [!success]- Answer
> **(a)** A pure node has no uncertainty left, so its entropy is 0 and it becomes a leaf.

**23.** When is the entropy of a node highest?
- (a) When one class dominates
- (b) When all classes are equally mixed
- (c) When the node has few records
- (d) When it is a leaf

> [!success]- Answer
> **(b)** Entropy is highest when the result is the most random.

**24.** Which statement about the final decision tree is true?
- (a) Every leaf must be pure
- (b) Every attribute must appear on every path
- (c) Not every leaf has to be pure; splitting stops when the data can't be split further
- (d) The root is always the attribute with the most values

> [!success]- Answer
> **(c)** This is stated on the "Final Decision Tree" slide.

---

## Part B: Written

Use the following data for Q1–Q7 and Q10–Q16.

| Student | Attendance | StudyTime | Assignments | Pass |
| --- | --- | --- | --- | --- |
| S1 | High | High | Done | Yes |
| S2 | Low | Low | Missed | No |
| S3 | Low | Medium | Done | Yes |
| S4 | Low | Low | Missed | No |
| S5 | High | High | Done | Yes |
| S6 | High | Medium | Missed | No |
| S7 | Low | High | Missed | Yes |
| S8 | High | Low | Done | Yes |
| S9 | Low | Medium | Missed | No |
| S10 | High | Medium | Done | Yes |
| S11 | Low | Low | Done | No |
| S12 | High | High | Missed | Yes |
| S13 | Low | Low | Missed | No |
| S14 | Low | Medium | Done | Yes |

**Q1.** Identify the features and the label.

> [!success]- Answer
> The features are Attendance, StudyTime and Assignments. The label is Pass.

**Q2.** Is this a classification or a regression problem? Is it binary or multi-class?

> [!success]- Answer
> It is classification, because the label is a category. It is binary, because there are 2 classes: Yes and No.

**Q3.** A model uses the rule: IF Assignments = Done THEN Pass = Yes ELSE Pass = No. Build the confusion matrix, with positive = Yes.

> [!success]- Answer
> Predictions: Done gives Yes and Missed gives No.
> - TP: S1, S3, S5, S8, S10, S14
> - TN: S2, S4, S6, S9, S13
> - FP: S11 (Done, but failed)
> - FN: S7, S12 (Missed, but passed)
>
> |  | Actual Yes | Actual No |
> | --- | --- | --- |
> | **Predicted Yes** | TP = 6 | FP = 1 |
> | **Predicted No** | FN = 2 | TN = 5 |

**Q4.** Compute the accuracy and the error rate.

> [!success]- Answer
> $$\text{Accuracy} = \frac{TP + TN}{\text{total}} = \frac{6 + 5}{14} = 0.786$$
> $$\text{Error rate} = 1 - 0.786 = 0.214$$

**Q5.** Compute the precision and the recall.

> [!success]- Answer
> $$p = \frac{TP}{TP + FP} = \frac{6}{7} = 0.857 \qquad r = \frac{TP}{TP + FN} = \frac{6}{8} = 0.750$$

**Q6.** Compute the F1-measure.

> [!success]- Answer
> $$F_1 = \frac{2pr}{p + r} = \frac{2(0.857)(0.750)}{0.857 + 0.750} = 0.800$$

**Q7.** Compute the precision and the recall when **No** is the positive class.

> [!success]- Answer
> The roles swap: $TP = 5$, $FP = 2$ (S7, S12), $FN = 1$ (S11).
> $$p = \frac{5}{7} = 0.714 \qquad r = \frac{5}{6} = 0.833$$

Use this confusion matrix for Q8 and Q9 (30 iris flowers, rows = predicted, columns = actual):

| Predicted \ Actual | setosa | versicolor | virginica |
| --- | --- | --- | --- |
| **setosa** | 10 | 0 | 0 |
| **versicolor** | 0 | 8 | 2 |
| **virginica** | 0 | 1 | 9 |

**Q8.** Compute the accuracy.

> [!success]- Answer
> $$\text{Accuracy} = \frac{\text{diagonal}}{\text{total}} = \frac{10 + 8 + 9}{30} = 0.900$$

**Q9.** Compute the precision, the recall and the F1-measure for versicolor.

> [!success]- Answer
> Use one-vs-rest: $TP = 8$, the row total is $10$, and the column total is $0 + 8 + 1 = 9$.
> $$p = \frac{8}{10} = 0.800 \qquad r = \frac{8}{9} = 0.889 \qquad F_1 = \frac{2(0.800)(0.889)}{0.800 + 0.889} = 0.842$$

**Q10.** Using the holdout method with one third for testing, how many records go to testing and how many to training?

> [!success]- Answer
> $\frac{14}{3} \approx 4.7$, so about **5** records for testing and **9** for training.

**Q11.** Using 7-fold cross-validation, how many records are in each fold? How many models are trained?

> [!success]- Answer
> There are $\frac{14}{7} = 2$ records per fold. **7** models are trained, each on 12 records and tested on 2. The final error is the average of the 7 errors.

**Q12.** Compute the entropy of Pass.

> [!success]- Answer
> There are 8 Yes and 6 No:
> $$E = -\tfrac{8}{14}\log_2\tfrac{8}{14} - \tfrac{6}{14}\log_2\tfrac{6}{14} = 0.985$$

**Q13.** Compute the information gain of Attendance, StudyTime and Assignments. Which attribute is the root?

> [!success]- Answer
> | Attribute | Value | Yes / No | Entropy |
> | --- | --- | --- | --- |
> | Attendance | High (6) | 5 / 1 | 0.650 |
> | | Low (8) | 3 / 5 | 0.954 |
> | StudyTime | High (4) | 4 / 0 | 0.000 |
> | | Medium (5) | 3 / 2 | 0.971 |
> | | Low (5) | 1 / 4 | 0.722 |
> | Assignments | Done (7) | 6 / 1 | 0.592 |
> | | Missed (7) | 2 / 5 | 0.863 |
>
> $$\text{info}_{\text{Attendance}} = \tfrac{6}{14}(0.650) + \tfrac{8}{14}(0.954) = 0.824 \Rightarrow \text{gain} = 0.985 - 0.824 = 0.161$$
> $$\text{info}_{\text{StudyTime}} = \tfrac{4}{14}(0) + \tfrac{5}{14}(0.971) + \tfrac{5}{14}(0.722) = 0.605 \Rightarrow \text{gain} = 0.985 - 0.605 = 0.381$$
> $$\text{info}_{\text{Assignments}} = \tfrac{7}{14}(0.592) + \tfrac{7}{14}(0.863) = 0.727 \Rightarrow \text{gain} = 0.985 - 0.727 = 0.258$$
>
> **Root = StudyTime**, because it has the highest gain (0.381).

**Q14.** Compute the information gain of the remaining attributes for StudyTime = Medium and StudyTime = Low.

> [!success]- Answer
> **StudyTime = High** (4 / 0) is pure, so it is a leaf: **Yes**.
>
> **StudyTime = Medium** (S3, S6, S9, S10, S14): 3 Yes / 2 No, so $E = 0.971$.
> - Attendance: High 1/1 ($E = 1$), Low 2/1 ($E = 0.918$). Gain $= 0.971 - [\tfrac{2}{5}(1) + \tfrac{3}{5}(0.918)] = 0.020$
> - Assignments: Done 3/0, Missed 0/2, both pure. Gain $= 0.971 - 0 = \mathbf{0.971}$, so split on **Assignments**.
>
> **StudyTime = Low** (S2, S4, S8, S11, S13): 1 Yes / 4 No, so $E = 0.722$.
> - Attendance: High 1/0, Low 0/4, both pure. Gain $= 0.722 - 0 = \mathbf{0.722}$, so split on **Attendance**.
> - Assignments: Done 1/1 ($E = 1$), Missed 0/3. Gain $= 0.722 - \tfrac{2}{5}(1) = 0.322$

**Q15.** Draw the final decision tree.

> [!success]- Answer
> ```mermaid
> graph TD
>   A[StudyTime] -->|High| B((Yes))
>   A -->|Medium| C[Assignments]
>   A -->|Low| D[Attendance]
>   C -->|Done| E((Yes))
>   C -->|Missed| F((No))
>   D -->|High| G((Yes))
>   D -->|Low| H((No))
> ```
> Every leaf is pure, so splitting stops.

**Q16.** Classify the new student: Attendance = Low, StudyTime = Medium, Assignments = Done.

> [!success]- Answer
> StudyTime = Medium, then Assignments = Done, so **Pass = Yes**.

---

## Formula sheet

$$\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN} \qquad \text{Error rate} = 1 - \text{Accuracy}$$

$$p = \frac{TP}{TP + FP} \qquad r = \frac{TP}{TP + FN} \qquad F_1 = \frac{2pr}{p + r}$$

$$\text{Entropy}(S) = -\sum_{i=1}^{l} \frac{|S_i|}{|S|}\log_2\frac{|S_i|}{|S|}$$

$$\text{info}_A(D) = \sum_{j=1}^{n} \frac{|D_j|}{|D|}\,\text{info}(D_j) \qquad \text{gain}(A) = \text{info}(D) - \text{info}_A(D)$$

Calculator tip: $\log_2 x = \frac{\ln x}{\ln 2}$, and $0 \cdot \log_2 0$ counts as $0$.
