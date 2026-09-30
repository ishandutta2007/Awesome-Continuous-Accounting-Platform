# Awesome-Continuous-Accounting-Platform

# Top Continuous Accounting Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Financial Close Automation, Reconciliation, Consolidation & Continuous Reporting*
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Continuous Accounting**. These tools help finance teams move beyond periodic month-end closes toward continuous reconciliation, real-time consolidation, and audit-ready financial reporting.

**Examples** include FloQast, BlackLine, Numeric, Rillet, Campfire, OneStream, Trintech, Vena, Cube, and Workiva (the category leaders).

**Open-source emphasis**: Continuous accounting has a **narrow but emerging open-source foundation**. No production-ready open-source platform matches the breadth of FloQast or BlackLine. The practical path combines **double-entry accounting engines** (Beancount, Akaunting, BrassLedger) with **reconciliation tools** (YARS, Blnk) and **automated iXBRL reporting** (ixbrl-reporter). This section documents these foundations honestly.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[FloQast](https://floqast.com/)**
  Close management platform focused on checklist automation, reconciliation workflows, and flux analysis. Popular with mid-market and enterprise accounting teams.

- **[BlackLine](https://www.blackline.com/)**
  Enterprise financial close automation platform. Provides account reconciliation, task management, transaction matching, and intercompany accounting.

- **[Numeric](https://www.numeric.io/)**
  AI-first close automation that sits on top of existing ERP (NetSuite, Sage Intacct, QuickBooks, SAP). Automates accruals, reconciliations, and flux analysis with transaction-level ERP visibility.

- **[Rillet](https://www.rillet.com/)**
  AI-native ERP that replaces the accounting workflow itself. The GL is continuously updated from connected systems, subledgers post near-real-time, and reconciliations run continuously.

- **[Campfire](https://campfire.ai/)**
  AI-native ERP designed for startups. Features Ember AI for cross-functional accessibility and real-time data flows.

- **[OneStream](https://www.onestream.com/)**
  Unified corporate performance management platform. Provides financial consolidation, close management, reporting, and planning.

- **[Trintech](https://trintech.com/)**
  Financial close and reconciliation software. Provides transaction matching, account reconciliation, and close task management.

- **[Vena](https://venasolutions.com/)**
  Financial planning and analysis platform with close management and consolidation capabilities.

- **[Cube](https://cube software.com/)**
  Spreadsheet-native FP&A platform that connects to ERP for real-time financial data and reporting.

- **[Workiva](https://www.workiva.com/)**
  Cloud platform for financial reporting, compliance, and data collaboration. Supports SEC reporting, iXBRL, and consolidated financial statements.

## Open-Source GitHub Projects

### Double-Entry Accounting Engines

- **[Beancount](https://github.com/beancount/beancount)**
  **The most mature open-source double-entry accounting engine.** Uses plain-text files as input, provides an SQL-like query language for filtering and aggregating financial data, and generates balance sheets and income statements . Version 3.2.3 (May 2026) signed by GitHub Actions and verified by PyPI . **Python-based**. The foundation for continuous accounting: every transaction is version-controlled, auditable, and queryable.

- **[Akaunting](https://github.com/akaunting/akaunting)**
  **Free, open-source accounting software for small businesses and freelancers.** Built with Laravel, VueJS, and Bootstrap 4 . Features invoicing, billable expenses, bank account tracking, multi-currency, multi-company, customer management, and detailed financial reports . Version 3.2.3 (August 2026) with 218 votes on Softaculous . **GPL-3.0**. While not a continuous close platform, it provides the GL foundation for automated accounting workflows.

- **[BrassLedger](https://github.com/rhamenator/BrassLedger)**
  **Open-source cross-platform accounting and business management system.** **In active development** (v0.1.0-pre.6). Provides general ledger workspaces for journal activity, balances, and month-end review; receivables with cash application; payables with disbursement preparation; payroll; project tracking; and **reporting support for financial statements, checks, paychecks, labels, and management output** . **GPL-3.0**. .NET application with installers for Windows, macOS, and Linux .

### Reconciliation & Matching

- **[YARS (Yet Another Reconciliation System)](https://github.com/aferryc/yars)**
  **Open-source financial reconciliation system for comparing internal transaction records with bank statements.** Microservices architecture with API Server, Compiler Service, and Reconciliation Service . Uses PostgreSQL for storage, Kafka for event-driven communication, and provides a web UI for uploading transaction files and viewing reconciliation summaries . **Go-based, MIT License** . **Reconciliation only**—does not include GL posting or close management.

- **[Blnk](https://github.com/blnkfinance/blnk)**
  **Source-available, cloud-native ledger platform for financial infrastructure.** Multi-currency, multi-asset, double-entry accounting with n:n transaction support . Features **reconciliation** via `StartInstantReconciliation` and `StartReconciliation` with configurable strategies (one_to_one), grouping criteria, and matching rules . Also provides `CreateBulkTransactions` with atomic rollback and async processing . **Go-based**. Enterprise-grade ledger engine.

### Consolidation & Reporting

- **[ixbrl-reporter](https://github.com/cybermaggedon/ixbrl-reporter)**
  **Automated creation of iXBRL financial report files from template configuration and account data** . **35 stars, 12 forks**. **Python-based**. Enables programmatic generation of regulatory-compliant financial reports. **Open source**.

- **[Nexus Accounting](https://github.com/azaharizaman/nexus-accounting)**
  **Financial statement generation, period close, consolidation, and variance analysis package.** Part of the Nexus ERP ecosystem . **Planned capabilities** include `GetBalanceSheetQuery`, `GetIncomeStatementQuery`, `GetCashFlowStatementQuery`, `GetTrialBalanceQuery`, `GetVarianceReportQuery`, and `GetConsolidatedStatementQuery` . **Currently in planning/development stage**—provides architectural patterns for building consolidation systems. **PHP 8.3+**.

### Additional Strong Open-Source Options

- **Double-Entry Engines**: **Beancount** (plain-text, Python, mature), **Akaunting** (Laravel/Vue, GPL-3.0, small business), **BrassLedger** (GPL-3.0, .NET, in development) .
- **Reconciliation**: **YARS** (Go, MIT, bank reconciliation), **Blnk** (Go, source-available, ledger + reconciliation) .
- **Reporting**: **ixbrl-reporter** (Python, iXBRL generation) .
- **Consolidation**: **Nexus Accounting** (PHP, planned) .

**Frameworks for building custom systems**: Combine **Beancount** for the plain-text double-entry GL foundation, **YARS** or **Blnk** for transaction reconciliation, **ixbrl-reporter** for automated iXBRL financial reporting, and **Akaunting** or **BrassLedger** for business management workflows. Add **PostgreSQL** for persistence and **Git** for audit trails.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Continuous accounting platforms handle sensitive financial data; ensure compliance with internal controls, audit requirements, and relevant financial regulations.
- **Open-source reality**: **No production-ready open-source continuous accounting platform exists** that matches FloQast, BlackLine, or Numeric. The open-source ecosystem provides **double-entry accounting engines** (Beancount, Akaunting, BrassLedger), **reconciliation tools** (YARS, Blnk), and **automated reporting** (ixbrl-reporter) . A viable continuous accounting stack can be assembled from these components, but it requires significant integration work, lacks the workflow automation and close management features of commercial platforms, and has no unified UI for finance teams. Commercial platforms remain the primary choice for organizations seeking turnkey continuous accounting.

---

**Made for controllers, finance managers, accounting operations teams, and financial systems architects.**
Let's make continuous accounting more open, transparent, and auditable.
