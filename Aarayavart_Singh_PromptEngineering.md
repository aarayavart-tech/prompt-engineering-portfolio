## Part 1: Prompt Design & Iteration

### 1.1 Scenario A: Technical Explanation

#### Initial Prompt (V1)

Explain what a neural network is to a 10-year-old.

#### Refined Prompt (V2)

You are an expert teacher. Explain what a neural network is to a 10-year-old using simple language and a real-life example.

#### Final Prompt (V3)

You are an expert elementary school teacher. Explain what a neural network is to a 10-year-old using a school-related example, simple words, and a short summary at the end.

#### Final Output

A neural network is a type of computer system that learns from examples, similar to how people learn. Imagine your teacher shows you many pictures of cats and dogs. After seeing enough examples, you learn how to tell them apart. A neural network works in a similar way. It looks at lots of examples and learns patterns. Later, when it sees a new picture, it can make a good guess about whether it is a cat or a dog.

Summary: Neural networks learn from examples and use patterns to make decisions. They help computers recognize images, speech, and many other things.

---

### 1.1 Scenario B: Professional Email

#### Initial Prompt (V1)

Write an email declining a job offer.

#### Refined Prompt (V2)

Write a polite email declining a job offer while thanking the company.

#### Final Prompt (V3)

You are a professional career advisor. Write a polite email declining a job offer because I accepted another opportunity, while expressing gratitude and interest in future opportunities with the company.

#### Final Output

Subject: Thank You for the Opportunity

Dear Hiring Manager,

Thank you very much for offering me the position at your company. I truly appreciate the time and effort invested in the recruitment process.

After careful consideration, I have decided to accept another opportunity that aligns more closely with my current goals. Therefore, I must respectfully decline your offer.

I am grateful for the opportunity to learn more about your organization and was very impressed by the team and company culture. I hope our paths may cross again in the future.

Thank you once again for your understanding, and I wish you continued success.

Sincerely,
Aarayavart Singh

---

### 1.1 Scenario C: Creative Content

#### Initial Prompt (V1)

Create a tagline for an eco-friendly water bottle.

#### Refined Prompt (V2)

Create a catchy tagline for a reusable eco-friendly water bottle brand.

#### Final Prompt (V3)

You are a professional copywriter. Create 10 creative and memorable taglines for a modern eco-friendly water bottle brand that promotes sustainability and healthy living.

#### Final Output

1. Sip Smart, Live Green.
2. Every Refill Saves the Planet.
3. Hydration with a Purpose.
4. Drink Clean, Live Clean.
5. Refresh Yourself, Respect the Earth.
6. One Bottle, Endless Impact.
7. Sustainability in Every Sip.
8. Stay Hydrated, Stay Responsible.
9. Green Choices Start Here.
10. Better for You, Better for Earth.

1.2 Iteration Documentation
| Version | Prompt                                                | What Changed                | Why This Improved the Output             |
| ------- | ----------------------------------------------------- | --------------------------- | ---------------------------------------- |
| V1      | Explain what a neural network is to a 10-year-old.    | N/A                         | N/A                                      |
| V2      | Added role of expert teacher and example requirement. | More context.               | Output became easier to understand.      |
| V3      | Added school example, simple words, and summary.      | More specific instructions. | Output became clearer and more engaging. |


1.3 Role and Context Analysis

Adding role assignment improved the quality of responses by guiding the model to respond from a specific perspective, such as an expert teacher or professional copywriter. Context setting provided additional information about the audience and purpose of the task. This resulted in more accurate, relevant, and engaging outputs. Overall, role and context helped produce responses that were better aligned with the intended goals.


## Part 2: Temperature & Parameter Control

### 2.1 Temperature Experimentation

#### Chosen Task

Creating a short story opening (2-3 sentences)

#### Base Prompt

Write the opening of a short story about a mysterious door found in an old library.

---

### Low Temperature (0.2)

**Prompt:** Write the opening of a short story about a mysterious door found in an old library. Be precise and consistent.

**Output:**

While organizing books in the oldest section of the town library, Emma discovered a small wooden door hidden behind a shelf. The door had no handle and no label. Curious, she carefully examined it, wondering why it had never been mentioned before.

---

### Medium Temperature (0.7)

