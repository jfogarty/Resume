John's Résumé in LaTeX
======================

This is my résumé typesettable to a hyperlinked PDF using LaTeX.
([Click HERE](https://rawgithub.com/jfogarty/Resume/master/jfogarty-resume-2017.pdf))

This version is based on the [nice GitHub project of cies-breijs](https://github.com/cies/resume).

Obviously it only relies on open source stuff.

## Generating the PDF

There are several ways to generate a PDF from the Latex sources. 
My preferred mechanism is to use the interactive TeXLive editor.


#### LaTeX TeXLive 2016

 I **strongly** recommend
that you install [TeX Live 2016](https://www.tug.org/texlive/doc/texlive-en/texlive-en.html).
All of the tools required by this project are already part of the 
TexLive 2016 distribution. If you try to use ad-hoc versions of LaTeX 
and packages, you may spend a very long time debugging.

You will need to make sure that TexLive is in your path (on my system
this is `/usr/local/texlive/2016/bin/x86_64-linux`).

You can check that you have a proper TeXLive install with **tex --version**:

```
  $ which tex # This is a linux command to discover the install path.
      /usr/local/texlive/2016/bin/x86_64-linux/tex
  $ tex --version
      TeX 3.14159265 (TeX Live 2016)
      kpathsea version 6.2.2
      ...

```

#### Using ShareLatex (no need to install any software)

[ShareLatex](http://www.sharelatex.com) is a web application for creating
and collaborating on LaTeX documents.  They have a free account that
can be used to compile this resume.

To get this resume compiled into a PDF with ShareLatex:

  1. Go to [sharelatex.com](http://www.sharelatex.com) and create first an account and then a project.
  2. In your new project replace the content of the `main.tex` file with the LaTeX source of resume's content (`cies-breijs-resume.tex` in this case) from Github.
  3. In your new project create a new file `resume.sty` and copy-paste
     the content of the same named file from the Github repo.
  4. Finally hit the "Compile" button to view and/or download the resulting PDF.

The result will be nice, but IMO will be nicer if you change the
rendering engine to XeLaTeX -- you can do so from the projects 'Setting' form
which hides behind the gear-icon on the left.

*TIP:* In the 'User Settings' (under 'Account' menu in the top-right) form you can set the spell-check language.


#### Using XeLaTeX

XeLaTeX is a version of Latex with great font rendering fuctionality (unicode, bidi,
special font features).  Since my resume uses 'lower case numerals' it
looks slightly better with XeLaTeX.

In recent Ubuntu versions you simply clone this project, change
directory to the root of the project and do:

        sudo apt-get install texlive-xetex texlive-latex-recommended tex-gyre
        ./xelatex *-resume.pdf

If all went well an updated version of the PDF is found in your current
working directory, alongside a bunch of `.log` and `.aux` files that
you can safely ignore.


### Using pdfLatex

Follow the same steps as for XeLaTeX, just replace the `./xelatex`
command with `./pdflatex`.


## Terms of sharing

Feel free to use, copy, fork, share, study and/or modify it because the LaTeX source code of the `resume.sty` file is [MIT](http://en.wikipedia.org/wiki/MIT_License) licensed.

The text of my resume in the `jfogarty-resume.tex` file is [CC-NC-ND](http://creativecommons.org/licenses/by-nc-nd/3.0/) licensed.
