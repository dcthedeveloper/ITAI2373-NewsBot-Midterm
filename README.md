# NewsBot Intelligence System

This project is an end-to-end Natural Language Processing (NLP) system designed to automatically process, categorize, and extract insights from news articles. The goal is to replicate a real-world media intelligence tool, moving from raw text to actionable business insights.

## How to Run This Project
1. Clone this repository.
2. Open the `.ipynb` file in Google Colab or Jupyter Notebook.
3. Create a `kaggle.json` API key from your Kaggle account.
4. Run the cells in order from top to bottom. You will be prompted to upload your `kaggle.json` file during the setup.

---

## Executive Summary
================================================================================
EXECUTIVE SUMMARY - NewsBot Intelligence System
================================================================================

### Project Overview
This notebook implements an end-to-end NLP intelligence system for automated news analysis,
designed for Global Insights Inc.'s market intelligence platform. The system processes 2,000
carefully curated news articles across 5 major categories using 8 advanced NLP modules.

### Key Achievements
- **Classification Accuracy**: 74.5% using Linear SVM for 5-way category prediction
- **Sentiment Intelligence**: Dual-method analysis (TextBlob + VADER) with 0.43 correlation
- **Entity Extraction**: 3,033 unique named entities (PERSON, ORG, GPE, DATE, MONEY)
- **Feature Engineering**: TF-IDF vectorization with 2,000 optimized features
- **Web Application**: Professional React-based frontend (NuVision News) - *Bonus component*

### Business Impact Summary
Financial Services: \$2M annual value (analyst time + trading alpha)
Corporate PR: \$150K+ annual value (monitoring + crisis prevention)
Political Campaigns: \$100K+ per cycle (data-driven strategy)

Total Addressable ROI: \$2.25M+ annually

### Technical Stack
- **Dataset**: HuffPost News (2,000 articles, 5 balanced categories)
- **NLP Libraries**: spaCy, NLTK, TextBlob, VADER
- **ML Models**: Logistic Regression, Naive Bayes, Linear SVM
- **Visualization**: matplotlib, seaborn, WordCloud

---

## Step 0: Initial Setup
### Analysis & Findings
✅ All libraries are installed and imported successfully.

## Step 1: Dataset Acquisition and Preparation
### Analysis & Findings
✅ Kaggle API setup complete using file: kaggle.json!
Dataset URL: https://www.kaggle.com/datasets/rmisra/news-category-dataset
Full dataset downloaded with 209,527 articles.
✅ Dataset prepared with 2,000 articles across 5 categories.

## Module 1: Real-World NLP Application Context
### Business Case
Global Insights Inc. requires a real-time media intelligence dashboard for clients in finance,
PR, and political strategy. Current manual analysis costs \$500K+/year in analyst time.

### Module 1 Analysis: Strategic Business Positioning
- Balanced dataset ensures unbiased model training.
- 5 categories cover 80% of client monitoring needs.
- News intelligence market growing at 12.3% CAGR through 2028.

### Visualizations
- Count Plot

## Module 2: Text Preprocessing Pipeline
### Methodology
5-step pipeline: Lowercase → Remove special chars → Tokenize → Remove stopwords → Lemmatize

### Module 2 Analysis: Preprocessing Pipeline Impact
- **Token Reduction**: 47.9% (from 30.7 to 16.0 tokens on average), improving computational efficiency.
- **Lemmatization over stemming**: Produces valid words for better interpretability.
- **NER applied to original text**: Preserves entity capitalization before processing.

### Visualizations
- Histogram & Text Plot

## Module 3: TF-IDF Feature Extraction and Analysis
### Methodology
TF-IDF Configuration: max_features=2000, ngram_range=(1,2), min_df=3. Bigrams help capture context such as "donald trump", "super bowl", and "new york".

### Visualizations
- Word Cloud

## Module 4: Part-of-Speech (POS) Pattern Analysis
### Methodology
Analyzed POS distributions across news categories to identify stylistic patterns.

