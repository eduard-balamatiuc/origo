---
tags:
  - concept
status: covered
---

# Data Science

> [!info] In short
> Combines [[Data]], statistics, and [[Machine Learning]] models to predict what's going to happen and help businesses act on it.

If a data analyst is like a detective who investigates what happened at a crime scene, a data scientist is more like a profiler who predicts where the criminal will strike next. They use the same evidence, but they're trying to get ahead of the future instead of just understanding the past.

Data scientists are often described as the "full stack" people of the data world. They need to understand the business problem, wrangle the data, pick the right statistical or [[Machine Learning]] technique, build a model, and then explain the results to people who don't speak math. A typical project might look like this: a telecom company notices customers are leaving. The data scientist pulls historical customer data, identifies patterns in who churns (maybe people who call support more than three times a month, or whose usage drops suddenly), and builds a model that flags at-risk customers before they cancel. The business can then step in with a retention offer. Other classic projects include recommendation systems (like Netflix suggesting what to watch), demand forecasting (how many units to stock next month), and fraud detection.

The go-to tools are Python and its ecosystem of libraries — pandas for data manipulation, scikit-learn for traditional machine learning, and Jupyter notebooks for the kind of exploratory, iterative work where you want to see results as you go. R is still used in some circles, especially in academia and healthcare. For bigger problems, data scientists use frameworks like TensorFlow or PyTorch to build [[Deep Learning]] models like [[Neural Network|neural networks]].

The role has shifted a lot in the past few years with the rise of [[LLMs]]. A lot of the traditional modeling work — training a classifier, tuning hyperparameters, doing basic feature engineering — is getting faster and partially automated by AI tools. What's becoming more valuable is the ability to work with LLMs directly: knowing how to set up [[RAG]] systems, how to evaluate model outputs, how to [[Fine-Tuning|fine-tune]] a language model on company data, and how to build AI-powered applications. Data scientists who can bridge the gap between old-school ML and the new LLM-driven world are in very high demand. The coding part of the job isn't going away, but the tedious parts are getting automated, which frees data scientists up for the harder, more strategic thinking about what problems to solve and how to frame them.

## Related
- [[Data]] - one half of the equation
- [[Model]] - the other half
- [[Machine Learning]] - the core techniques data scientists use
- [[Data Analysis]] - a related discipline focused on describing, not predicting
- [[Data Engineering]] - provides the clean data pipelines scientists depend on
- [[LLMs]] - reshaping what data scientists work on
- [[Deep Learning]] - used for the most complex modeling tasks
