# WebScraping

## Agenda
1. create project
2. install library
3. Add logic

### 1. Create Project

1. Click this link [https://colab.research.google.com/notebook#create=true&language=python3](https://colab.research.google.com/notebook#create=true&language=python3)

### 2. Install Library

```JavaScript
!pip install beautifulsoup4
!pip install requests
```

### 3. Add logic
1. Access website

    ```Python
    import requests
    from bs4 import BeautifulSoup

    # URL
    url = "https://www.google.com/search?q=example"

    # Get html from the url
    html = requests.get(url)
    ```

2. Print title for Check access

    ```Python
    soup = BeautifulSoup(html.content, "html.parser")

    title = soup.find('title').text
    print(title)
    ```