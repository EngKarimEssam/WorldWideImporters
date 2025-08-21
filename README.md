

# WorldWideImporters🌍

- This project demonstrates how to build a scalable data ingestion, transformation, and reporting pipeline in Microsoft Fabric using:
  -	Lakehouse
  -	Pipelines
  -	Shortcuts
  -	PySpark
  -	SQL
# Project Overview📌
- This project showcases techniques for:
  - Data virtualization using OneLake Shortcuts
  - Dynamic ETL pipelines for multiple tables
  - Leveraging PySpark for performance optimization
  - Querying data with SQL & Notebooks
  - Designing a solution that balances simplicity and scalability

 
# Project Steps🚀
1️⃣ Create a Lakehouse
- Lakehouse is the foundation for storing and managing structured/unstructured data in Fabric.



2️⃣ Access Data via Shortcut
- Shortcuts in Microsoft OneLake allow you to unify data across domains, clouds, and accounts by creating a single virtual data lake for your enterprise.

- All Fabric experiences and analytical engines can directly connect to your existing data sources (Azure, AWS, OneLake, etc.).

- Benefits:
  - No redundant data copies
  - Reduced process latency
  - Simplified security (OneLake manages credentials)
- Source: Azure Data Lake Storage Gen2
  - URL: https://pwadlsfabric.dfs.core.windows.net/
  - Authentication: SAS
  - Token sv=2022-11-02&ss=b&srt=sco&sp=rlx&se=2026-03-05T22:36:26Z&st=2025-03-05T14:36:26Z&spr=https&sig=uOFNOXp6wQKgNdkKw6GUzaSF99UX%2Bma%2B244NWHdHxx0%3D



3️⃣ Build Pipelines
- Ingest Fact_Sales into the Lakehouse using Copy Assistant.
- Load Dim_City using Add to Canvas.
- 💡 Dynamic Loading for Multiple Tables, Instead of creating 100 pipelines for 100 tables:
    - Create a child pipeline with a parameter for the file name.
    - Create a parent pipeline to:
      - Fetch file metadata
      - Filter out Fact_Sales
      - Use a ForEach container to loop through and load files via the child pipeline



4️⃣ Use a Notebook for Performance
- Connect Lakehouse tables and shortcut files.
- Example with Fact_Sales:
  - Pipeline load: ~12 minutes
  - PySpark load: ~1 minute ⚡
 
<img width="1425" height="627" alt="2025-08-21_224122" src="https://github.com/user-attachments/assets/f74562a0-7bf6-4715-b3b1-0f63552b3158" />
<img width="1488" height="459" alt="2025-08-21_224202" src="https://github.com/user-attachments/assets/8fa3b6c7-8ca1-457b-897a-d9e1ef566fc1" />



5️⃣ Query with SQL
- In the Notebook, you can query tables using magic commands and SQL syntax for flexible exploration.


🛠️ Tools & Technologies
- Microsoft Fabric
- OneLake Shortcuts
- Data Pipelines
- PySpark (Notebooks)
- SQL Analytics Endpoint



📚 Key Learnings
- Shortcuts eliminate redundant data copies and simplify security.
- Dynamic pipelines scale better than creating one pipeline per table.
- PySpark engine drastically improves performance vs pipelines.
- Lakehouse + SQL endpoint provides flexibility for analysts and engineers.

[Watch the project on YouTube](https://youtu.be/fCnlzTd5n8E?si=O-j5GrFnxIAbpzJ9)

