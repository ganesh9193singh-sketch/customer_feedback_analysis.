# Customer Feedback Analysis

## 📌 Project Overview

**Customer Feedback Analysis** is a Python data analysis and GenAI automation project that studies customer reviews from a women's clothing e-commerce dataset.

The project helps identify **critical customer feedback**, understand the main complaint areas, and generate **personalized customer-support apology emails** using Google Gemini.

> **Important:** The analysis uses a simple rule-based approach. Reviews with **1 or 2 stars are classified as Critical**. No Machine Learning model is used.

---

## 🎯 Project Objectives

- Clean and prepare customer review data
- Handle missing values and duplicate records
- Clean review text for analysis
- Understand the distribution of customer ratings
- Identify critical 1-star and 2-star reviews
- Find common complaint words and phrases
- Group complaints into meaningful categories
- Select the most detailed critical reviews
- Generate personalized apology emails with Google Gemini
- Save the generated emails for further review

---

## 🔄 Project Workflow

1. Load the customer review dataset
2. Check and handle missing values
3. Remove duplicate records
4. Clean review text
5. Analyze rating distribution
6. Filter 1-star and 2-star reviews
7. Find common words in critical reviews
8. Analyze complaint keywords
9. Analyze complaint categories
10. Create calculated insights
11. Select 3 detailed critical reviews
12. Connect to Google Gemini
13. Create a customer-support prompt
14. Generate personalized apology emails
15. Display and save the results
16. Summarize findings and limitations

---

## 📊 Main Analysis

### Critical Reviews

The project uses this simple business rule:

| Rating | Classification |
|---|---|
| ⭐ 1 | Critical |
| ⭐ 2 | Critical |
| ⭐ 3 | Not Critical |
| ⭐ 4 | Not Critical |
| ⭐ 5 | Not Critical |

This makes the analysis easy to understand and explain.

### Complaint Categories

Critical reviews are checked against manually defined complaint groups:

- **Fit & Size**
- **Quality & Fabric**
- **Looks & Color**
- **Comfort**
- **Service & Delivery**
- **Disappointment & Returns**

A single review can belong to more than one complaint category.

---

## 🤖 GenAI Customer Support Automation

The project uses **Google Gemini** to create short, personalized apology emails for selected critical reviews.

The prompt instructs the model to:

- Start with a subject line
- Use a professional greeting
- Mention the customer's specific problems
- Show empathy
- Suggest a return, exchange, or refund as a next step
- Avoid inventing order numbers, discount codes, names, dates, or policies
- Keep the email short
- End professionally

A human should review AI-generated emails before they are sent to customers.

---

## 🛠️ Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Regular Expressions
- Collections / Counter
- Jupyter Notebook
- Google Gemini API
- Google GenAI Python SDK

---

## 📁 Project Files

- `customer_feedback_analysis.ipynb` — Main analysis notebook
- `README.md` — Project documentation
- `generated_emails.csv` — Created after running the notebook and generating the AI responses
- `Womens Clothing E-Commerce Reviews.csv` — Input dataset required to run the analysis

---

## ▶️ How to Run

### 1. Install the required libraries

```bash
pip install pandas matplotlib seaborn google-genai
```

### 2. Open the notebook

Open:

```
customer_feedback_analysis.ipynb
```

using Jupyter Notebook, JupyterLab, or another compatible notebook environment.

### 3. Add the dataset

Place:

```
Womens Clothing E-Commerce Reviews.csv
```

in the expected notebook location, or update the file path in the notebook.

### 4. Set the Gemini API key

The notebook first looks for:

```
GEMINI_API_KEY
```

If it is not available, it asks for the key using a hidden input.

**Never commit your API key to GitHub.**

### 5. Run the notebook

Run the cells from top to bottom.

The notebook performs the complete analysis and can create:

```
generated_emails.csv
```

---

## 📈 Expected Output

The notebook produces:

- Rating distribution analysis
- Critical review counts
- Top words in critical reviews
- Complaint keyword analysis
- Complaint category analysis
- Calculated insight tables
- Three selected detailed critical reviews
- AI-generated apology emails
- A final project summary
- Limitations and future improvements

---

## ⚠️ Limitations

1. **Star ratings are not perfect.** A 3-star review can still contain an important problem.
2. **Keyword matching is manually defined.** New, misspelled, or unexpected complaint words may be missed.
3. **Keyword matching does not understand sarcasm or context.**
4. **AI-generated responses can contain mistakes** and should be checked by a human before being sent.

---

## 🚀 Future Improvements

- Add an urgency score
- Expand the complaint keyword list automatically
- Add a human approval workflow
- Add sentiment analysis
- Compare complaint trends by product category
- Build a dashboard for customer-support teams
- Add more advanced NLP or Machine Learning in a future version

---

## 👨‍💻 Author

**Ganesh Singh**

BCA Student | Data Analysis & Python Project

---

## 📌 Conclusion

This project combines **data cleaning, exploratory analysis, rule-based complaint detection, keyword analysis, and Generative AI** to turn customer feedback into useful business insights and ready-to-edit customer-support responses.

**Simple rules identify unhappy customers, while GenAI helps turn those findings into personalized responses.**
