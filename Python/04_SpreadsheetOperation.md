# SpreadsheetOperation

## agenda
1. Install library
2. Get authentication for spreadsheet
3. Make SpreadSheet for output
4. output data
5. practice

# example
https://colab.research.google.com/drive/1pYHji-qVnKDv71rUmw5dF7oaf8_oLgvX

1. Install library

  ```Python
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

4. output data

  ```Python
  worksheet.update_acell('A11','This is A11')
  worksheet.update_acell('B12','This is B12')
  worksheet.update_acell('C13','This is C13')

  worksheet.update_cell(14,1, "This is A14")
  worksheet.update_cell(15,2, "This is B15")
  worksheet.update_cell(16,3, "This is C16")
  ```

5. Practice (9 * 9)

  ```Python
  for i in range(1, 10):
    for j in range(1, 10):
      worksheet.update_cell(i,j, i*j)
  ```