# SC-900 — Section 4, Module 4
# Describe the Data Governance Solutions of Microsoft Purview

> **Source:** Microsoft Learn — SC-900  
> **Learning Path:** Introduction to Microsoft Purview and Microsoft's privacy principles  
> **Module:** Describe the data governance solutions of Microsoft Purview  
> **Verified against current Microsoft Learn content:** November 23, 2026  
> **Duration:** 23 minutes | 6 units | 700 XP  
> **Official Module:** https://learn.microsoft.com/en-us/training/modules/describe-purview-data-governance/

---

# Important Product Lifecycle Update — November 2026

**Microsoft announced the retirement of Microsoft Purview Data Governance on November 12, 2026.**

This retirement includes:

- Microsoft Purview Data Map
- Microsoft Purview Unified Catalog
- Related data governance workflows
- Classic Azure Purview governance capabilities

**End of support: November 12, 2027**

New Purview data governance accounts can no longer be created. Existing capabilities remain in maintenance mode during the transition.

Microsoft is shifting its data governance strategy toward:

**Microsoft Fabric + OneLake catalog**

The retirement does **not** apply to the broader Microsoft Purview product family.

**Microsoft Purview Data Security and Data Compliance remain supported.**

## Why These Notes Still Matter

The current SC-900 Microsoft Learn module continues to teach Data Map and Unified Catalog.

Therefore, these notes preserve the module's concepts and feature descriptions while documenting Microsoft's newly announced product transition.

The underlying principles—metadata management, data discovery, quality, stewardship, access governance, and accountability—remain applicable to current and future data governance platforms.

**Official announcement:**

https://techcommunity.microsoft.com/blog/microsoft-security-blog/a-next-step-in-the-evolution-of-the-microsoft-data-governance-strategy/4572227

---

# Module Overview

Data governance helps organizations understand, manage, secure, and use their information appropriately.

Modern organizations store information across many environments.

Examples include:

- Databases
- File servers
- Cloud storage
- Business applications
- Data warehouses
- Analytics platforms
- On-premises systems
- Multiple cloud providers

Without effective governance, organizations may struggle to determine what information exists, who owns it, whether it is trustworthy, and how it should be used.

Microsoft Learn introduces two primary Purview data governance solutions:

**Microsoft Purview Data Map**

**Microsoft Purview Unified Catalog**

## The Big Idea

**Data Map discovers and describes organizational data.**

**Unified Catalog organizes, explains, and governs that data for business use.**

### ELI5

Imagine a military organization maintaining thousands of records across multiple installations and departments.

Some information is stored in shared folders.

Other information resides in databases, cloud applications, and local systems.

Personnel need to find relevant records, determine whether those records are accurate, and understand whether they are authorized to use them.

**Data Map** creates an inventory describing the available information.

**Unified Catalog** organizes the inventory into understandable business categories and provides governance capabilities.

### Master Memory Trick

**DATA MAP = WHAT DATA EXISTS, AND WHERE?**

**UNIFIED CATALOG = WHAT DOES IT MEAN, AND HOW SHOULD IT BE USED?**

---

# 1. What Is Data Governance?

## Big Idea

Data governance refers to the policies, processes, responsibilities, standards, and controls used to manage organizational information.

It helps ensure data is:

**Discoverable**

**Accurate**

**Trustworthy**

**Secure**

**Compliant**

**Useful**

Data governance is not simply preventing unauthorized access.

It also helps organizations obtain meaningful value from their information.

### ELI5

Imagine two departments maintaining separate spreadsheets showing the same equipment inventory.

One spreadsheet lists 120 vehicles.

The other lists 135.

Neither identifies when the information was updated.

Nobody knows which department owns the authoritative record.

The organization has a data governance problem.

Effective governance would establish who owns the information, how accuracy is verified, and which source should be trusted.

### Memory Trick

**Data Governance = Manage information so it can be trusted and used appropriately**

---

# 2. Why Data Governance Matters

Organizations increasingly rely on information for:

- Daily operations
- Business decisions
- Financial reporting
- Regulatory compliance
- Automation
- Artificial intelligence
- Strategic planning

Poorly governed information can produce:

- Inaccurate reports
- Duplicate records
- Unauthorized access
- Inconsistent business decisions
- Unreliable AI outputs
- Compliance difficulties

### Important Concept

**Data that is available is not necessarily data that is trustworthy.**

An organization needs visibility into data quality, ownership, meaning, and appropriate use.

---

# 3. Data Governance and Artificial Intelligence

The current Microsoft Learn module emphasizes that AI increases the importance of effective data governance.

AI applications depend on trustworthy information.

When an AI system processes incomplete, inconsistent, outdated, or incorrectly classified data, its results may be unreliable.

### Example

An AI assistant generates a report using two conflicting equipment inventories.

One inventory is outdated.

The other contains duplicate records.

The AI assistant may produce an inaccurate report even if the model itself functions correctly.

### ELI5

An AI system cannot automatically correct every problem in the information it receives.

Providing better-governed information improves the foundation for reliable analysis.

### Memory Trick

**Poor Data Quality → Unreliable AI Results**

---

# 4. Five Core Data Governance Concepts

Microsoft Learn identifies five concepts.

| Concept | Primary purpose |
|---|---|
| Data Access | Provide appropriate access and enforce proper use |
| Data Curation | Organize, annotate, and publish usable data |
| Data Discovery | Help users find relevant information |
| Data Health | Maintain data quality and lifecycle standards |
| Data Understanding | Explain what data means and how it should be used |

These concepts work together.

---

# 5. Data Access

## Big Idea

Data access concerns providing the right people with appropriate access to information.

It balances:

**Security**

and

**Usability**

### ELI5

An employee needs financial data to perform an authorized task.

The employee should not have to navigate unnecessary administrative obstacles.

However, the system must still enforce appropriate restrictions.

### Example

A financial analyst requests access to an approved reporting dataset.

The request follows the organization's access governance process.

Authorized access is granted according to the applicable policy.

### Memory Trick

**DATA ACCESS = Right person, right information, appropriate use**

---

# 6. Data Curation

## Big Idea

Data curation involves organizing, annotating, and publishing data so it is understandable, reusable, and appropriately protected.

### ELI5

Imagine entering a storage room containing hundreds of unlabeled boxes.

The supplies may be valuable, but nobody can easily find or understand them.

A properly organized storage room has:

- Clear labels
- Logical categories
- Accurate descriptions
- Assigned responsibility
- Instructions for appropriate use

Data curation provides comparable organization for information.

### Example

A database table is named:

`tbl_fin_042`

Most employees cannot determine its purpose.

A data steward adds a meaningful description explaining that it contains approved quarterly financial reporting information.

The data becomes easier to discover and understand.

### Memory Trick

**DATA CURATION = Organize, describe, and prepare data for use**

---

# 7. Data Discovery

## Big Idea

Data discovery helps users locate information relevant to their work.

### ELI5

Imagine searching for the authoritative personnel-strength report.

