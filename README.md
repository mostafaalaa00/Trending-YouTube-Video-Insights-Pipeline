# Trending-YouTube-Video-Insights-Pipeline

### Overview
In the Trending YouTube Video Insights Pipeline Project, we create a data pipeline for the top trending videos on the platform using data from ten countries. and try to answer questions about YouTube trending like views, likes, dislikes, and other factors that determine or improve a video's chance of becoming a trend

### Objective
* Data Source: reading data from multiple sources CSV, JSON, and SQL
    * JSON Files
       * [CA_category_id.json](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/files/15142439/CA_category_id.json)
       * DE_category_id.json
       * US_category_id.json
       * RU_category_id.json
       * MX_category_id.json
       * KR_category_id.json
       * JP_category_id.json
       * IN_category_id.json
       * GB_category_id.json
       * FR_category_id.json
    * CSV Files
      *  CAvideos.csv
      *  DEvideos.csv
      *  USvideos.csv
      *  RUvideos.csv
      *  MXvideos.csv
      *  KRvideos.csv
      *  JPvideos.csv
      *  INvideos.csv
      *  GBvideos.csv
      *  FRvideos.csv
        
* Data Ingestion & Staging Area: Using the power of Pyspark to read, extract, and transform data into structured row data before analysis and CSV   
  as a staging area to store and as a backup for data.
    1. read data from JSON and CSV files using Pyspark
    2. Convert JSON root objects into a list of objects
    3. apply some transformation and marge on JSON and CSV to be one file
    4. transform JSON files into CSV files and load both into two CSV files

* Data Integration & ETL Process: talend data integration tool to extract, clean, transform, and load it into a database
    * Data integration with Talend to load JSON and CSV as tables in MYSQL
      * Date Cleaning Map
        
        ![load csv map](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/db87f0ab-bf7e-4ae0-b3ee-fc34be02b44b)

      * JSON to SQL
        
        ![load json](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/463e467e-431d-426e-9af0-7e09feb14054)

      * CSV to SQL
        
        ![load csv](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/6e0b41e4-d264-4c7d-b94e-da552ed416d1)

     * Final Result Table (after concatenation)
       
       ![final result table2](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/8ae3ddab-96c0-4d82-8254-2107f4950700)

       
* Data Warehousing: build a star schema dimension model using Talend open-source
    * SQL Metadata

      ![schema](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/303dc13f-ba9d-40ca-a8f6-b479a9511a15)

    * ERD Diagram
      
      ![youtube dw2](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/1369ab1d-fecd-4aba-845c-c2e80717c91c)
    * Date Dimension
      
      ![Date Dim](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/c1bd633c-1a61-4e67-be9e-e7d1b9e0ba60)
    * Video Dimension
      
      ![video dim](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/b796ea93-c495-4f84-8528-6c5ad5c75f21)
    * Fact Measures (views, likes, dislikes, comments)
      
      ![fact](https://github.com/mostafaalaa00/Trending-YouTube-Video-Insights-Pipeline/assets/61460174/8de71cc7-4334-41c4-a761-3ba7215a4a09)

* Visualization: Utilize Microsoft Power-Bi to transform data into valuable insight dashboard
