# pdf

Best tools are pdfid, pdf-parser and peepdf (python2 only)

**First use pdfid to have an overview of what is inside the pdf:**
```
pdfid.py PDF.PDF
```

**Display stats with pdf-parser:**
```
pdf-parser.py -a PDF.PDF
```

**Parse the whole pdf with pdf-parser:**
```
pdf-parser.py PDF.PDF
```

**Show detail on a specific object:**
```
pdf-parser.py --object id file.pdf
```

**Search for javascript:**
```
pdf-parser.py --search=javascript pdf.pdf
```

Search for :
* / OpenAction && /AA #usually where the script or action will run automatically
* /JavaScript & /JS where JS will run
* / GoTo will change the view to a specified destination within the PDF or in another PDF
* /Launch will launch a program or open a document
* /URI open a URL
* / SubmitForm / GoToR can send data to URL
* / RichMeda can be used to embed flash
* / ObjStm can hide objects inside it
* Obfsucation with hex code, is a pattern i.e. /JavaScript vs. /J#61vaScripto
