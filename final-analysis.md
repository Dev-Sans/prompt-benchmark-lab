# Final Analysis

The results show that the Few-Shot prompt performed the best out of the three prompt variations tested, with 100% accuracy and a rubric score of 100%. The Basic and Instruction-Heavy prompts both achieved 87.5% accuracy, but their overall rubric scores differed.

The Basic prompt misclassified TC08, while the Instruction-Heavy prompt misclassified TC05. This shows that adding more instructions does not necessarily guarantee better classification results. In this experiment, providing examples through Few-Shot prompting was more effective.

The rubric scores also showed a difference between the three approaches. The Instruction-Heavy prompt scored 96.88%, while the Basic prompt scored 84.38%. The Basic prompt's lower score was partly due to its response format, as it included a `Category:` prefix instead of returning only the category name.

However, these results are based on only eight test cases. A larger and more varied dataset would be needed to determine whether the same pattern holds across different customer complaints.

Overall, the Few-Shot prompt was the most effective approach in this experiment. While the results are promising, further testing would be needed to draw more general conclusions about the effectiveness of different prompting techniques.
