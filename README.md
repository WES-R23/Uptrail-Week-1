# Uptrail-Week-1
Data cleaning and analysis project in Excel — identifying and resolving data quality issues, followed by business insight reporting.

**Preface**

This is the first project in my data analytics portfolio, completed as part of an ongoing effort to build practical, end-to-end analytical experience. The goal was to simulate a real-world data pipeline — from receiving messy raw data through to delivering business insights to a stakeholder audience

**Customer Data Cleaning & Analysis — Uptrail Week 1**

**Project Overview**

A full data cleaning and analysis project using two raw datasets — customer sign-up records and support ticket logs — for a fictional SaaS business called Uptrail. The goal was to audit data quality, resolve integrity issues, and generate actionable business insights.
Files

customer_signups.csv — raw sign-up data (messy)
support_tickets.csv — raw support ticket data
Cleaned.xlsx — cleaned and standardised Workbook
Week1_Report.docx — full business insights report

**Data Quality Issues Identified**

Missing values across multiple columns, most critically email (11% missing) — flagged as high risk for marketing operations
Inconsistent casing in categorical fields: plan_selected contained values like basic, BASIC, Basic; gender contained male, Male, MALE, FEMALE etc — standardised using a helper column with a PROPER()/IF() formula approach
Invalid entries: one age recorded as 206, several gender values recorded as "123" — identified via range and type validation checks
Duplicate email across two distinct customer IDs — likely a data entry error, flagged for review
Blank customer ID — structurally invalid as this is a primary key field; raised as a system-level data governance risk

**Cleaning Approach**

Helper columns (Plan Proper, Gender Proper) were added alongside original values rather than overwriting them, preserving a full audit trail of changes made.
Applied PROPER() for name and gender normalisation, manual correction for plan casing
Filtered and flagged invalid/blank records separately rather than deleting them outright
Validated email format visually and cross-referenced for duplicates using COUNTIF()

**Analysis & Insights**

Following cleaning, the data was analysed to answer four business questions covering acquisition source performance, regional data completeness, demographic opt-in behaviour and plan distribution. Key findings included YouTube as the top acquisition channel, Google leading on marketing opt-in rate despite lower sign-up volume, and the 18–24 age group showing the lowest opt-in rate across all demographics.
Full findings and recommendations are in the report.

**Tools Used**

Microsoft Excel — data cleaning, validation, pivot tables, XLOOKUP, COUNTIF, nested IFs
