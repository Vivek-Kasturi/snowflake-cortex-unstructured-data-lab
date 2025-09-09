# Analyzing Unstructured Data with Snowflake Cortex AI

This repository contains my work from the Snowflake Virtual Hands-on Lab: "Build an LLM-Powered App in 10 min with Snowflake Cortex AI". The project demonstrates how to use Snowflake Cortex AI functions to gain insights from various forms of unstructured data.

## Lab Overview

The lab focused on Tasty Bytes, a global food truck company, and used AI to analyze their customer feedback from multiple sources and languages.

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

## Resources

- [Official Snowflake Quickstart Guide](https://quickstarts.snowflake.com/guide/gain_insights_from_unstructured_data/index.html)
- [Snowflake Cortex AI Documentation](https://docs.snowflake.com/en/user-guide/cortex/cortex-ai)

## Disclaimer

This is a learning project based on a Snowflake-provided lab. The data and core concepts are from Snowflake Quickstarts.

## Data

This lab utilizes sample data (customer reviews, images, and audio files) provided by Snowflake and hosted on a public S3 bucket.

**The data is automatically loaded when you run the `setup.sql` script.** The script creates external stages that reference the following location:

`s3://sfquickstarts/tastybytes-voc/`

You do not need to download any data manually. The SQL `COPY INTO` and stage `TO_FILE()` commands will seamlessly ingest the data directly from this source into your Snowflake tables and stages.
