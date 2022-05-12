# Convert-any-eBook-into-Audiobook
Convert any eBook into Audiobook: 12 lines of Python
# Contents  
1  Step -  Installing Requirements
2  Step -  Importing Libraries
3  Step - Extracting Pdf
4  Step - Making Python Read

# Complete Code

import pyttsx3
import PyPDF2
book = open('abcd', 'rb')
pdfReader = PyPDF2.PdfFileReader(book)
pages = pdfReader.numPages
print(pages)
speaker = pyttsx3.init()
page = pdfReader.getPage(6)
text = page.extractText()
speaker.say(text)
speaker.runAndWait()
