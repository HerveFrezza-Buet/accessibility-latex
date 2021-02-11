# accessibility-latex

Few simple tips for writing accessible documents in latex. Indeed, visually impaired persons may appreciate bigger font sizes, wide figures, and more contrasted math equations. The present tools allows for editing, from the same latex code, two versions of a document: a regular version for standard readers, and a version with the previously mentioned features. This is done effortlessly, so that any author can consider producing the two kind of documents for any lecture material, article, etc.


# Getting the files

git clone https://github.com/HerveFrezza-Buet/accessibility-latex.git


# How to

There is no specific package to be added, but only few files to copy at the root of your latex project. These files are

- set-accessibility.tex
- unset-accessibility.tex
- accessibility-header.tex

Once you are done, instrument your latex file as done in the example.tex (only few commands need to be added). Let us use this example file here.

On the header, comment out only the 'unset-accessibility' input in the example.tex file, and then compile as usual.

```
pdflatex example.tex
mv example.pdf example-regular.pdf
```


Then edit the example.tex file again, change the comments so that only the 'set-accessibility' input is commented out. Compile the new version.

```
pdflatex example.tex
mv example.pdf example-accessible.pdf
```

Compare the two pdfs you have generated to see the effect of accessibility setting.
