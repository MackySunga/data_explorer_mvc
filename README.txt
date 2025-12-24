Data Explorer MVC
=================

Overview
--------
A lightweight PHP MVC web app for exploring CSV datasets. It supports
previewing tables with filters, profiling columns, generating insights,
building charts, and exporting reports to PDF (including queued charts and
optional regression tables).

Features
--------
- Upload and manage CSV datasets
- Table exploration with search, filters, sorting, and column selection
- Summary statistics, missing values, outliers, and correlation views
- Regression (OLS) analysis with diagnostics and charting
- Report generation and PDF export (tables + charts)
- Saved reports with download and cleanup of unused charts

Project Structure
-----------------
- app/Controllers      HTTP controllers and endpoints
- app/Models           Dataset metadata and storage
- app/Services         CSV reading, stats, insights, PDF export, workflows
- app/Views            Server-rendered UI pages
- public/              Entry point and static assets
- storage/             Uploaded files, cache, reports, and chart images

Requirements
------------
- PHP 8.1+ (recommended)
- A web server (XAMPP/Apache or similar)
- Write permissions for storage/ and public/ if generating files

Running Locally (XAMPP)
-----------------------
1) Place the project in your XAMPP htdocs directory.
2) Start Apache in the XAMPP control panel.
3) Open in browser:
   http://localhost/data_explorer_mvc/public/

Notes
-----
- PDF export uses server-side rendering and stores report JSON in storage/reports.
- The chart queue and regression tables are stored in browser localStorage.

License
-------
MIT License. See LICENSE.txt.