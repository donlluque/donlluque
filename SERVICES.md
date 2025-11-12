# 🔧 Services & Workflow

## Overview

I provide Python automation focused on **accuracy** and **repeatability**. All deliveries include:

- Clear, terminal-ready scripts (no notebook dependency)
- Explicit validations: missing required columns trigger errors before processing
- Comprehensive logging for debugging and audit trails
- Extensible structure (ready for Google Sheets API / cron scheduling)

---

## 📦 Core Services

### 1. CSV/Excel Processing
- Merge multiple sources with different structures
- Apply column mappings (`original_name` → `standardized_name`)
- Detect and report missing required columns
- Output clean CSV/XLSX files ready for analysis

**Common Use Cases:**
- Combining monthly exports from different systems
- Standardizing vendor data feeds
- Preparing datasets for database ingestion

### 2. API Data Extraction
- Paginated endpoint handling with automatic continuation
- Field filtering to reduce payload size
- Rate limiting and retry logic for stability
- Response validation and error handling

**Common Use Cases:**
- Extracting records from REST APIs (pagination handling)
- Filtering specific fields from large JSON responses
- Scheduled data pulls with incremental updates

### 3. Data Validation & Quality
- Required column presence checks
- Basic type validation (dates, numbers, emails)
- Missing value summaries by column
- Simple duplicate detection with configurable keys

**Outputs:**
- Validation reports (JSON/CSV)
- Processing logs with row-level errors
- Summary statistics

### 4. PDF Operations
- Text extraction using pdfplumber
- Batch renaming based on:
  - Regex patterns in filenames
  - Internal text content extraction
  - Sequential numbering with prefixes

**Common Use Cases:**
- Renaming invoice PDFs by extracted invoice number
- Organizing document batches by internal dates
- Standardizing filename conventions

### 5. Backend APIs (FastAPI/Flask)
- REST endpoints for file processing tasks
- Asynchronous job handling with Celery + Redis
- Database integration (PostgreSQL/MySQL)
- Docker containerization for deployment

---

## 🔄 Typical Workflow

### Step 1: Scope Confirmation
You send:
- **Sample files** (1-2 examples with representative data)
- **Column requirements**:
  - Original column names
  - Desired output names (mapping)
  - Required columns (cannot be missing)
- **Output format** (CSV, XLSX, JSON)
- **Volume** (approximate row counts per file)

I respond with:
- Feasibility assessment
- Edge cases to handle (date formats, encoding, special characters)
- Estimated delivery time

### Step 2: Initial Delivery
I provide:
- CLI script with `--help` documentation
- Example command: `python script.py --input data/ --output result.csv --config mappings.json`
- README with setup instructions
- Sample run log

### Step 3: Testing & Adjustment
You run with your data and report:
- Any unexpected behaviors
- Column naming preferences
- Additional validations needed

I deliver minor adjustments (usually same day).

### Step 4: Final Delivery
Complete package includes:
- Final script with all adjustments
- `requirements.txt` with exact dependency versions
- Full documentation (setup, usage, troubleshooting)
- Example data and expected output

---

## 🛠️ Technology Stack

**Core:**
- Python 3.9+ (type hints, dataclasses)
- pandas (data manipulation)
- requests (API calls with retry logic)
- pdfplumber (PDF text extraction)
- openpyxl (Excel read/write)

**CLI & Logging:**
- argparse (command-line interfaces)
- logging (structured logs with levels)
- pathlib (cross-platform file handling)

**Backend (when needed):**
- FastAPI / Flask
- Celery + Redis (async task queues)
- SQLAlchemy + Alembic (database ORM/migrations)
- Docker (containerization)

---

## ✨ Differentiators

### 1. **Terminal-Ready Scripts**
No Jupyter notebooks. All scripts run from CLI with:
```bash
python process.py --input files/ --output result.csv --validate
```

### 2. **Early Validation**
Scripts fail fast with clear messages:
```
ERROR: Missing required columns in file1.csv: ['customer_id', 'purchase_date']
```

### 3. **Extensible Architecture**
Code structured for future enhancements:
- Add Google Sheets API integration
- Schedule with cron/Airflow
- Expose as REST API

### 4. **Reproducible Results**
- Deterministic processing (same input → same output)
- Comprehensive logging (every decision is logged)
- Version-pinned dependencies

---

## 🚀 Getting Started

**Send me:**

1. **File samples** (Dropbox/Drive link or email attachment)
2. **Requirements document** (can be simple bullet points):
   ```
   Input: 5 CSV files with different column names
   Mapping: see attached spreadsheet
   Required columns: user_id, transaction_date, amount
   Output: single CSV with 10 standardized columns
   Volume: ~50k rows per file
   ```

**I'll respond within 24h with:**
- Confirmation of feasibility
- Questions about edge cases
- Delivery timeline (typically 2-5 days depending on complexity)

---

## 📞 Contact

- **Email:** donlluque@gmail.com
- **LinkedIn:** [linkedin.com/in/donlluque](https://www.linkedin.com/in/donlluque/)

**Timezone:** UTC-3 (Argentina) - Usually respond within 12 hours