The information may exist, but it provides little value if employees cannot locate it.

Data discovery helps users find the right source.

### Example

An analyst searches a catalog for:

> Monthly transportation performance data

The catalog returns relevant data assets or data products.

### Memory Trick

**DATA DISCOVERY = Find the information**

---

# 8. Data Health

## Big Idea

Data health concerns the overall quality, reliability, security, and lifecycle condition of organizational information.

### Example

A customer database contains:

- Duplicate customer records
- Missing addresses
- Outdated phone numbers
- Inconsistent account identifiers

Those problems reduce data health.

### ELI5

Think of data health as an inspection of the condition of information.

Even if the data is stored securely, it may not be suitable for business decisions if it is incomplete or inaccurate.

### Memory Trick

**DATA HEALTH = Is the information reliable and maintained?**

---

# 9. Data Understanding

## Big Idea

Data understanding provides the context needed to interpret information correctly.

Examples of useful context include:

- Business definitions
- Descriptions
- Data ownership
- Classification
- Relationships
- Appropriate-use requirements

### Example

A report contains a column named:

`Active`

Does this mean:

- Currently employed?
- Currently assigned to a unit?
- Recently logged into a system?
- Financially active?

Without a clear business definition, users may interpret the same value differently.

### Memory Trick

**DATA UNDERSTANDING = Know what the information actually means**

---

# 10. Data Discovery vs. Curation vs. Understanding

These concepts are closely related but different.

| Concept | Question |
|---|---|
| Data Discovery | Where is the information? |
| Data Curation | How is the information organized and described? |
| Data Understanding | What does the information mean? |
| Data Health | Is the information trustworthy and maintained? |
| Data Access | Who can use it? |

### Exam Shortcut

**Organize, annotate, and publish data = Data Curation**

This distinction appears directly in the current Microsoft Learn assessment.

---

# 11. Federated Data Governance

## Big Idea

Federated governance combines centralized standards with distributed responsibility.

Organizations establish common policies and expectations while allowing individual departments or business areas to manage their own information.

### ELI5

Imagine a military organization establishing one records-management standard.

Every battalion follows the same general requirements.

However, each battalion is responsible for maintaining accurate records within its own area.

Central leadership defines the standards.

Individual units manage their information.

That is the basic idea behind federated governance.

---

# 12. Why Federated Governance Matters

A purely centralized model may create bottlenecks.

Every data-related decision could require approval from one central office.

A completely decentralized model may create inconsistency.

Different departments might use conflicting definitions, standards, and procedures.

Federated governance attempts to balance both approaches.

| Central Governance | Distributed Ownership |
|---|---|
| Establish common standards | Maintain department-specific data |
| Define organizational policies | Apply policies locally |
| Monitor enterprise-wide health | Correct local data-quality problems |
| Provide oversight | Improve business-specific information |

### Memory Trick

**Federated Governance = Central standards + Distributed accountability**

---

# 13. Data Governance Roles

Microsoft Learn identifies four major roles.

**Data Consumers**

**Data Owners**

**Data Stewards**

**Central Data Office**

Each has different responsibilities.

---

# 14. Data Consumers

## Big Idea

Data consumers are people or systems that use information to accomplish business objectives.

Examples include:

- Business analysts
- Managers
- Researchers
- Report developers
- Other authorized users

### Primary Responsibilities

Find relevant information and use it appropriately.

### ELI5

A logistics analyst needs a reliable transportation dataset.

The analyst searches the catalog and requests access.

The analyst is the data consumer.

### Memory Trick

**DATA CONSUMER = Uses the information**

---

# 15. Data Owners

## Big Idea

Data owners are accountable for particular data assets and their appropriate management.

Microsoft Learn identifies responsibilities involving:

- Registering data assets
- Managing classification
- Managing access
- Maintaining quality expectations

### ELI5

A finance director may be responsible for the organization's official financial reporting data.

The director establishes how that information should be governed and who should be authorized to use it.

### Memory Trick

**DATA OWNER = Accountable for the data**

---

# 16. Data Stewards

## Big Idea

Data stewards help maintain the quality, discoverability, definitions, and relationships of information.

The current module emphasizes:

- Data quality
- Data discovery
- Glossary consistency
- Data lineage

### ELI5

The data owner establishes accountability.

The data steward helps ensure the information is properly organized, accurately described, and maintained.

### Example

A data steward identifies that two departments use different names for the same business metric.

The steward works to establish a consistent definition.

### Memory Trick

**DATA STEWARD = Maintains quality and meaning**

---

# 17. Central Data Office

## Big Idea

The central data office establishes and oversees organizational data governance standards.

It may be responsible for:

- Governance policy
- Metadata standards
- Compliance alignment
- Enterprise-wide governance health
- Oversight and accountability

### ELI5

The central data office establishes the overall governance framework.

Data owners and stewards apply that framework within their areas.

### Memory Trick

**CENTRAL DATA OFFICE = Enterprise governance oversight**

---

# 18. Data Governance Roles Compared

| Role | Main responsibility |
|---|---|
| Data Consumer | Find and use trusted information |
| Data Owner | Be accountable for data assets |
| Data Steward | Maintain data quality and business context |
| Central Data Office | Establish governance standards and oversight |

### Example

An organization maintains a transportation database.

**Data Consumer:** Analyst preparing monthly reports.

**Data Owner:** Leader responsible for the transportation data.

**Data Steward:** Specialist maintaining definitions and quality.

**Central Data Office:** Organizational governance team defining common requirements.

---

# 19. Data Governance Benefits

The current module groups benefits by audience.

## Benefits for Data Consumers

**Data Discovery**

Find information more easily.

**Secure Access**

Request and obtain appropriate permissions.

**Data Understanding**

Understand what the data represents.

## Benefits for Data Owners and Stewards

**Data Curation and Management**

Produce useful, understandable datasets.

**Responsible Data Use**

Ensure information is used appropriately.

**Impact Analysis**

Understand changes or issues affecting the data.

## Benefits for Data Leadership

**Data Value Creation**

Improve organizational use of information.

**Standardization**

Apply common practices across departments.

### Important Concept

**Good governance improves both security and the practical value of data.**

---

# 20. Microsoft Purview Data Map

## Big Idea

Microsoft Purview Data Map provides the metadata foundation for data discovery and governance.

It identifies and describes organizational data assets across supported environments.

Examples include:

- Databases
- Tables
- Files
- Reports
- Analytics systems
- SaaS applications
- On-premises data sources
- Multicloud services

### ELI5

Think of a library catalog.

The catalog tells you:

**Which books exist?**

**Where are they?**

**What subjects do they cover?**

**How are they organized?**

Data Map performs a comparable function for data assets.

### Master Memory Trick

**DATA MAP = Automated inventory of data metadata**

---

# 21. What Is Metadata?

## Big Idea

**Metadata = Data about data**

Metadata describes information without necessarily containing the underlying content.

### Example

Imagine an Excel spreadsheet containing employee records.

