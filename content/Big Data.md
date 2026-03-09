---
tags:
  - concept
status: covered
---

# Big Data

> [!info] In short
> When your [[Data]] gets so large, fast, or messy that normal tools like Excel or a single database server just can't handle it anymore.

Imagine you're counting cars on your street — you can do that with a pen and paper. Now imagine counting every car on every road in your entire country, in real time, while also tracking their speed, color, and license plate. Pen and paper won't cut it. You need a completely different approach — multiple people counting simultaneously, radios to coordinate, computers to aggregate. That's the jump from regular data to big data.

The industry usually describes big data using three "V"s. **Volume** is the sheer amount — we're talking terabytes or petabytes of data, not the megabytes you deal with in a spreadsheet. The world generated roughly 400 million terabytes of data per day in 2025, and that number keeps climbing. **Velocity** is how fast data arrives — social media platforms process hundreds of millions of posts daily, stock exchanges handle thousands of transactions per second, and IoT sensors on factory floors stream readings continuously. **Variety** is about the different forms data takes — you've got structured data in databases, but also images, videos, sensor readings, log files, and free-form text. Some people add a fourth V for Veracity (is the data accurate?) and a fifth for Value (is it actually useful?), but the first three capture the core idea.

The problem with big data is that your regular tools break down. You can't open a 50-terabyte file in Excel. You can't run a SQL query on a billion rows with a single laptop. So the solution that emerged was distributed computing — instead of one powerful computer, you spread the work across hundreds or thousands of cheaper machines working in parallel. Hadoop was the pioneer here, built on ideas from Google about how to process massive datasets by splitting them across clusters of commodity hardware. Its file system (HDFS) could store huge amounts of data across many machines. But Hadoop's processing engine (MapReduce) was slow because it read from and wrote to disk constantly. That's where Apache Spark came in — it does the same distributed processing but keeps data in memory, making it up to 100 times faster for certain workloads. Spark has pretty much become the standard for big data processing.

The real game-changer was cloud computing. Before the cloud, if you wanted to do big data processing, you had to buy racks of servers, hire people to maintain them, and you were stuck with that capacity whether you needed it or not. Now, with AWS, Google Cloud, or Azure, you can spin up a massive Spark cluster for a few hours to crunch through your data, and then shut it down — paying only for what you use. Services like Google BigQuery and Amazon Redshift let you run queries on petabytes of data without managing any infrastructure at all. This made big data accessible to companies that aren't Google or Facebook. Real-world examples are everywhere: banks analyzing transaction logs in real time to catch fraud, retailers processing billions of clickstream events to personalize your shopping experience, hospitals aggregating patient data from thousands of IoT-connected medical devices, and streaming services processing viewing habits to power their recommendation engines.

## Related
- [[Data]] - the thing that got too big
- [[Data Engineering]] - big data requires serious engineering to manage
- [[Machine Learning]] - many ML models need big data to train effectively
- [[GPU]] - hardware that accelerates big data and AI workloads
- [[Data Science]] - data scientists work with big data to build models
