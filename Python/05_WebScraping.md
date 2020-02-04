# WebScraping

## agenda
1. Install libraries
2. Get authentication for spreadsheet
3. Make SpreadSheet for output
4. output header
5. access webpage and output

## example
https://colab.research.google.com/drive/1RizXlz1XvFYXlgcpEJ0gQhymiAKxzd7y#scrollTo=In4Qz5WPmWVU

1. Install libraries

  ```Python
  !pip install beautifulsoup4
  !pip install requests
  !pip install --upgrade -q gspread
  ```

2. Get authentication for spreadsheet

  ```Python
  from google.colab import auth
  auth.authenticate_user()

  import gspread
  from oauth2client.client import GoogleCredentials

  gc = gspread.authorize(GoogleCredentials.get_application_default())
  ```

3. Make SpreadSheet for output

  ```Python
  output_sheet_name = 'Optional Class'
  sh = gc.create(output_sheet_name)
  worksheet = gc.open(output_sheet_name).sheet1
  ```

4. output header

  ```Python
  worksheet.update_acell('A1','Title')
  worksheet.update_acell('B1','Description')
  worksheet.update_acell('C1','Link')
  ```

5. access webpage and output

  ```Python
  import requests
  from bs4 import BeautifulSoup

  # URL
  url = "https://ja.stackoverflow.com/questions"

  # Get html from the url
  html = requests.get(url)

  soup = BeautifulSoup(html.content, "html.parser")

  # repositories = soup.find_all(itemprop="name codeRepository")
  repositories = soup.select(".question-summary")

  # print(repositories)

  row = 2

  for repository in repositories:

    title = repository.select('.question-hyperlink')[0].string
    excerpt = repository.select('.excerpt')[0].string
    link = repository.select('.question-hyperlink')[0].get('href')

    worksheet.update_cell(row,1, title)
    worksheet.update_cell(row,2, excerpt)
    worksheet.update_cell(row,3, link)

    row += 1

  ```