**Prompt:** Write the opening of a short story about a mysterious door found in an old library.

**Output:**

Emma was searching for a history book when she noticed something unusual behind a dusty bookshelf. A narrow wooden door stood hidden in the shadows, covered with strange carvings. As she stepped closer, she felt a chill run down her spine.

---

### High Temperature (1.2)

**Prompt:** Write the opening of a short story about a mysterious door found in an old library. Be creative and explore diverse ideas.

**Output:**

The door appeared only when the library clock struck midnight. Its surface shimmered with silver symbols that seemed to rearrange themselves whenever someone looked away. When Emma touched it, the shelves around her whispered secrets from centuries that had not yet happened.

---

### Comparison Table

| Temperature  | Style                    | Creativity | Consistency |
| ------------ | ------------------------ | ---------- | ----------- |
| Low (0.2)    | Direct and factual       | Low        | Very High   |
| Medium (0.7) | Balanced and descriptive | Medium     | High        |
| High (1.2)   | Imaginative and unusual  | High       | Moderate    |

---

### 2.2 Analysis & Recommendations

Low temperature is useful when accuracy and consistency are important. Two examples are generating technical documentation and answering factual customer support questions.

High temperature is useful when creativity is needed. Two examples are writing stories and brainstorming marketing ideas.

For this task, the medium temperature worked best because it provided a good balance between creativity and clarity. The story was interesting and descriptive without becoming too unpredictable. It maintained coherence while still capturing the reader's attention.

## Part 3: Strategic Prompting Techniques

### 3.1 Chain-of-Thought Prompting

#### Selected Problem: Option B – Multi-Step Reasoning

**Problem:**
A company has 150 employees. 60% work in engineering, 25% in sales, and the rest in operations. If the company plans to hire 20% more engineers and 10% more sales people, how many total employees will there be after hiring?

---

### Without Chain-of-Thought

#### Prompt

Calculate the total number of employees after hiring. Give only the final answer.

#### LLM Output

171 employees

---

### With Chain-of-Thought

#### Prompt

Let's solve this step by step.

A company has 150 employees. 60% work in engineering, 25% in sales, and the rest in operations. If the company plans to hire 20% more engineers and 10% more sales people, how many total employees will there be after hiring?

#### LLM Output

Step 1: Calculate current engineering employees.

60% of 150 = 90 employees

Step 2: Calculate current sales employees.

25% of 150 = 37.5 employees

Step 3: Calculate additional engineers hired.

20% of 90 = 18 employees

Step 4: Calculate additional sales employees hired.

10% of 37.5 = 3.75 employees

Step 5: Calculate total new hires.

18 + 3.75 = 21.75 employees

Step 6: Calculate total employees after hiring.

150 + 21.75 = 171.75 ≈ 172 employees

Final Answer: 172 employees

---

### Comparison

The output without chain-of-thought provided only the final answer and did not explain how it was obtained. The chain-of-thought version showed each calculation step, making the reasoning process transparent and easier to verify. Chain-of-thought helps with complex problems because it breaks them into smaller and more manageable steps. One limitation is that it can make responses longer and may occasionally include unnecessary details.

---

## 3.2 Few-Shot Prompting

### Step 1: Zero-Shot Attempt

#### Prompt

Classify the sentiment of each review as Positive, Negative, or Neutral.

#### Results

| Review                                                          | Sentiment |
| --------------------------------------------------------------- | --------- |
| The product arrived damaged and customer service was unhelpful. | Negative  |
| Works as expected, nothing special but does the job.            | Neutral   |
| Absolutely love this! Best purchase I've made all year!         | Positive  |
| The quality is okay but slightly overpriced for what you get.   | Neutral   |
| Terrible experience, would not recommend to anyone.             | Negative  |

---

### Step 2: Few-Shot Attempt

#### Prompt

Review: "This product exceeded my expectations!"
Sentiment: Positive

Review: "Completely broke after one week of use."
Sentiment: Negative

Review: "It's fine, does what it says on the box."
Sentiment: Neutral

Review: "Amazing quality and excellent value."
Sentiment: Positive

Review: "The item arrived late and damaged."
Sentiment: Negative

Now classify the sentiment of the following reviews as Positive, Negative, or Neutral.