The spreadsheet's underlying data might include employee names and personnel details.

Metadata might include:

- File name
- Storage location
- Column names
- Data types
- Document description
- Classification
- Relationships to other assets

### ELI5

A library catalog describes a book without reproducing the entire book.

Data Map describes data assets without storing all their underlying data in the catalog.

---

# 22. Critical Data Map Security Distinction

Microsoft Learn explicitly states that Data Map stores **metadata, not the underlying data itself**.

Data Map permissions do not automatically grant access to the actual data.

### Example

An employee can view metadata describing a database.

That does not mean the employee can open the database and read every record.

Access to the source data still depends on the appropriate authorization controls.

### Memory Trick

**DISCOVERING DATA ≠ ACCESSING DATA**

This is one of the most important security concepts in the module.

---

# 23. Data Map Scanning

## Big Idea

Data Map uses scanning to discover data assets and capture metadata.

A scan can identify:

- Available assets
- Structures
- Locations
- Relationships
- Classifications

### ELI5

Imagine automatically inspecting several storage facilities and generating an updated inventory.

The inventory identifies the available items and their characteristics.

Data Map performs a comparable function for connected data sources.

---

# 24. Data Map Scanning Workflow

```text
Connected Data Sources
         |
         v
Data Map Scanning
         |
         v
Discover Data Assets
         |
         v
Capture Metadata
         |
         v
Apply Supported Classifications
         |
         v
Maintain Data Inventory
```

### Example

An organization connects an Azure SQL database.

Data Map scans the supported data source.

The scan identifies tables, column names, data types, and other metadata.

The resulting catalog information helps administrators understand the database structure.

---

# 25. Automated Data Classification

Data Map can apply classifications to discovered assets.

These help identify information such as:

- Personal information
- Financial information
- Other sensitive categories

Microsoft Learn describes:

**Built-in classifications**

and

**Custom classifications**

## Built-In

Microsoft-provided detection patterns and rules.

## Custom

Organization-defined classifications.

### Example

A database column appears to contain personal identification information.

Data Map records the applicable classification metadata.

### Important Distinction

**Data Map Classification = Describe sensitive characteristics of data assets**

**Purview Sensitivity Labels = Classify and potentially enforce protection on supported content**

Classification metadata alone does not automatically grant or restrict access to the underlying data.

---

# 26. Four Types of Metadata

Microsoft Learn identifies four categories.

| Metadata type | Purpose |
|---|---|
| Technical | Describe the structure of information |
| Business | Explain information in business terms |
| Semantic | Describe organization and classification |
| Operational | Describe processing activity |

### Memory Trick

**TECHNICAL → STRUCTURE**

**BUSINESS → MEANING**

**SEMANTIC → ORGANIZATION**

**OPERATIONAL → PROCESSING**

---

# 27. Technical Metadata

## Big Idea

Technical metadata describes the structure and technical characteristics of data.

Examples include:

- Database schemas
- Column names
- Data types
- Tables
- Technical asset properties

### Example

```text
Table: Vehicle_Inventory

Vehicle_ID: Integer
Vehicle_Type: Text
Unit_Assigned: Text
Last_Updated: Date
```

This describes how the data is structured.

### Memory Trick

**TECHNICAL METADATA = How the data is organized technically**

---

# 28. Business Metadata

## Big Idea

Business metadata explains the meaning, purpose, and business context of information.

Examples include:

- Business descriptions
- Glossary terms
- Documented definitions
- Business annotations

### Example

Technical field:

`Vehicle_Status`

Business description:

> Indicates whether the vehicle is operationally available for assigned transportation requirements.

### ELI5

Technical metadata explains what the column looks like.

Business metadata explains what the column means.

### Memory Trick

**BUSINESS METADATA = What the information means to the organization**

---

# 29. Semantic Metadata

## Big Idea

Semantic metadata describes how information is organized and classified.

Microsoft Learn identifies examples including:

- Collection mappings
- Classification information

### Example

A data source belongs to a particular organizational collection and contains classified financial information.

Semantic metadata helps describe these relationships and categories.

### Memory Trick

**SEMANTIC METADATA = How information is categorized and related**

---

# 30. Operational Metadata

## Big Idea

Operational metadata describes activity involving data processing.

Examples include:

- Processing status
- Execution time
- Last processing activity
- Run information

### Example

An automated data pipeline runs every morning.

Operational metadata identifies when the process last ran and whether the operation completed successfully.

### Memory Trick

**OPERATIONAL METADATA = What happened during data processing**

---

# 31. Metadata Types Compared

| Question | Metadata type |
|---|---|
| What are the column names? | Technical |
| What does this field mean? | Business |
| Which category or collection contains the data? | Semantic |
| When was the processing job executed? | Operational |

### Exam Shortcut

**Schema or data type = Technical**

**Glossary description = Business**

**Collection or classification mapping = Semantic**

**Execution status = Operational**

---

# 32. Multicloud and Hybrid Data Discovery

The current module describes Data Map support for data sources distributed across multiple environments.

Examples include:

**Microsoft Azure**

**Amazon Web Services (AWS)**

**Google Cloud**

**On-Premises Systems**

**Software-as-a-Service Applications**

### ELI5

An organization does not need to store every dataset in Azure for Data Map to discover metadata from supported sources.

The governance objective is broader visibility across the organization's information estate.

### Memory Trick

**Data Map = Metadata visibility across supported hybrid and multicloud sources**

---

# 33. Data Map and AI Readiness

Data Map classifications help organizations identify potentially sensitive information before it is used with AI systems.

### Example

A business team wants to use customer data for machine-learning analysis.

The governance team needs to understand:

- Where the relevant dataset is stored
- Which fields contain personal information
- Who owns the data
- Whether the dataset is appropriately classified

Data Map can help establish that visibility.

### Important Concept

**Metadata discovery supports AI governance, but does not itself authorize AI use of the data.**

---

# 34. Microsoft Purview Unified Catalog

## Big Idea

Unified Catalog provides the business-facing governance capabilities built on Data Map's metadata inventory.

It helps users:

- Find relevant information
- Understand its meaning
- Organize data into business areas
- Discover data products
- Review governance requirements
- Request appropriate access
- Evaluate data quality
- Monitor data health

### ELI5

Data Map produces an inventory.

Unified Catalog turns that inventory into a useful organizational catalog.

### Master Memory Trick

**DATA MAP = Discover and describe**

**UNIFIED CATALOG = Organize, understand, and govern**

---

# 35. Data Map vs. Unified Catalog

| Data Map | Unified Catalog |
|---|---|
| Discover data assets | Organize assets into business categories |
| Scan supported sources | Build governance domains |
| Capture metadata | Define data products |
| Record classifications | Manage business glossary terms |
| Maintain asset inventory | Manage data quality and health |
| Describe technical characteristics | Support access governance |

### Critical Exam Concept

**Data Map captures metadata. Unified Catalog uses that metadata to support business governance.**

---

# 36. Governance Domains

## Big Idea

