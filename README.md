# Ticket_classifier_Pipeline

# Customer Support Ticket Classifier & Entity Extractor

## 🔍 Objective
Develop a traditional NLP + ML pipeline to:
- Classify customer support tickets by `issue_type` and `urgency_level`
- Extract key entities from ticket text (product names, complaint words, dates)

---

## 🗃️ Dataset
Provided file: `ai_dev_assignment_tickets_complex_1000.xlsx`  
We used a cleaned CSV version: `cleaned_tickets_ready.csv`

### Columns Used:
- `ticket_text` (text input)
- `issue_type` (label 1)
- `urgency_level` (label 2)
- `product` (ground truth for entity extraction)

---

## ⚙️ Technologies Used
- Python (Pandas, scikit-learn, re)
- Traditional NLP: TF-IDF, regex, string matching
- Logistic Regression for classification

---

## 📐 Steps Performed

### ✅ 1. Data Preprocessing
- Converted text to lowercase
- Removed special characters
- Dropped nulls

### ✅ 2. Feature Engineering
- `TF-IDF` from ticket text
- `Ticket Length` (number of words)
- (Sentiment score explored, but not included — didn’t improve performance)

### ✅ 3. Multi-Task Learning
- **Model 1:** `issue_type` classifier (accuracy: 100%)
- **Model 2:** `urgency_level` classifier (accuracy: ~35%)

### ✅ 4. Entity Extraction
Used regex & rule-based logic to extract:
- Product names from known list
- Dates (DD/MM/YYYY, March 5 etc.)
- Complaint keywords (e.g. broken, error, damaged, etc.)

### ✅ 5. Integration
Also done integration 
