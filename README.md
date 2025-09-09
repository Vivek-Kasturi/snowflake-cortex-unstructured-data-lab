# Analyzing Unstructured Data with Snowflake Cortex AI

This repository contains my work from the Snowflake Virtual Hands-on Lab: "Build an LLM-Powered App in 10 min with Snowflake Cortex AI". The project demonstrates how to use Snowflake Cortex AI functions to gain insights from various forms of unstructured data.

## Lab Overview

The lab focused on Tasty Bytes, a global food truck company, and used AI to analyze their customer feedback from multiple sources and languages.

## 🔑 Key Learnings & Insights

This lab reinforced critical concepts about the modern data landscape and the power of the Snowflake Data Cloud:

*   **The Unstructured Data Challenge:** A massive 80% of today's enterprise data is unstructured (reviews, images, audio, etc.), with a 60% annual growth rate. Historically, less than 1% of this data is ever analyzed due to the complexity of processing it.
*   **Traditional Challenges:** Working with unstructured data typically involves:
    *   **Format and Schema Variance:** No consistent structure makes it hard to query.
    *   **Siloed and Fragmented Data:** Data locked away in different systems.
    *   **Scale and Performance Limitations:** Traditional tools struggle with the volume and complexity.
*   **The Snowflake Solution:** Snowflake provides an ideal unified platform that is:
    *   **Comprehensive:** Handles all data types (structured, semi-structured, unstructured) in one place.
    *   **AI-Powered:** Cortex AI functions bring the power of large language models (LLMs) directly to the data with simple SQL.
    *   **Secure:** All processing happens within Snowflake's governed and secure environment, ensuring data never leaves the platform.
*   **Real-World Impact:** The lab showcased a real-world scenario from **Nissan Motor Corp**, where using Cortex AI reduced the time to analyze millions of customer feedback records from **6 months down to 1 week**, while achieving 97% accuracy in sentiment analysis.

## Key Features & Cortex Functions Used

- **Translation:** `CORTEX.TRANSLATE()` to convert non-English reviews.
- **Summarization:** `AI_SUMMARIZE_AGG()` to get an overview of customer feedback.
- **Classification:** `AI_CLASSIFY()` to predict if a customer would recommend the service.
- **Sentiment Analysis:** `CORTEX.SENTIMENT()` to gauge customer emotion from text.
- **Image Analysis:** `AI_COMPLETE()` with Anthropic's Claude model to describe images.
- **Audio Transcription:** `AI_TRANSCRIBE()` to convert speech in audio files to text.

## Repository Structure

*   `/sql` - Contains the `setup.sql` script to create the database, schemas, tables, views, and stages.
*   `/notebooks` - Contains the exported Jupyter Notebook (`gaining_insights_from_unstructured_data.ipynb`) with the full analysis code in both Python (Snowpark) and SQL.
*   `README.md` - This file.

## Data

This lab utilizes sample data (customer reviews, images, and audio files) provided by Snowflake and hosted on a public S3 bucket.

**The data is automatically loaded when you run the `setup.sql` script.** The script creates external stages that reference the following location:

`s3://sfquickstarts/tastybytes-voc/`

You do not need to download any data manually. The SQL `COPY INTO` and stage `TO_FILE()` commands will seamlessly ingest the data directly from this source into your Snowflake tables and stages.

## Resources

- [Official Snowflake Quickstart Guide](https://quickstarts.snowflake.com/guide/gain_insights_from_unstructured_data/index.html)
- [Snowflake Cortex AI Documentation](https://docs.snowflake.com/en/user-guide/cortex/cortex-ai)
- *For additional resources on Snowflake Native Apps and upcoming events, please visit the official Snowflake website or attend a future webinar.*
  
## Disclaimer

This is a learning project based on a Snowflake-provided lab. The data and core concepts are from Snowflake Quickstarts.