A governance domain organizes data around a business concept, organizational function, or subject area.

Examples include:

- Human Resources
- Finance
- Sales
- Supply Chain
- Business Intelligence
- Customer Experience

### ELI5

Imagine organizing records by responsible department.

A Finance domain contains financial information.

A Human Resources domain contains personnel-related information.

A Supply Chain domain contains relevant logistics and procurement information.

### Memory Trick

**GOVERNANCE DOMAIN = Business-oriented data organization**

---

# 37. Governance Domain Responsibilities

A governance domain provides a boundary for:

- Data ownership
- Data products
- Glossary terms
- Critical data
- Objectives and key results
- Applicable governance requirements

### Example

```text
Governance Domain: Supply Chain
│
├── Data Products
├── Business Glossary Terms
├── Critical Data Elements
├── Governance Objectives
└── Access Policies
```

### Important Concept

Governance domains distribute responsibility while maintaining common organizational standards.

This connects directly to federated governance.

---

# 38. Data Products

## Big Idea

A data product is a business-oriented grouping of related data assets.

Microsoft Learn describes data products as having:

- A name
- A description
- An owner
- Associated data assets
- A business use case

### ELI5

Imagine a logistics analyst needs information about vehicle readiness.

That information is spread across:

- An equipment database
- A maintenance database
- A reporting dataset

A data product can group those assets into one discoverable business package.

### Memory Trick

**DATA PRODUCT = Related data assets packaged for a business purpose**

---

# 39. Data Product Example

```text
Data Product: Fleet Readiness Reporting
│
├── Vehicle Inventory Dataset
├── Maintenance Status Dataset
├── Equipment Availability Dataset
└── Monthly Readiness Report
```

The data product helps consumers understand how those assets support fleet-readiness analysis.

### Important Distinction

A data product does not necessarily create another physical copy of every dataset.

It is a business construct that associates relevant data assets with a defined use case.

---

# 40. Data Products and Governance Domains

The current module explains that a data product is managed by one governance domain but can be discovered across different domains.

### Example

A data product is managed by the Finance domain.

Employees from Supply Chain may discover that product because it supports procurement analysis.

### Important Concept

**Governance ownership and data discoverability are not the same thing.**

Data can be discoverable across business areas while still having clearly assigned ownership.

---

# 41. Glossary Terms

## Big Idea

Glossary terms establish consistent business definitions.

They help employees understand the meaning of information across departments and systems.

### ELI5

Imagine two departments using the word:

> Readiness

One department defines readiness as equipment operational status.

Another defines readiness as personnel availability.

Without clear definitions, reports may be misunderstood.

A business glossary helps establish the intended meaning of organizational terms.

### Memory Trick

**GLOSSARY TERM = Shared business definition**

---

# 42. Glossary Terms and Governance

Microsoft Learn describes glossary terms as more than static definitions.

They can also carry governance information, including policies associated with business concepts.

### Example

A glossary term identifies:

**Customer Personal Information**

The term includes relevant data-handling and governance expectations.

Data assets associated with that business concept can be governed using the applicable policies.

### Important Concept

**Glossary terms provide meaning and can help apply business-context governance.**

---

# 43. Critical Data Elements — CDEs

## Big Idea

A Critical Data Element represents information that is especially important to an organization.

Not every field in every database requires equal governance attention.

Organizations identify critical elements and apply stronger quality and governance requirements where appropriate.

### ELI5

Imagine an organization maintains a large personnel database.

Some fields are less important to operational decision-making.

Other fields are essential.

Examples might include:

- Employee identifier
- Duty status
- Unit assignment
- Required qualification status

These may require particularly accurate and consistent treatment.

### Memory Trick

**CDE = Important data element requiring focused governance**

---

# 44. Critical Data Element Example

The current module describes an example involving inconsistent customer identifier names.

Database A uses:

`CustID`

Database B uses:

`CID`

Both represent the same business concept:

**Customer ID**

A Critical Data Element can provide one common logical definition.

### Conceptual Example

```text
Critical Data Element: Customer ID
              |
       +------+------+
       |             |
       v             v
     CustID          CID
   Database A     Database B
```

### Why It Matters

Organizations can standardize terminology and expectations across different systems.

Critical data elements can also have associated data quality rules and access policies.

---

# 45. Critical Data Elements vs. Glossary Terms

These concepts are related but different.

## Glossary Term

Defines a business concept.

## Critical Data Element

Identifies an important logical data element requiring focused management.

### Example

**Glossary Term:** Customer

Defines what the organization considers a customer.

**Critical Data Element:** Customer ID

Establishes the importance and consistent interpretation of customer identifiers across systems.

### Memory Trick

**GLOSSARY = Define the concept**

**CDE = Govern the critical information element**

---

# 46. Objectives and Key Results — OKRs

## Big Idea

OKRs connect organizational objectives with measurable outcomes.

**OKR = Objectives and Key Results**

### Objective

What does the organization want to accomplish?

### Key Result

How will the organization measure progress?

### ELI5

Imagine a logistics department establishes:

**Objective:** Improve equipment-readiness reporting.

**Key Result:** Reduce discrepancies between authoritative datasets.

The department can connect relevant data products to those goals.

### Memory Trick

**OBJECTIVE = Desired outcome**

**KEY RESULT = Measurable progress**

---

# 47. Why OKRs Belong in Data Governance

Data governance should provide business value, not merely enforce technical rules.

OKRs help organizations connect governance work to practical objectives.

### Example

A company invests in improving the accuracy of customer records.

The project should support a meaningful business objective, such as improving service delivery or reducing reporting errors.

### Important Concept

**Data governance should support measurable organizational outcomes.**

---

# 48. Unified Catalog Access Policies

## Big Idea

Unified Catalog provides capabilities for governing access to data products.

These can support self-service access requests.

### ELI5

An analyst discovers a useful data product.

The analyst does not automatically receive unrestricted access.

Instead, the analyst requests access through an appropriate process.

The organization evaluates whether the request is authorized.

### Memory Trick

**ACCESS POLICY = Govern who may use the data product**

---

# 49. Self-Service Data Access

Self-service access enables users to request appropriate permissions without navigating unnecessarily complex processes.

### Example

A financial analyst needs an approved reporting dataset.

The analyst locates the relevant data product.

The analyst submits a request.

The organization uses configured governance and approval controls to manage the request.

### Important Concept

**Self-service does not mean unrestricted access.**

Authorization remains important.

---

# 50. Search and Browse

Unified Catalog provides two complementary discovery experiences.

## Search

Useful when the user knows what they want.

### Example

Search for:

> Customer Revenue Data

## Browse

Useful when the user wants to explore available information.

### Example

Open a Finance governance domain and examine its data products.

### Memory Trick

**SEARCH = I know what I'm looking for**

**BROWSE = Show me what is available**

---

# 51. AI-Powered Catalog Search

The current Microsoft Learn module describes an AI-powered copilot within Unified Catalog.

Users can search using natural language.

