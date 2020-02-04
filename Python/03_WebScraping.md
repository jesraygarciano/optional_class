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
1. import libraries

    ```Python
    import requests
    from bs4 import BeautifulSoup
    ```

2. Access website

    ```Python
    # URL
    url = "https://ja.stackoverflow.com/"

    # Get html from the url
    html = requests.get(url)

    soup = BeautifulSoup(html.content, "html.parser")

    print(soup)
    ```

3. print html by prettify()

    ```Python
    print(soup.prettify())
    ```

4. try to print title

    ```Python
    titleTag = soup.find('title')
    print(titleTag)

    title = soup.find('title').string
    print(title)
    ```

5. get questions by selector

    ```Python
    questions = soup.select(".question-summary")
    print(questions)
    ```

6. print question by loop

    ```Python
    for question in questions:
        print("=" * 10)
        votes = question.select('.votes > .mini-counts > span')[0].string
        status = question.select('.status > .mini-counts > span')[0].string
        views = question.select('.views > .mini-counts > span')[0].string
        title = question.select('.question-hyperlink')[0].string
        link = question.select('.question-hyperlink')[0].get('href')

        print("votes：" + votes)
        print("status：" + status)
        print("views：" + views)

        print("title：" + title)
        print("link：" + link)
    ```