# WorldWideImporters

- Create a Lakehouse
- Access data through a shortcut
  - Shortcuts in Microsoft OneLake allow you to unify your data across domains, clouds, and accounts by creating a single virtual data lake for your entire enterprise. All Fabric experiences and analytical engines can directly connect to your existing data sources, such as Azure, Amazon Web Services (AWS), and OneLake, through a unified namespace. OneLake manages all permissions and credentials, so you don't need to separately configure each Fabric workload to connect to each data source. Additionally, you can use shortcuts to eliminate        edge copies of data and reduce process latency associated with data copies and staging.

  - get the data using Azure Data Lake Storage Gen2
    - I get the data from https://pwadlsfabric.dfs.core.windows.net/
    - Authentication: SAS, and here is the  Token: sv=2022-11-02&ss=b&srt=sco&sp=rlx&se=2026-03-05T22:36:26Z&st=2025-03-05T14:36:26Z&spr=https&sig=uOFNOXp6wQKgNdkKw6GUzaSF99UX%2Bma%2B244NWHdHxx0%3D

- Pipeline:
  - using a pipeline for ingestion & transformation and loading Fact_Sales into the table folder in the lakehouse (using copy assistant)
  - load Dim_City using a pipeline (using add to canvas)
  - What if we have 100 tables? will we create 100 pipeline? Noooo
    - We can load it dynamically:
      - 1. edit child_piepline and add a parameter
        2. 
- 
- 