### Example

Instead of knowing the exact asset name, an analyst asks:

> Find datasets that can be used to analyze monthly transportation performance.

The AI-powered experience helps identify potentially relevant catalog entries.

### Important Concept

**AI-powered discovery makes data easier to find without removing underlying access requirements.**

The catalog can explain what exists, but access to the source data must still be appropriately authorized.

---

# 52. Data Health Management

## Big Idea

Unified Catalog includes features for monitoring and improving data governance health.

Microsoft Learn emphasizes:

**Health Controls**

**Health Actions**

**Data Quality**

These features work together.

### Memory Trick

**CONTROL = Measure**

**ACTION = Improve**

**QUALITY = Assess the information itself**

---

# 53. Data Health Controls

## Big Idea

Health controls assess how well data governance requirements are being satisfied.

Examples of objectives include:

- Improve data quality
- Improve security
- Support regulatory compliance
- Increase operational efficiency

### ELI5

Imagine an inspection checklist evaluating whether a dataset has:

- A designated owner
- An appropriate description
- Relevant classifications
- Adequate quality information

Health controls help evaluate governance maturity and condition.

---

# 54. Data Health Actions

## Big Idea

Health actions are recommended steps for improving governance health.

### Example

A data product lacks an owner or sufficient descriptive metadata.

The catalog identifies a corrective action.

A responsible data steward updates the required information.

### Important Concept

Addressing health actions can improve a product's governance health score.

### Memory Trick

**HEALTH CONTROL = What needs improvement?**

**HEALTH ACTION = What should be fixed?**

---

# 55. Data Quality

## Big Idea

Data quality concerns the reliability and suitability of information.

Unified Catalog supports:

- No-code quality rules
- Low-code quality rules
- Built-in quality checks
- AI-generated quality-rule suggestions
- Data quality scores

### ELI5

Imagine a personnel database containing thousands of records.

A data quality rule could identify records missing required information.

Another rule could identify duplicate identifiers.

These checks help determine whether the data is reliable.

---

# 56. Common Data Quality Dimensions

The following provides supplemental context commonly used in data governance.

| Dimension | Question |
|---|---|
| Accuracy | Is the information correct? |
| Completeness | Are required values present? |
| Consistency | Do related systems agree? |
| Timeliness | Is the information current? |
| Uniqueness | Are records unnecessarily duplicated? |
| Validity | Does information meet expected formats and rules? |

### Example

An equipment inventory contains:

- Incorrect vehicle types — Accuracy problem
- Missing assignment fields — Completeness problem
- Conflicting status records — Consistency problem
- Outdated inspection dates — Timeliness problem
- Duplicate vehicle identifiers — Uniqueness problem
- Improperly formatted serial numbers — Validity problem

### Memory Trick

**High-quality data is correct, complete, consistent, current, nonduplicative, and valid.**

---

# 57. Data Quality Scores

Unified Catalog can aggregate data quality results at different levels.

The current module identifies:

**Data Asset**

**Data Product**

**Governance Domain**

### Example

```text
Governance Domain: Finance
          |
          v
Data Product: Quarterly Reporting
          |
          v
Data Assets and Quality Rules
```

Quality results can contribute to broader reporting across the domain.

### Important Concept

**A data quality score measures information quality, not the effectiveness of every cybersecurity control.**

---

# 58. AI-Generated Data Quality Rules

The current Learn module describes AI-generated quality-rule suggestions.

These help reduce the manual effort required to establish quality monitoring.

### Example

An AI feature analyzes a dataset and suggests a rule requiring a particular identifier field to be populated.

A data owner or steward reviews the recommendation.

### Important Principle

AI-generated rules should be evaluated for correctness and business relevance.

A technically reasonable rule may still be inappropriate for a particular dataset.

---

# 59. AI-Assisted Data Curation

Unified Catalog can provide AI-enabled recommendations for improving metadata.

These may help identify gaps affecting data discoverability.

### Example

A dataset has a technical name but no useful business description.

An AI-assisted feature suggests improvements.

A data steward reviews and applies appropriate changes.

### Memory Trick

**AI Curation = Help improve how data is described and discovered**

---

# 60. Data Lineage

## Additional Data Governance Context

Data lineage describes how information moves and changes between sources and downstream systems.

The module identifies lineage as an important responsibility for data stewards.

### ELI5

Imagine a final readiness report.

The numbers in that report came from several databases and spreadsheets.

Data lineage helps establish where the information originated and how it reached the report.

### Example

```text
Vehicle Maintenance System
          |
          v
Data Transformation
          |
          v
Readiness Dataset
          |
          v
Monthly Readiness Report
```

### Why It Matters

Lineage can help organizations investigate:

- Inaccurate reporting
- Unexpected data changes
- Broken data pipelines
- Downstream impacts
- Data ownership issues

### Memory Trick

**DATA LINEAGE = Where did the information come from, and where did it go?**

---

# 61. Data Map and Unified Catalog Together

Microsoft Learn presents Data Map and Unified Catalog as complementary solutions.

## Step 1 — Connect Data Sources

Register and connect supported organizational data sources.

## Step 2 — Scan the Sources

Data Map scans for data assets and metadata.

## Step 3 — Capture Metadata

Record structures, descriptions, classifications, and relationships.

## Step 4 — Organize Business Context

Unified Catalog uses the metadata to create business-oriented governance domains.

## Step 5 — Curate Data Products

Related data assets are organized into discoverable business products.

## Step 6 — Apply Business Definitions

Glossary terms and critical data elements establish meaning and standards.

## Step 7 — Govern Access

Appropriate access policies manage how users request and receive access.

## Step 8 — Monitor Quality and Health

Health controls, actions, and quality rules support ongoing improvement.

### Complete Conceptual Architecture

```text
ORGANIZATIONAL DATA SOURCES
Azure | AWS | GCP | On-Premises | SaaS
                  |
                  v
       MICROSOFT PURVIEW DATA MAP
                  |
          Scan Data Sources
                  |
          Capture Metadata
                  |
        Classify Data Assets
                  |
                  v
       MICROSOFT PURVIEW UNIFIED CATALOG
                  |
       +----------+-----------+
       |          |           |
       v          v           v
 Governance    Data       Glossary Terms
  Domains     Products    and Critical Data
       |          |           |
       +----------+-----------+
                  |
                  v
         BUSINESS DATA GOVERNANCE
                  |
       +----------+-----------+
       |          |           |
       v          v           v
  Discovery   Access       Data Quality
              Policies     and Health
```

**This diagram describes the architecture taught in the Microsoft Learn module. It is not a recommended new deployment architecture following Microsoft's November 2026 retirement announcement.**

---

# 62. Data Governance vs. Data Security

These subjects overlap but have different primary objectives.

## Data Governance

Focuses on making information understandable, trustworthy, accessible, accountable, and appropriately managed.

## Data Security

Focuses on preventing unauthorized access, disclosure, modification, and destruction.

### Example

An organization might have a securely encrypted database.

