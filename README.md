# n8n-Scraping-workflows
## ⚙️ Automated Workflow Diagrams

These diagrams illustrate the logical flow and processing steps for various data operations within this system, including product retrieval, image processing, database updates, and data export.

### 1. Product Data Retrieval and Image Processing Workflows

These workflows handle fetching product lists, processing associated images (validation, compression), and persisting the data into a PostgreSQL database.

| Diagram Title | Description | File Name |
| :--- | :--- | :--- |
| **Product Retrieval, Image Processing, and DB Insertion (V1)** | Fetches multiple products, processes image data through a validation/compression sequence, merges the results, formats for the database, executes the PostgreSQL query, and logs success/error. | `Screenshot 2025-08-30 124012.png` |
| **Product Retrieval, Image Processing, and DB Insertion (V2)** | A revised version where product data is processed first (`Process Data`), followed by parallel image compression and formatting before merging and executing the DB query. | `Screenshot 2025-08-30 125618.png` |
| **Detailed Product Data, Image Processing, and DB Insertion** | A complex workflow involving initial fetching, debugging, detailed data extraction, parallel image processing (extract, validate, compress), merging, and final DB insertion. | `Screenshot 2025-08-19 162100.png` |

#### Workflow V1: Image Processing and DB Insertion
![Product Retrieval, Image Processing, and DB Insertion Workflow V1](Screenshot 2025-08-30 124012.png)

---

#### Workflow V2: Image Processing and DB Insertion
![Product Retrieval, Image Processing, and DB Insertion Workflow V2](Screenshot 2025-08-30 125618.png)

---

#### Detailed Extraction and Image Processing
![Detailed Product Data, Image Processing, and DB Insertion Workflow](Screenshot 2025-08-19 162100.png)

---

### 2. Core Data Extraction and Database Load

These focus on initial data extraction, preparation, and bulk loading into the database.

| Diagram Title | Description | File Name |
| :--- | :--- | :--- |
| **Main Page Extract, Process, and PostgreSQL Load** | Extracts product lists from a main page URL, processes the data, prepares the SQL statements, executes the PostgreSQL query, and handles success/error logging. | `Screenshot 2025-08-19 162213.png` |
| **Feature Data Merge and PostgreSQL Load** | Fetches two distinct data streams (`Feature Values` and `Product Features`) via API calls, merges the results, builds a feature map, and inserts the structure into PostgreSQL. | `Screenshot 2025-08-19 162648.png` |

#### Main Page Extract and PostgreSQL Load
![Main Page Extract, Process, and PostgreSQL Load Workflow](Screenshot 2025-08-19 162213.png)

---

#### Feature Data Merge and PostgreSQL Load
![Feature Data Merge and PostgreSQL Load Workflow](Screenshot 2025-08-19 162648.png)

---

### 3. Database Update and Data Export Workflows

These cover periodic updates and final data output.

| Diagram Title | Description | File Name |
| :--- | :--- | :--- |
| **Product List Fetch and Database Update** | Fetches an external product list, processes it using custom code, updates existing rows in a table, checks for success, and logs the outcome. | `Screenshot 2025-08-25 123129.png` |
| **Data Extraction, CSV Preparation, and Google Drive Export** | Extracts data from a URL, processes it, prepares the final data structure, converts it to binary (for file handling), and uploads the resulting file to Google Drive. | `Screenshot 2025-08-19 162321.png` |

#### Product List Fetch and Database Update
![Product List Fetch and Database Update Workflow](Screenshot 2025-08-25 123129.png)

---

#### Data Extraction and Google Drive Export
![Data Extraction, CSV Preparation, and Google Drive Export Workflow](assets/images/Screenshot 2025-08-19 162321.png)