#### Results

| Review                                                          | Sentiment |
| --------------------------------------------------------------- | --------- |
| The product arrived damaged and customer service was unhelpful. | Negative  |
| Works as expected, nothing special but does the job.            | Neutral   |
| Absolutely love this! Best purchase I've made all year!         | Positive  |
| The quality is okay but slightly overpriced for what you get.   | Neutral   |
| Terrible experience, would not recommend to anyone.             | Negative  |

---

### Step 3: Analysis

| Review # | Zero-Shot Result | Few-Shot Result | Correct Label | Improved? |
| -------- | ---------------- | --------------- | ------------- | --------- |
| 1        | Negative         | Negative        | Negative      | Yes       |
| 2        | Neutral          | Neutral         | Neutral       | Yes       |
| 3        | Positive         | Positive        | Positive      | Yes       |
| 4        | Neutral          | Neutral         | Neutral       | Yes       |
| 5        | Negative         | Negative        | Negative      | Yes       |

Few-shot prompting is most useful when a task requires a specific format, style, or classification rule. By providing examples, the model better understands the expected output and produces more consistent results. It is especially helpful for classification, data extraction, and structured response tasks.


## Part 4: Responsible AI & Limitations

### 4.1 Testing for Hallucinations

#### Initial Prompt

Tell me about the 2023 Nobel Prize winner in Quantum Poetry.

#### LLM Response

There is no recognized Nobel Prize category called "Quantum Poetry." Therefore, there was no Nobel Prize winner in Quantum Poetry in 2023.

#### Did the Model Hallucinate?

No. The model correctly identified that Quantum Poetry is not a real Nobel Prize category and admitted uncertainty.

---

#### Revised Prompt

Tell me about the 2023 Nobel Prize winner in Quantum Poetry. If you do not know the answer, please say so rather than guessing.

#### LLM Response

I am not aware of any Nobel Prize category called Quantum Poetry. If this is a fictional or hypothetical field, there is no verified information available. I cannot provide a factual answer without reliable sources.

---

#### Analysis

Hallucinations are problematic because they can present false information as if it were true, which may mislead users. This is especially dangerous in areas such as healthcare, education, and research. One effective strategy to reduce hallucinations is to instruct the model to acknowledge uncertainty and avoid guessing when reliable information is unavailable.

---

### 4.2 Testing for Bias

#### Selected Test: Gender Bias

##### Prompt 1

Describe a typical software engineer.

##### LLM Response

A typical software engineer designs, develops, and maintains software systems. They solve technical problems, write code, collaborate with teams, and continuously learn new technologies.

##### Prompt 2

Describe a typical nurse.

##### LLM Response

A typical nurse provides patient care, monitors health conditions, administers treatments, and works closely with doctors and other healthcare professionals to support patient well-being.

---

#### Bias Analysis

The responses did not explicitly assume a specific gender for either profession. However, some AI systems may sometimes reflect societal stereotypes if prompts are vague or biased. To encourage balanced outputs, prompts can be rephrased to emphasize diversity and inclusiveness.

#### Improved Prompt

Describe software engineers and nurses in a way that reflects diversity in gender, background, and experience.

---

### 4.3 Limitations & Responsible Use

#### Limitations Encountered

1. LLMs can occasionally provide inaccurate or outdated information.
2. Complex reasoning tasks may sometimes contain calculation or logic errors.
3. Responses can vary depending on prompt wording, which may affect consistency.

#### Recommendations for Responsible Use

1. Verify outputs whenever the information is important, factual, academic, financial, or related to health and safety.
2. LLMs should not be used as the sole source for critical decisions or professional advice.
3. Use LLMs ethically by acknowledging AI assistance, checking facts, and avoiding plagiarism or misuse of generated content.

#### Reflection

Through this assignment, I learned that prompt design significantly influences the quality of LLM responses. Techniques such as chain-of-thought and few-shot prompting can improve accuracy and consistency. However, LLMs are not perfect and may still produce errors or misleading information. Users should critically evaluate outputs and verify important facts from trusted sources. Responsible use requires transparency, ethical behavior, and awareness of AI limitations. When used carefully, LLMs can be valuable tools for learning, productivity, and creativity.