However, nobody knows which department owns it, what its fields mean, or whether its contents are accurate.

The database may have good technical security but poor data governance.

### Memory Trick

**DATA GOVERNANCE = Manage and trust the information**

**DATA SECURITY = Protect the information**

---

# 63. Data Governance vs. Data Compliance

## Data Governance

Establishes practices and responsibilities for managing information.

## Data Compliance

Addresses applicable legal, regulatory, contractual, and organizational requirements.

### Example

A governance policy establishes that personnel records must have designated owners.

A compliance requirement may establish how certain personnel records must be retained or protected.

### Memory Trick

**GOVERNANCE = How data is managed**

**COMPLIANCE = Which requirements must be satisfied**

---

# 64. Data Map vs. Content Explorer

This comparison connects the Data Governance module to the earlier Purview Data Security module.

| Data Map | Content Explorer |
|---|---|
| Broad metadata inventory | Sensitive-content visibility |
| Scan and describe data assets | Locate classified content |
| Technical and business metadata | Sensitive information types and labels |
| Hybrid and multicloud data discovery | Supported Microsoft 365 classification locations |
| Foundation for catalog governance | Supports data security investigations |

### Example

**Identify database assets across cloud platforms:** Data Map.

**Find Microsoft 365 documents classified with sensitive information types:** Content Explorer.

---

# 65. Unified Catalog vs. DSPM

## Unified Catalog

Organizes information for business use and governance.

## Data Security Posture Management — DSPM

Evaluates the security exposure and protection of sensitive information.

### Example

**Find an approved financial reporting data product:** Unified Catalog.

**Identify sensitive data exposed through excessive sharing permissions:** DSPM.

### Memory Trick

**UNIFIED CATALOG = Business data discovery and governance**

**DSPM = Sensitive-data security posture**

---

# 66. Data Quality Score vs. Secure Score

These scores address different objectives.

| Score | Primary meaning |
|---|---|
| Data Quality Score | How well information satisfies defined quality rules |
| Data Health Score | Progress toward data governance health expectations |
| Microsoft Secure Score | Progress toward evaluated security recommendations |
| Compliance Score | Progress toward compliance improvement actions |

### Important Exam Concept

**Not every Microsoft score measures security.**

Always identify the product and objective associated with the score.

---

# 67. November 2026 Transition to Microsoft Fabric

## Important Current Development

Microsoft announced on **November 12, 2026**, that its strategic data governance platform is moving to:

**Microsoft Fabric**

with:

**OneLake catalog**

as its central governance catalog.

Purview Data Map and Unified Catalog remain relevant to the SC-900 module, but Microsoft is retiring those governance capabilities.

### Timeline

| Date | Development |
|---|---|
| November 12, 2026 | Microsoft announces the Purview Data Governance retirement |
| November 2026 onward | Existing capabilities enter maintenance and transition planning |
| November 12, 2027 | End of support for retiring Purview Data Governance capabilities |

### Important Scope

**Retiring:** Purview Data Map, Unified Catalog, and related governance capabilities.

**Not retiring:** Microsoft Purview's Data Security and Data Compliance solutions.

---

# 68. What Is Microsoft Fabric?

Microsoft Fabric is Microsoft's integrated analytics and data platform.

It provides capabilities for working with data across supported analytics and business intelligence experiences.

The data governance strategy is increasingly centered on the platform where data is analyzed and consumed.

### ELI5

Instead of operating a separate data governance catalog disconnected from the main analytics environment, Microsoft is moving more governance functionality into the analytics platform itself.

### Important Concept

**Fabric is Microsoft's strategic destination for data governance following the Purview governance retirement announcement.**

---

# 69. What Is OneLake?

**OneLake** is the unified data lake associated with Microsoft Fabric.

It provides a central foundation for supported analytical data in Fabric.

### ELI5

Imagine a shared organizational data environment that multiple approved analytical tools and teams can use.

OneLake supplies that common foundation.

### Important Distinction

**OneLake = Data lake foundation**

**OneLake catalog = Data discovery and governance experience**

---

# 70. OneLake Catalog

## Big Idea

Microsoft identifies OneLake catalog as the central experience for discovering and governing data across Microsoft Fabric.

Its documentation describes three major experiences.

**Explore**

**Govern**

**Secure**

| Experience | Purpose |
|---|---|
| Explore | Discover and understand available data |
| Govern | Monitor governance status and manage improvements |
| Secure | Work with applicable data security and access controls |

### Important Concept

OneLake catalog represents Microsoft's current direction for data discovery, governance, and security management within Fabric.

Organizations migrating from Purview Data Governance should evaluate actual feature availability, integration requirements, and migration guidance rather than assume every older Unified Catalog capability has a one-to-one replacement.

---

# 71. Why Microsoft Is Making the Change

Microsoft's November 2026 announcement emphasizes placing governance closer to the data and the tools that use it.

The stated goals include:

- Reduce separation between governance and analytics
- Improve discovery and usability
- Bring policies and lineage closer to data consumers
- Support organizational AI adoption
- Reduce unnecessary complexity

Microsoft also describes support for governance across Fabric, Azure, and supported third-party sources.

### Memory Trick

**PURVIEW GOVERNANCE = Retiring catalog platform**

**FABRIC / ONELAKE = Microsoft's strategic governance direction**

---

# 72. Practical SC-900 Scenarios

## Scenario 1 — Find Organizational Data

An organization wants an automated inventory of databases, tables, and data assets across cloud and on-premises systems.

**Module answer: Microsoft Purview Data Map**

---

## Scenario 2 — Capture Metadata

A data governance team wants to identify table schemas, data types, and asset locations.

**Module answer: Data Map**

---

## Scenario 3 — Organize by Department

An organization wants to organize information around Finance, HR, and Supply Chain.

**Module answer: Governance Domains**

---

## Scenario 4 — Group Related Datasets

An analyst wants several related datasets presented as one business-oriented package.

**Module answer: Data Product**

---

## Scenario 5 — Standardize Business Terms

Two departments use different definitions for the same business concept.

**Module answer: Glossary Terms**

---

## Scenario 6 — Standardize Critical Identifiers

A customer identifier appears as `CustID` in one table and `CID` in another.

**Module answer: Critical Data Element**

---

## Scenario 7 — Monitor Data Quality

An organization wants to evaluate completeness and consistency using configurable rules.

**Module answer: Unified Catalog Data Quality**

---

## Scenario 8 — Monitor Governance Health

A data product is missing important governance information.

The organization wants recommended corrective steps.

**Module answer: Health Actions**

---

## Scenario 9 — Connect Business Goals to Data

A department wants to connect data products to measurable organizational goals.

**Module answer: OKRs**

---

## Scenario 10 — Request Data Access

A user discovers a data product and needs to obtain authorization.

**Module answer: Unified Catalog Access Policies**

---

## Scenario 11 — Search Without Technical Names

An analyst wants to describe the information needed in ordinary language.

**Module answer: AI-Powered Catalog Search**

