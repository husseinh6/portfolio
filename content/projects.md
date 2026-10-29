# Projects

## Fraud detection in Apache Spark (2025)

A distributed PySpark pipeline comparing four classification models for mobile-money fraud detection, on a sampled and heavily imbalanced subset of the 6.3 million transaction PaySim dataset. Because raw accuracy is misleading when fraud is rare, I evaluated with F1, recall and MCC instead. Random Forest reached an F1 score of 0.96. Gradient Boosted Trees matched it with perfect recall, catching every fraud case at a small cost in precision. I deliberately left out destination-balance features from an auxiliary regression task to avoid target leakage.

## Autonomous data analyst agent (2026)

An AI agent built on the Anthropic API that cleans messy data and answers plain-English questions against a live MySQL database by writing its own SQL. I added a second, independent validation layer whose only job is to catch the first layer's mistakes. It caught a real bug the agent had introduced itself: outlier-clipping logic that had silently corrupted a bounded rating column. I documented and fixed it rather than hiding it. The agent is deployed live with Streamlit and a cloud MySQL database.

## MSc dissertation: topological data analysis meets NLP (2025)

I designed a framework that adds persistent homology to NLP models, including a differentiable topological loss inside a Skip-gram model, and ran a direct comparison of baseline against enhanced models to test whether the extra complexity was justified. The enhanced models improved F1 by up to 6.88 percent.

## Ground truth: measuring an AI labeller (2026)

For an AI and machine learning mentorship programme I hand-labelled 30 AG News headlines, had a language model label the same 30 through the Groq API, and compared both against the official benchmark labels. The model agreed with the benchmark on 25 of 30 items, a Cohen's kappa of 0.78, against my own 0.47. A simple TF-IDF and logistic regression model trained on 5,700 labelled examples did better than both, at 28 of 30. I also showed data leakage directly: the same model scored 1.00 when tested on data it had seen and 0.62 when tested honestly.

## Newsroom triage app (2026)

A deployed news classification app on Render with a scoring page, retrieval from a small knowledge base, and guardrails, with tests running automatically on GitHub Actions. The supplied app scored 4 of 30. I traced that to two engine bugs: an 80-token limit that left the model no room to answer, and a kappa calculation that silently reported a perfect 1.0. Fixing them took it to 24 of 30, and my prompt took it to 25 of 30 with a kappa of 0.78. I also added a second-opinion feature for low-confidence answers, with tests, taking the suite to 19 passing tests.

## Gaussian process regression for education data (2025)

I compared Gaussian process regression against linear, lasso and ridge regression for predicting student grades from 32 features. The Gaussian process did not win on raw accuracy, but its uncertainty estimates let me flag at-risk students only when the model was both pessimistic and confident, which the linear models could not do.

## NLP stance detection (2025)

A pipeline classifying viewpoints in text on the SemEval-2016 dataset, comparing SVM, naive Bayes and perceptron models against CNN, LSTM and transformer architectures, and judging which approach was justified once performance, interpretability and cost were weighed together.
