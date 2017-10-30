# Columbia University Latex Dissertation Template
by Stephanie Lackner (2017)

## Introduction (by Charles McNamara)

If you're writing a dissertation in a Ph.D. program at Columbia University, you need to follow a very strict [set of formatting guidelines](http://gsas.columbia.edu/content/formatting-guidelines) set by the university. These guidelines can be difficult to follow if your writing software refuses to cooperate. I have seen too many highly credentialed adults cry over page numbers and bibliography spacing.

I write my dissertation using LaTeX, and I've written a template that follows the guidelines set by the dissertation office. If you're a student at another university, you may find this template useful, but you should of course consult your own university's guidelines for dissertation formatting.

The file that controls the dissertation formatting is Dissertation.tex in the parent folder. I've set up subdirectories for every chapter just to keep things tidy when LaTeX compiles all the documents.

I hope this template helps you finish your dissertation with a little less stress! Good luck!

## How do I use this template? (by Charles McNamara)

The Dissertation.tex file in the parent directory sets up the required formatting for the whole document. It also creates the title page, copyright page, abstract, table of contents, acknowledgements, and dedication pages. To edit those pages, you'll have to look for the appropriate sections in that file. Everything has extensive commenting to help you navigate the file. This file also sets up the bibliography, which appears at the end of the document.

Dissertation.tex should not include any text for your chapters, introduction, or conclusion. These files are kept in their own subdirectories (Chapter1, etc.) to keep your files tidy. I've already set up .tex files in those subdirectories to get your started.

Just compile Dissertation.tex: it includes all the chapter .tex files.

You can comment out the chapters in Dissertation.tex if you don't want to compile the whole thing.

## Compiling the individual chapters
This template allows to compile the individual chapters on their own or as part of the entire dissertation with relatively minimal effort.

To compile an individual chapter, the comment environments at the beginning and end of the document have to be deactivated (put a `%` in front of each of the `\begin{comment}` and `\end{comment}` to comment out the four lines), and activate the comment environment around the chapter title (remove the `%` in front of the `\begin{comment}` and `\end{comment}` to uncomment the two lines).

To compile the entire dissertation the reverse has to be done for each chapter, introduction, and conclusion. The comment environments at the beginning and end of each of the individual documents have to be activated and the comment environment around the chapter title in each individual document has to be inactive.

The workflow I used was to write on each chapter separately as if it was its own document, keeping the comment environments at the beginning and end of the document deactivated and the comment environment around the chapter title activated. Once the chapter was done (and I sent a compiled pdf version of the chapter to my advisers), I switched the activation status (activated / deactivated the respective comment environments), so that the file was ready to be included in the entire dissertation. I did not switch around much between compiling the entire dissertation and compiling individual chapters. It was therefore really minimal effort to do this.

I am aware that this is not the most elegant solution. A more elegant solution would be, for example, to have a separate .tex document in each folder that basically only includes the parts that have to be uncommented to run the dissertation, and an include the chapter line, and you would have to put the chapter titles in the dissertation file. However, if you are using automatic citation completion that wouldn't work in this setup and you would need to go into the other document every time you want to compile the chapter you are working on. That would have been to much annoyance for me. My solution is definitely less elegant, but I think it is actually quite practical (at least for my workflow).


## How is this different to Charles McNamara's version?
I was really happy when I came across Charles McNamara's template. However, I and some of my colleagues ran into issues and we all had to make a number of changes to it to be able to use it. This is why I decided to create my own template and share it again.

Here is a list of the main changes compared to Charles McNamara's version:
* I and some of my colleagues had troubles with XeTex, so I adjusted the template to work without XeTex
* Adjusted the individual files so that they can be compiled with relatively minimal effort either alone or as part of the entire dissertation
* Added more useful packages (e.g. grapicx to include images)
* Added a folder for figures and set the graphicspath to that folder
* Changed the memoir option from twosided to onesided
* Added list of figures and list of tables

#LaTeX and "Should I use this?" (by Charles McNamara)

## What is LaTeX? Why should I use it to write my dissertation?

LaTeX is a piece of writing software. It's especially good for writing long, technical documents like dissertations. If you'd like to learn more about it, head over to the [official website](http://latex-project.org).

People use LaTeX for different reasons. I like a few things about it:

* I like writing in regular text files. I can write my dissertation on any computer, and I don't have to worry about screwing up the formatting.
* I can write each sentence on its own line. By breaking down my writing by sentence, I have a better sense of what each sentence is doing.
* By writing each sentence on its own line, I can use GitHub to make version-controlled backups of my dissertation. This kind of backup lets me look through old revisions easily.
* LaTeX has some really great tricks for managing your bibliography and using references throughout your work. I use [JabRef](http://jabref.sourceforge.net/) to manage my bibliography, and I prefer it to Zotero.
* The output looks great!

## Why should I not use LaTeX?

* It can be disorienting to write in a markup language. If you're used to writing HTML, it should be okay. It helps to use a text editor with good syntax highlighting. I use Vim.
* You may not be able to send files back and forth with your adviser so easily. My adviser doesn't use Word's Track Changes function or anything like that. We just use hand-written comments on hard copies or comments on PDF files.
* It can be a real struggle to force LaTeX to format pages exactly how you want to format them. I'm posting this document so that you don't have to think about the specific formatting Columbia requires, and you can just write the dang thing.

## This sounds like a headache.

It is kind of a headache. I learned how to use LaTeX in some math coursework in college, and I strongly prefer it to Word. But getting started can be rough. It might not be worth writing your dissertation in LaTeX if you've never used it before. If you are comfortable using it, however, this template will save you a lot of time.

Saving time is the name of the game here. You shouldn't have to fight with Word to finish your Ph.D., and you shouldn't have to fight with LaTeX either. I can't help with Word, but this LaTeX template should help.


## Good Luck!