---

## Scenario 12 — Understand Data Processing

An analyst wants to determine when a data-processing operation last executed.

**Module answer: Operational Metadata**

---

## Scenario 13 — Locate Sensitive Documents

A Microsoft 365 security administrator wants to locate documents containing sensitive information types.

**Correct cross-module answer: Content Explorer**

Not Data Map.

---

## Scenario 14 — Investigate Sharing Behavior

A security administrator wants to see which users printed or copied sensitive documents.

**Correct cross-module answer: Activity Explorer**

---

## Scenario 15 — New Data Governance Deployment

In November 2026, an organization wants to deploy Microsoft's strategic data governance platform.

**Current operational direction: Microsoft Fabric and OneLake catalog**

The retiring Purview Data Map and Unified Catalog should not be recommended as a new long-term deployment.

---

# 73. GRC / ISSO Career Connection

> **Additional professional context:** This section applies the module's concepts to information assurance, governance, risk, and compliance work. It is not a separate official Microsoft Learn instructional unit.

Data governance is relevant to cybersecurity because an organization must understand what information it possesses before determining how that information should be protected.

An ISSO or GRC analyst may need to determine:

**What information exists?**

**Where is it located?**

**Who owns it?**

**Which systems process it?**

**How sensitive is it?**

**Who is authorized to use it?**

**Are the records complete and reliable?**

**Can the organization demonstrate appropriate governance?**

Data governance supports these activities by establishing visibility, ownership, definitions, and accountability.

---

# 74. Data Governance and RMF

The NIST Risk Management Framework requires organizations to identify and manage risks associated with information systems.

Understanding the information processed by a system helps support:

- System categorization
- Security control selection
- Risk assessment
- Control implementation
- Continuous monitoring

### Example

An organization operates an application containing personnel information.

Before evaluating the system's security requirements, the security team needs to understand:

- Which information is processed
- How sensitive that information is
- Where it is stored
- Which systems exchange it
- Who has access
- What consequences could result from compromise

Data governance can provide useful context for those decisions.

### Important Distinction

**Data governance provides information that can support RMF activities.**

It does not itself replace formal RMF categorization, assessment, authorization, or monitoring requirements.

---

# 75. Data Governance and NIST SP 800-53

The following relationships are illustrative rather than direct product-to-control compliance mappings.

| Governance concept | Related control area |
|---|---|
| Data access policies | AC-3 — Access Enforcement |
| Limiting unnecessary data access | AC-6 — Least Privilege |
| Protecting information flows | AC-4 — Information Flow Enforcement |
| Evaluating information-related risks | RA-3 — Risk Assessment |
| Continuous oversight | CA-7 — Continuous Monitoring |
| Managing information retention | SI-12 — Information Management and Retention |

### Important Principle

Implementing a catalog or metadata inventory does not automatically satisfy these controls.

The organization must verify how the relevant requirements are implemented.

---

# 76. Data Ownership and Accountability

Data governance is particularly important when several teams share information.

### Example

An organization stores transportation performance information in a shared data platform.

The operations team relies on the information.

The IT team maintains the underlying database.

The security team controls access and monitoring.

Who is accountable for the meaning and accuracy of the data?

A data governance framework should establish appropriate ownership and responsibilities.

### Memory Trick

**System Administrator ≠ Automatically Data Owner**

Managing the technology does not necessarily mean owning the business information.

---

# 77. Data Lineage and Audit Readiness

Data lineage helps an organization explain how a report was produced.

### Example

An auditor questions a readiness figure in a monthly report.

The organization needs to determine:

- Which source contained the original value
- Whether the value was transformed
- Which reporting system used it
- Whether the source was accurate

Lineage information can support that investigation.

### GRC Connection

Reliable traceability can improve confidence in evidence and operational reporting.

However, lineage metadata is not a substitute for validating the underlying records.

---

# 78. Data Quality as a Risk

Poor data quality can create operational and security-related risks.

### Examples

**Duplicate Accounts**

May complicate identity governance or financial reporting.

**Missing Data Owners**

May leave important information without clear accountability.

**Outdated Records**

May cause incorrect decisions.

**Inconsistent Classifications**

May cause the organization to apply inadequate safeguards.

### Important Concept

**Poor data quality can undermine both organizational decisions and the effectiveness of security controls.**

---

# 79. Data Governance and AI Risk

Organizations increasingly use AI agents to retrieve and process enterprise information.

The governance team may need to determine:

- Whether the data source is authoritative
- Whether information is properly classified
- Whether access is authorized
- Whether the data is accurate
- Whether usage restrictions apply
- Whether AI-generated conclusions can be traced to reliable sources

### Example

An AI agent prepares a logistics report.

The agent retrieves information from multiple systems.

If those sources use inconsistent definitions or outdated values, the resulting report may be misleading.

Data governance helps reduce these risks by improving source quality, consistency, and accountability.

---

# 80. GRC Implications of the November 2026 Retirement

The retirement announcement itself creates an important governance concern for organizations currently using Purview Data Map or Unified Catalog.

Existing customers should evaluate:

**System Dependencies**

Which workflows depend on the retiring platform?

**Metadata and Catalog Records**

What information must be migrated or preserved?

**Access Governance**

How will existing approval processes continue?

**Data Quality Controls**

Which measurements and reports require replacement?

**Regulatory Obligations**

Are there requirements to maintain governance evidence or records?

**Transition Timeline**

Can the organization complete its transition before November 12, 2027?

### Practical GRC Principle

**A technology retirement can create operational, security, and compliance risk if essential capabilities are not transitioned appropriately.**

Microsoft recommends early coordination with its account team for organizations with contractual obligations or demanding regulatory requirements.

---

# 81. SC-900 Quick Reference

| If the question mentions... | Think... |
|---|---|
| Manage organizational data responsibly | Data Governance |
| Central standards with distributed responsibility | Federated Governance |
| Provide appropriate access | Data Access |
| Organize, annotate, and publish information | Data Curation |
| Help users find information | Data Discovery |
| Maintain quality and lifecycle standards | Data Health |
| Explain business meaning | Data Understanding |
| Person using the dataset | Data Consumer |
| Person accountable for a data asset | Data Owner |
| Maintain definitions and quality | Data Steward |
| Establish enterprise governance standards | Central Data Office |
| Automated inventory of data assets | Data Map |
| Discover schemas and data types | Data Map |
| Data describing another data asset | Metadata |
| Column names and schemas | Technical Metadata |
| Business definitions and descriptions | Business Metadata |
| Classification and collection mappings | Semantic Metadata |
| Execution times and processing status | Operational Metadata |
| Organize data by business area | Governance Domain |
| Group datasets for a business use case | Data Product |
| Standardize business definitions | Glossary Terms |
| Standardize important data fields | Critical Data Elements |
| Connect data to measurable goals | OKRs |
| Request authorized access to data products | Access Policies |
| Search for data using natural language | AI-Powered Catalog Search |
| Measure governance condition | Health Controls |
| Address governance deficiencies | Health Actions |
| Assess accuracy and completeness | Data Quality |
| Trace where data originated | Data Lineage |
| Current Microsoft governance direction | Fabric / OneLake catalog |

