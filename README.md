
# Web Crawler Project

## Overview

This project is a **Python-based web crawler** that traverses websites, collects content, and builds a **graph structure** of the URLs. The focus of this crawler is on educational websites, and it filters URLs based on a user-provided search term. The crawler ensures that it only visits pages within the same domain, making it more controlled and focused.

## Features

- **URL Filtering**: The crawler filters and starts from URLs that match a search term specified by the user.
- **Graph Structure**: The URLs are represented as a graph where each node is a URL and edges represent links between them.
- **Content Indexing**: The textual content of each visited page is indexed and stored.
- **Same-Domain Crawling**: The crawler only follows links within the same domain to avoid irrelevant external content.
- **Customization**: You can set the number of pages to crawl and the search term for filtering relevant URLs.

## Installation

1. **Install Dependencies**:
   Use `pip` to install the necessary Python packages:
   ```bash
   pip install -r requirements.txt
   ```

   The project requires the following libraries:
   - `requests`: For sending HTTP requests.
   - `BeautifulSoup4`: For parsing and navigating HTML content.
   - `collections`: For managing the graph and queue efficiently.

2. **Run the Crawler**:
   ```bash
   python crawler.py
   ```

## Usage

1. **Input the Starting URLs**:
   - You can modify the list of starting URLs in the script. By default, the starting URLs are a collection of popular educational websites such as:
     - `https://www.scaler.com`
     - `https://www.guvi.in`
     - `https://www.coursera.org`
     - `https://www.udemy.com`

2. **Provide a Search Term**:
   The crawler allows you to filter the URLs based on a search term. For example, if you want to crawl content related to "guvi," you can input `guvi` as the search term.

3. **Max Pages to Crawl**:
   You can set the maximum number of pages the crawler should visit. The default is set to 10 pages.

## Project Structure

```bash
web-crawler/
│
├── crawler.py          # Main Python script for the web crawler
├── requirements.txt    # List of dependencies
└── README.md           # Project documentation
```

## Example

### Running the Crawler
```bash
python crawler.py
```

### Sample Output:
```plaintext
Enter search term to filter URLs: guvi
Crawling: https://www.guvi.in
Crawling: https://www.guvi.in/courses
...
```

### Output: 
The program will display the list of crawled URLs and their graph structure.

---

## Future Enhancements

- **Multithreading**: Implement concurrent crawling to improve the speed of large-scale crawls.
- **Content Analysis**: Add functionality to analyze the content for specific keywords or phrases.
- **Storage Options**: Implement saving the crawled content and graphs to a database for future reference.

