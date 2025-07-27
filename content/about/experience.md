---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience

active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 40

title: Experience
subtitle:

# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.

experience:
  - title: Data Engineer
    company: Ministry for the Environment
    company_url: "https://environment.govt.nz/"
    location: (remote)
    date_start: '2023-04-01'
    description: |2-
      Built a scalable data ingestion and processing system leveraging cloud technologies (AWS S3, Lambda, Snowflake, dbt-core) and an ELT framework, transforming ad-hoc manual updates into an automated, continuously-updated system. Implemented robust data quality checks and monitoring systems across the pipeline to ensure accuracy and integrity. This resulted in improved data efficiency, scalability, and reliability, enabling faster and more informed decision-making across the organization.

  - title: Kaitātari Matua | Seniror Data Analyst
    company: Ministry for the Environment
    company_url: "https://environment.govt.nz/"
    location: (remote)
    date_start: '2022-04-01'
    date_end: '2023-04-01'
    description: |2-
      Delivered a critical public data product by aggregating, cleaning, and integrating datasets from 76 local councils into a unified, scalable system. Designed and deployed interactive dashboards to visualize complex data insights, enabling public accessibility and supporting data-driven decision-making for stakeholders.

  - title: Kaitātari | Data Analyst
    company: Ministry for the Environment
    company_url: "https://environment.govt.nz/"
    location: (remote)
    date_start: '2021-03-01'
    date_end: '2022-04-01'
    description: |2-
      Responsibilities include:
    
      * R/Shiny app development and deployment
      * Statistical analysis
      
  - title: Geospatial Analyst
    company: Dunedin City Council
    company_url: "https://www.dunedin.govt.nz/"
    location: Dunedin, New Zealand
    date_start: '2018-08-01'
    date_end: '2021-03-01'
    description: |2-
      Responsibilities included:
  
      * Geospatial product development
      * Designing machine learning tools
      * Data visualisation
      
  - title: "Postdoctoral Researcher"
    company: "University of Otago, School of Surveying"
    company_url: "https://www.otago.ac.nz/surveying/index.html"
    location: "Dunedin, New Zealand"
    date_start: "2015-09-01"
    date_end: "2018-08-01"
    description: Developed a new multivariate statistical analysis method for interpreting present-day changes to Antarctica’s ice shelves.  This method combined computational models with geospatial-time series data to create statistical fingerprints for ice shelf events, which correctly identified the timing and magnitude of past known events.  Model used to forecast next 300 years of ice shelf evolution.
  

  - title: "Postdoctoral/Graduate Researcher"
    company: "University of Washington, Department of Earth and Space Science"
    company_url: "https://www.ess.washington.edu/"
    location: "Seattle, Washington, USA"
    date_start: "2009-09-01"
    date_end: "2015-09-01"
    description: Developed computational models and analysed data using a variety of statistical approaches on 4 major projects, responsible of managing research databases.

design:
  columns: '2'
---