---

# 82. Final Module 4 Cram Sheet

```text
MICROSOFT PURVIEW DATA GOVERNANCE
= DISCOVER + UNDERSTAND + GOVERN DATA

DATA GOVERNANCE
= TRUSTWORTHY, SECURE, USABLE INFORMATION

FEDERATED GOVERNANCE
= CENTRAL STANDARDS + DISTRIBUTED OWNERSHIP

DATA ACCESS
= RIGHT ACCESS AND APPROPRIATE USE

DATA CURATION
= ORGANIZE + ANNOTATE + PUBLISH DATA

DATA DISCOVERY
= FIND RELEVANT INFORMATION

DATA HEALTH
= MAINTAIN QUALITY AND LIFECYCLE STANDARDS

DATA UNDERSTANDING
= KNOW WHAT THE INFORMATION MEANS

DATA CONSUMER
= USES THE DATA

DATA OWNER
= ACCOUNTABLE FOR THE DATA

DATA STEWARD
= MAINTAINS QUALITY AND DEFINITIONS

CENTRAL DATA OFFICE
= ESTABLISHES ENTERPRISE GOVERNANCE

DATA MAP
= AUTOMATED METADATA INVENTORY

METADATA
= DATA ABOUT DATA

DATA MAP SCANNING
= DISCOVER DATA ASSETS AND METADATA

DATA MAP CLASSIFICATION
= IDENTIFY SENSITIVE DATA CHARACTERISTICS

DATA MAP PERMISSIONS
= DO NOT AUTOMATICALLY GRANT SOURCE DATA ACCESS

TECHNICAL METADATA
= SCHEMAS + COLUMNS + DATA TYPES

BUSINESS METADATA
= DESCRIPTIONS + BUSINESS DEFINITIONS

SEMANTIC METADATA
= ORGANIZATION + CLASSIFICATION

OPERATIONAL METADATA
= PROCESSING STATUS + EXECUTION TIMES

UNIFIED CATALOG
= BUSINESS DATA DISCOVERY AND GOVERNANCE

GOVERNANCE DOMAIN
= BUSINESS-ORIENTED DATA BOUNDARY

DATA PRODUCT
= RELATED ASSETS FOR A BUSINESS USE CASE

GLOSSARY TERM
= BUSINESS DEFINITION AND CONTEXT

CDE
= CRITICAL DATA ELEMENT

OKR
= OBJECTIVES AND KEY RESULTS

ACCESS POLICY
= GOVERN AUTHORIZED DATA PRODUCT ACCESS

SEARCH
= FIND KNOWN INFORMATION

BROWSE
= EXPLORE AVAILABLE INFORMATION

AI-POWERED CATALOG SEARCH
= FIND DATA USING NATURAL LANGUAGE

HEALTH CONTROL
= MEASURE GOVERNANCE HEALTH

HEALTH ACTION
= RECOMMENDED GOVERNANCE IMPROVEMENT

DATA QUALITY
= INFORMATION ACCURACY AND RELIABILITY

DATA LINEAGE
= TRACE ORIGIN AND MOVEMENT OF DATA

CONTENT EXPLORER
= LOCATE SENSITIVE MICROSOFT 365 CONTENT

ACTIVITY EXPLORER
= REVIEW DATA-HANDLING ACTIVITY

DSPM
= DATA SECURITY POSTURE MANAGEMENT

CSPM
= CLOUD SECURITY POSTURE MANAGEMENT

MICROSOFT FABRIC
= MICROSOFT DATA AND ANALYTICS PLATFORM

ONELAKE
= UNIFIED DATA LAKE

ONELAKE CATALOG
= FABRIC DATA DISCOVERY AND GOVERNANCE

PURVIEW GOVERNANCE RETIREMENT ANNOUNCEMENT
= NOVEMBER 12, 2026

PURVIEW GOVERNANCE END OF SUPPORT
= NOVEMBER 12, 2027

PURVIEW DATA SECURITY AND COMPLIANCE
= NOT INCLUDED IN THE GOVERNANCE RETIREMENT
```

---

# 83. Final Mental Model

Imagine an organization has valuable information scattered across multiple databases, cloud platforms, and business applications.

**Data governance** establishes the policies, standards, and responsibilities needed to manage that information.

**Federated governance** allows individual departments to maintain their information while following organization-wide requirements.

**Data owners** are accountable for the information.

**Data stewards** maintain quality, descriptions, and definitions.

**Data consumers** discover and use authorized information.

**Microsoft Purview Data Map**, as described in the SC-900 module, scans supported sources and maintains metadata describing the organization's data assets.

**Microsoft Purview Unified Catalog** builds on that metadata to organize information into governance domains and data products.

**Glossary terms** establish business meaning.

**Critical data elements** establish consistent treatment of important information.

**Access policies** support appropriate authorization.

**Data health controls** measure governance progress.

**Data quality rules** help determine whether information is trustworthy.

**AI-assisted discovery and curation** improve the ability to find and understand information.

The resulting governance framework helps organizations make better decisions, protect information, and use data responsibly.

Microsoft is now transitioning these governance capabilities toward **Microsoft Fabric and OneLake catalog**, but the fundamental governance principles remain important.

**The central concept:**

**Data governance ensures that organizational information can be found, understood, trusted, managed, and used appropriately.**

---

# Official Microsoft Learn References

The following instructional pages were verified against the live module on November 23, 2026.

[Module Overview](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-governance/)

[Introduction](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-governance/1-introduction)

[Describe the Concepts and Benefits of Data Governance](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-governance/2-describe-benefits-data-governance)

[Describe Microsoft Purview Data Map](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-governance/3a-describe-data-map)

[Describe Microsoft Purview Unified Catalog](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-governance/3-describe-data-catalog)

[Module Assessment](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-governance/4-knowledge-check)

[Summary](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-governance/5-summary)

---

# Additional Official Microsoft References

[Microsoft's November 12, 2026 Data Governance Retirement Announcement](https://techcommunity.microsoft.com/blog/microsoft-security-blog/a-next-step-in-the-evolution-of-the-microsoft-data-governance-strategy/4572227)

[Microsoft Purview Data Map Overview](https://learn.microsoft.com/en-us/purview/data-map)

[Microsoft Purview Unified Catalog](https://learn.microsoft.com/en-us/purview/unified-catalog)

[Microsoft Fabric OneLake Catalog Overview](https://learn.microsoft.com/en-us/fabric/governance/onelake-catalog-overview)

[Microsoft Fabric Governance and Compliance](https://learn.microsoft.com/en-us/fabric/governance/governance-compliance-overview)

---

**Study status:** Microsoft Purview — Module 4 notes prepared  
**Verified:** November 23, 2026  
**Certification:** Microsoft SC-900 — Passed October 17, 2026
