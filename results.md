# Results

## 1. Classification Results

The three prompt variations were evaluated using the same eight customer complaint test cases. Each predicted category was compared against its expected category.

| Test Case | Expected Category | Basic Prompt | Few-Shot Prompt | Instruction-Heavy Prompt |
|---|---|---|---|---|
| TC01 | Delivery | Delivery | Delivery | Delivery |
| TC02 | Billing | Billing | Billing | Billing |
| TC03 | Product Quality | Product Quality | Product Quality | Product Quality |
| TC04 | Customer Service | Customer Service | Customer Service | Customer Service |
| TC05 | Billing | Billing | Billing | Delivery |
| TC06 | Billing | Billing | Billing | Billing |
| TC07 | Product Quality | Product Quality | Product Quality | Product Quality |
| TC08 | Billing | Customer Service | Billing | Billing |

## 2. Accuracy Comparison

Accuracy was calculated by dividing the number of correct predictions by the total number of test cases and multiplying by 100.

| Prompt Variation | Correct Predictions | Incorrect Predictions | Accuracy |
|---|---:|---:|---:|
| Basic | 7/8 | 1 | 87.5% |
| Few-Shot | 8/8 | 0 | 100% |
| Instruction-Heavy | 7/8 | 1 | 87.5% |

## 3. Rubric-Based Evaluation

Each model output was evaluated using four criteria: correctness, format compliance, hallucination, and consistency. Each criterion was scored out of 2, giving a maximum of 8 points per test case and 64 points per prompt variation.

| Prompt Variation | Total Score | Maximum Score | Score Percentage |
|---|---:|---:|---:|
| Basic | 54 | 64 | 84.38% |
| Few-Shot | 64 | 64 | 100% |
| Instruction-Heavy | 62 | 64 | 96.88% |

The rubric-based scores complement the accuracy results by accounting for output formatting and the other evaluation criteria.

## 4. Error Analysis

### Basic Prompt

The Basic prompt incorrectly classified TC08 as Customer Service instead of Billing. The complaint mentioned an unreceived order confirmation and uncertainty about whether payment had gone through.

### Few-Shot Prompt

The Few-Shot prompt correctly classified all eight test cases. No classification errors were observed in this test set.

### Instruction-Heavy Prompt

The Instruction-Heavy prompt incorrectly classified TC05 as Delivery instead of Billing. The complaint involved both a late delivery and an additional delivery fee.

## 5. Observations

1. The Few-Shot prompt achieved the highest accuracy, correctly classifying all eight test cases.
2. The Basic and Instruction-Heavy prompts both achieved 87.5% accuracy but made errors on different test cases.
3. The Basic prompt misclassified TC08, while the Instruction-Heavy prompt misclassified TC05.
4. The Few-Shot prompt achieved the highest overall rubric score, followed by the Instruction-Heavy prompt and then the Basic prompt.
5. The Basic prompt returned category labels with a `Category:` prefix, while the Few-Shot and Instruction-Heavy prompts returned only the category names.

## 6. Conclusion

In this experiment, the Few-Shot prompt performed best, achieving 100% accuracy and a rubric score of 100%. The Instruction-Heavy prompt achieved 87.5% accuracy and a rubric score of 96.88%, while the Basic prompt achieved 87.5% accuracy and a rubric score of 84.38%.

The results suggest that providing examples was effective for this specific customer complaint classification task. The results may vary for different datasets. 
