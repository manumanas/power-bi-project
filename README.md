# Transportation Analytics Dashboard

## Overview

This repository contains the Power BI project for the **Transportation Analytics Dashboard**, which leverages cloud-hosted data on MacLeod servers. The solution integrates large-scale trip and delivery datasets from EFS fuel transactions, maintenance payments, and GPS logs. Interactive dashboards and DAX-driven reports provide actionable insights into cost, performance, and forecasting.

---

## Table of Contents

- [Features](#features)
- [Data Sources](#data-sources)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [DAX Measures](#dax-measures)
- [Dashboard Walkthrough](#dashboard-walkthrough)
- [Contributing](#contributing)

---

## Features

- **Revenue per Mile**: Efficiency analysis by route and vehicle class.
- **On-Time Delivery Rate**: Punctuality tracking with lane-level performance.
- **Geo-Distribution Maps**: Heatmaps to highlight regional trip densities.
- **Cost Analysis**: Cost-per-mile calculations combining fuel and maintenance.
- **Delivery Performance Index**: Composite score including timeliness and feedback.
- **Trend Forecasting**: 30-day rolling averages for revenue and volume.
- **Interactive Experience**: Drill-through, bookmarks, and parameterized slicers.
- **Automated Refresh**: Nightly data refresh via Power BI Gateway & Azure Data Factory.

---

## Data Sources

- **Azure SQL Database** on MacLeod servers (EFS-hosted files).
- **EFS Fuel Transactions**: Fuel purchase records.
- **Maintenance Payments**: Service and repair costs.
- **GPS Logs**: Trip coordinates and timestamps.

---

## Prerequisites

- Power BI Desktop (≥ March 2025 release)
- Access to Azure SQL Database on MacLeod servers
- Power BI Pro or Premium license (for sharing and scheduled refresh)
- External Tools (optional for DAX review): Tabular Editor, DAX Studio

---

## Installation & Setup

1. **create repository**
   ```bash
   https://github.com/<YourUsername>/transportation-analytics-dashboard.git
   cd transportation-analytics-dashboard
   ```
2. **Open Power BI Report**
   - Launch **Power BI Desktop**.
   - Open `TransportationAnalytics.pbix`.
3. **Configure Data Source**
   - In **Home > Transform Data > Data source settings**, update connection string to your Azure SQL instance.
   - Ensure credentials have **Data Reader** permissions.
4. **Set up Scheduled Refresh**
   - Publish the report to **Power BI Service**.
   - Configure **Gateway** and set a **nightly refresh** schedule.

---

## Usage

- Navigate through the **Report** view to explore KPIs.
- Use **Date Slicer** to filter by custom time frames.
- Drill through visuals for detailed analysis.
- Toggle parameters in bookmarks for “what-if” scenarios.

---

## Dashboard Walkthrough



1. **Overview Page**: High-level KPIs and trend lines.
2. **Map View**: Geo-distribution of trip density.
3. **Cost Analysis**: Breakdowns of cost per mile and asset-level expenses.
4. **Performance Insights**: Delivery performance index and benchmarks.

---

## Contributing

Contributions are welcome! Please:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/YourFeature`.
3. Commit your changes: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin feature/YourFeature`.
5. Open a Pull Request.

