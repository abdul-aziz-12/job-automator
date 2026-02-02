# Automated Job Application Pipeline (n8n + Gemini)

This project is a fully automated job application pipeline built using **n8n**, **Google Sheets**, and **Google Gemini**.

It automates the entire pre-application process — from job discovery to generating tailored cover letters and application answers — with minimal manual effort.

## What it does

### 1. Job Discovery
- Fetches job listings directly from company ATS APIs (e.g. Greenhouse, Lever)
- Supports scheduled runs (daily / weekly) or manual triggers
- Filters roles by:
  - Location (France / EMEA / Remote)
  - Job title keywords (Product, Data, BI, Analyst, etc.)

### 2. Deduplication & Tracking
- Stores all jobs in Google Sheets
- Skips duplicate jobs from previous runs using a unique JobID / hash
- Acts as a lightweight application CRM

### 3. AI-Generated Applications
- Parses job descriptions and application questions
- Uses Google Gemini to generate:
  - A tailored cover letter
  - Answers to application questions (if present)
- Leaves fields blank automatically when questions don’t exist
- Ensures identity consistency using JobID throughout the workflow

### 4. Optional Auto-Fill (Paid Add-On)
- Can be extended with tools like PhantomBuster
- Automatically fills application forms on platforms like:
  - Greenhouse
  - Lever

After the automation runs, the only manual step left is **review and submit**.

## Tech Stack
- n8n (self-hosted)
- Google Sheets
- Google Gemini
- Greenhouse / Lever APIs
- JavaScript (custom logic nodes)

## Use cases
- High-volume job applications
- Consistent, tailored applications
- Reducing repetitive application work
