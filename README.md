# Convert-any-eBook-into-Audiobook
Convert any eBook into Audiobook: 12 lines of Python
# Contents  
1. Step -  Installing Requirements
2. Step -  Importing Libraries
3. Step - Extracting Pdf
4. Step - Making Python Read

# Complete Code

 1. import pyttsx3 
 2. import PyPDF2 
 3. book = open('abcd', 'rb') 
 4. pdfReader = PyPDF2.PdfFileReader(book) 
 5. pages = pdfReader.numPages 
 6. print(pages) 
 7. speaker = pyttsx3.init() 
 8. page = pdfReader.getPage(6) 
 9. text = page.extractText() 
 10. speaker.say(text) 
 11. speaker.runAndWait() 
