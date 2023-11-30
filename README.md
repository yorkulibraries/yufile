# LaTeX template for continuing appointment and tenure files

At [York University](https://www.yorku.ca/) (in Toronto, Canada) faculty achieve *tenure* while librarians and archivists achieve *continuing appointment*, which is equivalent but managed slightly differently.  Both processes are documented in the collective agreement of the [York University Faculty Association](https://www.yufa.ca/).

For everyone, a file preparation committee works with the candidate to build a file that forms the candidate's application for advancement or promotion.  The file is made up of various documents that show the candidate meets or exceeds all the necessary criteria.  In the Libraries, it will be a PDF with usually over 300 pages.

+ [2021–2024 tenure and promotion, and continuing appointment, document](https://www.yufa.ca/2021_24_t_p)
+ [T&P toolkit for faculty](https://www.yorku.ca/secretariat/senate/tenure-and-promotions-committee/tp-toolkit/)

Collecting many different documents into one, while managing a table contents and sensible pagination, is not easy.  Reportedly many committees use PDF-XChange Editor or Adobe Acrobat, but this involves a lot of finicky work.

Another approach is to use [LaTeX](https://www.latex-project.org/) (see the [Wikipedia entry](https://en.wikipedia.org/wiki/LaTeX) for more, including how to pronounce the name).  It will be most familiar to people in the sciences.  To those who have not used it, LaTeX may appear quite technical at first glance.  It is, but it's possible to use it to make attractive and readable documents with just surface knowledge (admittedly, as long as nothing goes wrong).

Using LaTeX means one constituent document of the file can be replaced and the entire thing regenerated in seconds, with the table of contents and pagination updating automatically.  No tedious manual renumbering is needed.

## Template structure

The template LaTeX file here is structured for librarians and archivists advancing from Pre-Candidacy to Candidacy (staying at Assistant rank) or from Candidacy to continuing appointment (and moving from Assistant to Associate).  Sections could easily be renamed to suit faculty.  Files for candidates applying for promotion to full Professor, Senior Librarian or Senior Archivist would be structured differently.

## Naming the included PDFs

PDFs should have names that begin with their location in the file and (except for in the front matter) then add another number to indicate the placement. For example:

+ 0.1 CV.pdf
+ 0.2 Job Description 2023.pdf
+ 0.3 Personal statement.pdf
+ A 1.1.1 Slides.pdf
+ A 1.1.2 Worksheet.pdf
+ A 1.1.3 Handout.pdf
+ A 1.2.1 Slides.pdf
+ A 1.2.2 Handout.pdf
+ A 2.1.1 Reference example 1.pdf
+ A 2.2.1 Reference example 2.pdf
+ B 1.1.1 Chapter.pdf
+ B 1.2.1 Article.pdf
+ B 2.1.1 Presentation slides.pdf
+ B 3.1.1 Association report.pdf
+ C 1.1.1 Library committee report.pdf
+ C 2.1.1 University committee report.pdf

PDFs go in the `pdfs` directory.

## File checklist

All of this can be set out in a spreadsheet (see [example file checklist](file-checklist.ods)) which can be used first to plan the contents and then to note whether the pieces have been found and are in place.

## Requirements

This requires a current LaTeX installation and some knowledge of the command line and file system.

The template uses the [`pdfpages`](https://ctan.org/pkg/pdfpages) package to include PDFs into the file.  `pdfpages` can't handle Word documents or other formats, so they must be converted to PDFs first.

## Building the file

+ Copy the template `candidate-file-template.tex` to `Candidate-Name-Promotion-File.tex` or the like.
+ Edit the file as needed, changing names, adding links to PDFs, etc.
+ Put PDFs in the `pdfs` directory, using the naming scheme.
+ Compile the file into one PDF by running `pdflatex Candidate-Name-Promotion-File.tex` *twice* (the second time will generate the table of contents properly).
+ View `Candidate-Name-Promotion-File.pdf` and appreciate how easy it all was.

See [candidacy-file-template.pdf](candidacy-file-template.pdf) for an example using placeholder documents and slides.

## Contact information

Contact York librarian William Denton <wdenton@yorku.ca> with questions or problems.

## License

This template is licensed as [CC 0](https://creativecommons.org/publicdomain/zero/1.0/).  You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission.
