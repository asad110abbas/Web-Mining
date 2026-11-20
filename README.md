# 🕸️ BRIHA · Web Mining with Pagination

![Part of BRIHA](https://img.shields.io/badge/Part_of-BRIHA-8B5CF6?style=for-the-badge&labelColor=0B1024)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Requests](https://img.shields.io/badge/Requests-2CA5E0?style=flat-square) ![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4B8BBE?style=flat-square) ![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

> ⚡ **Part of [BRIHA](https://github.com/asad110abbas)** · Briha Research, built by Syed Asad Abbas.

A complete **web-scraping pipeline** that walks through every page of a paginated website, extracts
structured records and saves them as a clean dataset ready for analysis.

## Pipeline
```mermaid
flowchart LR
    A[Start URL] --> B[requests: fetch page]
    B --> C[BeautifulSoup: parse records]
    C --> D{Next page?}
    D -- yes --> B
    D -- no --> E[(pandas → CSV)]
```

## Highlights
- **Automatic pagination:** follows "next" links or page numbers until the last page
- **Structured extraction** with BeautifulSoup selectors
- **Clean output** as a pandas DataFrame exported to CSV
- **Polite scraping** with request headers and delays

## Run
```bash
pip install requests beautifulsoup4 pandas
```
Open `Web_Mining.ipynb`, set the target URL and run all cells.

> Use responsibly and respect the website's terms of service.
