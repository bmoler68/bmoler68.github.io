---
tags: ["2026", "Releases"]
---

## XAUlytics v1.2.0

![XAUlytics Banner](/images/XAUlytics/banner.png)

I'm excited to announce the release of **XAUlytics v1.2.0**.  This release adds a gold/silver ratio chart to the dashboard.

### About the Application

XAUlytics is a **precious metal price automated ETL flow**. It ingests metal and FX-related quotes from MetalpriceAPI, normalizes them in Python, and loads idempotent rows into Supabase (PostgreSQL). A static browser dashboard reads pricing and symbol catalog data from Supabase. The stack includes Docker (containerized CLI for Linux-style runs anywhere) and GitHub Actions for scheduled jobs. You can use it as a reference for extract → transform → load layout, environment-driven configuration, and automation.

This project is a demonstration of my use of generative AI to create a fully automated front-to-end ETL flow, sourcing data from an API and loading daily precious metal pricing data to a Supabase instance to produce an analytics dashboard.

### What's New in v1.2.0

Version **1.2.0** is now available. For a detailed list of changes in this release, see the [XAUlytics releases on GitHub](https://github.com/bmoler68/XAUlytics/releases).

### Download and Resources

- **🔗 GitHub Repository**: [XAUlytics on GitHub](https://github.com/bmoler68/XAUlytics)

For questions, support, or feedback, please contact me at bmoler@brianmoler.com.
