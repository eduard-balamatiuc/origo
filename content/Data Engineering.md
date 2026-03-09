---
tags:
  - concept
status: covered
---

# Data Engineering

> [!info] In short
> Building and maintaining the plumbing that moves [[Data]] from where it's created to where it's useful — clean, reliable, and on time.

Think of a city's water system. Someone has to build the pipes, pumps, and treatment plants that take water from rivers and lakes, clean it, and deliver it to your tap. You don't think about it until it breaks. Data engineers do the same thing but for data — they build the pipelines that collect raw data from dozens of sources, clean out the junk, and deliver it in a usable format to the people who need it.

Data in any real company is a mess. You've got customer records in one database, website clicks in another, sales numbers in a spreadsheet someone emailed around, and support tickets in yet another system. None of it uses the same formats, some of it has gaps, and half of it is duplicated. Data engineers are the people who wrangle all of that into something usable. Their day-to-day involves building what the industry calls ETL pipelines — Extract data from various sources, Transform it (clean it, reformat it, combine it), and Load it into a central place like a data warehouse where analysts and data scientists can actually work with it.

The tools of the trade include things like Apache Airflow for scheduling and orchestrating pipelines (basically telling the system "run this job every night at 2am, and if it fails, alert someone"), Apache Spark for processing large volumes of data fast, and cloud platforms like AWS, Google Cloud, or Azure that provide managed services for storage and computation. A lot of modern data engineering has shifted to what's called ELT — you load the raw data first into a powerful cloud warehouse like Snowflake or BigQuery, and then transform it there. The cloud changed the game because you no longer need to buy and maintain your own servers.

This role exists because without it, nothing else in the [[Data Science]] or [[Data Analysis]] world works. You can have the smartest data scientist on the planet, but if the data they're working with is stale, incomplete, or scattered across fifteen systems, their models are going to be garbage. Data engineers are the unsung heroes who make sure the data is actually there, actually correct, and actually fresh when someone needs it. As companies have started building more [[AI]] and [[Machine Learning]] systems, data engineers have taken on even more responsibility — they now often manage feature stores (organized collections of data specifically prepared for ML models) and vector databases that power things like [[RAG]].

## Related
- [[Data]] - what data engineering works with
- [[Data Analysis]] - analysts depend on the pipelines engineers build
- [[Data Science]] - data scientists need clean, reliable data to build models
- [[Big Data]] - when scale demands serious engineering
- [[Machine Learning]] - data engineers increasingly support ML infrastructure
