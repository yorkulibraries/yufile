# LaTeX template for continuing appointment and tenure files

At York University faculty achieve tenure while librarians and archivists achieve continuing appointment, which is equivalent but managed with a slightly different process.  For everyone, a file preparation committee works with the candidate to build a file that forms the candidate's application for advancement or promotion.  The file is made up of various documents that show the candidate meets all the necessary criteria.  In the Libraries, it will usually be over 300 pages.

+ [2021–2024 tenure and promotion, and continuing appointment, document](https://www.yufa.ca/2021_24_t_p)
+ [T&P toolkit for faculty](https://www.yorku.ca/secretariat/senate/tenure-and-promotions-committee/tp-toolkit/)

Collecting many different documents into one, while managing a table contents and sensible pagination, is not easy.  Reportedly many committees use PDF-XChange Editor or Adobe Acrobat, but this involves a lot of finicky work.

Another approach is to use [LaTeX](https://www.latex-project.org/) (see the [Wikipedia entry](https://en.wikipedia.org/wiki/LaTeX) for more, including how to pronounce the name).  It will be most familiar to people in the sciences.  To those who have not used it, LaTeX may appear quite technical at first glance.  It is, but it's possible to use it to make attractive and readable documents with just surface knowledge (admittedly, as long as nothing goes wrong).  In this case, using LaTeX means one consitutent document of the file can be replaced and the entire thing regenerated in seconds, with the table of contents and pagination updating automatically.  No tedious manual renumbering is needed.

## Naming the included PDFs

PDFs should have names that begin with their location in the file and (except for in the front matter) then add another number to indicate the placement. For example:

+ 0.1 CV.pdf
+ 0.2 Job Description 2023.pdf
+ 0.3 Personal statement.pdf
+ A 1.1.1 Course 1 name slides.pdf
+ A 1.1.2 Course 1 name worksheet.pdf
+ A 1.1.3 Course 1 name handout.pdf
+ A 1.2.1 Course 2 name slides.pdf
+ A 1.2.2 Course 2 name handout.pdf
+ A 2.1.1 Reference example 1.pdf
+ A 2.2.1 Reference example 2.pdf
+ B 1.1.1 Chapter.pdf
+ B 1.2.1 Article.pdf
+ B 2.1.1 Presentation slides.pdf
+ B 3.1.1 Association report.pdf
+ C 1.1.1 Library committee report.pdf
+ C 1.2.1 University committee report.pdf

All of this can be set out in a spreadsheet, which can first be used to plan the contents and then to note whether the pieces have been found and are in place.

PDFs go in the `pdfs` directory.

## Requirements

This requires a current LaTeX installation and some knowledge of the command line and file system.

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