### Module 4 Analysis: Grammatical Pattern Insights
- **SPORTS** uses 27% more verbs than **TECHNOLOGY**, indicating event-driven vs. descriptive language.
- **TECHNOLOGY** has the highest proper noun density, reflecting its company-centric coverage.
- **POLITICS** is noun-heavy, focusing on entities and concepts over actions.

### Visualizations
- Grouped Bar Chart & Pie Chart

## Module 5: Syntax Parsing and Semantic Analysis
### Methodology
Used spaCy's dependency parser to analyze grammatical relationships, SVO patterns, and sentence complexity.

### Module 5 Analysis: Syntactic Structure Insights
- **Syntactic Complexity**: BUSINESS news was the most complex (avg tree depth: 4.4), while SPORTS was the least complex (avg tree depth: 3.6).
- **Semantic Roles**: Subjects in POLITICS are often institutions (Congress, Senate), while subjects in SPORTS are athletes or teams.
- **Business Application**: This analysis can be used for content complexity scoring to match articles to reader skill levels.

### Visualizations
- Bar Chart (Complexity Metrics)

## Module 6: Sentiment and Emotion Analysis (Dual Method)
### Methodology
Used a dual-method approach (TextBlob and VADER) for robust validation of sentiment scores.

### Module 6 Analysis: Dual-Method Sentiment Intelligence
- **Overall Correlation**: 0.428, indicating positive agreement between the two methods.

### Visualizations
- Box Plots, Scatter Plot, Heatmap

## Module 7: Multi-Class Text Classification System
### Module 7 Analysis: Multi-Model Classification Performance
- **Linear SVM**: 0.7450 (Top performing model, candidate for production)
- **Logistic Regression**: 0.7400
- **Multinomial Naive Bayes**: 0.7325

### Visualizations
- Horizontal Bar Chart & Confusion Matrix

## Module 8: Named Entity Recognition and Analysis
### Module 8 Analysis: Named Entity Recognition & Knowledge Extraction
- **Total Entity Mentions**: 4,175
- **Unique Entities**: 3,033
- **Article Coverage**: 83.8% of articles contained at least one named entity.

### Visualizations
- Bar Plot (Top Entities) & Stacked Bar Plot (Entity Types)

---

## Advanced Content Analysis (Bonus Modules)

### Topic Modeling with LDA
- Applied Latent Dirichlet Allocation (LDA) to discover 5 underlying topics across the dataset, such as a political topic dominated by "trump", "donald", and "clinton".

### Text Summarization
- Implemented an extractive summarization technique to select key sentences from articles to form a concise summary.

### Multilingual Intelligence
- Demonstrated a pipeline for translating non-English text to English before applying NLP analysis.

---

## Conclusions & Future Work

### Project Summary
Successfully implemented an end-to-end NLP intelligence system achieving high multi-class accuracy, dual-method sentiment validation, and comprehensive named entity extraction.

### Academic Learning Outcomes
- **Technical Skills**: Text preprocessing (NLTK), feature engineering (TF-IDF), ML classification (scikit-learn), and application of core NLP libraries (spaCy, TextBlob, VADER).
- **Business Skills**: Use case design, ROI framing, error analysis, and roadmap planning.

### Final Reflection
This project demonstrates that classical NLP techniques can deliver strong performance for news analysis. It provides a solid foundation for future enhancements like multi-label classification, aspect-based sentiment, and expanded multilingual support.

### Credits
- **Author**: DeMarcus Crump
- **Course**: ITAI 2373 - Natural Language Processing
- **Semester**: Fall 2025

### References
- Misra, R. (2022). News Category Dataset. Kaggle.
- Honnibal & Montani. spaCy.
- Bird et al. NLTK.
- Pedregosa et al. scikit-learn.
- Loria. TextBlob.
- Hutto & Gilbert. VADER.

