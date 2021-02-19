# Email-Mobile-Extractor-python
Python code to Extract Emails, Mobiles from docx or PDF files and assign it to dataframe for further analysis

Have used glob() to read all the files in the given folder of desired extensions
Extracting E-Mails from the doc file was little challenging as it was not getting captured in open() functions
SO Beside opening the file using docx open() we converted it into text format so as to extract email and mobile number

Regex to Extract Mobile number of different format we have used Regex 

  re.findall(r'[\+\(]?[1-9][0-9 .\-\(\)]{8,}[0-9]',string)

   [ '+91 989420701' ,'+919892420701', '+30 (0)4 1723 0900', '+63 (0)2 4723 7000', '60 (0)6 255 9000', '+6 (03) 9894 8686', '+6 (03) 8924 2070', '60 (7) 260-5270', '+60 (7) 228-6301', '+603-540-905']

   Basically, the regex lays out these rules

    The matched string may start with + or ( symbol
    It has to be followed by a number between 1-9
    It has to end with a number between 0-9
    It may contain 0-9 (space) .-() in the middle.


Regex to Extract Email Id's 

re.findall(r"[a-z0-9\.\-+_]+@[a-z0-9\.\-+_]+\.[a-z]+", string)