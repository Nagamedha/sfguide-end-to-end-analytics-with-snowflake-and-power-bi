# sfguide-end-to-end-analytics-with-snowflake-and-power-bi
# End-to-End Analytics Pipeline: Snowflake & Power BI

## Overview
In this guide we will learn how to easily transform raw data into an optimal format for analysis within Power BI. This quickstart will build upon the [An Introduction to Tasty Bytes](https://quickstarts.snowflake.com/guide/tasty_bytes_introduction/index.html?index=..%2F..index#0) quickstart. We'll begin by profiling the data within Snowsight, followed by creating new roles and granting appropriate privileges for our fictitious global BI Analyst team. Next, we'll enrich our data with third party location data from the Snowflake Marketplace in a matter of minutes. From there, we'll transform our raw data into an optimal model for downstream analysis within Power BI. Next, we'll add column and row-level data protections to our data model. Lastly, we'll connect the provided Power BI template (.pbit) file to our Snowflake data model and analyze sales transactions live.

## Project Completion & Technical Achievements

This section documents the successful completion of the end-to-end pipeline, including advanced setup and real-world troubleshooting.

### How This Project is Useful

This lab demonstrates a comprehensive skill set critical for modern Data Engineering and BI Analyst roles:

| Skill Focus | Value Demonstrated |
| :--- | :--- |
| **Cloud Data Modeling** | Implementing an optimized **Star Schema** with **Dynamic Tables (DTs)** shows proficiency in building declarative, low-maintenance ELT pipelines directly within a cloud data warehouse (Snowflake). |
| **Data Governance** | Applying **Row Access Policies** and **Dynamic Masking** confirms the ability to secure sensitive data *at the source* before it reaches the BI layer, a requirement for enterprise-grade compliance. |
| **DevOps Integration** | Successfully linking a **Snowsight Project Workspace** to this Git repository for code synchronization demonstrates practical application of **CI/CD principles** in a data environment. |
| **BI Troubleshooting** | Resolving complex live connection errors (Key errors, Gateway errors) proves the ability to troubleshoot platform-specific issues between MS Power BI and Snowflake. |

---

## ⚙️ Critical Troubleshooting Overcome

Successfully deploying the solution required solving platform compatibility issues specific to a modern setup:

| Challenge | Root Cause & Context | Resolution Implemented |
| :--- | :--- | :--- |
| **Mac/VM Setup Barrier** | Required complex virtualization (VMware Fusion Pro) to run the **Windows-exclusive** Power BI Desktop and open the `.pbit` template. | Successfully configured and used the free **VMware Fusion Pro** (Trial/Personal Use) environment for development. |
| **Git Push Failure** | The initial GitHub **Personal Access Token (PAT)** lacked the required `write` scope for the Snowflake Workspace push. | Updated the PAT permissions on GitHub from `Read-only` to **`Read and write`** to enable successful version control of the code. |
| **Power BI Service Failure** | The published report failed in the cloud ("No Gateway") because the **Data Source Credentials** were not saved correctly after publishing. | Manually updated the **Basic Authentication** (Username/Password) and set the **Privacy Level** to **Organizational** in the Power BI Service Dataset Settings. |

---

### Final Dashboard Validation
The published Power BI dashboard is accessible via the cloud and accurately visualizes the secure data model created in Snowflake. The visual proof of the finished report is available in the repository screenshots.

**Report URL (Private Access):** `https://app.powerbi.com/groups/me/reports/9d64e181-160c-4e9e-8076-d32025effc9e/ReportSection8ef24f75d1188cde0036?experience=power-bi` (Access requires login: `nsakhamuri1@student.gsu.edu`)
## Step-By-Step Guide

For prerequisites, environment setup, step-by-step guide and instructions, please refer to the **[QuickStart Guide](https://quickstarts.snowflake.com/guide/end-to-end-analytics-with-snowflake-and-power-bi/)**. The SQL files within this repository contain the final, working code used for the successful deployment.
