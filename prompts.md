# Prompt Versions

This experiment compares three prompt styles for classifying customer complaints: Basic, Few-shot, and Instruction-heavy.  
The same eight test cases were used with each prompt.

## 1. Basic Prompt

```text
Classify the following customer complaint into one category: Delivery, Billing, Product Quality, or Customer Service.

Complaint: [INSERT COMPLAINT]
```

## 2. Few-shot Prompt

```text
Classify each customer complaint into exactly one of these categories: Delivery, Billing, Product Quality, or Customer Service.

Use these examples as guidance:

Complaint: "The courier left my parcel at the wrong building."
Category: Delivery

Complaint: "My discount code was accepted, but the full price was charged to my account."
Category: Billing

Complaint: "The electric kettle switches off before the water boils."
Category: Product Quality

Complaint: "The support agent was rude and refused to answer my questions."
Category: Customer Service

Now classify the following complaint using the same approach.

Complaint: [INSERT COMPLAINT]

Return only the category name, with no explanation or extra text.
```

## 3. Instruction-heavy Prompt

```text
You are a customer complaint classification assistant. Classify each complaint into exactly ONE of the following categories:

1. Delivery — Problems involving late, missing, misdelivered, or incorrectly handled deliveries.
2. Billing — Problems involving incorrect charges, duplicate payments, refunds, discounts, or payment processing.
3. Product Quality — Problems involving damaged, defective, malfunctioning, or poorly made products.
4. Customer Service — Problems involving rude or unhelpful staff, unanswered enquiries, or poor customer support.

Follow these rules carefully:

- Identify the customer's main problem rather than relying on emotional or positive/negative wording.
- If a complaint mentions multiple issues, select the category that best represents the main concern.
- Do not assume facts that are not explicitly stated.
- Do not invent details or explanations.
- If the complaint is ambiguous, choose the closest category based on the available information.
- Select exactly one category from the four permitted categories.
- Return only the category name. Do not include labels, explanations, punctuation, or additional text.

Classify the following complaint:

Complaint: [INSERT COMPLAINT]
```

## Experimental Consistency

- The classification task and permitted categories remained the same across all three prompts.
- The same eight complaints were tested for each prompt version, which differed in the amount and type of guidance provided.
- Model responses were evaluated using correctness, format compliance, hallucination, and consistency.
