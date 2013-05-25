TrY
===

TeX/LaTeX compilation automation.

Author: Ajabu Tex <ajabutex@gmail.com>  
Version: 3.2 - May 7, 2013

* * *

Program for automating the compilation of TeX/LaTeX documents. Scans the
commands from the comment lines of the document and executes them
automatically.

Great attention is paid to the flexibility and ease of use.


Limitations
-----------

TrY is written for Linux and works on Linux. I didn't test the program on
Windows.  
**I don't know if the program properly works on Windows. I think not.**


Contents of the package
-----------------------

*   try.nw: the source code of the program and the documentation
*   try: the python program
*   try-doc.pdf: the documentaton
*   sha1.sum: checksum report
*   README: this file


How to compile it
-----------------

The source file (`try.nw') is written in noweb, a tool by Norman Ramsey
for Literate Programming. To extract and compile the program and the
documentation use the following commands:

*   program

        $ notangle -Rtry try.nw > try
        $ chmod +x try

*   documentation

        $ noweave -index try.nw > try-doc.tex
        $ pdflatex try-doc.tex
        $ pdflatex try-doc.tex
        $ pdflatex try-doc.tex


Installation
------------

Copy the file `try` into the `bin` directory of your system, e.g.:

    $ sudo cp try /usr/bin/try


Use
---

Open a terminal and use the following command line:

    $ try [file [--log] [--verbose] | --help | --version]

More on this in `try-doc.pdf`


Contributing
------------

If you want to fork the project or want to send a pull request go to

    https://github.com/AjabuTex/TrY
    

License
-------

This material is subject to the LaTeX Project Public License. See

    http://www.ctan.org/tex-archive/help/Catalogue/licenses.lppl.html 

for the details of that license.


Happy TeXing.
