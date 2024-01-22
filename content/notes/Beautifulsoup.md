---
title: "Beautifulsoup"
---

## What is Beautifulsoup?

From my understanding Beautifulsoup is a parser that can parse HTML and XML and return specific parts you're looking for.

TLDR: Makes life easier with web scraping

Documentation: https://www.crummy.com/software/BeautifulSoup/bs4/doc/

## Quick Start

### Installation

Python:

```bash
pip install beautifulsoup4
```

### Import

```Python
from bs4 import BeautifulSoup
```

### Creating Soup Object 

```Python
soup = BeautifulSoup(html_content, 'lxml') # This is for HTML if you want to parse xml instead of using 'lxml' use 'xml'
```

### Use Cases

```Python
title_tag = soup.title # Gets first instance of the tag "<title>"

all_paragraphs = soup.find_all('p') # Gets all instances of the tag <p>

first_paragraph
```










