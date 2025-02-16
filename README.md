# PubMed Paper Fetcher

A Python tool to fetch research papers from PubMed based on a search query, extract relevant details, and save the results to a CSV file.

---

## Features

- Fetch PubMed IDs for a given search query.
- Extract detailed information (e.g., title, publication date, authors, affiliations, emails) for each paper.
- Identify non-academic authors and their company affiliations.
- Save results to a CSV file for further analysis.
- Debug mode for detailed logging.

---

## Installation

### Prerequisites

- Python 3.8 or higher.
- Poetry (for dependency management).

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Surath15/PubMed_Paper_Fetcher.git
   cd PubMed_Paper_Fetcher
   ```

2. **Install dependencies**:
   ```bash
   poetry install
   ```

3. **Activate the virtual environment**:
   ```bash
   poetry shell
   ```

---

## Usage

### Basic Usage

Run the program with a search query:
```bash
poetry run python PubMed/main.py "cancer research"
```

### Save Results to CSV

To export the results to a CSV file, use the `-f` flag:
```bash
poetry run python PubMed/main.py "cancer research" -f results.csv
```

### Debug Mode

Enable debug mode for detailed logs:
```bash
poetry run python PubMed/main.py "cancer research" -d
```

---

## Command-Line Arguments

| Argument       | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `query`        | The search query to be used with PubMed (e.g., "cancer research").          |
| `-f / --file`  | (Optional) Filename for saving the output CSV.                              |
| `-d / --debug` | (Optional) Toggle debug mode for additional logging.                        |

---

## Example Output

The CSV file will contain the following columns:
- **PubmedID**: The PubMed ID of the paper.
- **Title**: The title of the paper.
- **Publication Date**: The publication date (YYYY/MM/DD or YYYY).
- **Non-academic Author(s)**: Authors with industry affiliations.
- **Company Affiliation(s)**: Companies associated with non-academic authors.
- **Corresponding Author Email**: Email of the corresponding author.

---

## Dependencies

- **requests**: For making HTTP requests to the PubMed API.
- **pytest**: For testing (development dependency).

---

## Project Structure

```
my_project/
├── PubMed/
│   ├── main.py              # Main script to fetch and process papers
│   ├── pubmed_utils.py      # Utility functions for PubMed API interaction
├── pyproject.toml           # Poetry configuration file
├── README.md                # This file

```

---
 
