# NLP-chatbot
This project analyzes hospital patient survey data using Natural Language Processing (NLP) to derive sentiment insights and categorize feedback by theme and department. The analysis incorporates text preprocessing, sentiment scoring with VADER, custom classification of survey questions, and performance evaluation across hospitals. It concludes with tailored visualizations for exploring sentiment and star rating trends within and across facilities.

__Core Objectives__
- Classify and group patient experience survey responses by theme (e.g., communication, responsiveness)
- Identify associated hospital departments (e.g., doctors, nurses, support staff)
- Clean and lemmatize free-text responses using NLP techniques
- Apply sentiment analysis with VADER to quantify patient tone
- Evaluate and visualize average sentiment and star ratings by facility, theme, and department

# Workflow Summary
__Data Loading__
- Imported structured HCAHPS survey dataset via pandas
- Explored dataset size and hospital distribution

__Text Classification and Metadata Engineering__
- Developed keyword-based mapping to assign each survey question a theme (e.g., "communication", "medication")
- Built custom logic to identify responsible departments (doctors, nurses, staff) based on keywords
- Created a new column (survey_response) by merging questions with categorical interpretation of response percentages

__Preprocessing__
- Tokenized and cleaned text using NLTK
- Removed stopwords and applied POS-aware lemmatization
- Stored processed results in a new column Cleaned_Text

__Sentiment Analysis__
- Used VADER's sentiment intensity analyzer on cleaned text
- Assigned each response a sentiment label (positive, neutral, negative) and compound sentiment score
- Aggregated sentiment scores and star ratings by theme and department

__Visualization and Insights__
- Visualized sentiment scores vs. survey star ratings across themes and departments
- Created dashboards per facility to explore feedback distribution, performance, and tone
- Enabled user input to dynamically generate visual insights by facility

# Technology Used
- Pandas – for data loading and transformation
- NumPy – for numerical processing
- NLTK – for tokenization, POS tagging, stopword removal, and lemmatization
- VADER (from NLTK) – for sentiment scoring
- Matplotlib – for visualizations and plots
- Google Colab – as the runtime environment
