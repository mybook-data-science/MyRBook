--- 
title: "An Introduction to R for the Field of Data Science"
author: "Moritz Ebach (400104774), Niklas Strolz (400098595), Frederik Miebach (KOWH116385)"
date: "Last update: July 29, 2019"
site: bookdown::bookdown_site
output: bookdown::gitbook
documentclass: report
bibliography: [book.bib, packages.bib, online.bib]
biblio-style: apalike
link-citations: yes
github-repo: rstudio/bookdown-demo
description: "These are notes gathering our experience to set up R-Studio and use R for data science."
---








# Foreword {-}



> "The statistic is the rhetoric of the empirical sciences."   
>
> --- paraphrase of Alexander Eiler's quote on statistics 



Students with a focus on economics and science have to work a lot with statistical data sets and calculations in order to be able to carry out evaluations. Traditionally, educational institutions work with formula collections and calculators, which has several disadvantages. On the one hand, solutions have to be documented in a laborious way, on the other hand, statistical calculations with formula collections are very time-consuming. The programming language R in combination with R Studio enables students like us to analyze and visualize complex data sets and to adapt them according to our own criteria with less effort compared to the traditional methods. With this book we want to give a practical guide on how to apply these benefits of R to beginners.

So we focus on three questions.

1. What steps must be undertaken to be able to work productively with R and R studio?
2. How can R be used for data science using practical examples?
3. What does a complex project look like in R and what steps must be taken to solve it?

<!--chapter:end:index.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# (PART) Preface {-}

# About the Authors

Frederik Miebach (LinkedIn: Frederik Miebach) is a business student at Hochschule Fresenius, currently studying in the master's degree of International Business Management. He earned his bachelor's degree in International Business Administration at Hochschule Fresenius in Cologne and is currently working in the field of human resources at the Bayer AG in Leverkusen.

Niklas Strolz (LinkedIn: Niklas Strolz) is also a business student at Hochschule Fresenius, currently studying in the master's degree of International Business Management. He earned his bachelor's degree in International Business Management (German) at Hochschule Fresenius in Cologne and is currently working in the field of business consultancy at Deloitte in Düsseldorf.

Moritz Ebach (LinkedIn: Moritz Ebach) is also a business student at Hochschule Fresenius, currently studying in the master's degree of International Business Management. He earned his bachelor's degree in International Business Management at Hochschule Fresenius in Cologne and just finished an internship in the field of M&A at BELGRAVIA & Co. GmbH in Cologne.

After working with R for the first time for a period of in total four months, the group of students is now working on a student project, which focuses on the design of a book about "R in Data Science". 

<!--chapter:end:01-authors.Rmd-->

# Structure of the book

The preface of the book focuses on a short description of the authors, a short introduction to the book itself, an explanation of what R is and how it can be used, as well as the first steps of a project with R (including the linkage between R and GitHub). The preface is therefore a basic introduction to R and how projects are and can be designed. The first chapter of the book then focuses on source and output files. It is a continuation of the preface with much more detail on how R can be used and how data is imported into R. The first chapter therefore includes topics such as R Markdown files, importing data into R, using R as a calculator and using data structures. Note: The preface and first chapter of the book are fundaments of how to work with R and how to get started. Therefore, it is important to read these two parts of the book very carefully for the first time and follow every step carefully. The second chapter of the book focuses on tidyverse, which is an opinionated collection of R packages designed for data science. All packages share an underlying design philosophy, grammar, and data structures. The final chapter of the book then focuses on how to use R for data science. The knowledge of the first chapter should therefore be utilized for the second chapter of the book. For the chapter of data science or data analysis, we have decided to meke use R basics, in order to analyze various data (e.g. simple functions on vectors, subsetting, functions etc.). 

To sum it up, this book is a reference for working with R as a tool or language for data science. Make sure to make use of the Pareto principle (80/20 rule) when reading it. Not all sections are equally useful or important to the particular book or even books that you intend to write.

<!--chapter:end:02-structureofthebook.Rmd-->

# Introduction

"Data science is the field of study that combines domain expertise, programming skills, and knowledge of math and statistics to extract meaningful insights from data" (DataRobot, 2019).
It is therefore a discipline that allows you to convert raw data into a valuable source of understanding, insight, and knowledge. 

This book is an introduction to R for the field of data science. It was designed in the course of a project study in data science at Hochschule Fresenius in Cologne and is a guide to the language of R with a linkage to the platform GitHub and data science. It is therefore a guide on how to design a book or project with R and afterwards publish it. The goal of the book “An Introduction to R for the Field of Data Science” is therefore designed to help you learn some of the most important tools in R that will enable you to do data science or data analysis. After reading this book, you will have access to a variety of tools to tackle a wide range of data science challenges, using the fundamental parts of R. In order to understand every part of the book, it might be useful to acquire some basic knowledge about R and data science. Therefore, beginners can start with the cheatsheet, which is available at [RStudioCheatsheet](https://www.rstudio.com/resources/cheatsheets/).

<!--chapter:end:03-introduction.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# Explaining R - What is it?

This chapter of the book starts with the explanation of what R is and how R can be used.

## What is R?

Let's start with a short definition of R: "R is a programming language developed by Ross Ihaka and Robert Gentleman in 1993, which possesses an extensive catalog of statistical and graphical methods." 

R includes machine learning algorithm, linear regression, time series, statistical inference and many other features.

Not only academic companies trust in R, but many large companies also use the R programming language, including Google, Airbnb, Facebook, Uber and many others.

Focusing on data science or analysis with R, it is important to understand that this is done in a series of steps; programming, transforming, discovering, modeling and communicate the results.

1. Program: R is a programming tool.
2. Transform: R is consists of a collection of libraries designed for data science.
3. Discover: Import the data, optimize them, rethink them and analyze them.
4. Model: R offers a wide ranges of tools to capture an appropriate model for your data.
5. Communicate: Integrate codes, graphs, and outputs to a report with R Markdown and share it with the world via different platforms.

## What is R used for?

1. Statistical inference
2. Data analysis
3. Machine learning algorithm

## R package

Many of the functions available in R come in packages. To install an R package, open an R session and type the following command into the command line:

```{r
install.packages("the package's name")
```

Once the package is installed, the content will be available for usasge.

The fundamental or primary functions of R are statitical interference, visualization, and machine learning.

The most important R packages are listed below, which are mainly uses for the workflow of data science (Data preparation and communication of the results):

```{r
1. dplyr (Command line: install.packages("dplyr"))
2. ggplot2 (Command line: install.packages("ggplot2"))
3. data.table (Command line: install.packages("data.table"))
4. shiny (Command line: install.packages("shiny"))
5. plyr (Command line: install.packages("plyr"))
```

## Communication with R

R offers a variety of ways to present and share work. As explained in previous chapters of the book, this mainly happens through an R Markdown file or document. The results of the work in R can then be published or shared on GitHub, on business websites or other platforms available for R.

Rstudio therefore offers you via R Markdown files to write a document. You can then export the documents in many different formats:

Document:
- HTML
- PDF/Latex
- Word

Presentation:
- HTML
- PDF beamer

## Why use R as a language for programming?

1. R is not just a mix of statistical packages, it’s an own language.
2. R is designed to operate the way that problems are thought about.
3. R is both flexible and powerful.

R is not the only language that can be used for data analysis.  Why R rather than another?  

1. Data analysis can be described as an interactive process, which generally means that you can determine what to do next with what you see at one stage. Therefore, interactivity is very important for programming languages.  Language is very important.  And together, it is an interactive language, which can be used perfectly for programming and data analysis. 

2. The mechanism that R offeres is fantastic for creating a variety of data structures. If you are working on data analysis, you of course want to be able to put data into natural form, which is a key function of R. 

3. Producing graphs for data analysis is a fairly easy process when using R and offers a variety of different options for producing high quality graphs.

4. As mentioned in this chapter R has a package system, which will also be explained in detail in the chapter of "Tidyverse". The packages offered in R give people the opportunity to add own functionalities, which distinguishes it from the central part of R.

5. Important: Real data have missing values, which are a fundamental part of the R language. Functions in R therefore give you the opportunity to control how missing values should be handled. 

6. The R community is very strong. Everyone is committed to the prcoess of improving the language of R and therefore also the process of data analysis. Questions and answers about problems with R are offered online and help optimize the working process with R.

<!--chapter:end:04-explainingr.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# The first steps

## Installing the required applications

The first step of working with R is to download the following free applications, which are available on the following platforms:

  1. Download and install [R](https://cran.uni-muenster.de/) 
  2. Download and install [RStudio, free Desktop version](https://www.rstudio.com/products/rstudio/download/#download)
  3. Download and install [A Latex distribution](https://www.latex-project.org/get/) (e.g., MacTex for Mac or MiKTeX for Windows machines) 

The first two applications are easily and quickly installed for Mac and Windows. The third application is very large (a few Gb) and needs some time to be installed.  

Another application needed is a 

  4. [Git distribution](https://git-scm.com/downloads)

This application is also classified as a free software.  
Once you have installed Git for version control, activate it in RStudio: _Tools> Global Options> Git/SVN_ and click on _Enable version control interface for RStudio projects_.  
Also generate a SHH RSA key. Generating an SHH RSA key is required to link RStudio to a repository on GitHub.

(GitHub is a website and cloud-based service that helps developers store and manage their code, as well as track and control changes to their code)

## Signing up for GitHub

Create an account at GitHub at [https://github.com](https://github.com/join).

## Creating a new project

RStudio projects are associated with working directories in R. RStudio projects can be created: 

- In a new directory
- In an existing directory (R code and data already exists)
- By cloning a version control repository (Available on Git or any other subversion)

Focusing on our our project in Data Science, we will focus on creating an an RStudio project in an existing directory

_File> New project> Existing Directory_ and chose the suggested book folder. You can also change the location of the project working directory. 

Important: Every time you create new content for your book, you must start an Rstudio session _File> Open Project..._  
All the files of the project are the files of the folder (working directory), and vice versa.

## Create a new GitHub repository 

The next step of the process is to create a new repository (pronounced 'repo') on GitHub.com. 
1. Name the repository **exactly** by the name of the created R project / book folder (e.g., 'myRbook').   
2. Enter a description for the repository (Optional)
3. Select public visibility.
4. Select initialize this repository with a README (Optional)
5. Select add .ignore and select R.
6. Create the repository.

After having created the repository, go to the settings of the respective repo and deploy a new SSH key, which has been generated by RStudio. Go to _Settings> Deploy keys_ and click on 'add deploy key'. Copy and paste the SHH key generated by RStudio: _Tools> Global Options> Git/SVN_ and click on view public key.

In RStudio go to _Tools> Project Options...> Git/SVN_. Under _Version control system_, select 'Git'.    

## Link the repository to RStudio 

Still in RStudio, go to _Tools> Terminal> New Terminal_. This will open a Terminal where commands can be typed in.

Start by initializing Git on the terminal.
```{r, eval=FALSE
git init
```

Then paste the message shown at the creation of the repo (changing the names, of course):

```{r, eval=FALSE
git remote add origin https://github.com/YOURNAME/YOURREPO.git
git push -u origin master
```

After finalizing the above described process, the local `master` should now be connected to the `master` on GitHub.  
If necessary, restart RStudio. At the restart, a Git thumbnail should appear in a pane. You are now ready to commit and push your files.

## Commit and push any changes to GitHub

In the next chapter of the book, R Markdown documents or files are explained. In general, a R Markdown file is a record of your research. Whenever RMD files are changed or updated, it is time to commit and push them to your GitHub repository.

1. In RStudio click the "Git" tab in the upper right pane.
2. Click Commit.
3. In the Review changes view, check the staged box for all files you want to commit and push to GitHub.
4. Make sure to always include or add a commit message (e.g. Intial Commit).
5. Click Commit.
6. Click the Pull button to fetch any remote changes from GitHub.
7. Click the Push button to push any changes to the repository on GitHub.
8. On GitHub, navigate to the Code tab of the repository and refresh the page to see the changes.

Important: Before you push any changes to GitHub, make sure to commit the files you want to add.

### Troubleshooting

If this procedure works, great! You're good to go.

Yet: Please be aware that the above described process sometimes hits unexpected problems. These problems are often difficult to understand (especially as a "beginner" of R). If this is the cas, the best sultion is to copy and google the error message. 

The solutions offered on Google will definitely help solve the experienced problem.

## Collaboration on GitHub

There are various established ways for collaborating on a GitHub repo. As a matter of facts, collaboration on a project is the _raison d'etre_ of GitHub.  
We illustrate here the easiest of them, namely the joint reading and writing into one repo by all the members of a team.   
Importantly, it is assumed that all members of the group are able to push/pull code from RStudio to an experimental repo on GitHub (see above).   
The following are the steps in the collaboration's setup.  

### Creation of an organization

The following section focuses on the creation of an organization, which enables a group of people to work on the same project and therefore collaborate via GitHub. Every member of the organization will then have the opportunity to commit, push and pull any changes of the prokject.

Step 1: One member of the group creates an organization on GitHub under _Settings> Organizations> New organization_.  

Step 2: Under the newly created organization, this member of the team creates a new repo whose name is the same as the folder and R project that the group will work on (e.g., 'ouRbook').  

Step 3: The owner of the organization connects RStudio to the repo (Described process) and populates it with the current files of the project.  

### Creation of a team

Step 1: Still as a task of the owner, create a team. Under the organization page in GitHub, simply click on 'New team' and give it a name. A team now appears in the organization page.  In the page of that team, click on 'Add a member'. A window appears where the member to be added can be searched for and added.  

Step 2: Once that member is found and selected, make the double step of adding him/her to the team AND assign him/her to the repo. This second step can still be made later, but it is easier to do it right then.   

Important: Make sure that the new member has reading and **writing** rights to the repo, in order to be able to also make changes. This again can be changed later by navigating the team's page.

### Member of the team

After the steps above, the newly added member receives an email to confirm the participation of the organization and team.   
After accepting or confirming the participation, navigate to the page of the team and locate the repo that the owner has created.  
A button-menu allows to 'Clone or download the repo'. Click to show the https address of the repo, `https://github.com/ORGANIZATION/repo.git` and copy that link.  
Open a simple RStudio session (not a project!). Open a new Terminal (_Tools> Terminal> New Terminal_) and type `cd` (change directory) and a path to the folder where you want the repo to be saved. For instance,

```{r, eval=FALSE
cd Desktop/DataScience/OurRProject 
```

The terminal is writing into that folder, as indicated by the path before the `$` sign in the command line of the terminal.  
Recall that you copied the address of the team's repo. Then, in the command line, type the following commands and your copied address:

```{r, eval=FALSE
git clone https://github.com/ORGANIZATION/repo.git 
```

The whole repo is now a new folder in your directory. If all went well, you can now pull and push into that repo in GitHub.

<!--chapter:end:05-thefirststepsofr.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# (PART) R Basics {-}

# R Markdown files

The following chapter gathers general comments and information about `.Rmd` files.

## General description of R Markdown files

What is R Markdown?

An R Markdown file is a record of your research, or in other words, a format for making dynamic documents with R. In general, an R Markdwon file is written in "markdown", which is an easy-to-write plain text format. This particular text format contains chunks of embedded R codes. 

Requirement for R Markdown files:

R Markdown files are designed to be used with the "rmarkdown" package. "rmarkdown" comes installed with RStudio, yet you can install an own copy of rmarkdown by clicking on _Tools> Install packages_ and search for "rmarkdown".  You can also install the above mentioned package with the following command:


```r
install.packages("rmarkdown")

```

R Markdown files can be transformed in two ways: 1. Knit the file and 2. Convert the file.

1. Knit - The rmarkdown package includes or calls the knitr package. knitr runs each chunk of R codes in the document and append the results of the codes to the document next to the code chunk. This workflow saves time and facilitates reproducible reports.

In R Markdown, every single report contains codes or a code it needs to make own graphs, tables, numbers, etc. The report can therefore be automatically updated by the author via the process of re-knitting.

2. Convert - The rmarkdown package will use the pandoc program to transform the R Markdown file into a new format. For example, .Rmd file can be converted into a PDF, HTML, or Microsoft Word file. 

## Getting started with R Markdown files

1. Open a new .Rmd file: _File> New File> R Markdown_ and choose a name for the file.
2. Write the document by editing the template.
3. Knit the document to create a report and preview the output in a PDF, HTML or another output.
4. Save the .Rmd file and (optional) publish the file to a web server (e.g. GitHub) by commiting and pushing it.

This is the general process of creating or opening an R Markdwon file. 

## Options for R Markdown files

The options of R Markdown files focus on the .rmd structure and render options with YAML, which will be explained in the following section. 

### .rmd structure

YAML Header = Optional section of render (e.g. pandoc)

Text = Narration formatted with markdown, mixed with "Code Chunks":

A code chunk always begins with ```{r} and ends with ``` e.g.

```{r} <- Starting point of the chunk.

``` <- Ending point of the chunk.

R Markdown will run the code and append the results to the document. It will use the location of the .Rmd file as the working directory.

### Render options with YAML

When you render, R Markdown: 

1. runs the R code, embeds results and text ino .md file with knitr
2. then converts the .md file into the finished format with pandoc 

Rmd -> knitr -> md -> pandoc -> Defined output value. 

The defined output value can be defined as one of the following options: 

html_document -> html
pdf_document -> pdf
word_document -> Microsoft Word
md_document -> Markdown 
etc.

As a next step, the output can also be customized with sub-options: 

Examples of sub-options:

toc = Add a table of contents at start of document 
highlight = Syntax highlighting "tango", "pygments", "kate" etc.
css = CSS file to use to style document

Please keep in mind that not every sub-option is applicable for all output values, which means that the "toc" for example is applicable for most of the outputs, yet not for all of them.

## What is a Chunk?

Generally: Code chunks in an R Markdown document contain your R code. All code chunks start and end with ``` – three backticks or graves. Important note: Graves are not the same as an apostrophe!

A code chunk looks like this:


```r
# code entered here
```

1. The first line: ```{r chunk-name-without-any-spaces} contains the language that you are using (r), and the name of the chunk. Note: It is mandatory to specify the language.

2. Next to the {r}, there is a chunk name. The chunk name is not necessarily required however, it is good practice to give your .Rmd file a strucutre by naming each chunk. But: This is completely up to you.

## Improtant options for all chunks

You can also add options to each code chunk. It is very convenient to set options for all the R chunks of the document, due to the fact that this saves time when writing these chunks. A natural place to set these options is in a first R chunk.



```r
knitr::opts_chunk$set(OPTION1 = TRUE/FALSE,
                      OPTION2 = TRUE/FALSE,
                      ...)
```


Important: These options are overridden by the particular chunk options.

````markdown
```{r, OPTION2=FALSE}
````

Options actually take R code. So, the following are examples that could be used to define the option.


```{r, eval=4>3, echo=format(Sys.Date(), '%Y-%B-%d') > '2019-March-10'
# eval is always TRUE
# echo = TRUE if current date is after March 10, 2019
```

The list of options can be found here [https://yihui.name/knitr/options/](https://yihui.name/knitr/options/). Below are some comments on some of these options (the least trivial for the author).

- `collapse` determines whether the source code and the output should be merged into a single block.
Here is the same chunk with different values of the option:

`collapse=TRUE`

(If TRUE, knitr will collapse all the source and output blocks created by the chunk into a single block.)


```r
2+ 2
#R> [1] 4
3* 5
#R> [1] 15
```

`collapse=FALSE`

(If FALSE, knitr will not collapse all the source and output blocks created by the chunk into a single block.)

    

```r
2+ 2
```

```
#R> [1] 4
```

```r
3* 5
```

```
#R> [1] 15
```

Worth noting: a `#` as a first character of the comment string (with `collpase=TRUE`) turns the output font into a comment-like text.

- `comment` is known as a character string. Knitr will append the string to the start of each line of results in the final document

`comment='##'`


```r
2+ 2
## [1] 4
```

`comment='R>'`
    

```r
2+ 2
R> [1] 4
```

- `echo` determines whether to display the code in the code chunk above it's results in the final document or not.

`echo=FALSE`

If FALSE, knitr will not display the code in the code chunk above it’s results in the final document.


```
#R>      speed           dist       
#R>  Min.   : 4.0   Min.   :  2.00  
#R>  1st Qu.:12.0   1st Qu.: 26.00  
#R>  Median :15.0   Median : 36.00  
#R>  Mean   :15.4   Mean   : 42.98  
#R>  3rd Qu.:19.0   3rd Qu.: 56.00  
#R>  Max.   :25.0   Max.   :120.00
```

`echo=TRUE`

If TRUE, knitr will display the code in the code chunk above it’s results in the final document.


```r
summary(cars)
#R>      speed           dist       
#R>  Min.   : 4.0   Min.   :  2.00  
#R>  1st Qu.:12.0   1st Qu.: 26.00  
#R>  Median :15.0   Median : 36.00  
#R>  Mean   :15.4   Mean   : 42.98  
#R>  3rd Qu.:19.0   3rd Qu.: 56.00  
#R>  Max.   :25.0   Max.   :120.00
```

- `child` allows a document to call and use another file as input in the document.

````markdown
```{r, child='PATH/TO/OTHER/file.Rmd'}
````

The path can be either absolute or relative.  
For relative paths, the following applies:  

  - `~/` starts a path a the root,
  - `../` indicates the parent directory,
  - `../../` for parent of the parent directory,
  - to move forward, start with the name of the included folder in the current directory.

## Latex code {#latex}

The overwhelming reason to introduce Latex code in a `.Rmd` file is for typesetting mathematical expressions.  
There are two main ways to type math in Latex:   

  - in the text, surrounded by special delimiters, `\( math \)` (alternatively, one can use the deprecated `$ math $`),
  - in an equation, surrounded by special delimiters, `\[ math equation \]`, or in a dedicated environment such as `\begin{equation} math equation \end{equation}` (also deprecated, `$$ math equation $$`).

Math format is usually distinct from the text format. For instance, compare a^2^ + b^2^ = c^2^ (simple markdown) to \(a^2 + b^2 = c^2\) (Latex). Notice, however, that most mathematical symbols are not supported by markdown. This why basic knowledge of Latex is essential for producing documents with math formula.   
The first part of that knowledge consists in the list of Latex symbols. These are typed into a document starting with a slash `\`. For instance, the Latex symbol \(\alpha\) is produced by the code `\alpha` while \(\sum\) is given by `\sum`.   
Superscripts and subscripts are produced with the characters `^` and `_`, respectively, and the content of the super- and subscripts enclosed within `{ }`. For instance, \(x_{2}^{3}\) is produced by the code `x_{2}^{3}` (or `x^{3}_{2}`) and \(\sum_{i=1}^{4}\) is given by `\sum_{i=1}^{4}`.  
A comprehensive list of symbols (some of them requiring special Latex packages) can be found in @latexlist. Shorter lists can be found online, including on [wiki](https://oeis.org/wiki/List_of_LaTeX_mathematical_symbols).  
A web-based application helps beginners by offering suggestions to a hand-drawn symbol, [detexify](http://detexify.kirelabs.org/classify.html).    
A second bulk in the knowledge of Latex is the understanding of special environments. But then, if a document requires lots of special Latex environments, then `.Rmd` files are not the most appropriate type of files to use.  
Some of these environments, however, have a perfect integration in `.Rmd` files, such as the most common, the equation. Here is an example, given by the code

```markdown
\[
\sum_{i=0}^{\infty} ak^{i} = \frac{a}{1-k} \text{, for }  
\lvert k \rvert < 1
\]
```
\[
\sum_{i=0}^{\infty} ak^{i} = \frac{a}{1-k} \text{, for }  
\lvert k \rvert < 1
\]

## Figures

Figures usually appear after the chunk that calls them, except on `.pdf` format because Latex makes them float and they may appear in the next page.  
Beyond the actual R calls that produces the figure, the figure's appearance will be tweaked by the options specified in the R chunk. The following options are worth noticing:  

  - `fig.width` and `fig.height` set in inches the graphical device size of the R plots.
  - `out.width` and `out.height` set the size of the R plots, including possibly rescaled images. Easier use with percentages as `out-width = "50%"` means that the figure stretches over 50% of the page's width.
  - `fig.align` takes the value `left`, `right` or `center` and is self-explained.
  - `fig.cap` sets the caption of the figure.
  - `fig.show` takes the default value `asis` to produce the command as it is read by R. Contrast this with the value `hold` which forces R to wait until the end of the chunk to produce the plots. It may be useful to hold if one wants to put multiple plots on the same line (side-by-side).

As an example, the figure below was created with the chunk options

Own Example for figure required

## Cross-references {#cr}

Cross-references are references to different elements somewhere in the content such as a specific chapter, figure, equation, etc.  
These work under a simple rule: the element to be referenced takes a **label**, e.g., 'foo', and this label is called from anywhere in the text with the command `\@ref(foo)`.  
Slightly different rules apply depending on which element is to be referenced. Below is a selected list.  
Notice that all labels in `bookdown` can only contain alphanumeric characters, or the special characters `:`, `-`, and `/`.

### Chapters, sections, ... {#cr-chapters}

Headers (chapters, sections, ...) have an ID that serves as a label. By default, it is formed by the words of the header in small letters separated by dashes (e.g., `my-great-chapter`). It is better practice, however, to assign a label to useful headers by appending to them the code `{#foo}` where `foo` is the chosen label for the header.
This subsection, for instance, has the header

```markdown
### Chapters, sections, ... {#cr-chapters}
```

The cross-reference is then achieved with `\@ref(foo)`.  
As an example, notice that this line belongs to Subsection \@ref(cr-chapters), included in Section \@ref(cr) of Chapter \@ref(rmd).  
These cross-references were obtained by the text/code: 

```markdown
As an example, notice that this line belongs to 
Subsection \@ref(cr-chapters), 
included in Section \@ref(cr) of Chapter \@ref(rmd).
```

For `.html` formats, one may use a direct link to the header by using the format for regular links but with  `#label` as the destination. For instance, since the label of this section is `cr`, the code `[Cross-references](#cr)` produces this link: [Cross-references](#cr).

### Figures

The label of a figure is given by the name of the chunk where it was created preceded by `fig:`.   
The chunk that created Figure \@ref(fig:plot-one) had the name `plot-one`. Therefore, the cross-reference is achieved through `\@ref(fig:plot-one)`.

### Tables

The label of a table is given by the name of the chunk where it was created preceded by `tab:`.   
If the chunk that created a Table had the name `table-one`, then cross-reference is achieved through `\@ref(tab:table-one)`.


### Equations

As explained in Section \@ref(latex), good rendering of equations requires coding in a Latex environment. For numbering of equations, various environments can be used, such as `equation`, `eqnarray`, etc.  
The label is then included in this environment within parentheses and by adding the prefix `\#eq:`, e.g., `\#eq:foo`.  
As for the cross-reference, one uses `\@ref(eq:foo)`.   
Below is a modified version of the equation in Section \@ref(latex) to include a number and a label.  
This is Equation \@ref(eq:series).

\begin{equation} 
\sum_{i=0}^{\infty} ak^{i} = \frac{a}{1-k} \text{, for }  
\lvert k \rvert < 1
  (\#eq:series)
\end{equation}


The previous lines were obtained with the code:

```markdown
This is Equation \@ref(eq:series).

\begin{equation} 
\sum_{i=0}^{\infty} ak^{i} = \frac{a}{1-k} \text{, for }  \lvert k \rvert < 1
  (\#eq:series)
\end{equation}
```

## Citations

It is of utmost importance to give credit to sources. This subsection illustrates a simple way to make citations in `bookdown`. For further details, including for changing references styles, see this [RStudio page](https://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html).   
The general idea is similar to the cross-references. The source has a label `foo` and the citation is made with `@foo`.  
There are numerous ways to tweak the format of the citation, but default format is often good enough.  
The citation procedure in `bookdown` is borrowed from the Latex constellation.  
Sources are listed in a separated bibliography file, `.bib`.  
For use in `bookdown`, this file must be given in the `YAML` (along with its path if it is not in the same folder) under the entry `bibliography`:

```yaml
---
title: "Great title"
output: pdf_document
bibliography: BIBLIOGRAPHY_FILE.bib
---
```

The `BIBLIOGRAPHY_FILE.bib` is a simple text file that has one entry for each source.  
The format of this entry depends on the type of source (article, book, blogpost, etc). Its construction, however, is quite similar and simply requires some fields (some compulsory, other optional) such as in the following example for a book.

```markdown
@book{wickham2014,
  title={Advanced {R}},
  author={Wickham, Hadley},
  year={2014},
  publisher={Chapman and Hall/CRC}
}
```

All the fields shown (`title`, `author`, `year` and `publisher`) are required for a book. Further fields such as `volume` or `edition` would be optional.  
Importantly, notice the very first element in the curly brackets: that is the label of the source, freely chosen by the author.  
The citation of this particular book would then be made thanks to the label, with the code `@wickham2014`.  
A few comments are the following:  

  - a reference inside square brackets with or without a prefix and a suffix puts the citation inside parentheses: `[see the reference (prefix) @wickham2014 for further details (suffix)]` produces [see the reference (prefix) @wickham2014 for further details (suffix)],
  - without square brackets, no parentheses in the output,
  - multiple references are separated by a semi-column `;`: `[@wickham2014; @xie2015]`produces [@wickham2014; @xie2015],
  - a minus sign `-` in front of the `@` suppresses the name of the author in the text:  `-@wickham2014` produces -@wickham2014,
  - the references are **automatically** put at the end of the book; the last level-one header should therefore be 'Bibliography' or 'References'.

### Writing `.bib` entries

One advantage of using `.bib` files is that the fields for each entry, i.e., all the information about the source, are usually available online in the easiest of forms.  
The site Google Scholar, for instance, provides these entries in `.bib` form.  
As an example, search there the book mentioned above, e.g., "wickham advanced r".  Under each hit, there is an icon of inverted commas. By clicking it, the reference is given in different formats but also with a link to the BibTeX code (along with others). One can then simply copy this BibTex code and paste it anywhere in the bibliography file. For easier use, the label could be changed.

<!--chapter:end:06-rmd_files.Rmd-->

# Import data to R {#import}

Analyzing data with R is an important part of data science. Therefore, it is vital to understand the procedure of how to import data into R. Generally speaking, the process of importing data into R is very simple. Data out there exists in many formats and there are number of ways in importing data into R. Speakin the language of R, we will need to `read` the data and put or convert it into an object, wich often is a data frame. 

Base R has has base functions to read some types of files. For special types of files, special packages are needed.

**Important note:** these base functions are introduced here for documentation purpose only. 

## Reading rectangular data

Rectangular data is intended here as a data set with values of variables in columns and each row representing a case. Arguably, this is the simplest and probably most common way to store data sets.  
The ad hoc function in R is `read.table`. Other similar functions exist, e.g., `read.csv`, but they are essentially a wrapper of `read.table`.   
This function reads rectangular data and assigns it to an object, in almost all cases a data frame. The arguments of the function are numerous are, depending on the case, potentially very useful (check `?read.table`).  We mention here a few of them in the typical call:

```{r
my.data <- read.table(`file`)
``` 

`file` is the name of the file to be read. It requires a valid path. It can also be an `url`, with some adaptations.  
`header` is a logical indicating whether the data's first line gives the names of the variables.  
`sep` indicates the character that separates the values between columns.


```r
# assuming we have the file AH001.txt in the same folder
df <- read.table(file="AH001.txt",
				header=TRUE,
				sep=",")
head(df)
#R>   Area AreaCode AreaCode2 Grain Year Month LPrice HPrice
#R> 1   AH        1        NA    BO 1738     9     98    120
#R> 2   AH        1        NA    BO 1738    10     99    120
#R> 3   AH        1        NA    BO 1738    11    100    120
#R> 4   AH        1        NA    BO 1738    12     93    120
#R> 5   AH        1        NA    BO 1739     1     90    120
#R> 6   AH        1        NA    BO 1739     2     98    120
```

## Read other data types

R can import virtually all types of data. For special types, a ad hoc package will be necessary. `foreign` is one of them and it allows to import data from other applications. Its functions are of the form

```r
read.XXX
```
 where the `XXX` is an extension specific to the external software. Examples include "read.dta" for Stata data files, `read.spss` for SPSS files or `read.dbf` for dBASE files.   

A very important data source type is Excel. Functions for this type of data are covered in Chapter \@ref(readr) from the part on `tidyverse`.

Very often, the data source is in an Excel format, and needs to be imported into R prior to using it. Therefore, we can make use the function read.xls from the gdata package (Install the package: _Tools> Install packages_). It reads the data from an Excel spreadsheet and returns a data frame. 

The following example is an example of how to load an Excel spreadsheet named "datascienceproject.xls" into R (This method requires Perl runtime to be present in the system):

```{r
library(gdata)    # loading the above mentioned gdata package 
help(read.xls)    # documentation (help regarding read.xls) 
mydata = read.xls("datascienceproject.xls")  
                  # read from the excel spreadsheet
```

An alternative solution would be to make use of the function loadWorkbook from the XLConnect package to read the entire workbook, and then load the worksheets with readWorksheet (The XLConnect package requires the software Java to be pre-installed).

```{r
library(XLConnect)    # loading the above mentioned XLConnect package 
dsp1 = loadWorkbook("datascienceproject.xls") 
dsp2 = readWorksheet(dsp1, sheet="Sheet1")
                      # Example of reading sheet 1 of the entire worksheet.
```

SPSS File
For data files in the format of SPSS, it can be opened with the function read.spss, which is also part of the foreign package. There read.spss function also includes a "to.data.frame" option, in order to choose whether a data frame is to be returned. By default, it returns a list of components instead.

```{r
library(foreign)    # loading the above mentioned foreign package 
help(read.spss)     # documentation (help regarding read.spss) 
mydata = read.spss("datascienceproject", to.data.frame=TRUE)
```

CSV File

The sample data can also be in comma separated values (CSV) format. Each cell inside such data file is separated by a special character, which usually is a comma, although other characters can be used as well.

The first row of the data file should contain the column names instead of the actual data. Here is a sample of the expected format.

```{r
Col1,Col2,Col3 
100,a1,b1 
200,a2,b2 
300,a3,b3
```

After we copy and paste the data above in a file named "datascienceproject.csv" with a text editor, we can read the data with the function read.csv.

```{r
datascienceproject = read.csv("datascienceproject.csv")  # read the csv file 
mydata 
  Col1 Col2 Col3 
1  100   a1   b1 
2  200   a2   b2 
3  300   a3   b3

help(read.csv)    # If help is required for the read.csv function
```

Working Directory

Finally, the code samples above assume the data files are located in the R working directory, which can be found with the function getwd.

```{r
getwd()   # get current working directory
```

You can select a different working directory with the function setwd(), and thus avoid entering the full path of the data files.

```{r
setwd("<new path>")   # set working directory
```

Note that the forward slash should be used as the path separator even on Windows platform.

```{r
setwd("C:/MyDoc")
```

## Scanning a file

The base function `scan` can sometimes be useful, though it is not used to import data. `scan()` imports to a vector (or a list), which can then be used.   

- `what` gives the type of vector to be imported.  
- `skip` is the number of lines to be skipped in the file.  
- `nlines` determines the number of lines to be read and imported.


```r
df <- scan("AH001.txt", 
           what=character())
#df
df <- scan("AH001.txt", 
           what=character(), 
           skip=1, 
           sep=",")
#df
given.line <- scan("AH001.txt", 
              what=character(), 
              nlines=1, 
              sep=",")
given.line
#R> [1] "Area"      "AreaCode"  "AreaCode2" "Grain"     "Year"      "Month"    
#R> [7] "LPrice"    "HPrice"
```

<!--chapter:end:07-import.Rmd-->

# Customize output {#custom-ouptut}

This chapter is about choosing and/or modifying the way the output file looks like.
If you do not select a format, R Markdown renders the file to its default format, which you can set in the output field of a .Rmd file’s header.

The RStudio knit button renders a file to the first format listed in its output field. You can render to additional formats by clicking the dropdown menu beside the knit button.

Set the output_format argument of render to render your .Rmd file into any of R Markdown’s supported formats. For example, the chunk below renders this .Rmd file to a HTML document.

```
library(rmarkdown)
render("customize_output.Rmd", output_format = "html_document")
```


## Multiple built-in output types

However, there are a variety of output possibilities and formats that can be individually adapted to the user. In general, different formats offer advantages and disadvantages when compared with each other.

The following output formats are available to use with R Markdown:
"html_notebook"" - Interactive R Notebooks
"html_document" - HTML document w/ Bootstrap CSS
"pdf_document" - PDF document (via LaTeX template)
"word_document" - Microsoft Word document (docx)
"odt_document" - OpenDocument Text document
"rtf_document" - Rich Text Format document
"md_document" - Markdown document (various flavors)

Each output format is implemented as a function in R. You can customize the output by passing arguments to the function as sub-values of the output field. To learn which arguments a format takes, read the format’s help page in R, e.g. ?pdf_document.

If a certain option has sub-options (which means the value of this option is a list in R), the sub-options need to be further indented, e.g.:

output:
  html_document:
    toc: true
    includes:
      in_header: header.html
      before_body: before.html
      

Furthermore, there are several additional output formats that are suitable for special situations, such as slide presentations, dashboards, websites and interactive documents.

A helpful overview of formats and other useful information can be found in the official cheatsheet, available in RStudio at:
Go to File > Help > Cheatsheets > R Markdown Cheat Sheet to open the main R Markdown cheatsheet, pictured above

Additionally, general information about the structure of a rmd in RStudio can be accessed via the Quick Reference:
Go to File > Help > Markdown Quick Reference to open the Markdown Quick Reference in your help pane.


## New types provided by packages

Packages are bundles of code which extend the functionality of RStudio and R.

Anyone can make an R package, and anyone can install anyone else’s R package (if they make it available). This is part of the open source world, and using different R packages is essential to modern R workflows.

You can get packages from many different places, but the most common one: CRAN. CRAN is the Comprehensive R Archive Network, a global network of servers which make available for download a set of vetted R packages.

Most packages need to be loaded into the current environment to be accessible. RMarkdown is specially integrated in RStudio in a way that avoids this, but in general you should load packages with the library command:

```
library(name_of_the_package)

```

## CSS: custom html

Shiny apps use an HTML interface, which means that you can change the visual appearance of your apps quickly and simply with CSS files.
You can use CSS to customize the typefaces used in dygraph labels. In example CSS is used to make the main label bold and to reduce the size of the typefaces used on the axes:

```
.dygraph-title {
  color: navy;
  font-weight: bold;
}
.dygraph-axis-label {
  font-size: 11px;
}

dygraph(nhtemp, main = "New Haven Temperatures") %>%
  dyCSS("dygraph.css")
``  


## Latex preamble

This file is added to the preamble of the Latex file to modify how the `.pdf` output is compiled.   
Literally, these commands are placed in the Latex file before the self-explaining command: 
```latex
\begin{document}
```  
The most common commands call the packages to be used in the compilation of the Latex file, e.g.,
```latex
\usepackage{multirow}
```
Each package, in turn, includes a set of functions that can be used in the file to produce some particular output.  
The other set of commands are typically definitions of new commands or environments as well as redefinitions of existing commands to produced a special output.  

```latex
\usepackage{totcount}
\regtotcounter{section}
\makeatletter
    \renewcommand{\thesection}
    {\number\numexpr\c@section@totc-\c@section+1\relax}
\makeatother
```

<!--chapter:end:08-customize_output.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# Data stuctures {#datastructures}

This chapter lists the most common objects to store data. To make the best of the R language, you need a strong understanding of the basic data types and data structures and how to operate on those.

It is very important to understand because these are the objects to manipulate on a day-to-day basis in R. Dealing with object conversions is one of the most common sources of frustration for beginners.

To understand computations in R, two slogans are helpful:

Everything that exists is an object.
Everything that happens is a function call.


## Atomic vectors
The basic data structure in R is the vector. Vectors have three characteristics:

  - a type, `typeof()`,
  - a length, `length()`,
  - some attributes, `attributes()`. 
  
To illustrate:

typeof()  # what is it?
length()  # how long is it? What about two dimensional objects?
attributes()  # does it have any metadata?

e.g.:


```r
x <- "dataset"
typeof(x)
#R> [1] "character"
attributes(x)
#R> NULL

y <- 1:10
typeof(y)
#R> [1] "integer"
length(y)
#R> [1] 10
attributes(y)
#R> NULL

z <- c(1L, 2L, 3L)
typeof(z)
#R> [1] "integer"
```

### Types of data 

There are five common types of atomic vectors:

  - logical,
  - complex
  - integer,
  - double (often called numeric- real or decimal),
  - character.

Note that if vector elements not all of the same type, R makes coercion.  In that case, the order becomes:
"logical < numeric < character".

Here are a few illustrations.



```r
# logical vector
log_vector <- c(TRUE, FALSE, FALSE)
log_vector
#R> [1]  TRUE FALSE FALSE

# numeric vector
num_vector <- c(12, 10, 3)
typeof(num_vector)
#R> [1] "double"

# integer vector
int_vector <- c(12L, 10L, 3L)
typeof(int_vector)
#R> [1] "integer"


# character vector
chr_vector <- c("a", "b", "c")
typeof(chr_vector)
#R> [1] "character"

# mixed types vector
mix_vector <- c(2, "a")
is.numeric(mix_vector)
#R> [1] FALSE
typeof(mix_vector)
#R> [1] "character"
```

Numeric vectors can be created with the shortcut `:`, which is used to imply all the integers from the number on the left of `:` to the number on its right. Even if it is not good practice, these do not require the `c()` call. 


```r
vector_A <- 1:5
vector_A
#R> [1] 1 2 3 4 5
length(vector_A)
#R> [1] 5
```

### Factor vector

This is a special type of vector. It has a limited number of values, called levels. These levels can be unordered (e.g., gender is either "Female" or "Male") or ordered (e.g. school level is "Primary", "Secondary", "Tertiary")

```r
gender <- factor(c("Male", "Male", "Female", 
                   "Male", "Female", "Female", "Male"))
gender
#R> [1] Male   Male   Female Male   Female Female Male  
#R> Levels: Female Male
levels(gender)
#R> [1] "Female" "Male"
summary(gender)
#R> Female   Male 
#R>      3      4
school <- factor(c("Primary", "Secondary", "Tertiary"),
					ordered=TRUE)
school
#R> [1] Primary   Secondary Tertiary 
#R> Levels: Primary < Secondary < Tertiary

school2 <- factor(c("Primary", "Secondary","Secondary", "Tertiary"),
					labels=c( "Secondary", "Tertiary","Primary"),
					ordered=TRUE)
school2
#R> [1] Secondary Tertiary  Tertiary  Primary  
#R> Levels: Secondary < Tertiary < Primary
```

## Matrices and arrays

Matrices are a special vector in R. They are not a separate type of object but simply an atomic vector with dimensions added on to it. Matrices have rows and columns. However R is not often used for matrices calculations: it is too slow for that and there are better programs for it out there (e.g. Matlab).


```r
# populate a matrix with the elements in of the vector,
# and give the dimensions

M <- matrix(c(4, 1, 0, 3, 6, 8), nrow=3, ncol=2) 
M
#R>      [,1] [,2]
#R> [1,]    4    3
#R> [2,]    1    6
#R> [3,]    0    8
```

If we think of a matrix as a 2 dimensions vector, then arrays are $n$ dimensions vectors. Is it important? It might be in some very specific cases.


```r
mya <- array(data=1:18, dim=c(2,3,3))
mya
#R> , , 1
#R> 
#R>      [,1] [,2] [,3]
#R> [1,]    1    3    5
#R> [2,]    2    4    6
#R> 
#R> , , 2
#R> 
#R>      [,1] [,2] [,3]
#R> [1,]    7    9   11
#R> [2,]    8   10   12
#R> 
#R> , , 3
#R> 
#R>      [,1] [,2] [,3]
#R> [1,]   13   15   17
#R> [2,]   14   16   18
```

## Lists
These are the one-size fit all structure... A list is an object composed of any other object, even... another list! Very useful data structure!


```r
school<-factor(c("Primary", "Secondary", "Tertiary"), ordered=TRUE)
mylist <- list(numbers=c(1:60),
				somenames=c("Jim","Jules"),
				results= c(T,F,F,T),
				school=school)
mylist
#R> $numbers
#R>  [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23
#R> [24] 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46
#R> [47] 47 48 49 50 51 52 53 54 55 56 57 58 59 60
#R> 
#R> $somenames
#R> [1] "Jim"   "Jules"
#R> 
#R> $results
#R> [1]  TRUE FALSE FALSE  TRUE
#R> 
#R> $school
#R> [1] Primary   Secondary Tertiary 
#R> Levels: Primary < Secondary < Tertiary

# change the names of the elements of the list
names(mylist) <- c("N", "O","R","S")
```

## Data frames

Data frames are the second most important data structure in R. We can think of it as a better version of a data set in Excel. It stacks together observations over many variables, each of these variables being a vector. A data frame is a special type of list where every element of the list has same length.

Data frames can have additional attributes such as rownames(), which can be useful for annotating data, like subject_id or sample_id. But most of the time they are not used.

Some additional information on data frames:

Usually created by read.csv() and read.table().
Can convert to matrix with data.matrix()
Coercion will be forced and not always what you expect.
Can also create with data.frame() function.
Find the number of rows and columns with nrow(df) and ncol(df), respectively.
Rownames are usually 1..n.

e.g.:


```r
# mtcars is a built-in data set
data(mtcars)
class(mtcars)
#R> [1] "data.frame"
mtcars
#R>                      mpg cyl  disp  hp drat    wt  qsec vs am gear carb
#R> Mazda RX4           21.0   6 160.0 110 3.90 2.620 16.46  0  1    4    4
#R> Mazda RX4 Wag       21.0   6 160.0 110 3.90 2.875 17.02  0  1    4    4
#R> Datsun 710          22.8   4 108.0  93 3.85 2.320 18.61  1  1    4    1
#R> Hornet 4 Drive      21.4   6 258.0 110 3.08 3.215 19.44  1  0    3    1
#R> Hornet Sportabout   18.7   8 360.0 175 3.15 3.440 17.02  0  0    3    2
#R> Valiant             18.1   6 225.0 105 2.76 3.460 20.22  1  0    3    1
#R> Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
#R> Merc 240D           24.4   4 146.7  62 3.69 3.190 20.00  1  0    4    2
#R> Merc 230            22.8   4 140.8  95 3.92 3.150 22.90  1  0    4    2
#R> Merc 280            19.2   6 167.6 123 3.92 3.440 18.30  1  0    4    4
#R> Merc 280C           17.8   6 167.6 123 3.92 3.440 18.90  1  0    4    4
#R> Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
#R> Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
#R> Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
#R> Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
#R> Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
#R> Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
#R> Fiat 128            32.4   4  78.7  66 4.08 2.200 19.47  1  1    4    1
#R> Honda Civic         30.4   4  75.7  52 4.93 1.615 18.52  1  1    4    2
#R> Toyota Corolla      33.9   4  71.1  65 4.22 1.835 19.90  1  1    4    1
#R> Toyota Corona       21.5   4 120.1  97 3.70 2.465 20.01  1  0    3    1
#R> Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
#R> AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
#R> Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
#R> Pontiac Firebird    19.2   8 400.0 175 3.08 3.845 17.05  0  0    3    2
#R> Fiat X1-9           27.3   4  79.0  66 4.08 1.935 18.90  1  1    4    1
#R> Porsche 914-2       26.0   4 120.3  91 4.43 2.140 16.70  0  1    5    2
#R> Lotus Europa        30.4   4  95.1 113 3.77 1.513 16.90  1  1    5    2
#R> Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
#R> Ferrari Dino        19.7   6 145.0 175 3.62 2.770 15.50  0  1    5    6
#R> Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8
#R> Volvo 142E          21.4   4 121.0 109 4.11 2.780 18.60  1  1    4    2
head(mtcars)
#R>                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
#R> Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
#R> Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
#R> Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
#R> Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
#R> Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
#R> Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
str(mtcars)
#R> 'data.frame':	32 obs. of  11 variables:
#R>  $ mpg : num  21 21 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2 ...
#R>  $ cyl : num  6 6 4 6 8 6 8 4 4 6 ...
#R>  $ disp: num  160 160 108 258 360 ...
#R>  $ hp  : num  110 110 93 110 175 105 245 62 95 123 ...
#R>  $ drat: num  3.9 3.9 3.85 3.08 3.15 2.76 3.21 3.69 3.92 3.92 ...
#R>  $ wt  : num  2.62 2.88 2.32 3.21 3.44 ...
#R>  $ qsec: num  16.5 17 18.6 19.4 17 ...
#R>  $ vs  : num  0 0 1 1 0 1 0 1 1 1 ...
#R>  $ am  : num  1 1 1 0 0 0 0 0 0 0 ...
#R>  $ gear: num  4 4 4 3 3 3 3 4 4 4 ...
#R>  $ carb: num  4 4 1 1 2 1 4 2 2 4 ...

# names of the variables in the data frame
names(mtcars) 
#R>  [1] "mpg"  "cyl"  "disp" "hp"   "drat" "wt"   "qsec" "vs"   "am"   "gear"
#R> [11] "carb"
length(mtcars)
#R> [1] 11
nrow(mtcars)
#R> [1] 32
```

### Data frame creation

A data frame can be created manually by providing the function `data.frame` with the corresponding vectors or with the use of one method above. The vectors should be of same length, otherwise R recycles values. The data frame requires a name for each vector.



```r
df <- data.frame(let=LETTERS[1:7],
                 num1=10:16, 
                 num2=floor(rnorm(7,100,10)))
df
#R>   let num1 num2
#R> 1   A   10  105
#R> 2   B   11  102
#R> 3   C   12   95
#R> 4   D   13   97
#R> 5   E   14   97
#R> 6   F   15  105
#R> 7   G   16   92
names(df)
#R> [1] "let"  "num1" "num2"
```


```r
students <- data.frame(name= c("tr", "ga", "mi", "st", 
                               "eb", "ha", "fo", "fi"),
                       age=c(23, 23, 24, 33, 
                             28, 24, 33, 41),
                       like= c(T, T, T, T, 
                               F, F, T, T)) 
students
#R>   name age  like
#R> 1   tr  23  TRUE
#R> 2   ga  23  TRUE
#R> 3   mi  24  TRUE
#R> 4   st  33  TRUE
#R> 5   eb  28 FALSE
#R> 6   ha  24 FALSE
#R> 7   fo  33  TRUE
#R> 8   fi  41  TRUE
```

Useful functions:

head() - see first 6 rows
tail() - see last 6 rows
dim() - see dimensions
nrow() - number of rows
ncol() - number of columns
str() - structure of each column
names() - will list the names attribute for a data frame (or any object really), which gives the column names.

### Data frame combination

Example for data set combination:


```r
df <- data.frame(id = letters[1:10], x = 1:10, y = rnorm(10))
df
#R>    id  x          y
#R> 1   a  1  0.2019669
#R> 2   b  2 -0.5368354
#R> 3   c  3 -0.7158510
#R> 4   d  4 -1.1126736
#R> 5   e  5  0.8499099
#R> 6   f  6  1.1225251
#R> 7   g  7 -0.8275152
#R> 8   h  8 -0.5911885
#R> 9   i  9  0.9448212
#R> 10  j 10 -2.4752355
```
     id x       y


```r
cbind(df, data.frame(z = 4))
#R>    id  x          y z
#R> 1   a  1  0.2019669 4
#R> 2   b  2 -0.5368354 4
#R> 3   c  3 -0.7158510 4
#R> 4   d  4 -1.1126736 4
#R> 5   e  5  0.8499099 4
#R> 6   f  6  1.1225251 4
#R> 7   g  7 -0.8275152 4
#R> 8   h  8 -0.5911885 4
#R> 9   i  9  0.9448212 4
#R> 10  j 10 -2.4752355 4
```

## A word about attributes

Attributes are important characteristics of vectors (and other data structures).   
They can be seen as some meta data that defines the nature of the object. This is to say that a given attribute can determine how a function applies to an object. Here are three important attributes:

  - the names, `names()`,
  - the dimensions, `dim()`,
  - the class, `class`.

To illustrate the use of attributes, recall the case of a factor vector. The fact that the vector on which it builds is given the attribute of a class (factor) turns that vector into a special one.


```r
vec <- c(1.7, 1.3, 4, 3.3, 3.3, 2, 2.3, 2.3)
vec
#R> [1] 1.7 1.3 4.0 3.3 3.3 2.0 2.3 2.3
table(vec)
#R> vec
#R> 1.3 1.7   2 2.3 3.3   4 
#R>   1   1   1   2   2   1

vec.f <- factor(vec,
                levels=c(1, 1.3, 1.7, 2, 2.3, 2.7, 3, 3.3, 3.7, 4, 5),
                ordered=TRUE)
vec.f
#R> [1] 1.7 1.3 4   3.3 3.3 2   2.3 2.3
#R> Levels: 1 < 1.3 < 1.7 < 2 < 2.3 < 2.7 < 3 < 3.3 < 3.7 < 4 < 5
table(vec.f)
#R> vec.f
#R>   1 1.3 1.7   2 2.3 2.7   3 3.3 3.7   4   5 
#R>   0   1   1   1   2   0   0   2   0   1   0
```


## Environments

An environment is similar to a bag/list of names. It can be seen as the space were these names "live".   
Environments can include environments. In that case, the enclosing environment is called the parent environment.  
The most common environment is the `globalenv()` also called the `workspace`. 

<!--chapter:end:09-data_structures.Rmd-->

# R as a calculator {#rcalc}

R can also be used as a simple calculator. For instance, 25+12=37.

Here are a few more examples of how R can be used as a calculator with different commands:

## Usual operators

### Simple operations

The usual symbols `+, -, *, /` apply .

```r
2 + 6
#R> [1] 8
56/ 6
#R> [1] 9.333333
```

## Order of operations

The order of arithmetic operations is determined by the PEMDAS (Parenthesis, exponents, multiplication, division, addition, subtraction) convention, which implies that parentheses get highest priority, followed by exponentiation, followed by multiplication and division, followed by addition and subtraction. The second example of using R in the calculator mode is listed below:

```{r
4 + 9 * 6 # PEMDAS (Multiplication before addition)
```
[1] 58

For R operations, it is not necessary to use an equal sign is. The return key serves that role and gives you the result of the operation As you can see above, the response from R is [1] 58, which shows you that R made use of the PEMDAS convention (Multiplication before addition). The [1] that appears before the 38 indicates that the result is a vector of length one. More details on vectors will be given in the final chapter of the book.

Operation without making use of spaces: 
```{r
> 5+9*6 # no spaces
[1] 58
```

This still works, yet you could imagine how difficult this would be to read if it was 40 or 50 characters long.

## Number of digits displayed

The default number of digits displayed in R is seven digits. Yet, R must make the decision on how many digits to display. Therefore, the number of digits shown can be altered, as shown below (Important: R does not include commas to separate groups of three digits when displaying the result): 

```{r
10 * 10 ˆ 3 # exponentiation first
```
[1] 10000

Now consider a calculation of larger numbers.

```{r
55555555 * 55555555 # result in scientific notation
[1] 3.08642e+15
```

The result of this calculation is expressed in scientific notation: 3.08642 · 1015. With only seven digits displayed, it is not possible to know the exact value of the product.

By default, R displays seven digits, but more digits are stored. As an illustration, the built-in constant π is designated with pi.

```{r
pi # built in constant
```
[1] 3.141593

### Parentheses 

Parentheses are or can be used to alter the order of operations. But they are also a common source of error when they are not matched.


```r
(4+3)*((7-3)/(1+.05))
#R> [1] 26.66667
```
The next expression will generate an error and prevent the compilation of the whole book.
```r
(4+3)*((7-3/(1+.05))
```

Other examples of different orders through adding parantheses:

```{r
5 + (6 / 7) ˆ 2 # division first, then exponentiation, then addition
```
[1] 5.73

```{r
(2 + 1) / 5 ˆ 2 # addition first, then exponentiation, then division
```
[1] 0.12

```{r
(9 + 3 / 4) ˆ 2 # division first, then addition, then exponentiation
```
[1] 95.06

```{r
((4 + 7) / 10) ˆ 2 # addition first, then division, then exponentiation
```
[1] 1.21

### Exponents 

There are two ways of expressing the power of a number: `^` and `**`.


```r
3^4
#R> [1] 81
3**4
#R> [1] 81
```

## Unusual operators

### Special operations

The symbols `%/%` and `%%` return the entire part of the result of the division and the rest of the division, respectively.

```r
56/6
#R> [1] 9.333333
56%/%6
#R> [1] 9
56%%6
#R> [1] 2
```

## Usual functions

The common functions found in any calculator also have an equivalent on R. The following examples need no further comment.


```r
log(100)
#R> [1] 4.60517
sqrt(100)
#R> [1] 10
```

## Unusual functions

There are several other functions applied to numbers that one does not usually find in a calculator.  
A few examples below:


```r
# floor / ceiling for the closest integer
floor(13.47)
#R> [1] 13
ceiling(13.47)
#R> [1] 14
```









<!--chapter:end:10-calculator.Rmd-->

# (PART) Tidyverse Packages {-}

# What is `tidyverse`? {#tidyverse}

As already mentioned in the preface of the book, many of the functions available in R come in packages. The tidyverse is a collection or bundle of open source R packages introduced by Hadley Wickham (Statistician from New Zealand who is currently Chief Scientist at RStudio) and his team. The fundamental packages of `tidyverse` are dplyr, tidyr, readr, tibble, stringr, ggplot2 and many other packages that provide the functionality to model, transform and visualize data. In general, the packages provided with `tidyverse` make R even better, faster, simpler and just more beautiful. The huge benefits of embracing the `tidyverse` come at the cost needing to learn a sub-dialect of R. This can be daunting for a beginner in R programming that put lots of effort into learning basic R functions. In general, tidyverse packages are intended to make the various processes of statistics and data science more productive through a variety of workflows. It is also the case that the tidyverse is work in progress. 

The next chapters all develop a relevant package, selected from the `tidyverse`. The list of all packages along with a fuller description of the system can be found on [tidyverse.org](https://www.tidyverse.org/).

Let's begin with the installation process of `tidyverse`:

```r
install.packages("tidyverse")
```

<!--chapter:end:11-tidyverse.Rmd-->

# `tibble` {#tibble}

A tibble is the equivalent of a data frame in the `tidyverse`. The specific package of the bundle is called `tibble`.  
All the packages in the `tidyverse` work with tibbles.   
Notice that all the functions applicable to a data frame will also work on a tibble. This is because **all tibbles are data frames** (while the reverse is not true, all data frames are not necessarily tibbles).  
So why bother?  
The reasons to choose tibbles include: 

- faster calculations,
- better printing of the content,
- more information about the content,
- more useful warnings of errors,
- simpler and more limited functionalities.

To install the CRAN version:

```{r
install.packages("tibble")
```

## Creating a tibble

There are various ways to create a tibble.

### `as_tibble`

The simplest way is declare a data frame a tibble with the function `as_tibble`. 


```r
require(tidyverse)
data(iris)
# print the data frame
iris
#R>     Sepal.Length Sepal.Width Petal.Length Petal.Width    Species
#R> 1            5.1         3.5          1.4         0.2     setosa
#R> 2            4.9         3.0          1.4         0.2     setosa
#R> 3            4.7         3.2          1.3         0.2     setosa
#R> 4            4.6         3.1          1.5         0.2     setosa
#R> 5            5.0         3.6          1.4         0.2     setosa
#R> 6            5.4         3.9          1.7         0.4     setosa
#R> 7            4.6         3.4          1.4         0.3     setosa
#R> 8            5.0         3.4          1.5         0.2     setosa
#R> 9            4.4         2.9          1.4         0.2     setosa
#R> 10           4.9         3.1          1.5         0.1     setosa
#R> 11           5.4         3.7          1.5         0.2     setosa
#R> 12           4.8         3.4          1.6         0.2     setosa
#R> 13           4.8         3.0          1.4         0.1     setosa
#R> 14           4.3         3.0          1.1         0.1     setosa
#R> 15           5.8         4.0          1.2         0.2     setosa
#R> 16           5.7         4.4          1.5         0.4     setosa
#R> 17           5.4         3.9          1.3         0.4     setosa
#R> 18           5.1         3.5          1.4         0.3     setosa
#R> 19           5.7         3.8          1.7         0.3     setosa
#R> 20           5.1         3.8          1.5         0.3     setosa
#R> 21           5.4         3.4          1.7         0.2     setosa
#R> 22           5.1         3.7          1.5         0.4     setosa
#R> 23           4.6         3.6          1.0         0.2     setosa
#R> 24           5.1         3.3          1.7         0.5     setosa
#R> 25           4.8         3.4          1.9         0.2     setosa
#R> 26           5.0         3.0          1.6         0.2     setosa
#R> 27           5.0         3.4          1.6         0.4     setosa
#R> 28           5.2         3.5          1.5         0.2     setosa
#R> 29           5.2         3.4          1.4         0.2     setosa
#R> 30           4.7         3.2          1.6         0.2     setosa
#R> 31           4.8         3.1          1.6         0.2     setosa
#R> 32           5.4         3.4          1.5         0.4     setosa
#R> 33           5.2         4.1          1.5         0.1     setosa
#R> 34           5.5         4.2          1.4         0.2     setosa
#R> 35           4.9         3.1          1.5         0.2     setosa
#R> 36           5.0         3.2          1.2         0.2     setosa
#R> 37           5.5         3.5          1.3         0.2     setosa
#R> 38           4.9         3.6          1.4         0.1     setosa
#R> 39           4.4         3.0          1.3         0.2     setosa
#R> 40           5.1         3.4          1.5         0.2     setosa
#R> 41           5.0         3.5          1.3         0.3     setosa
#R> 42           4.5         2.3          1.3         0.3     setosa
#R> 43           4.4         3.2          1.3         0.2     setosa
#R> 44           5.0         3.5          1.6         0.6     setosa
#R> 45           5.1         3.8          1.9         0.4     setosa
#R> 46           4.8         3.0          1.4         0.3     setosa
#R> 47           5.1         3.8          1.6         0.2     setosa
#R> 48           4.6         3.2          1.4         0.2     setosa
#R> 49           5.3         3.7          1.5         0.2     setosa
#R> 50           5.0         3.3          1.4         0.2     setosa
#R> 51           7.0         3.2          4.7         1.4 versicolor
#R> 52           6.4         3.2          4.5         1.5 versicolor
#R> 53           6.9         3.1          4.9         1.5 versicolor
#R> 54           5.5         2.3          4.0         1.3 versicolor
#R> 55           6.5         2.8          4.6         1.5 versicolor
#R> 56           5.7         2.8          4.5         1.3 versicolor
#R> 57           6.3         3.3          4.7         1.6 versicolor
#R> 58           4.9         2.4          3.3         1.0 versicolor
#R> 59           6.6         2.9          4.6         1.3 versicolor
#R> 60           5.2         2.7          3.9         1.4 versicolor
#R> 61           5.0         2.0          3.5         1.0 versicolor
#R> 62           5.9         3.0          4.2         1.5 versicolor
#R> 63           6.0         2.2          4.0         1.0 versicolor
#R> 64           6.1         2.9          4.7         1.4 versicolor
#R> 65           5.6         2.9          3.6         1.3 versicolor
#R> 66           6.7         3.1          4.4         1.4 versicolor
#R> 67           5.6         3.0          4.5         1.5 versicolor
#R> 68           5.8         2.7          4.1         1.0 versicolor
#R> 69           6.2         2.2          4.5         1.5 versicolor
#R> 70           5.6         2.5          3.9         1.1 versicolor
#R> 71           5.9         3.2          4.8         1.8 versicolor
#R> 72           6.1         2.8          4.0         1.3 versicolor
#R> 73           6.3         2.5          4.9         1.5 versicolor
#R> 74           6.1         2.8          4.7         1.2 versicolor
#R> 75           6.4         2.9          4.3         1.3 versicolor
#R> 76           6.6         3.0          4.4         1.4 versicolor
#R> 77           6.8         2.8          4.8         1.4 versicolor
#R> 78           6.7         3.0          5.0         1.7 versicolor
#R> 79           6.0         2.9          4.5         1.5 versicolor
#R> 80           5.7         2.6          3.5         1.0 versicolor
#R> 81           5.5         2.4          3.8         1.1 versicolor
#R> 82           5.5         2.4          3.7         1.0 versicolor
#R> 83           5.8         2.7          3.9         1.2 versicolor
#R> 84           6.0         2.7          5.1         1.6 versicolor
#R> 85           5.4         3.0          4.5         1.5 versicolor
#R> 86           6.0         3.4          4.5         1.6 versicolor
#R> 87           6.7         3.1          4.7         1.5 versicolor
#R> 88           6.3         2.3          4.4         1.3 versicolor
#R> 89           5.6         3.0          4.1         1.3 versicolor
#R> 90           5.5         2.5          4.0         1.3 versicolor
#R> 91           5.5         2.6          4.4         1.2 versicolor
#R> 92           6.1         3.0          4.6         1.4 versicolor
#R> 93           5.8         2.6          4.0         1.2 versicolor
#R> 94           5.0         2.3          3.3         1.0 versicolor
#R> 95           5.6         2.7          4.2         1.3 versicolor
#R> 96           5.7         3.0          4.2         1.2 versicolor
#R> 97           5.7         2.9          4.2         1.3 versicolor
#R> 98           6.2         2.9          4.3         1.3 versicolor
#R> 99           5.1         2.5          3.0         1.1 versicolor
#R> 100          5.7         2.8          4.1         1.3 versicolor
#R> 101          6.3         3.3          6.0         2.5  virginica
#R> 102          5.8         2.7          5.1         1.9  virginica
#R> 103          7.1         3.0          5.9         2.1  virginica
#R> 104          6.3         2.9          5.6         1.8  virginica
#R> 105          6.5         3.0          5.8         2.2  virginica
#R> 106          7.6         3.0          6.6         2.1  virginica
#R> 107          4.9         2.5          4.5         1.7  virginica
#R> 108          7.3         2.9          6.3         1.8  virginica
#R> 109          6.7         2.5          5.8         1.8  virginica
#R> 110          7.2         3.6          6.1         2.5  virginica
#R> 111          6.5         3.2          5.1         2.0  virginica
#R> 112          6.4         2.7          5.3         1.9  virginica
#R> 113          6.8         3.0          5.5         2.1  virginica
#R> 114          5.7         2.5          5.0         2.0  virginica
#R> 115          5.8         2.8          5.1         2.4  virginica
#R> 116          6.4         3.2          5.3         2.3  virginica
#R> 117          6.5         3.0          5.5         1.8  virginica
#R> 118          7.7         3.8          6.7         2.2  virginica
#R> 119          7.7         2.6          6.9         2.3  virginica
#R> 120          6.0         2.2          5.0         1.5  virginica
#R> 121          6.9         3.2          5.7         2.3  virginica
#R> 122          5.6         2.8          4.9         2.0  virginica
#R> 123          7.7         2.8          6.7         2.0  virginica
#R> 124          6.3         2.7          4.9         1.8  virginica
#R> 125          6.7         3.3          5.7         2.1  virginica
#R> 126          7.2         3.2          6.0         1.8  virginica
#R> 127          6.2         2.8          4.8         1.8  virginica
#R> 128          6.1         3.0          4.9         1.8  virginica
#R> 129          6.4         2.8          5.6         2.1  virginica
#R> 130          7.2         3.0          5.8         1.6  virginica
#R> 131          7.4         2.8          6.1         1.9  virginica
#R> 132          7.9         3.8          6.4         2.0  virginica
#R> 133          6.4         2.8          5.6         2.2  virginica
#R> 134          6.3         2.8          5.1         1.5  virginica
#R> 135          6.1         2.6          5.6         1.4  virginica
#R> 136          7.7         3.0          6.1         2.3  virginica
#R> 137          6.3         3.4          5.6         2.4  virginica
#R> 138          6.4         3.1          5.5         1.8  virginica
#R> 139          6.0         3.0          4.8         1.8  virginica
#R> 140          6.9         3.1          5.4         2.1  virginica
#R> 141          6.7         3.1          5.6         2.4  virginica
#R> 142          6.9         3.1          5.1         2.3  virginica
#R> 143          5.8         2.7          5.1         1.9  virginica
#R> 144          6.8         3.2          5.9         2.3  virginica
#R> 145          6.7         3.3          5.7         2.5  virginica
#R> 146          6.7         3.0          5.2         2.3  virginica
#R> 147          6.3         2.5          5.0         1.9  virginica
#R> 148          6.5         3.0          5.2         2.0  virginica
#R> 149          6.2         3.4          5.4         2.3  virginica
#R> 150          5.9         3.0          5.1         1.8  virginica
t_iris <- as_tibble(iris)
# print the tibble
class(t_iris)
#R> [1] "tbl_df"     "tbl"        "data.frame"
t_iris
#R> # A tibble: 150 x 5
#R>    Sepal.Length Sepal.Width Petal.Length Petal.Width Species
#R>           <dbl>       <dbl>        <dbl>       <dbl> <fct>  
#R>  1          5.1         3.5          1.4         0.2 setosa 
#R>  2          4.9         3            1.4         0.2 setosa 
#R>  3          4.7         3.2          1.3         0.2 setosa 
#R>  4          4.6         3.1          1.5         0.2 setosa 
#R>  5          5           3.6          1.4         0.2 setosa 
#R>  6          5.4         3.9          1.7         0.4 setosa 
#R>  7          4.6         3.4          1.4         0.3 setosa 
#R>  8          5           3.4          1.5         0.2 setosa 
#R>  9          4.4         2.9          1.4         0.2 setosa 
#R> 10          4.9         3.1          1.5         0.1 setosa 
#R> # ... with 140 more rows
```

### Manually

A tibble can also be created manually. Notice the following two points:

- vectors of length 1 (only) are recycled,  
- vectors that depend on others can be directly created.
  

```r
example_tibble <- tibble(
  value1 = 1:10, 
  value2 = 5, 
  value3 = value1^2 * value2
)
example_tibble 
#R> # A tibble: 10 x 3
#R>    value1 value2 value3
#R>     <int>  <dbl>  <dbl>
#R>  1      1      5      5
#R>  2      2      5     20
#R>  3      3      5     45
#R>  4      4      5     80
#R>  5      5      5    125
#R>  6      6      5    180
#R>  7      7      5    245
#R>  8      8      5    320
#R>  9      9      5    405
#R> 10     10      5    500
```

Another example for manually creating a tibble:


```r
tibble(
  x = 1:10, 
  y = x ^ 3, 
  xy = x+y
)
#R> # A tibble: 10 x 3
#R>        x     y    xy
#R>    <int> <dbl> <dbl>
#R>  1     1     1     2
#R>  2     2     8    10
#R>  3     3    27    30
#R>  4     4    64    68
#R>  5     5   125   130
#R>  6     6   216   222
#R>  7     7   343   350
#R>  8     8   512   520
#R>  9     9   729   738
#R> 10    10  1000  1010
```


### `tribble`

A tribble is a tibble created in a transposed way. To be noticed:

- column headings are entered (as a formula) with a `~`,
- data are entered in rows,
- all values are separated by commas.


```r
example_tribble <- tribble(
	~Data1, ~Data2, ~Data3,
	"X", 2, 7,
	"Y", 5, 12,
	"Z", 4, 8 
	)
example_tribble
#R> # A tibble: 3 x 3
#R>   Data1 Data2 Data3
#R>   <chr> <dbl> <dbl>
#R> 1 X         2     7
#R> 2 Y         5    12
#R> 3 Z         4     8
```

<!--chapter:end:12-tibble.Rmd-->

# `readr`  and `readxl`  {#readr}  
 
 


## `readr`



As shown in Chapter \@ref(import), base R has many functions to read some types of files. Readr therefore provides a fast and simple way to read rectangular data, such as csv, fwf etc. 



`readr` improves on them because it:  

- is much faster,
- has mainly functionalities,
- converts data directly into tibbles,
- handles the conversion of the type of data in a better way.


Notice that `readr` uses names of functions that are very close to the base R functions: e.g., `read_csv` instead of `read.csv` in base R.    
The functions form  a `read_xxx` family where 'xxx' stands for the way the data you want read was recorded:

read_csv(): comma separated (CSV) files
read_tsv(): tab separated files
read_delim(): general delimited files
read_fwf(): fixed width files
read_table(): tabular files where columns are separated by white-space.
read_log(): web log files

In my experience, using the right member of the family yields better results, for instance in parsing the columns.

To install the CRAN version:

```{r
install.packages("readr")
```

### `read.csv`

read_csv() reads comma delimited files and is one of the most common forms of data storage. Therefore, if you understand how read.csv() works, the other functions of readr are also fairly easy to understand. 

When you run read_csv() it prints out a column specification that gives the name and type of each column. Example:


```r
read_csv
#R> function (file, col_names = TRUE, col_types = NULL, locale = default_locale(), 
#R>     na = c("", "NA"), quoted_na = TRUE, quote = "\"", comment = "", 
#R>     trim_ws = TRUE, skip = 0, n_max = Inf, guess_max = min(1000, 
#R>         n_max), progress = show_progress(), skip_empty_rows = TRUE) 
#R> {
#R>     tokenizer <- tokenizer_csv(na = na, quoted_na = quoted_na, 
#R>         quote = quote, comment = comment, trim_ws = trim_ws, 
#R>         skip_empty_rows = skip_empty_rows)
#R>     read_delimited(file, tokenizer, col_names = col_names, col_types = col_types, 
#R>         locale = locale, skip = skip, skip_empty_rows = skip_empty_rows, 
#R>         comment = comment, n_max = n_max, guess_max = guess_max, 
#R>         progress = progress)
#R> }
#R> <bytecode: 0x7fa496f418e0>
#R> <environment: namespace:readr>
```

The first step of the process is then the selection of the path to the file to read (As shown in the following example CSV File:


```r
read_csv("Insurance_sample.csv")
#R> Parsed with column specification:
#R> cols(
#R>   policyID = col_double(),
#R>   statecode = col_character(),
#R>   county = col_character(),
#R>   eq_site_limit = col_double(),
#R>   hu_site_limit = col_double(),
#R>   fl_site_limit = col_double(),
#R>   fr_site_limit = col_double(),
#R>   tiv_2011 = col_double(),
#R>   tiv_2012 = col_double(),
#R>   eq_site_deductible = col_double(),
#R>   hu_site_deductible = col_double(),
#R>   fl_site_deductible = col_double(),
#R>   fr_site_deductible = col_double(),
#R>   point_latitude = col_double(),
#R>   point_longitude = col_double(),
#R>   line = col_character(),
#R>   construction = col_character(),
#R>   point_granularity = col_double()
#R> )
#R> # A tibble: 36,634 x 18
#R>    policyID statecode county eq_site_limit hu_site_limit fl_site_limit
#R>       <dbl> <chr>     <chr>          <dbl>         <dbl>         <dbl>
#R>  1   119736 FL        CLAY ~       498960        498960        498960 
#R>  2   448094 FL        CLAY ~      1322376.      1322376.      1322376.
#R>  3   206893 FL        CLAY ~       190724.       190724.       190724.
#R>  4   333743 FL        CLAY ~            0         79521.            0 
#R>  5   172534 FL        CLAY ~            0        254282.            0 
#R>  6   785275 FL        CLAY ~            0        515036.            0 
#R>  7   995932 FL        CLAY ~            0      19260000             0 
#R>  8   223488 FL        CLAY ~       328500        328500        328500 
#R>  9   433512 FL        CLAY ~       315000        315000        315000 
#R> 10   142071 FL        CLAY ~       705600        705600        705600 
#R> # ... with 36,624 more rows, and 12 more variables: fr_site_limit <dbl>,
#R> #   tiv_2011 <dbl>, tiv_2012 <dbl>, eq_site_deductible <dbl>,
#R> #   hu_site_deductible <dbl>, fl_site_deductible <dbl>,
#R> #   fr_site_deductible <dbl>, point_latitude <dbl>, point_longitude <dbl>,
#R> #   line <chr>, construction <chr>, point_granularity <dbl>
```

The data might not have column names. You can use col_names = FALSE to tell read_csv() not to treat the first row as headings, and instead label them sequentially from X1 to Xn:

```{r
read_csv("Insurance_sample.csv", col_names = FALSE)
```

The insurance example above has column names and it is therefore not necessary to tell read_csv() to treat the first row as headings.

At this point in time, this is all you need to now about reading or treating CSV files. There are many other functions with regards to reading and writing CSV files, yet for the sake of this project, it is not necessary to have that level of detail.

### `read_delim`  

We'll also describe `read_delim` because functions of the family behave are special cases of this function. For instance, `read_csv` is equivalent to `read_delim` with a `,` as a character to separate the columns.  

- The `file` argument gives the name of a file, possibly with the path to it, if it is not in the same folder. Again, the path can also be an url.  
- `delim` provides the character that separates columns in the data.



```r
# assuming that the AH001.txt is in the folder
df <- read_delim ("AH001.txt", delim = "," , trim_ws=TRUE)
#R> Parsed with column specification:
#R> cols(
#R>   Area = col_character(),
#R>   AreaCode = col_character(),
#R>   AreaCode2 = col_logical(),
#R>   Grain = col_character(),
#R>   Year = col_double(),
#R>   Month = col_double(),
#R>   LPrice = col_double(),
#R>   HPrice = col_double()
#R> )
df
#R> # A tibble: 9,765 x 8
#R>    Area  AreaCode AreaCode2 Grain  Year Month LPrice HPrice
#R>    <chr> <chr>    <lgl>     <chr> <dbl> <dbl>  <dbl>  <dbl>
#R>  1 AH    001      NA        BO     1738     9     98    120
#R>  2 AH    001      NA        BO     1738    10     99    120
#R>  3 AH    001      NA        BO     1738    11    100    120
#R>  4 AH    001      NA        BO     1738    12     93    120
#R>  5 AH    001      NA        BO     1739     1     90    120
#R>  6 AH    001      NA        BO     1739     2     98    120
#R>  7 AH    001      NA        BO     1739     3    100    124
#R>  8 AH    001      NA        BO     1739     4    100    121
#R>  9 AH    001      NA        BO     1739     9     90    125
#R> 10 AH    001      NA        BO     1740     6     75    130
#R> # ... with 9,755 more rows
class(df)
#R> [1] "spec_tbl_df" "tbl_df"      "tbl"         "data.frame"
```

Notice an important message, the types of the columns were guessed by the function. For instance, the column "Area" was guessed to be of type "character". With that respect, the next arguments are particularly useful.    
- First, `trim_ws` is a logical for whether the leading white space in each recording should be erased before parsing. With a white space, columns of numeric values with different number of digits could be guessed as character vectors.  
Second, we can override the guess of `read_delim` by specifying the types: this is called "to parse" a file.  
We can parse into many types and use abbreviations to set them: c = character, i = integer, n = number, d = double, l = logical, D = date, T = date time, t = time, ? = guess.

All of these parsing calls can cause unexpected problems. For instance, one may need to change the symbol for decimal with the extra argument for the column type `locale=locale(decimal_mark=",")`. 
Notice the behavior when an observation is not of the same type as expected: it is changed to `NA`.  
The function `problems` lists the rows with problems.


```r
df <- read_delim("AH001.txt", delim=",", trim_ws=TRUE,
                col_types = cols(LPrice="d", HPrice ="d") )
df
#R> # A tibble: 9,765 x 8
#R>    Area  AreaCode AreaCode2 Grain  Year Month LPrice HPrice
#R>    <chr> <chr>    <lgl>     <chr> <dbl> <dbl>  <dbl>  <dbl>
#R>  1 AH    001      NA        BO     1738     9     98    120
#R>  2 AH    001      NA        BO     1738    10     99    120
#R>  3 AH    001      NA        BO     1738    11    100    120
#R>  4 AH    001      NA        BO     1738    12     93    120
#R>  5 AH    001      NA        BO     1739     1     90    120
#R>  6 AH    001      NA        BO     1739     2     98    120
#R>  7 AH    001      NA        BO     1739     3    100    124
#R>  8 AH    001      NA        BO     1739     4    100    121
#R>  9 AH    001      NA        BO     1739     9     90    125
#R> 10 AH    001      NA        BO     1740     6     75    130
#R> # ... with 9,755 more rows
problems(df)
#R> [1] row      col      expected actual  
#R> <0 rows> (or 0-length row.names)
```

Notice that the names of the variables are not within `" "`. This is a general feature of the `tidyverse`.   
By default, the first line of the data file is used for naming the columns. This can be changed.  
- `col_names` is the vector of names set for the variables.
- `skip` determines how many lines to be skipped in the file. This is useful when the file does contain names that one does not want to keep.


```r
df <- read_delim("AH001.txt", delim = "," , trim_ws=TRUE,
                skip = 1, col_names = FALSE)
#R> Parsed with column specification:
#R> cols(
#R>   X1 = col_character(),
#R>   X2 = col_character(),
#R>   X3 = col_logical(),
#R>   X4 = col_character(),
#R>   X5 = col_double(),
#R>   X6 = col_double(),
#R>   X7 = col_double(),
#R>   X8 = col_double()
#R> )
df
#R> # A tibble: 9,765 x 8
#R>    X1    X2    X3    X4       X5    X6    X7    X8
#R>    <chr> <chr> <lgl> <chr> <dbl> <dbl> <dbl> <dbl>
#R>  1 AH    001   NA    BO     1738     9    98   120
#R>  2 AH    001   NA    BO     1738    10    99   120
#R>  3 AH    001   NA    BO     1738    11   100   120
#R>  4 AH    001   NA    BO     1738    12    93   120
#R>  5 AH    001   NA    BO     1739     1    90   120
#R>  6 AH    001   NA    BO     1739     2    98   120
#R>  7 AH    001   NA    BO     1739     3   100   124
#R>  8 AH    001   NA    BO     1739     4   100   121
#R>  9 AH    001   NA    BO     1739     9    90   125
#R> 10 AH    001   NA    BO     1740     6    75   130
#R> # ... with 9,755 more rows
colnames(df) <- LETTERS[1:length(df)]
df
#R> # A tibble: 9,765 x 8
#R>    A     B     C     D         E     F     G     H
#R>    <chr> <chr> <lgl> <chr> <dbl> <dbl> <dbl> <dbl>
#R>  1 AH    001   NA    BO     1738     9    98   120
#R>  2 AH    001   NA    BO     1738    10    99   120
#R>  3 AH    001   NA    BO     1738    11   100   120
#R>  4 AH    001   NA    BO     1738    12    93   120
#R>  5 AH    001   NA    BO     1739     1    90   120
#R>  6 AH    001   NA    BO     1739     2    98   120
#R>  7 AH    001   NA    BO     1739     3   100   124
#R>  8 AH    001   NA    BO     1739     4   100   121
#R>  9 AH    001   NA    BO     1739     9    90   125
#R> 10 AH    001   NA    BO     1740     6    75   130
#R> # ... with 9,755 more rows
```

Data often contain specific special character, in particular for comments and NA's.

- `comment` takes the character that signals comments.
- `na` signals what values should be consider as NA's.


```r
df <- read_delim("AH001.txt", delim = "," , trim_ws=TRUE,
                skip = 1, col_names = FALSE, 
                comment = "%", na = "9999")
```



## `readxl`

Lots of rectangular data out there is in Excel files. One way is to handle it could be to first transform the data into a `.csv` file and then import it as described above.  
Thanks to the `readxl` package, one can also read it directly.[^Notice that R can also write to an Excel file. Why would one do that? Maybe because collaborators only work with Excel. This is achieved with the package `XLConnect` but we won't dig into these details here.]
As part of the `tidyverse` bundle, `readxl` shares features and rules with `readr`.   
Below are some of the specific features.  

- `read_excel` is the function that reads the data in the file and assigns it to an object, as illustrated in the following chunk.


```r
df <- readxl::read_excel("data_china.xlsx")
df 
#R> # A tibble: 19 x 8
#R>    Area  AreaCode AreaCode2 Grain  Year Month LPrice HPrice
#R>    <chr>    <dbl> <lgl>     <chr> <dbl> <dbl>  <dbl>  <dbl>
#R>  1 AH           1 NA        BO     1738     9     98    120
#R>  2 AH           1 NA        BO     1738    10     99    120
#R>  3 AH           1 NA        BO     1738    11    100    120
#R>  4 AH           1 NA        BO     1738    12     93    120
#R>  5 AH           1 NA        BO     1739     1     90    120
#R>  6 AH           1 NA        BO     1739     2     98    120
#R>  7 AH           1 NA        BO     1739     3    100    124
#R>  8 AH           1 NA        BO     1739     4    100    121
#R>  9 AH           1 NA        BO     1739     9     90    125
#R> 10 AH           1 NA        BO     1740     6     75    130
#R> 11 AH           1 NA        BO     1740     7     75    130
#R> 12 AH           1 NA        BO     1740     8     75    150
#R> 13 AH           1 NA        BO     1740     9     75    150
#R> 14 AH           1 NA        BO     1740    10     75    150
#R> 15 AH           1 NA        BO     1740    11     75    150
#R> 16 AH           1 NA        BO     1740    12     75    150
#R> 17 AH           1 NA        BO     1741     1     75    150
#R> 18 AH           1 NA        BO     1741     2     75    138
#R> 19 AH           1 NA        BO     1741     3     90    125
```
Importantly, notice that the exact extension does not matter as `readxl` recognizes both `.xls` and `.xlsx`.  
Notice that if the file contains multiple sheets, these can all be accessed.

- `excel_sheets` is a function that yields the names of the different sheets in a file.  


```r
readxl::excel_sheets("data_china.xlsx")
#R> [1] "AH" "FJ"
```

To know the specific sheets allows to call them directly by name. Alternatively, this can also be done by a number.

- The `sheet` argument specifies the required sheet either by a name or by a number.
```r
df <- read_excel("data_china.xlsx", sheet="FJ") 
```

A specific range for the data to be read can also be specified. Here are arguments that allow that.  

- `n_max` for the maximum number of line to be read.
- `range` for a specific range, describe in one of the possible ways:
  - extreme cells of rectangular data: `range="B1:D10"`,
  - with `cell_rows` for the required rows: `range=cell_rows(1:10)`,
  - with `cell_cols` for the required columns: `range=cell_cols("B:E")`.













<!--chapter:end:13-readr.Rmd-->

# `magrittr` {#magrittr}


The `magrittr` package offers an operator, the pipe `%>%`, which ultimately will improve coding in R by:

- Structuring sequences of data operations from left-to-right
- Minimizing the need for local variables and function definitions
- Avoiding nested function calls
- Simplifying the process of adding steps anywhere in the sequence of operations

In a few words, that are not as clear as the examples below, the functions calls are now decomposed into steps and these steps are "_piped_" thanks to the operator `%>%`.    

To install the CRAN version:

```{r
install.packages("magrittr")
```

## How to pipe

A basic pipeline is constructed under the following general idea: the call to the left of the pipe is used as an argument (by default the first argument) in the call to the right of the pipe.  
Using the mathematical notation for functions, the following statements give a pretty accurate idea of the procedure.  

Basic piping:
x %>% f is equivalent to f(x)
x %>% f(y) is equivalent to f(x, y)
x %>% f %>% g %>% h is equivalent to h(g(f(x)))

Example for `x %>% f` (This is the most basic rule for piping):


```r
BasicPipe <- c(1:5, 10, 12)
mean(BasicPipe)
#R> [1] 5.285714
BasicPipe %>%
	mean()
#R> [1] 5.285714
```

Notice that it is usual to break lines after the pipe `%>%` as it facilitates reading and addition of new steps. Also, the `()` pasted to `mean` is not necessary, but, again, it makes it clear that we pipe a vector into a function.  
Generally, the construction of the code must be re-thought as the calls above are read in reverse ways: `mean(BasicPipe)` reads use the function `mean` on the vector `BasicPipe`, while `BasicPipe %>% mean()` reads take the vector `BasicPipe` and apply the function `mean` to it.



Example for `x %>% f(y)`  (This rule shows how the left-to-pipe element is used as first argument in the right-to-pipe call):

Recall this property as the _first argument rule_.


```r
BasicPipe <- c(1:5, 10, 12)
mean(BasicPipe, trim=0.1)
#R> [1] 5.285714

BasicPipe %>%
	mean(trim=0.1)
#R> [1] 5.285714
```



Example for `x %>% f %>% g %>% h` (This rule shows that the pipeline can include many steps):


```r
BasicPipe <- c(1:5, 10, 12)
round(sqrt(mean(BasicPipe)),2)
#R> [1] 2.3

BasicPipe %>%
	mean() %>%
	sqrt() %>%
	round(2)
#R> [1] 2.3
```


## Using a placeholder

One can actually decide where the left-to-pipe element should be included in the right-to-pipe call. For that, use a dot, `.`, as a placeholder in the right-to-pipe call.

- `x %>% f(y, .)` is equivalent to `f(y, x)`

The `.` indicates where the left-to-pipe element should be used.


```r
round(17.23893,3)
#R> [1] 17.239

3 %>%
	round(17.23893, .)
#R> [1] 17.239
```


- `x %>% f(y, z = .)` is equivalent to `f(y, z = x)`

Notice that the left-to-pipe element need not be an argument, but can also be the value of an argument.


## Multiple placeholders

The placeholder can be used multiple times. Notice, however, that if the placeholder is not an argument (but simply a value of an argument), then `magrittr` still applies the _first argument rule_, unless the call on the right-to-pipe is enclosed in curly brackets.

- `x %>% f(y = nrow(.), z = ncol(.))` is equivalent to `f(x, y = nrow(x), z = ncol(x))`

- `x %>% {f(y = nrow(.), z = ncol(.))}` is equivalent to `f(y = nrow(x), z = ncol(x))`


```r
require(tidyverse)
data(iris)


t_iris <- as_tibble(iris)
t_iris2 <- t_iris[t_iris$Sepal.Length==5, ]
av.sw <- mean(t_iris2$Sepal.Width) 
av.sw
#R> [1] 3.12

av.sw2 <- iris %>%
            as_tibble() %>%
            .[.$Sepal.Length==5, ] %>%
            {mean(.$Sepal.Width)}
av.sw2  
#R> [1] 3.12
```

<!--chapter:end:14-magrittr.Rmd-->

---
title: "StringR"
output: html_document
---

The stringr package focuses on and provides you with a set of functions designed to make working with strings as easy as possible. Stringr focusses on the most important and commonly used string manipulation functions.

Let's start with the installation of StringR:

```{r
install.packages("stringr")
```

Usage
All functions in stringr start with str_ and take a vector of strings as the first argument.


```r
x <- c("stadium", "football", "players", 
       "halftime", "referee", "goalkeeper")
str_length(x) 
#R> [1]  7  8  7  8  7 10

str_c(x, collapse = ", ")
#R> [1] "stadium, football, players, halftime, referee, goalkeeper"

str_sub(x, 1, 3)
#R> [1] "sta" "foo" "pla" "hal" "ref" "goa"
```

There are seven main verbs that work with patterns:

str_detect(x, pattern) tells you if there’s any match to the pattern.


```r
str_detect(x, "[a]")
#R> [1]  TRUE  TRUE  TRUE  TRUE FALSE  TRUE
```

str_count(x, pattern) counts the number of patterns.


```r
str_count(x, "[a]")
#R> [1] 1 1 1 1 0 1
```

str_subset(x, pattern) extracts the matching components.


```r
str_subset(x, "[r]")
#R> [1] "players"    "referee"    "goalkeeper"
```

str_locate(x, pattern) gives the position of the match.


```r
str_locate(x, "[a]")
#R>      start end
#R> [1,]     3   3
#R> [2,]     6   6
#R> [3,]     3   3
#R> [4,]     2   2
#R> [5,]    NA  NA
#R> [6,]     3   3
```

str_extract(x, pattern) extracts the text of the match.


```r
str_extract(x, "[a]")
#R> [1] "a" "a" "a" "a" NA  "a"
```

str_match(x, pattern) extracts parts of the match defined by parentheses.

# extract the characters on either side of the vowel

```r
str_match(x, "(.)[ae](.)")
#R>      [,1]  [,2] [,3]
#R> [1,] "tad" "t"  "d" 
#R> [2,] "bal" "b"  "l" 
#R> [3,] "lay" "l"  "y" 
#R> [4,] "hal" "h"  "l" 
#R> [5,] "ref" "r"  "f" 
#R> [6,] "oal" "o"  "l"
```

str_replace(x, pattern, replacement) replaces the matches with new text.


```r
str_replace(x, "[aei]", "X")
#R> [1] "stXdium"    "footbXll"   "plXyers"    "hXlftime"   "rXferee"   
#R> [6] "goXlkeeper"
```

str_split(x, pattern) splits up a string into multiple pieces.

```r
str_split(c("a,b", "c,d,e"), ",")
#R> [[1]]
#R> [1] "a" "b"
#R> 
#R> [[2]]
#R> [1] "c" "d" "e"
```

<!--chapter:end:15-stringr.Rmd-->

# `tidyr` {#tidyr}


Among the many ways of organizing a dataset, the `tidyr` way is a convenient, thought-through and consistent way of thinking of a dataset.  
There are many types of messy data. We introduce here the tools to bring each to a tidy version.  
The general principle for creating tidy data is expressed in these three rules:

- every column is a variable,
- every row is an observation,
- every type of observation in a different table.

The tidying of a data set is mainly obtained with two functions/verbs: `gather` and `spread`.  
Further tidying is obtained with the functions/verbs `separate` and `unite`.

To install the CRAN version:

```{r
install.packages("tidyr")
```

## `gather`

`gather` takes multiple columns, and gathers them into key-value pairs. From a wide data set, we obtain a (vertically) longer data set.  
Let's illustrate this verb with an example.

Consider the following data set that gives the gains of each person in a lottery between Monday and Thursday.


```r
flights <- tibble(person= c("Philipp","Corinna","Laurin"),
                  jan= c(2, 5, 1),
                  feb= c(3, 7, 4),
                  mar= c(1, 3, 4),
                  apr= c(1, 2, 5)
                  )
flights
#R> # A tibble: 3 x 5
#R>   person    jan   feb   mar   apr
#R>   <chr>   <dbl> <dbl> <dbl> <dbl>
#R> 1 Philipp     2     3     1     1
#R> 2 Corinna     5     7     3     2
#R> 3 Laurin      1     4     4     5
```

This data set has 5 columns. Clearly, this does not correspond to 5 variables. Instead, a tidy data set should only include 3 columns for the variables 'name', 'day' and 'gains'. Each row would then be an observation with one value for each of these variables: e.g., Beth won 7 on Tuesday.  
For the tidying, observe that the appropriate variable 'day' is spread across four columns 'mon', 'tue', 'wed' and 'thu'. These must `gather`ed into one column/variable.

- `tidyr` calls `key` the tidy variable whose values are the names of the messy columns
('day' in the example above),   
- `tidyr` calls `value` the tidy variable whose values are spread over the messy cells
('gains' in the example above).

The call of the function is then:

```r
gather(df, key, value, messy_col1, ..., messy_coln)
```

In the example above, we would obtain the tidy data set in the following way.

```r

tidy_flights <- gather(flights,
                        key= "months",
                        value= "flights",
                        jan:apr
                        ) 
tidy_flights
#R> # A tibble: 12 x 3
#R>    person  months flights
#R>    <chr>   <chr>    <dbl>
#R>  1 Philipp jan          2
#R>  2 Corinna jan          5
#R>  3 Laurin  jan          1
#R>  4 Philipp feb          3
#R>  5 Corinna feb          7
#R>  6 Laurin  feb          4
#R>  7 Philipp mar          1
#R>  8 Corinna mar          3
#R>  9 Laurin  mar          4
#R> 10 Philipp apr          1
#R> 11 Corinna apr          2
#R> 12 Laurin  apr          5
```
Notice how `tidyr` understands the name of the columns when separated by `:`. It simply uses all the columns in the positions from (including) the first column given to the last (including) column given.   
Alternatively, one can obtain the same result by excluding variables to be gathered using the minus symbol `-`.

```r
tidy_lottery <- gather(flights, key="months", value="flights", -person)
```



```r
wine <- tribble(
  ~name, ~`2018`, ~`2011`, ~`2020`,
  "mie", 10, 20, 30,
  "eba", 1, 2, 3,
  "str", 14, 24, 5
)

wine
#R> # A tibble: 3 x 4
#R>   name  `2018` `2011` `2020`
#R>   <chr>  <dbl>  <dbl>  <dbl>
#R> 1 mie       10     20     30
#R> 2 eba        1      2      3
#R> 3 str       14     24      5

tidy_wine <- gather(wine, key=year, value=glassesofwine, `2018`, `2011`, `2020`)
  
tidy_wine
#R> # A tibble: 9 x 3
#R>   name  year  glassesofwine
#R>   <chr> <chr>         <dbl>
#R> 1 mie   2018             10
#R> 2 eba   2018              1
#R> 3 str   2018             14
#R> 4 mie   2011             20
#R> 5 eba   2011              2
#R> 6 str   2011             24
#R> 7 mie   2020             30
#R> 8 eba   2020              3
#R> 9 str   2020              5
```


## `spread`

`spread` does the opposite of `gather`. It takes two columns (key & value), and spreads into multiple columns: From a (vertically) long data set, we obtain a wider data set.  
Let's illustrate this verb with an example.



```r
students <- tibble(student= rep(c("Moritz","Philipp","Niklas"),2),
                  info= rep(c("hair","age"),3),
                  measure= c("red", 23, "brown", 23, "blond", 23)
                  )
students
#R> # A tibble: 6 x 3
#R>   student info  measure
#R>   <chr>   <chr> <chr>  
#R> 1 Moritz  hair  red    
#R> 2 Philipp age   23     
#R> 3 Niklas  hair  brown  
#R> 4 Moritz  age   23     
#R> 5 Philipp hair  blond  
#R> 6 Niklas  age   23

students3 <- rbind(students, c("Freddy", "height", 185))
students3
#R> # A tibble: 7 x 3
#R>   student info   measure
#R>   <chr>   <chr>  <chr>  
#R> 1 Moritz  hair   red    
#R> 2 Philipp age    23     
#R> 3 Niklas  hair   brown  
#R> 4 Moritz  age    23     
#R> 5 Philipp hair   blond  
#R> 6 Niklas  age    23     
#R> 7 Freddy  height 185

students2 <- tibble(
student= c(rep(c("Moritz","Philipp","Niklas"),2),   "Freddy"),
info= c(rep(c("hair","age"),3),    "height"),
measure= c("red", 23, "brown", 23, "blond", 23,   185)
                  )
students2
#R> # A tibble: 7 x 3
#R>   student info   measure
#R>   <chr>   <chr>  <chr>  
#R> 1 Moritz  hair   red    
#R> 2 Philipp age    23     
#R> 3 Niklas  hair   brown  
#R> 4 Moritz  age    23     
#R> 5 Philipp hair   blond  
#R> 6 Niklas  age    23     
#R> 7 Freddy  height 185

tidy_students2 <- spread(students2, key=info, value=measure)
tidy_students2
#R> # A tibble: 4 x 4
#R>   student age   hair  height
#R>   <chr>   <chr> <chr> <chr> 
#R> 1 Freddy  <NA>  <NA>  185   
#R> 2 Moritz  23    red   <NA>  
#R> 3 Niklas  23    brown <NA>  
#R> 4 Philipp 23    blond <NA>
```

Clearly, here, each single observation (of one person) has information over different rows. These must be `spread` into appropriate variables.  
Recall that the `key` refers to the tidy variable _vs_ messy columns.  
Also, recall that `value` refers to the tidy variable _vs_ messy cells.


```r
tidy_students <- spread(students, key=info, value=measure)
tidy_students
#R> # A tibble: 3 x 3
#R>   student age   hair 
#R>   <chr>   <chr> <chr>
#R> 1 Moritz  23    red  
#R> 2 Niklas  23    brown
#R> 3 Philipp 23    blond
```



## `separate` 

`separate` is used on a column to separate its content into various columns.  
The simplest call is generally the following:

```r
separate(df, messy_var, into=c(tidy_var1, tidy_var2))
```  

We now illustrate the use of this verb.


```r
tennisplayers <- tibble(info=c("Federer, Swiss","Kohlschreiber, 
                               German","Kyrgios, Australian"))
tennisplayers
#R> # A tibble: 3 x 1
#R>   info                                                    
#R>   <chr>                                                   
#R> 1 Federer, Swiss                                          
#R> 2 "Kohlschreiber, \n                               German"
#R> 3 Kyrgios, Australian

tidy_tennisplayers <- separate(tennisplayers,
                          info,
                          into= c("name", "nationality")
                          )
tidy_tennisplayers
#R> # A tibble: 3 x 2
#R>   name          nationality
#R>   <chr>         <chr>      
#R> 1 Federer       Swiss      
#R> 2 Kohlschreiber German     
#R> 3 Kyrgios       Australian
```

By default, the separation is made on a character that is neither a number nor a letter. But we can also define the separation character.

```r
separate(tennisplayers,
          info,
          into= c("name", "nationality"),
          sep= "r"
          )
#R> Warning: Expected 2 pieces. Additional pieces discarded in 3 rows [1, 2,
#R> 3].
#R> # A tibble: 3 x 2
#R>   name    nationality
#R>   <chr>   <chr>      
#R> 1 Fede    e          
#R> 2 Kohlsch eibe       
#R> 3 Ky      gios, Aust
```

Furthermore, we can also `separate` based on the number of characters in the values of the variable. Positive integers are used to start from the left while negative integers start from the right.


```r
separate(tennisplayers,
          info,
          into=c("name", "nationality"),
          sep=5
          )
#R> # A tibble: 3 x 2
#R>   name  nationality                                        
#R>   <chr> <chr>                                              
#R> 1 Feder er, Swiss                                          
#R> 2 Kohls "chreiber, \n                               German"
#R> 3 Kyrgi os, Australian

separate(tennisplayers,
          info,
          into= c("name", "nationality"),
          sep= -4
          )
#R> # A tibble: 3 x 2
#R>   name                                                 nationality
#R>   <chr>                                                <chr>      
#R> 1 Federer, S                                           wiss       
#R> 2 "Kohlschreiber, \n                               Ge" rman       
#R> 3 Kyrgios, Austra                                      lian
```

## `unite`

`unite` is used on columns to gather their content into one variable.  
The simplest call is generally the following:

```r
unite(df, tidy_var, messy_var1, messy_var2, sep="")
```

A main use of this verb is to paste characters from various columns.  
By default, these character values are united with a `_` in between, but the separator can be chosen.



```r
mail <- unite(tidy_tennisplayers, mail, name, nationality, sep="#")
mail
#R> # A tibble: 3 x 1
#R>   mail                
#R>   <chr>               
#R> 1 Federer#Swiss       
#R> 2 Kohlschreiber#German
#R> 3 Kyrgios#Australian
```






<!--chapter:end:16-tidyr.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# `dplyr` {#dplyr}


There are essentially two parts in this package, both dealing with manipulating data set.  
The first gives tools to work on a given data frame, the second to combine data frames. We describe both in turn.  

To install the CRAN version:

```{r
install.packages("dplyr")
```

## Grammar of data manipulation  

`dplyr` introduces a easier and faster way to manipulate datasets and extract information from them.
Hence, all the functions introduced here are redundant with other functions in base R. As for the rest of the `tidyverse`, they just happen to do the job in a clearer way (among other advantages).  
The approach builds on "verbs" (functions) applied successively thanks to the pipe operator `%>%`.

`dplyr` is therefore a system or grammar of data manipulation, providing a set of verbs that help you solve the most common data manipulation challenges:

- `select`
- `mutate`
- `filter`
- `arrange`
- `summarize`

These operations can be made on groups thanks to the function `group_by`.  
A few comments before we describe the verbs are in turn.

- These verbs are better used in tidy data: 
  - each column is a variable,  
  - each row is an observation.

- `select` and `mutate` manipulate/apply on the variables (columns).  

- `filter` and `arrange` manipulate/apply on the observations (rows).

- `summarise` manipulates groups of observations.

- Like in other packages of the `tidyverse`, there is no need for the usual quotes `" "` for the names.  


For the examples below, we will be using the `starwars` data set from the `dplyr`package. So, we can first have a glimpse at it.


```r
require(dplyr)
starwars
#R> # A tibble: 87 x 13
#R>    name  height  mass hair_color skin_color eye_color birth_year gender
#R>    <chr>  <int> <dbl> <chr>      <chr>      <chr>          <dbl> <chr> 
#R>  1 Luke~    172    77 blond      fair       blue            19   male  
#R>  2 C-3PO    167    75 <NA>       gold       yellow         112   <NA>  
#R>  3 R2-D2     96    32 <NA>       white, bl~ red             33   <NA>  
#R>  4 Dart~    202   136 none       white      yellow          41.9 male  
#R>  5 Leia~    150    49 brown      light      brown           19   female
#R>  6 Owen~    178   120 brown, gr~ light      blue            52   male  
#R>  7 Beru~    165    75 brown      light      blue            47   female
#R>  8 R5-D4     97    32 <NA>       white, red red             NA   <NA>  
#R>  9 Bigg~    183    84 black      light      brown           24   male  
#R> 10 Obi-~    182    77 auburn, w~ fair       blue-gray       57   male  
#R> # ... with 77 more rows, and 5 more variables: homeworld <chr>,
#R> #   species <chr>, films <list>, vehicles <list>, starships <list>
```

## `select`

The call for this function is of the form:

```r
select(df, var1, ..., varn)
```

where `df` is the original data frame from which one wishes to select data.    
Alternatively, we can write the above code. with the pipe operator

```r
df %>%
  select(var1, ..., varn)
```

Notice that the underlying data frame is not modified. However, the extracted data can be saved in the usual way, i.e., as an object with a name. 

```r
piece_df <- df %>%
              select(var1, ..., varn)
```

Here is an example of a selection of variables.


```r
require(MASS)
require(dplyr)
starwars %>% 
  dplyr::select(name, species)
#R> # A tibble: 87 x 2
#R>    name               species
#R>    <chr>              <chr>  
#R>  1 Luke Skywalker     Human  
#R>  2 C-3PO              Droid  
#R>  3 R2-D2              Droid  
#R>  4 Darth Vader        Human  
#R>  5 Leia Organa        Human  
#R>  6 Owen Lars          Human  
#R>  7 Beru Whitesun lars Human  
#R>  8 R5-D4              Droid  
#R>  9 Biggs Darklighter  Human  
#R> 10 Obi-Wan Kenobi     Human  
#R> # ... with 77 more rows
# compare with base R

starwars[,c("name", "species")]
#R> # A tibble: 87 x 2
#R>    name               species
#R>    <chr>              <chr>  
#R>  1 Luke Skywalker     Human  
#R>  2 C-3PO              Droid  
#R>  3 R2-D2              Droid  
#R>  4 Darth Vader        Human  
#R>  5 Leia Organa        Human  
#R>  6 Owen Lars          Human  
#R>  7 Beru Whitesun lars Human  
#R>  8 R5-D4              Droid  
#R>  9 Biggs Darklighter  Human  
#R> 10 Obi-Wan Kenobi     Human  
#R> # ... with 77 more rows
```

There are any ways of selecting variables:


```r
## columns/variables 1 to 4
dplyr::select(starwars, 1:4) 
#R> # A tibble: 87 x 4
#R>    name               height  mass hair_color   
#R>    <chr>               <int> <dbl> <chr>        
#R>  1 Luke Skywalker        172    77 blond        
#R>  2 C-3PO                 167    75 <NA>         
#R>  3 R2-D2                  96    32 <NA>         
#R>  4 Darth Vader           202   136 none         
#R>  5 Leia Organa           150    49 brown        
#R>  6 Owen Lars             178   120 brown, grey  
#R>  7 Beru Whitesun lars    165    75 brown        
#R>  8 R5-D4                  97    32 <NA>         
#R>  9 Biggs Darklighter     183    84 black        
#R> 10 Obi-Wan Kenobi        182    77 auburn, white
#R> # ... with 77 more rows
## works also with the name
dplyr::select(starwars, name:hair_color) 
#R> # A tibble: 87 x 4
#R>    name               height  mass hair_color   
#R>    <chr>               <int> <dbl> <chr>        
#R>  1 Luke Skywalker        172    77 blond        
#R>  2 C-3PO                 167    75 <NA>         
#R>  3 R2-D2                  96    32 <NA>         
#R>  4 Darth Vader           202   136 none         
#R>  5 Leia Organa           150    49 brown        
#R>  6 Owen Lars             178   120 brown, grey  
#R>  7 Beru Whitesun lars    165    75 brown        
#R>  8 R5-D4                  97    32 <NA>         
#R>  9 Biggs Darklighter     183    84 black        
#R> 10 Obi-Wan Kenobi        182    77 auburn, white
#R> # ... with 77 more rows
## with a negative number for all but some variable
dplyr::select(starwars, -3) 
#R> # A tibble: 87 x 12
#R>    name  height hair_color skin_color eye_color birth_year gender homeworld
#R>    <chr>  <int> <chr>      <chr>      <chr>          <dbl> <chr>  <chr>    
#R>  1 Luke~    172 blond      fair       blue            19   male   Tatooine 
#R>  2 C-3PO    167 <NA>       gold       yellow         112   <NA>   Tatooine 
#R>  3 R2-D2     96 <NA>       white, bl~ red             33   <NA>   Naboo    
#R>  4 Dart~    202 none       white      yellow          41.9 male   Tatooine 
#R>  5 Leia~    150 brown      light      brown           19   female Alderaan 
#R>  6 Owen~    178 brown, gr~ light      blue            52   male   Tatooine 
#R>  7 Beru~    165 brown      light      blue            47   female Tatooine 
#R>  8 R5-D4     97 <NA>       white, red red             NA   <NA>   Tatooine 
#R>  9 Bigg~    183 black      light      brown           24   male   Tatooine 
#R> 10 Obi-~    182 auburn, w~ fair       blue-gray       57   male   Stewjon  
#R> # ... with 77 more rows, and 4 more variables: species <chr>,
#R> #   films <list>, vehicles <list>, starships <list>
## works also with the name
dplyr::select(starwars, -mass) 
#R> # A tibble: 87 x 12
#R>    name  height hair_color skin_color eye_color birth_year gender homeworld
#R>    <chr>  <int> <chr>      <chr>      <chr>          <dbl> <chr>  <chr>    
#R>  1 Luke~    172 blond      fair       blue            19   male   Tatooine 
#R>  2 C-3PO    167 <NA>       gold       yellow         112   <NA>   Tatooine 
#R>  3 R2-D2     96 <NA>       white, bl~ red             33   <NA>   Naboo    
#R>  4 Dart~    202 none       white      yellow          41.9 male   Tatooine 
#R>  5 Leia~    150 brown      light      brown           19   female Alderaan 
#R>  6 Owen~    178 brown, gr~ light      blue            52   male   Tatooine 
#R>  7 Beru~    165 brown      light      blue            47   female Tatooine 
#R>  8 R5-D4     97 <NA>       white, red red             NA   <NA>   Tatooine 
#R>  9 Bigg~    183 black      light      brown           24   male   Tatooine 
#R> 10 Obi-~    182 auburn, w~ fair       blue-gray       57   male   Stewjon  
#R> # ... with 77 more rows, and 4 more variables: species <chr>,
#R> #   films <list>, vehicles <list>, starships <list>
```


### Helper arguments

These are arguments to help `select` the variables/columns. Here are a few of them (see `?select` for a complete list):

- `starts_with("x")`
- `ends_with("x")`
- `contains("x")`
- `matches("x")`

Notice the use of the quotes `" "` for the strings because they are not variables names.   
For instance, here, we select all the variables that have `color` in their name.

```r
require(tidyverse)
starwars %>%
  dplyr::select(
    name,
    contains("color")
    )
#R> # A tibble: 87 x 4
#R>    name               hair_color    skin_color  eye_color
#R>    <chr>              <chr>         <chr>       <chr>    
#R>  1 Luke Skywalker     blond         fair        blue     
#R>  2 C-3PO              <NA>          gold        yellow   
#R>  3 R2-D2              <NA>          white, blue red      
#R>  4 Darth Vader        none          white       yellow   
#R>  5 Leia Organa        brown         light       brown    
#R>  6 Owen Lars          brown, grey   light       blue     
#R>  7 Beru Whitesun lars brown         light       blue     
#R>  8 R5-D4              <NA>          white, red  red      
#R>  9 Biggs Darklighter  black         light       brown    
#R> 10 Obi-Wan Kenobi     auburn, white fair        blue-gray
#R> # ... with 77 more rows

starwars %>%
  dplyr::select(name, hair_color, films)
#R> # A tibble: 87 x 3
#R>    name               hair_color    films    
#R>    <chr>              <chr>         <list>   
#R>  1 Luke Skywalker     blond         <chr [5]>
#R>  2 C-3PO              <NA>          <chr [6]>
#R>  3 R2-D2              <NA>          <chr [7]>
#R>  4 Darth Vader        none          <chr [4]>
#R>  5 Leia Organa        brown         <chr [5]>
#R>  6 Owen Lars          brown, grey   <chr [3]>
#R>  7 Beru Whitesun lars brown         <chr [3]>
#R>  8 R5-D4              <NA>          <chr [1]>
#R>  9 Biggs Darklighter  black         <chr [1]>
#R> 10 Obi-Wan Kenobi     auburn, white <chr [6]>
#R> # ... with 77 more rows
```

## `mutate`

The `mutate` function allows to create new variables/columns, based on the existing variables.   
The generic call is as follows.

```r
mutate(df, new_variable = expression)

# with pipe

df %>%
  mutate(new_variable = expression)
``` 

We play a bit with it.  


```r
## add variable bmi
starwars %>%
         mutate(bmi = mass / (height/100)^2 )  
#R> # A tibble: 87 x 14
#R>    name  height  mass hair_color skin_color eye_color birth_year gender
#R>    <chr>  <int> <dbl> <chr>      <chr>      <chr>          <dbl> <chr> 
#R>  1 Luke~    172    77 blond      fair       blue            19   male  
#R>  2 C-3PO    167    75 <NA>       gold       yellow         112   <NA>  
#R>  3 R2-D2     96    32 <NA>       white, bl~ red             33   <NA>  
#R>  4 Dart~    202   136 none       white      yellow          41.9 male  
#R>  5 Leia~    150    49 brown      light      brown           19   female
#R>  6 Owen~    178   120 brown, gr~ light      blue            52   male  
#R>  7 Beru~    165    75 brown      light      blue            47   female
#R>  8 R5-D4     97    32 <NA>       white, red red             NA   <NA>  
#R>  9 Bigg~    183    84 black      light      brown           24   male  
#R> 10 Obi-~    182    77 auburn, w~ fair       blue-gray       57   male  
#R> # ... with 77 more rows, and 6 more variables: homeworld <chr>,
#R> #   species <chr>, films <list>, vehicles <list>, starships <list>,
#R> #   bmi <dbl>

## two variables created, including one created in the same call
df_b <- starwars %>%
          mutate(
            bmi = mass / (height/100)^2,
            sr.bmi = sqrt(bmi)
            ) 
df_b
#R> # A tibble: 87 x 15
#R>    name  height  mass hair_color skin_color eye_color birth_year gender
#R>    <chr>  <int> <dbl> <chr>      <chr>      <chr>          <dbl> <chr> 
#R>  1 Luke~    172    77 blond      fair       blue            19   male  
#R>  2 C-3PO    167    75 <NA>       gold       yellow         112   <NA>  
#R>  3 R2-D2     96    32 <NA>       white, bl~ red             33   <NA>  
#R>  4 Dart~    202   136 none       white      yellow          41.9 male  
#R>  5 Leia~    150    49 brown      light      brown           19   female
#R>  6 Owen~    178   120 brown, gr~ light      blue            52   male  
#R>  7 Beru~    165    75 brown      light      blue            47   female
#R>  8 R5-D4     97    32 <NA>       white, red red             NA   <NA>  
#R>  9 Bigg~    183    84 black      light      brown           24   male  
#R> 10 Obi-~    182    77 auburn, w~ fair       blue-gray       57   male  
#R> # ... with 77 more rows, and 7 more variables: homeworld <chr>,
#R> #   species <chr>, films <list>, vehicles <list>, starships <list>,
#R> #   bmi <dbl>, sr.bmi <dbl>

starwars %>%
  mutate(
    g_b = sample(c("G", "B"),
                 87,
                 replace = TRUE
                 )
    )
#R> # A tibble: 87 x 14
#R>    name  height  mass hair_color skin_color eye_color birth_year gender
#R>    <chr>  <int> <dbl> <chr>      <chr>      <chr>          <dbl> <chr> 
#R>  1 Luke~    172    77 blond      fair       blue            19   male  
#R>  2 C-3PO    167    75 <NA>       gold       yellow         112   <NA>  
#R>  3 R2-D2     96    32 <NA>       white, bl~ red             33   <NA>  
#R>  4 Dart~    202   136 none       white      yellow          41.9 male  
#R>  5 Leia~    150    49 brown      light      brown           19   female
#R>  6 Owen~    178   120 brown, gr~ light      blue            52   male  
#R>  7 Beru~    165    75 brown      light      blue            47   female
#R>  8 R5-D4     97    32 <NA>       white, red red             NA   <NA>  
#R>  9 Bigg~    183    84 black      light      brown           24   male  
#R> 10 Obi-~    182    77 auburn, w~ fair       blue-gray       57   male  
#R> # ... with 77 more rows, and 6 more variables: homeworld <chr>,
#R> #   species <chr>, films <list>, vehicles <list>, starships <list>,
#R> #   g_b <chr>
```


## `filter`

The `filter` function is equivalent of a selection, but for rows. The call is generically

```r
filter(df, condition)

# with the pipe

df %>%
  filter(condition) 
```

At this stage, it might be useful to recall the operators for conditions under `?Comparison`.  
Here are examples for this function.


```r
starwars %>%
  filter(species != "Droid")
#R> # A tibble: 77 x 13
#R>    name  height  mass hair_color skin_color eye_color birth_year gender
#R>    <chr>  <int> <dbl> <chr>      <chr>      <chr>          <dbl> <chr> 
#R>  1 Luke~    172    77 blond      fair       blue            19   male  
#R>  2 Dart~    202   136 none       white      yellow          41.9 male  
#R>  3 Leia~    150    49 brown      light      brown           19   female
#R>  4 Owen~    178   120 brown, gr~ light      blue            52   male  
#R>  5 Beru~    165    75 brown      light      blue            47   female
#R>  6 Bigg~    183    84 black      light      brown           24   male  
#R>  7 Obi-~    182    77 auburn, w~ fair       blue-gray       57   male  
#R>  8 Anak~    188    84 blond      fair       blue            41.9 male  
#R>  9 Wilh~    180    NA auburn, g~ fair       blue            64   male  
#R> 10 Chew~    228   112 brown      unknown    blue           200   male  
#R> # ... with 67 more rows, and 5 more variables: homeworld <chr>,
#R> #   species <chr>, films <list>, vehicles <list>, starships <list>

starwars %>%
  filter(
    species != "Droid" &
    eye_color == "blu"
    )
#R> # A tibble: 0 x 13
#R> # ... with 13 variables: name <chr>, height <int>, mass <dbl>,
#R> #   hair_color <chr>, skin_color <chr>, eye_color <chr>, birth_year <dbl>,
#R> #   gender <chr>, homeworld <chr>, species <chr>, films <list>,
#R> #   vehicles <list>, starships <list>

# in base R

starwars[starwars$species!="Droid" & starwars$eye_color=="blue" , ]
#R> # A tibble: 19 x 13
#R>    name  height  mass hair_color skin_color eye_color birth_year gender
#R>    <chr>  <int> <dbl> <chr>      <chr>      <chr>          <dbl> <chr> 
#R>  1 Luke~    172  77   blond      fair       blue            19   male  
#R>  2 Owen~    178 120   brown, gr~ light      blue            52   male  
#R>  3 Beru~    165  75   brown      light      blue            47   female
#R>  4 Anak~    188  84   blond      fair       blue            41.9 male  
#R>  5 Wilh~    180  NA   auburn, g~ fair       blue            64   male  
#R>  6 Chew~    228 112   brown      unknown    blue           200   male  
#R>  7 Jek ~    180 110   brown      fair       blue            NA   male  
#R>  8 Lobot    175  79   none       light      blue            37   male  
#R>  9 Mon ~    150  NA   auburn     fair       blue            48   female
#R> 10 Qui-~    193  89   brown      fair       blue            92   male  
#R> 11 Fini~    170  NA   blond      fair       blue            91   male  
#R> 12 <NA>      NA  NA   <NA>       <NA>       <NA>            NA   <NA>  
#R> 13 Adi ~    184  50   none       dark       blue            NA   female
#R> 14 Mas ~    196  NA   none       blue       blue            NA   male  
#R> 15 Clie~    183  NA   brown      fair       blue            82   male  
#R> 16 Lumi~    170  56.2 black      yellow     blue            58   female
#R> 17 Barr~    166  50   black      yellow     blue            40   female
#R> 18 Joca~    167  NA   white      fair       blue            NA   female
#R> 19 Tarf~    234 136   brown      brown      blue            NA   male  
#R> # ... with 5 more variables: homeworld <chr>, species <chr>, films <list>,
#R> #   vehicles <list>, starships <list>
```


## `arrange`

This function reorders the rows of the data set, by default in ascending order of a given variable. The typical call, for a reordering over `var1`, is:

```r
arrange(df, var1)

# with pipe

df %>%
  arrange(var1)

```

The use of multiple variables for reordering is sometimes necessary in order to break ties.

```r
## in case of several rows with same value of var1, use var2
df %>%
  arrange(
    var1,
    var2)
```

Use `desc` on the variable to show in descending order.  
Here is an example that combines these two points.


```r
starwars %>%
        arrange(
          height, 
          desc(mass))

starwars %>%
  arrange(desc(name))
```

## `summarise`

Contrary to the other verbs, the `summarise` function creates a new data frame. The usual call is:

```r
summarise(df, name = expr)

# with the pipe
df %>%
  summarise(name = expr)
```  

where `expr` stands for any function on a vector (most of the time, one of the variables) that returns a single value. That function can either be built-in or a function provided by the user.  
In that sense, notice that `summarise` does not mean to make a summary but, instead, to collapse a full vector into one single value.


```r
starwars %>%
  summarise(min_h = min(height, na.rm = TRUE),
            av_m= mean(mass, na.rm = TRUE)
            )
#R> # A tibble: 1 x 2
#R>   min_h  av_m
#R>   <dbl> <dbl>
#R> 1    66  97.3
```

### Helper functions

These are functions to help `summarise`, but are essentially wrappers for the function `[[`. These include `first(x)`, `last(x)`, `nth(x,n)`, `n()`... where `x` is the variable.


```r
starwars %>%
  summarise(nth(species, 3))
#R> # A tibble: 1 x 1
#R>   `nth(species, 3)`
#R>   <chr>            
#R> 1 Droid
```
Other functions can be used as logical tests.


```r
starwars %>%
  summarise(sum(species == "Human", na.rm=TRUE))
#R> # A tibble: 1 x 1
#R>   `sum(species == "Human", na.rm = TRUE)`
#R>                                     <int>
#R> 1                                      35

starwars %>%
  summarise(mean(species != "Human", na.rm=TRUE))
#R> # A tibble: 1 x 1
#R>   `mean(species != "Human", na.rm = TRUE)`
#R>                                      <dbl>
#R> 1                                    0.573
```


## Piping verbs

Since each verb requires a data frame and returns a data frame, we can combine verbs in a pipe.  
Here is an example.


```r
## average mass of humans 
starwars %>%
  filter(species == "Human") %>%
  summarise(av_m=mean(mass, na.rm=TRUE))
#R> # A tibble: 1 x 1
#R>    av_m
#R>   <dbl>
#R> 1  82.8

# without pipe
summarise(filter(starwars, species == "Human"), av_m=mean(mass, na.rm=TRUE))
#R> # A tibble: 1 x 1
#R>    av_m
#R>   <dbl>
#R> 1  82.8

temp1 <- filter(starwars, species == "Human")
summarise(temp1, av_m=mean(mass, na.rm=TRUE))
#R> # A tibble: 1 x 1
#R>    av_m
#R>   <dbl>
#R> 1  82.8

# with base R
temp2 <- starwars[starwars$species=="Human",]
av_m <- mean(temp2$mass, na.rm=TRUE)

av_m <- mean(starwars[starwars$species=="Human",]$mass, na.rm=TRUE)
av_m
#R> [1] 82.78182
```

Another example.


```r
# create the variable n_films for each name

# with base R
aa <- numeric(length(starwars$films))
for (i in 1:length(starwars$films)){
  aa[i] <- length(starwars$films[[i]])
}

starwars$n_films <- aa

# with dplyr 
c_l <- function(ll){
  aa <- numeric(length(ll))
  for (i in 1:length(ll)){
   aa[i] <- length(ll[[i]])
  }
  return(aa)
}

starwars %>%
  mutate(n_films = c_l(films)) %>%
  select(name, n_films) %>%
  filter( n_films >=5)
#R> # A tibble: 8 x 2
#R>   name           n_films
#R>   <chr>            <dbl>
#R> 1 Luke Skywalker       5
#R> 2 C-3PO                6
#R> 3 R2-D2                7
#R> 4 Leia Organa          5
#R> 5 Obi-Wan Kenobi       6
#R> 6 Chewbacca            5
#R> 7 Yoda                 5
#R> 8 Palpatine            5
```

## `group_by`

The function `group_by` allows to make manipulations on groups.  
Let's make an example.


```r
starwars %>%
  group_by(eye_color) %>%
  summarise(
    n_per_group = n()
  ) %>%
  filter(n_per_group > 1)
#R> # A tibble: 8 x 2
#R>   eye_color n_per_group
#R>   <chr>           <int>
#R> 1 black              10
#R> 2 blue               19
#R> 3 brown              21
#R> 4 hazel               3
#R> 5 orange              8
#R> 6 red                 5
#R> 7 unknown             3
#R> 8 yellow             11
```

## Keys for joins

`dplyr` also contains tools to join data sets. We have a glimpse at them here.  
Notice that joining data sets means forming a third data set with columns of a first and a second data set.  

A key is a column or a combination of columns.  
In order to join two data sets, two keys: a primary and a secondary key.  
The primary key must **uniquely identify the rows** of the primary data set; hence it can consist on many variables.  
The secondary key only needs to match the primary key.  

An example to illustrate this point uses the two following data sets `population` and `capital`.  

- If `population` was the primary data set, then the variable `country` alone could not be the primary key because it has repeated values.  

- On the other hand, if `capitals` was the primary data set, then the variable `country` could be that primary key.


```r
population <- tribble(
~country, ~year, ~population,
"UK", 2010, 62.7,
"UK", 2000, 58.9,
"FR", 2010, 65,
"FR", 2000, 60.9,
"RSA", 2010, 50.7,
"PT", 2010, 10.5
)

capitals <- tribble(
  ~country, ~capital, 
  "RSA", "Pretoria",
  "FR", "Paris",
  "UK", "London",
  "SP", "Madrid"
)
```

## Joins

Some joins are called mutate because they create a new data set: left_, right_, inner_ or full_ joins are of this type. Filter joins include semi_ and anti_join and they filter one data set.

inner_join():
Returning all rows from x where there are matching values in y, and all columns from x and y. Important: In the case of multiple matches between x and y, all combinations of the matches are returned.

left_join():
Returning all rows from x, and all columns from x and y. Rows in x with no match in y will have NA values in the new columns. Important: In the case of multiple matches between x and y, all combinations of the matches are returned.

right_join():
Returning all rows from y, and all columns from x and y. Rows in y with no match in x will have NA values in the new columns. Important: In the case of multiple matches between x and y, all combinations of the matches are returned.

full_join():
Returning all rows and all columns from both x and y. Important: In the case of no matching values, NA is returned for the one missing.

- `left_join` and `right_join`

The usage is, for instance,

```r
left_join(df1, df2, by=c("key1", "key2"))
# with pipe
df1 %>%
  left_join(
    df2,
    by=c("key1", "key2")
    )

```
This call will keep all the rows of `df1` and augment it with columns of `df2`. Notice that some `NA`s will be created and the rows on `df2` that do not match the primary key will not appear.  
`right_join` would do for `df2` what `left_join` join does for `df1`.


```r
capitals %>%
  left_join(
    population,
    by = "country"
    )
#R> # A tibble: 6 x 4
#R>   country capital   year population
#R>   <chr>   <chr>    <dbl>      <dbl>
#R> 1 RSA     Pretoria  2010       50.7
#R> 2 FR      Paris     2010       65  
#R> 3 FR      Paris     2000       60.9
#R> 4 UK      London    2010       62.7
#R> 5 UK      London    2000       58.9
#R> 6 SP      Madrid      NA       NA

population %>%
  left_join(
    capitals,
    by= "country"
    )
#R> # A tibble: 6 x 4
#R>   country  year population capital 
#R>   <chr>   <dbl>      <dbl> <chr>   
#R> 1 UK       2010       62.7 London  
#R> 2 UK       2000       58.9 London  
#R> 3 FR       2010       65   Paris   
#R> 4 FR       2000       60.9 Paris   
#R> 5 RSA      2010       50.7 Pretoria
#R> 6 PT       2010       10.5 <NA>
```


- `inner_join` and `full_join` 

The call is similar to above.  
`inner` takes the rows that match in **both** datasets while `full` takes all the rows that match and those that do not match.


```r
capitals %>%
  inner_join(
    population,
    by = "country"
    )
#R> # A tibble: 5 x 4
#R>   country capital   year population
#R>   <chr>   <chr>    <dbl>      <dbl>
#R> 1 RSA     Pretoria  2010       50.7
#R> 2 FR      Paris     2010       65  
#R> 3 FR      Paris     2000       60.9
#R> 4 UK      London    2010       62.7
#R> 5 UK      London    2000       58.9

capitals %>%
  full_join(
    population,
    by = "country"
    )
#R> # A tibble: 7 x 4
#R>   country capital   year population
#R>   <chr>   <chr>    <dbl>      <dbl>
#R> 1 RSA     Pretoria  2010       50.7
#R> 2 FR      Paris     2010       65  
#R> 3 FR      Paris     2000       60.9
#R> 4 UK      London    2010       62.7
#R> 5 UK      London    2000       58.9
#R> 6 SP      Madrid      NA       NA  
#R> 7 PT      <NA>      2010       10.5
```


- `semi_join` and `anti_join`

These give a copy of the first data set filtered with the second data set. Hence, it's a way to filter data from the first dataset based on information in a second dataset.  
It can be used to quickly check which rows appear in both datasets


```r
capitals %>%
  semi_join(
    population,
    by = "country"
    )
#R> # A tibble: 3 x 2
#R>   country capital 
#R>   <chr>   <chr>   
#R> 1 RSA     Pretoria
#R> 2 FR      Paris   
#R> 3 UK      London

capitals %>%
  anti_join(
    population,
    by = "country"
    )
#R> # A tibble: 1 x 2
#R>   country capital
#R>   <chr>   <chr>  
#R> 1 SP      Madrid
```


## Operations on data sets

A few other functions allow to compare data sets. These include  the self-explanatory `union`, `intersect` and `setdiff`

`setdiff`:


```r
population2 <- add_row(population, country="GER", year=2015, population=10)

setdiff(population, population2)
#R> # A tibble: 0 x 3
#R> # ... with 3 variables: country <chr>, year <dbl>, population <dbl>
setdiff(population2, population)
#R> # A tibble: 1 x 3
#R>   country  year population
#R>   <chr>   <dbl>      <dbl>
#R> 1 GER      2015         10
```

`intersect`:


```r
population2 <- add_row(population, country="GER", year=2015, population=10)

intersect(population, population2)
#R> # A tibble: 6 x 3
#R>   country  year population
#R>   <chr>   <dbl>      <dbl>
#R> 1 UK       2010       62.7
#R> 2 UK       2000       58.9
#R> 3 FR       2010       65  
#R> 4 FR       2000       60.9
#R> 5 RSA      2010       50.7
#R> 6 PT       2010       10.5
intersect(population2, population)
#R> # A tibble: 6 x 3
#R>   country  year population
#R>   <chr>   <dbl>      <dbl>
#R> 1 UK       2010       62.7
#R> 2 UK       2000       58.9
#R> 3 FR       2010       65  
#R> 4 FR       2000       60.9
#R> 5 RSA      2010       50.7
#R> 6 PT       2010       10.5
```

Other useful functions are `setequal` and `identical`.
Use `setequal(df1, df2)` which will be `TRUE` if the datasets have the same data even if the rows are not in the same order, opposed to `identical(df1, df2)`

`identical`:


```r
capitals <- tribble(
  ~country, ~capital, 
  "RSA", "Pretoria",
  "FR", "Paris",
  "UK", "London",
  "SP", "Madrid"
)

capitals2 <- tribble(
  ~country, ~capital, 
  "RSA", "Pretoria",
  "UK", "London",
  "FR", "Paris",
  "SP", "Madrid"
)

identical(capitals, capitals2)
#R> [1] FALSE
```

`sequetal`


```r
capitals <- tribble(
  ~country, ~capital, 
  "RSA", "Pretoria",
  "FR", "Paris",
  "UK", "London",
  "SP", "Madrid"
)

capitals2 <- tribble(
  ~country, ~capital, 
  "RSA", "Pretoria",
  "UK", "London",
  "FR", "Paris",
  "SP", "Madrid"
)

setequal(capitals,capitals2)
#R> [1] TRUE
```



<!--chapter:end:17-dplyr.Rmd-->

# `ggplot2` {#ggplot2}

ggplot2 is a system for creating graphics and therefore a system for data visualization. You provide the data to R, tell ggplot2 how to map variables and what graphical primitives to use, and it takes care of the details for you.

Data visualization in general is part of the skill set of a data scientist.  
It is made to, either
    - explore (confirm, analyse)
    - explain (inform, convince)

Depends who you communicate to (can be you).

To install the CRAN version:

```{r
install.packages("ggplot2")
```

## Comparison with base `plot`

Limitations of base plot:
    - plot does not redraw, i.e., the range will not adapt to new data 
    - plot is drawn as an image, i.e., it's not an object
    - manual legend
    - no unified framework for plotting, i.e., need to master other commands for other types of graphs

Example:


```r
library(ggplot2)
rm(mtcarts)
#R> Warning in rm(mtcarts): object 'mtcarts' not found
data("mtcars")
mtcars$cyl <- as.factor(mtcars$cyl) # treat 'cyl' as a factor

plot(mtcars$wt, mtcars$mpg, col = mtcars$cyl)
abline(lm(mpg ~ wt, data = mtcars), lty = 2)
lapply(mtcars$cyl, function(x) {
  abline(lm(mpg ~ wt, mtcars, subset = (cyl == x)), col = x)
  })
legend(x = 5, y = 33, legend = levels(mtcars$cyl),col = 1:3, pch = 1, bty = "n")
       
plot1 <- ggplot(mtcars, aes(x = wt, y = mpg, col = factor(cyl))) +
         geom_point() +
         geom_smooth(method=lm , se=FALSE, aes(col=cyl)) +
         geom_smooth(method=lm , se=FALSE, linetype=2, col="grey", aes(group=1))       
plot1 # print the object 'plot1'
```

![](MyR_files/figure-latex/unnamed-chunk-81-1.pdf) ![](MyR_files/figure-latex/unnamed-chunk-81-2.pdf) 

## Grammar of graphics - Leland Wilkinson

### A graphic = layers of grammatical elements
The layers are the adjectives and the nouns
Seven grammatical elements, three are essential

### Meaningful plots are built around appropriate aesthetic mappings
The mappings are the rules to assemble the nouns and adjectives


## Understanding the grammar

Building an example:


```r

p1 <- ggplot(data=diamonds, mapping= aes(x=carat, y= price)) # data and mappings

#p2 <- p1 + geom_point()  # + the general form

p2 <- p1 + geom_line()  # + the general form

p3 <- ggplot(diamonds, aes(x=carat, y= price, col=clarity)) +
      geom_point() # adding a mapping / variable

p3b <- ggplot(diamonds, aes(x=carat, y= price)) +
      geom_point(col="red") # adding a attribute


p4 <- p1 + geom_point(aes(col=clarity)) # or changing some attributes
grid.arrange(p1, p2, p3, p4, ncol=2)
```

![](MyR_files/figure-latex/unnamed-chunk-82-1.pdf)<!-- --> 

### Data and proper data format
The data being plotted
Includes: variables of interest
Tidy data helps make good `ggplot()`s


```r
iris.tidy <- iris %>%
  gather(key, Value, -Species) %>%
  separate(key, c("Part", "Measure"), "\\.")

p1 <- ggplot(iris.tidy, aes(x = Species, y = Value, col = Part)) +
geom_jitter() +
facet_grid(. ~ Measure)

p2 <- ggplot(iris.tidy, aes(x = Measure, y = Value, col = Part)) +
geom_jitter() +
facet_grid(. ~ Species)


p3 <- ggplot(iris.tidy, aes(x = Species, y = Value, col = Part)) +
geom_point()

grid.arrange(p1, p2, p3, ncol=2)
```

![](MyR_files/figure-latex/unnamed-chunk-83-1.pdf)<!-- --> 

### Aesthetics
The scales onto which we map our data
Includes: x-axis, y-axis, colour, fill, size, labels, line width, line type,...

### Geometries
The visual elements (shape) used for our data in the plot
Includes: point, line, histogram, bar, boxplot,...

### Other grammatical elements
These are
    - facets
    - statistics
    - coordinates
    - themes

### Juggling with `aes`

```r
data("mtcars")
p1 <- ggplot(mtcars, aes(x = wt, y = mpg)) +
      geom_point()

# color dependent on 'disp',
# 'disp' is continuous, hence the shades of same colour
p2 <- ggplot(mtcars, aes(x = wt, y = mpg, col = disp)) +
      geom_point()  + geom_smooth(se=FALSE)

# changing the colour depending on the variable 'clarity', 
# 'clarity' is a factor, hence the different colours
p3 <- ggplot(diamonds, aes(x = carat, y = price, col=clarity)) +
      geom_smooth()

# size dependent on 'disp'
p4 <- ggplot(mtcars, aes(x = wt, y = mpg, size = disp)) +
      geom_point()

grid.arrange(p1, p2, p3, p4, ncol=2)
#R> `geom_smooth()` using method = 'loess' and formula 'y ~ x'
#R> `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'
```

![](MyR_files/figure-latex/unnamed-chunk-84-1.pdf)<!-- --> 

### Juggling with `geom`


```r
# points and smoother layer
p1 <- ggplot(diamonds, aes(x = carat, y = price)) + 
      geom_point() + 
      geom_smooth(se=TRUE) # se = T by default

# only the smoother layer
p2 <- ggplot(diamonds, aes(x = carat, y = price)) + 
      geom_smooth()

# changing the parameters of the point geometry, much more transparent, here
p3 <- ggplot(diamonds, aes(x = carat, y = price)) + 
      geom_point(alpha=.04)

# only the smoother layer and different aesthetics,
# aes recognizes the groups and therefore separates for them
p4 <- ggplot(diamonds, aes(x = carat, y = price, col=clarity)) +
      geom_smooth() + geom_point(alpha=.04)

grid.arrange(p1, p2, p3,p4,  ncol=2)
#R> `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'
#R> `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'
#R> `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'
```

![](MyR_files/figure-latex/unnamed-chunk-85-1.pdf)<!-- --> 

## Aesthetics

### Understanding aesthetics
Usually considered as how something looks, as attributes: that's *notcorrect in `ggplot()` 
Aesthetics refers to what a variable is *mappedonto it
*Aesthetics is mapping*
We want to map as many variables as possible in a plot, that's visible aesthetics
Aesthetics/mappings are called in `aes()` while attributes are called in `geom_()`

For instance:
    - `aes(x = variable1, ...)`  means 'variable1' is mapped onto the x-axis
    - `aes(..., col = variable2)` means that 'variable2' is mapped onto a colour

Simply changing the colour of the dots, is NOT aesthetics
    - `ggplot(mtcars, aes(x = wt, y = mpg)) + geom_point(col="red")`
because there is no mapping
`aes()` includes: x-axis, y-axis, colour, fill, size, alpha, labels, line width, line type,...
Some aesthetics are only applicable to categorical variables: e.g., label and shape 


```r
p1 <- ggplot(mtcars, aes(x = wt, y = mpg, col = cyl)) +
      geom_point(shape = 1, size = 4)
p2 <- ggplot(mtcars, aes(x=mpg, y=qsec,size=(hp/wt), 
                         shape=factor(am), col=factor(cyl))) + 
      geom_point()

grid.arrange(p1, p2,  ncol=2)
```

![](MyR_files/figure-latex/unnamed-chunk-86-1.pdf)<!-- --> 

Attributes go to `geom_`

### Modifying aesthetics

Modifying aesthetics is modifying the mapping

`position` defaults to `identity`, `jitter` adds some random noise to the observations so that they do not overlap

```r

p1 <- ggplot(iris, aes(x=Sepal.Length, y=Sepal.Width, col=Species)) +
      geom_point()
p2 <- ggplot(iris, aes(x=Sepal.Length, y=Sepal.Width, col=Species)) +
      geom_point(position="jitter")

grid.arrange(p1, p2,  ncol=2)
```

![](MyR_files/figure-latex/unnamed-chunk-87-1.pdf)<!-- --> 

`scale_..._...(variable1, args)` modifies the scale of the mapping of 'variable1' with several arguments such as `limits`, `breaks`, etc...
Sometimes, you need to assign a dummy to the aesthetics, e.g., when you want to plot only one variable


```r
mtcars$mydummy <- 1
 
ggplot(mtcars, aes(x = mpg, y=mydummy, col=factor(cyl))) + 
geom_jitter() + 
scale_y_continuous(limits=c(-0,2)) + 
labs(title="My nice graph", x="Miles per gallon", y="", col="Cylindres")
```

![](MyR_files/figure-latex/unnamed-chunk-88-1.pdf)<!-- --> 

## Geometries

Geometries control how your plot is going to look like: currently, there are more than 37 gemoetries available
Common plots are: scatter, bar, line plots
Geometries required some aesthetics and can take other aesthetics as optional
Geometries can take their own aesthetics (useful to control mappings of each layer)
Geometries can take their own data, too!

### Scatter plots
We've seen a lot, already: recall `geom_point()`

### Bar plots
The simplest is a histogram

```r
p1 <- ggplot(iris, aes(x=Sepal.Length)) + geom_histogram()
p2 <- ggplot(iris, aes(x=Sepal.Length)) + 
      geom_histogram(binwidth = 1)
p3 <- ggplot(iris, aes(x=Sepal.Length, fill=Species)) +
      geom_histogram()
p4 <- ggplot(iris, aes(x=Sepal.Length, fill=Species)) +
      geom_histogram(position="dodge") # or "stack", or "fill"

grid.arrange(p1, p2, p3, p4,  ncol=2)
#R> `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
#R> `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
#R> `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

![](MyR_files/figure-latex/unnamed-chunk-89-1.pdf)<!-- --> 

A more general bar plot can be obtained with `geom_bar()`:


```r
data("mtcars")
mtcars$cyl <- as.factor(mtcars$cyl) # changing 'cyl' to factor, which is actually is 
mtcars$am <- as.factor(mtcars$am)
p1 <- ggplot(mtcars, aes(x=cyl, fill=am)) +
      geom_bar(position="stack")
p2 <- ggplot(mtcars, aes(x=cyl, fill=am)) +
      geom_bar(position="dodge") # or "stack", or "fill"

posn_d <- position_dodge(width=.2) # like for jitter
p3 <- ggplot(mtcars, aes(x=cyl, fill=am)) +
      geom_bar(position=posn_d, alpha=.6)

p4 <- ggplot(mtcars, aes(mpg, fill=cyl)) +
      geom_histogram(binwidth = 1, position="identity", alpha=.4)


grid.arrange(p1, p2, p3, p4,  ncol=2)
```

![](MyR_files/figure-latex/unnamed-chunk-90-1.pdf)<!-- --> 



```r
data <- data.frame(a=1:6, b=rep(1/6,6))

p1 <- ggplot(data, aes(x=a, y=b)) +
      geom_bar(position="stack", alpha = 0.7, stat = "identity") +
      labs(title = "Probability distribution of die roll", x = "Value on the die (x)", y = "P(x)") +
  scale_x_discrete(limits=1:6, labels=c("1", "2", "3", "4", "5", "6"))
      
p1
```

![](MyR_files/figure-latex/unnamed-chunk-91-1.pdf)<!-- --> 

### Line plots

Particularly suited for line plots over time

```r
p1 <- ggplot(economics, aes(x = date, y = unemploy)) + 
geom_line()

data("beavers")
p2 <- ggplot(beaver1, aes(x = time, y = temp, col=factor(activ))) + 
geom_line(aes(group=1)) # group = 1 indicates you want a single line connecting all the points, you can set group=variable

grid.arrange(p1, p2, ncol=2)
```

![](MyR_files/figure-latex/unnamed-chunk-92-1.pdf)<!-- --> 

<!--chapter:end:18-ggplot.Rmd-->

---
output:
  word_document: default
  html_document: default
---
# (PART) Use R for Data Science  {-}

After learning about the various functions of R and how they can be used in the previous two chapters, this chapter of the book focuses on how R can be and is used for data science. 

# Introduction to Data Science {#introduction}

In general, Data Science can be described as the overlap of computer science and IT, mathematics and statistics as well as domains and business knowledge. Data Science uses scientific methods, processes, algorithms and systems to extract knowledge. In this case, the focus lies on structured and unstructured data. It uses the above-mentioned methods to solve a variety of problems. It is of great importance to understand a set of data as well as to structure and analyze this data. 

One of the most efficient ways to conduct data science is the use of the programing language R. Due to the fact that many people study R programming during their academic years based on the fact that it is legally free available, R is a well-known tool for data science with many people having at least basic knowledge in the coding language. The huge amount of complex data that is usually processed in data science makes it difficult to structure and conduct data for further analysis. R therefore offers a number of packages that can be used to for reading various forms of data into R, which are explained in detail in the `tidyverse` chapter.

## Data Science = Artificial intelligence - Yes or No?

Artificial Intelligence can generally be seen as intelligence that is demonstrated by machines. Machine learning as part of artificial intelligence enables IT systems to recognize patterns and laws on the basis of existing data and algorithms and to develop solutions.

Additionally, R offers the opportunity to train the algorithm and therefore offers the opportunity to bring in automation for future predictions. R makes machine learning a lot easier and more approachable with the number of packages available especially for machine learning. In conclusion, due to the fact that data science uses statistical learning algorithms such as machine learning, data science can be seen as artificial intelligence. The fact that, broadly speaking, machine learning connects data science and AI, leads to the conclusion that data science and AI can complement each other perfectly. 

## R for Data Data Science

In this chapter of the book, we will discuss data science in the form of conditions, subsets, vectorized functions, plots, loops, functions and many other forms. 

<!--chapter:end:19-introductionDS.Rmd-->

# (PART) Use R for Data Science {-}

# Simple functions and operations on vectors 

This section gives simple calculations and examples for using vectors and their syntax in R language. The practical examples should help to achieve a general understanding.  


## Element by element evaluation

An important characteristic in relation to vectors is the use of functions. Each element of the vector is considered separately, evaluated and viewed in the sequence defined, also called **element by element**. 

The following example illustrates this evaluation and emphasizes the effect on the length of the vectors.

```r
# Creation of two numeric vector of same length (you can choose a random name)
shares1 <-  c(16, 23, 34, 32, 96, 22, 6)
shares2 <- c(11, 33, 2, 8, 36, 4, 69)
length(shares1)
#R> [1] 7
length(shares1) == length(shares2)
#R> [1] TRUE

total <- shares1 + shares1
# the sum of the vectors of the same length, with the element by element sums

length(total)
#R> [1] 7
total
#R> [1]  32  46  68  64 192  44  12
```

Another simple calculation with the function `^2`.



```r
total.p2 <- total^2
total.p2
#R> [1]  1024  2116  4624  4096 36864  1936   144

(trop <- total - 2)
#R> [1]  30  44  66  62 190  42  10
length(trop)
#R> [1] 7
```

You also can run this with other functions respective exponents.



```r
total.p2 <- total^3
total.p2
#R> [1]   32768   97336  314432  262144 7077888   85184    1728

(trop <- total - 3)
#R> [1]  29  43  65  61 189  41   9
length(trop)
#R> [1] 7
```

## Recycling rule


Now that we have examined functions in interaction with vectors of the same length, the question arises what happens if the selected vectors have a different length. What's important: the shortest vector has its elements **recycled** as much as it is necessary.


```r
l6 <- c(12, 34, 50, 8, 16, 15)
l4 <- c(10, 3, 13, 9)
tt <- l6 + 7
tt
#R> [1] 19 41 57 15 23 22

ltotal <- l6+l4 # recycling takes place!
#R> Warning in l6 + l4: longer object length is not a multiple of shorter
#R> object length
ltotal
#R> [1] 22 37 63 17 26 18
```


## Functions for the whole vector

Functions do not necessarily have to refer to vectors of different or equal length. With R various operations on vectors can be made.
Here are a few simple examples to illustrate this:


```r
coins <- c(36, 73, 16, 98, 22, 23, 87, 19, 12)
coins
#R> [1] 36 73 16 98 22 23 87 19 12
max(coins)
#R> [1] 98
length(coins)
#R> [1] 9
sum(coins)
#R> [1] 386
var(coins)
#R> [1] 1127.111

coins <- c(36, 73, 16, 98, 22, 23, 87, 19, 12)
mean(coins)
#R> [1] 42.88889

# for help on a command, simply type ? in front 
# of unknown command to search for explanation
?var
```

<!--chapter:end:20-vectorized_functions.Rmd-->

# Subsetting {#subset}

Subsetting means to create a data set out of the existing data structure.
In R the command “subset” is used to filter the data in a data frame based on the criteria you set. 


There are three operators that can be used to extract subsets of R objects:

The [ operator always returns an object of the same class as the original. It can be used to select multiple elements of an object

The [[ operator is used to extract elements of a list or a data frame. It can only be used to extract a single element and the class of the returned object will not necessarily be a list or data frame.

The $ operator is used to extract elements of a list or data frame by literal name. Its semantics are similar to that of [[.
 

Sub-setting is better used in complement with `str()`.

```r
va <- c(11, -19, 0.8, 0.9, 0.5, -1.3, 11.7) # create the vector va
str(va)
#R>  num [1:7] 11 -19 0.8 0.9 0.5 -1.3 11.7
str(mtcars)
#R> 'data.frame':	32 obs. of  11 variables:
#R>  $ mpg : num  21 21 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2 ...
#R>  $ cyl : Factor w/ 3 levels "4","6","8": 2 2 1 2 3 2 3 1 1 2 ...
#R>  $ disp: num  160 160 108 258 360 ...
#R>  $ hp  : num  110 110 93 110 175 105 245 62 95 123 ...
#R>  $ drat: num  3.9 3.9 3.85 3.08 3.15 2.76 3.21 3.69 3.92 3.92 ...
#R>  $ wt  : num  2.62 2.88 2.32 3.21 3.44 ...
#R>  $ qsec: num  16.5 17 18.6 19.4 17 ...
#R>  $ vs  : num  0 0 1 1 0 1 0 1 1 1 ...
#R>  $ am  : Factor w/ 2 levels "0","1": 2 2 2 1 1 1 1 1 1 1 ...
#R>  $ gear: num  4 4 4 3 3 3 3 4 4 4 ...
#R>  $ carb: num  4 4 1 1 2 1 4 2 2 4 ...
```

You can see from this call, that `va` is a simple vector with 7 elements. Subsetting means choosing among these.

## `[]`
Applies to vectors, matrices, lists and data frames.  
Can be used with:

    - positive or negative values,
    - many values in a vector,
    - logical, `NA`,
    - character vectors when names exist.

### On a vector

Vectors are basic objects in R and they can be subsetted using the [ operator.
Here are a few examples of that object used on a vector.


```r
va <- c(11, -19, 0.8, 0.9, 0.5, -1.3, 11.7)
va[1] # extract the first element
#R> [1] 11
va[c(3:5)] # elements 3 to 5
#R> [1] 0.8 0.9 0.5
va[c(2,7)] #elements 2 and 7 
#R> [1] -19.0  11.7
va[-3] # extract all elements minus the element 3
#R> [1]  11.0 -19.0   0.9   0.5  -1.3  11.7
va[c(-5,-4)]
#R> [1]  11.0 -19.0   0.8  -1.3  11.7
va[c(-5,-4)]
#R> [1]  11.0 -19.0   0.8  -1.3  11.7
va[c(TRUE,TRUE,TRUE,FALSE,FALSE,TRUE,FALSE)] 
#R> [1]  11.0 -19.0   0.8  -1.3
va[c(TRUE,FALSE)] # notice the recycling at play here
#R> [1] 11.0  0.8  0.5 11.7
va[NA] 
#R> [1] NA NA NA NA NA NA NA
va[] # nothing selected gives the full vector
#R> [1]  11.0 -19.0   0.8   0.9   0.5  -1.3  11.7
names(va)<-letters[1:length(va)] # give names to va
# notice that we subset the vector letters (given by R) and that we don't
# specify the length but give a general value
# now we can subset using names
va
#R>     a     b     c     d     e     f     g 
#R>  11.0 -19.0   0.8   0.9   0.5  -1.3  11.7
va[c("a","e","b")]
#R>     a     e     b 
#R>  11.0   0.5 -19.0
```

### On a list

Lists in R can be subsetted using all three of the operators mentioned above, and all three are used for different purposes.


```r
x <- list(foo = 1:4, bar = 0.6)
x$foo[1] #2,3,4
#R> [1] 1

x$bar[1] 
#R> [1] 0.6
```

The [[ operator can be used to extract single elements from a list. Here we extract the first element of the list:


```r
x[[1]]
#R> [1] 1 2 3 4
```

Another list example to illurstrate:


```r
mylist<- list(numbers=c(1:20), 
              ournames=c("Jim","Jules"), 
              results= c(T,F,F,T), 
              school=factor(c("Primary", "Secondary", "Tertiary"), ordered=TRUE))
str(mylist)
#R> List of 4
#R>  $ numbers : int [1:20] 1 2 3 4 5 6 7 8 9 10 ...
#R>  $ ournames: chr [1:2] "Jim" "Jules"
#R>  $ results : logi [1:4] TRUE FALSE FALSE TRUE
#R>  $ school  : Ord.factor w/ 3 levels "Primary"<"Secondary"<..: 1 2 3

mylist[1] # first element of the list
#R> $numbers
#R>  [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
class(mylist[1])
#R> [1] "list"
mylist[[3]][3]
#R> [1] FALSE
```
Notice that the result of this subsetting is a list!

### On a matrix


```r
set.seed(42)
my.mat <- matrix(floor(runif(30)*10), nrow=5)
my.mat
#R>      [,1] [,2] [,3] [,4] [,5] [,6]
#R> [1,]    9    5    4    9    9    5
#R> [2,]    9    7    7    9    1    3
#R> [3,]    2    1    9    1    9    9
#R> [4,]    8    6    2    4    9    4
#R> [5,]    6    7    4    5    0    8
str(my.mat)
#R>  num [1:5, 1:6] 9 9 2 8 6 5 7 1 6 7 ...
length(my.mat)
#R> [1] 30
```
The structure shows that there are r length(dim(my.mat)) dimensions. For subsetting, we must give r length(dim(my.mat)) dimensions! Same rules as for the vectors apply.


```r
# 2nd row, 3rd column
my.mat[2,3] 
#R> [1] 7
# all but first row, all columns
my.mat[-1,]
#R>      [,1] [,2] [,3] [,4] [,5] [,6]
#R> [1,]    9    7    7    9    1    3
#R> [2,]    2    1    9    1    9    9
#R> [3,]    8    6    2    4    9    4
#R> [4,]    6    7    4    5    0    8
colnames(my.mat) <- letters[1:ncol(my.mat)] # give names to the columns
rownames(my.mat) <- LETTERS[1:nrow(my.mat)] # give names to the rows
my.mat
#R>   a b c d e f
#R> A 9 5 4 9 9 5
#R> B 9 7 7 9 1 3
#R> C 2 1 9 1 9 9
#R> D 8 6 2 4 9 4
#R> E 6 7 4 5 0 8
my.mat["C",c("a","c","e")]
#R> a c e 
#R> 2 9 9
```

## `[[]]`
This object is used mainly for lists.


```r
mylist<- list(numbers=c(1:20), 
              ournames=c("Jim","Jules"), 
              results= c(T,F,F,T), 
              school=factor(c("Primary", "Secondary", "Tertiary"), ordered=TRUE))
str(mylist)
#R> List of 4
#R>  $ numbers : int [1:20] 1 2 3 4 5 6 7 8 9 10 ...
#R>  $ ournames: chr [1:2] "Jim" "Jules"
#R>  $ results : logi [1:4] TRUE FALSE FALSE TRUE
#R>  $ school  : Ord.factor w/ 3 levels "Primary"<"Secondary"<..: 1 2 3
mylist[[1]]
#R>  [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
```


## `$`
This object is usually for data frames, where it gives the variable.  
It allows partial matching (e.g., `mtcars$gear` is the same as `mtcars$gea`)


```r
data(mtcars)
mtcars
#R>                      mpg cyl  disp  hp drat    wt  qsec vs am gear carb
#R> Mazda RX4           21.0   6 160.0 110 3.90 2.620 16.46  0  1    4    4
#R> Mazda RX4 Wag       21.0   6 160.0 110 3.90 2.875 17.02  0  1    4    4
#R> Datsun 710          22.8   4 108.0  93 3.85 2.320 18.61  1  1    4    1
#R> Hornet 4 Drive      21.4   6 258.0 110 3.08 3.215 19.44  1  0    3    1
#R> Hornet Sportabout   18.7   8 360.0 175 3.15 3.440 17.02  0  0    3    2
#R> Valiant             18.1   6 225.0 105 2.76 3.460 20.22  1  0    3    1
#R> Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
#R> Merc 240D           24.4   4 146.7  62 3.69 3.190 20.00  1  0    4    2
#R> Merc 230            22.8   4 140.8  95 3.92 3.150 22.90  1  0    4    2
#R> Merc 280            19.2   6 167.6 123 3.92 3.440 18.30  1  0    4    4
#R> Merc 280C           17.8   6 167.6 123 3.92 3.440 18.90  1  0    4    4
#R> Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
#R> Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
#R> Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
#R> Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
#R> Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
#R> Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
#R> Fiat 128            32.4   4  78.7  66 4.08 2.200 19.47  1  1    4    1
#R> Honda Civic         30.4   4  75.7  52 4.93 1.615 18.52  1  1    4    2
#R> Toyota Corolla      33.9   4  71.1  65 4.22 1.835 19.90  1  1    4    1
#R> Toyota Corona       21.5   4 120.1  97 3.70 2.465 20.01  1  0    3    1
#R> Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
#R> AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
#R> Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
#R> Pontiac Firebird    19.2   8 400.0 175 3.08 3.845 17.05  0  0    3    2
#R> Fiat X1-9           27.3   4  79.0  66 4.08 1.935 18.90  1  1    4    1
#R> Porsche 914-2       26.0   4 120.3  91 4.43 2.140 16.70  0  1    5    2
#R> Lotus Europa        30.4   4  95.1 113 3.77 1.513 16.90  1  1    5    2
#R> Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
#R> Ferrari Dino        19.7   6 145.0 175 3.62 2.770 15.50  0  1    5    6
#R> Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8
#R> Volvo 142E          21.4   4 121.0 109 4.11 2.780 18.60  1  1    4    2
mtcars[1:5, 4]
#R> [1] 110 110  93 110 175
aa <- mtcars[1:5, c("cyl","hp")]
class(aa)
#R> [1] "data.frame"
aa
#R>                   cyl  hp
#R> Mazda RX4           6 110
#R> Mazda RX4 Wag       6 110
#R> Datsun 710          4  93
#R> Hornet 4 Drive      6 110
#R> Hornet Sportabout   8 175

names(mtcars)
#R>  [1] "mpg"  "cyl"  "disp" "hp"   "drat" "wt"   "qsec" "vs"   "am"   "gear"
#R> [11] "carb"
mtcars$hp[1:5]
#R> [1] 110 110  93 110 175

mtcars[["mpg"]] # just exactly the same, but R users prefer the $
#R>  [1] 21.0 21.0 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2 17.8 16.4 17.3 15.2
#R> [15] 10.4 10.4 14.7 32.4 30.4 33.9 21.5 15.5 15.2 13.3 19.2 27.3 26.0 30.4
#R> [29] 15.8 19.7 15.0 21.4
mtcars["mpg"] # NOT the same at all! [] preserves the class
#R>                      mpg
#R> Mazda RX4           21.0
#R> Mazda RX4 Wag       21.0
#R> Datsun 710          22.8
#R> Hornet 4 Drive      21.4
#R> Hornet Sportabout   18.7
#R> Valiant             18.1
#R> Duster 360          14.3
#R> Merc 240D           24.4
#R> Merc 230            22.8
#R> Merc 280            19.2
#R> Merc 280C           17.8
#R> Merc 450SE          16.4
#R> Merc 450SL          17.3
#R> Merc 450SLC         15.2
#R> Cadillac Fleetwood  10.4
#R> Lincoln Continental 10.4
#R> Chrysler Imperial   14.7
#R> Fiat 128            32.4
#R> Honda Civic         30.4
#R> Toyota Corolla      33.9
#R> Toyota Corona       21.5
#R> Dodge Challenger    15.5
#R> AMC Javelin         15.2
#R> Camaro Z28          13.3
#R> Pontiac Firebird    19.2
#R> Fiat X1-9           27.3
#R> Porsche 914-2       26.0
#R> Lotus Europa        30.4
#R> Ford Pantera L      15.8
#R> Ferrari Dino        19.7
#R> Maserati Bora       15.0
#R> Volvo 142E          21.4
class(mtcars["mpg"])
#R> [1] "data.frame"
```

## Combining subsetting
Notice that we can often subset further until having the desired subset. Here are a few examples.

```r
mtcars$mpg[1:4]
#R> [1] 21.0 21.0 22.8 21.4
mylist[["ournames"]][1]
#R> [1] "Jim"
mylist$ournames[1]
#R> [1] "Jim"
```



## Subsetting  with one condition
We can use conditions for subsetting

```r
mtcars[mtcars$mpg<=20, ]
#R>                      mpg cyl  disp  hp drat    wt  qsec vs am gear carb
#R> Hornet Sportabout   18.7   8 360.0 175 3.15 3.440 17.02  0  0    3    2
#R> Valiant             18.1   6 225.0 105 2.76 3.460 20.22  1  0    3    1
#R> Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
#R> Merc 280            19.2   6 167.6 123 3.92 3.440 18.30  1  0    4    4
#R> Merc 280C           17.8   6 167.6 123 3.92 3.440 18.90  1  0    4    4
#R> Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
#R> Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
#R> Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
#R> Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
#R> Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
#R> Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
#R> Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
#R> AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
#R> Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
#R> Pontiac Firebird    19.2   8 400.0 175 3.08 3.845 17.05  0  0    3    2
#R> Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
#R> Ferrari Dino        19.7   6 145.0 175 3.62 2.770 15.50  0  1    5    6
#R> Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8
mtcars[mtcars$cyl==8,]
#R>                      mpg cyl  disp  hp drat    wt  qsec vs am gear carb
#R> Hornet Sportabout   18.7   8 360.0 175 3.15 3.440 17.02  0  0    3    2
#R> Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
#R> Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
#R> Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
#R> Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
#R> Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
#R> Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
#R> Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
#R> Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
#R> AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
#R> Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
#R> Pontiac Firebird    19.2   8 400.0 175 3.08 3.845 17.05  0  0    3    2
#R> Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
#R> Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8
mtcars[mtcars$cyl==8 & mtcars$carb==4,]
#R>                      mpg cyl disp  hp drat    wt  qsec vs am gear carb
#R> Duster 360          14.3   8  360 245 3.21 3.570 15.84  0  0    3    4
#R> Cadillac Fleetwood  10.4   8  472 205 2.93 5.250 17.98  0  0    3    4
#R> Lincoln Continental 10.4   8  460 215 3.00 5.424 17.82  0  0    3    4
#R> Chrysler Imperial   14.7   8  440 230 3.23 5.345 17.42  0  0    3    4
#R> Camaro Z28          13.3   8  350 245 3.73 3.840 15.41  0  0    3    4
#R> Ford Pantera L      15.8   8  351 264 4.22 3.170 14.50  0  1    5    4
mtcars[mtcars$cyl==8, c("cyl", "mpg", "wt")]
#R>                     cyl  mpg    wt
#R> Hornet Sportabout     8 18.7 3.440
#R> Duster 360            8 14.3 3.570
#R> Merc 450SE            8 16.4 4.070
#R> Merc 450SL            8 17.3 3.730
#R> Merc 450SLC           8 15.2 3.780
#R> Cadillac Fleetwood    8 10.4 5.250
#R> Lincoln Continental   8 10.4 5.424
#R> Chrysler Imperial     8 14.7 5.345
#R> Dodge Challenger      8 15.5 3.520
#R> AMC Javelin           8 15.2 3.435
#R> Camaro Z28            8 13.3 3.840
#R> Pontiac Firebird      8 19.2 3.845
#R> Ford Pantera L        8 15.8 3.170
#R> Maserati Bora         8 15.0 3.570
```

## Subsetting and assignment
Subsetting can be used to change a part of an object through assignment.  Assign `NULL` to delete subset

```r
my.mat
#R>   a b c d e f
#R> A 9 5 4 9 9 5
#R> B 9 7 7 9 1 3
#R> C 2 1 9 1 9 9
#R> D 8 6 2 4 9 4
#R> E 6 7 4 5 0 8
my.mat[,1]<-1:nrow(my.mat)
my.mat
#R>   a b c d e f
#R> A 1 5 4 9 9 5
#R> B 2 7 7 9 1 3
#R> C 3 1 9 1 9 9
#R> D 4 6 2 4 9 4
#R> E 5 7 4 5 0 8
mtcars$mpg[1]<-1234
names(mtcars)
#R>  [1] "mpg"  "cyl"  "disp" "hp"   "drat" "wt"   "qsec" "vs"   "am"   "gear"
#R> [11] "carb"
mtcars$drat<-NULL # delete variable drat in data frame mtcars
# does not delete in matrix
names(mtcars)
#R>  [1] "mpg"  "cyl"  "disp" "hp"   "wt"   "qsec" "vs"   "am"   "gear" "carb"
```



## Using `which()`
`which()` gives the integers that correspond to the boolean (logical) `TRUE`.  
This can help subsetting

```r
vb<-1500:1530
vb
#R>  [1] 1500 1501 1502 1503 1504 1505 1506 1507 1508 1509 1510 1511 1512 1513
#R> [15] 1514 1515 1516 1517 1518 1519 1520 1521 1522 1523 1524 1525 1526 1527
#R> [29] 1528 1529 1530
which(vb%%5==0) # which is divisible by 5 (modulo is 0) ?
#R> [1]  1  6 11 16 21 26 31
# notice that this is asking each element of vb, 
# which() reports the positions for which the answer is TRUE 
vb[which(vb%%5==0)] 
#R> [1] 1500 1505 1510 1515 1520 1525 1530
```

## More advanced stuff

### Difference between simplifying and preserving
We say 'preserve' to say the same structure is maintained when subsetting (e.g., a subset of a data frame remains a data frame).  
Simplifying does not keep the structure but gives the simplest output possible.  
`drop` argument allows to preserve (`drop=FALSE`) or not (`drop= TRUE`).  
`[]` usually preserves, `[[]]` usually simplifies.  
To better understand, check the classes:

```r
all.equal(class(mylist[1]), class(mylist[[1]]))
#R> [1] "1 string mismatch"
class(mylist[1])
#R> [1] "list"
class(mylist[[1]])
#R> [1] "integer"
all.equal(class(mylist), class(mylist[1]))
#R> [1] TRUE
all.equal(class(mylist), class(mylist[[1]]))
#R> [1] "1 string mismatch"
```

We see that `[]` has preserved the class of `mylist` (r class(mylist)), while `[[]]` has not! 
Another striking example is the following.

```r
ma2 <- my.mat[1:2,1:3]
class(ma2)
#R> [1] "matrix"
ma3 <- my.mat[1,1:3]
class(ma3)
#R> [1] "numeric"
```
`ma3` is NOT a matrix anymore!!! This is because one of its dimensions is 1.
Losing track of the class when subsetting can generate lots of problems in the middle of a large code. And it is a common source of error!
To be sure of keeping the class, we can use `drop=FALSE` (the class will not be dropped to, usually, a vector).

```r
ma4 <- my.mat[1,1:3, drop=FALSE]
ma4
#R>   a b c
#R> A 1 5 4
class(ma4)
#R> [1] "matrix"
```


<!--chapter:end:21-subset.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# Conditions {#conditions}

The general intention and reason for conditions is to control the flow of the calculation and output when executed by R.  
With R language you can choose between a variety of conditions, but most common are `if` and `else`.

## `if` statement
The most simple conditions uses a `if` statement.  
The form is then:

```r 
if (the definded condition) {
# code to be executed if the condition is TRUE
}
```

It is important to point out here that R executes the code until a condition is identified, otherwise R runs through the next line in the chunk.

Here is a simple example uses this condition:

```r
losses <- c(13, 5, -60, 0, -7, 24, 8)
losses
#R> [1]  13   5 -60   0  -7  24   8
sum(losses)
#R> [1] -17

if (sum(losses) < 0) {
  print("Biggest looser in town")
}
#R> [1] "Biggest looser in town"

# change the -60 in 'losses' to -6

losses[losses==-60] <- -6
losses
#R> [1] 13  5 -6  0 -7 24  8

if (sum(losses) < 0) {
  print("Biggest looser in town")
} # remember that there is no print or output, because the defined condition was not met
```

## `else` statement

What can be the case if the condition was not met? It can be no output or... something else!
It is up to you to decide what you want to do in this situation if the first condition is not met!

```r
if (condition) { 
# code to be executed if the condition is TRUE
} else {
# code to be executed if the condition FALSE
}
```

To illustrate:


```r
#we take the same example as above
losses<- c(13, 5, -60, 0, -7, 24, 8)
losses[4] <- 50 # change the fourth element of losses
sum(losses)
#R> [1] 33

if (sum(losses) < 0) {
  print("Biggest looser in town")
} else {
  print("Lucky Cowboy")
} # notice that now there is an output!
#R> [1] "Lucky Cowboy"
```

## `else if` statement

`else if` allows to work with another condition additional to the current flow of code above

```r
if (condition_1) { 
# code to be executed if the condition_1 is TRUE
} else if (condition_2) {
# code to be executed if the condition_2 is TRUE
} else {
# code to be executed if NEITHER condition_1 NOR condition_2 is TRUE
}
```

There is no limitation in `else if` statements. Many multiple conditions are possible  
Here is an example with only one `else if`

```r
losses <- c(13, 5, -60, 0, -7, 24, 8)
losses[3] <- 25 # change the third element of 'losses'
sum(losses)
#R> [1] 68

losses <- c(13, 5, -60, 0, -7, 24, 8)
losses[6] <- 41 # another one
sum(losses)
#R> [1] 0

if (sum(losses) < 0) {
  print("Biggest looser in town")
} else if (sum(losses)==0) {
  print("No looser, but no champion at all")
} else {
  print("Lucky Cowboy")
}
#R> [1] "No looser, but no champion at all"
```

Pay attention the potential problem of not putting an  `else` statement at the end of the conditions system.

## `ifelse` statement

When using **shorter** conditions, we can use `ifelse` statements.  
Here is how the code looks like:

```r
ifelse(condition, value if condition met, value if value not met)
```
Now back to our real example:


```r
losses <- c(13, 5, -60, 0, -7, 24, 8)
sign <- ifelse(sum(losses)>=0,"+","-")
sign
#R> [1] "-"

?sign #sign returns a vector with the signs of the corresponding elements of x (the sign of a real number is 1, 0, or -1 if the number is positive, zero, or negative, respectively)
```

## Logical operators: `&`, `|` and `!`
Logical operators are used to combine, mix or negate several conditions:
- `&` means AND
- `|` means OR
- `!` means NOT

In Boolean algebra, there are two transformation rules named after the British mathematician Augustus De Morgan. These rules state that:

1. The complement of the union of two sets is the intersection of their complements.
2. The complement of the intersection of two sets is the union of their complements.

De Morgan's laws may help here.


```r
(27%%2==0 & 27%%3==0) # equivalent to (TRUE and TRUE), hence TRUE
#R> [1] FALSE
TRUE & FALSE
#R> [1] FALSE
!TRUE 
#R> [1] FALSE
!(TRUE & TRUE)
#R> [1] FALSE
!(TRUE & !TRUE)
#R> [1] TRUE
((27%%2==0 & 27%%2==0)) # equivalent to (TRUE and FALSE), hence FALSE
#R> [1] FALSE
((27%%2==0 | 27%%2==0)) # equivalent to (TRUE or FALSE), hence TRUE
#R> [1] FALSE
```


## Writing and interpreting a condition

It must be considered that R searches either a TRUE or a FALSE in a condition.  
When R encounters a TRUE, it executes the desired command, otherwise it does not.  
There are many ways to get one of these two logics, since each of these ways will work as a condition.

Here are examples of less common ways to write a condition:

```r
losses<- c(13, 5, -60, 0, -7, 24, 8)

if (is.numeric(losses)) {
  print("Wow a wild numeric vector...")
}
#R> [1] "Wow a wild numeric vector..."
# here, is.numeric(losses) evaluates to TRUE, hence, the code is executed!
# the beginner's way would be to replace the condition by
# if (class(losses)=="numeric")

if (!is.factor(losses)) {
  print("No factor no portuguese friday...")
}
#R> [1] "No factor no portuguese friday..."
# the amateur would write if (class(losses)!="factor")
```


<!--chapter:end:22-conditions.Rmd-->

# Functions {#functions}

Every operation in R language is a function call.
To understand computations in R, two slogans are helpful:

Everything that exists is an object.
Everything that happens is a function call.
— John Chambers

Functions are the necessary prerequisite for R to be able to execute certain commands or calculations. There are predefined functions in certain packages, but this chapter focuses on functions that have to be created itself in code form, because most new users of R have problems with this.

A function is itself an object. When applied to another object, the function "makes something" to that object and returns an object. The notion of a function is easily understood using the metaphor of a ***function machine*** that takes in an object for its input and, based on that input, spits out another object as its output.

## Structure of a simple function

Here is a simple example of a function that returns the square of the object provided.


```r
pow_two <- function(a){
  a^2
}
pow_two(12)
#R> [1] 144
```



### Name of the function
In the example above, the name of the function was `pow_two`. If you want to use the function later in the code, type `pow_two()`. Than you are possible to apply the function to specific inputs to create the desired output.

### Arguments

The arguments are given in the parentheses right after `function`.  
Arguments in the parentheses can be any object, e.g., a vector as in the example below:

```r
pow_two(1:25)
#R>  [1]   1   4   9  16  25  36  49  64  81 100 121 144 169 196 225 256 289
#R> [18] 324 361 400 441 484 529 576 625
#every value of the vector in the parentheses is squared through function `pow_two`
```
When using this function, we can see that one argument only must be passed.  
A value for the argument is then given in the parentheses when calling the function, e.g., `pow_two(12)`.  
A function can have several arguments

### Commands
The commands will only be run by R, if possible.  
One command source of error is when the class of the argument provided is NOT compatible with the commands in the function


```r
pow_two("Debiasing") # this can't work, because the argument is not compatible
#R> Error in a^2: non-numeric argument to binary operator
```


### Return of a function

The return of a function is given by the last expression executed inside the function.


```r
best_f <- function(a){
  a^2
  a^4 # this is the last expression, so R calculated the return as 6^4
  }
best_f(6)
#R> [1] 1296
```

We can use `return()` in the function in order to chose what it  returns.


```r
best_f2 <- function(a){
  return(a^2) #here you show R that you want to define the return with the first expression
  a^4
}
best_f2(6) #in contrast to best_f R calculated the outcome with 6^2
#R> [1] 36
```

A function can return only one object, but you can always use a `list()` where you include your expressions and have the function return the list.

A simple example to illustrate:

```r
best_f3 <- function(a){
  list(ptwo=a^2, pthree=a^3, pfour=a^4) 
}
best_f3(1:30)
#R> $ptwo
#R>  [1]   1   4   9  16  25  36  49  64  81 100 121 144 169 196 225 256 289
#R> [18] 324 361 400 441 484 529 576 625 676 729 784 841 900
#R> 
#R> $pthree
#R>  [1]     1     8    27    64   125   216   343   512   729  1000  1331
#R> [12]  1728  2197  2744  3375  4096  4913  5832  6859  8000  9261 10648
#R> [23] 12167 13824 15625 17576 19683 21952 24389 27000
#R> 
#R> $pfour
#R>  [1]      1     16     81    256    625   1296   2401   4096   6561  10000
#R> [11]  14641  20736  28561  38416  50625  65536  83521 104976 130321 160000
#R> [21] 194481 234256 279841 331776 390625 456976 531441 614656 707281 810000
```

If you want to use a specific return of the function you have to assign it to an object.

In this example a vector is used to show five values of the return, because a vector of lenght six is used:

```r
x <- best_f3(1:6) # evaluates the function above on the vector 1:6
x$pthree # shows the element pthree of the saved list x
#R> [1]   1   8  27  64 125 216
```

An example with return and conditions respective `else` statement:


```r
pow_three <- function(a){
  if (!is.numeric(a)) {
    return(print("Numeric Vectors rules!"))
  } else {
    return(a^4)
  }
  
}
pow_three(1:5)
#R> [1]   1  16  81 256 625
```



## Multiple arguments and their identification


```r
m_pow <- function(a, p){
  a^p
}
m_pow(8, 0.5)
#R> [1] 2.828427
```


As mentioned above, a function can have several arguments, but you have to be careful, you need the enough arguments in this case below:


```r
best_f4 <- function(abc, xyz){
  c(abc^4, xyz^2)
}
best_f4(3) # this won't work because xyz is missing (missing argument)
#R> Error in best_f4(3): argument "xyz" is missing, with no default
best_f4(5, 10)
#R> [1] 625 100
```

R has at least two ways of identifying arguments, by position and by name.  
If no name is specified, R uses the arguments according to their positions in the definition of the function.  
In the example above, R understands that `abc=5` and `xyz=10` because of the way they are given in the call `best_f4(5, 10)`.  
Identification by names would be

```r
best_f4(5, 10)
#R> [1] 625 100
best_f4(abc=5, xyz=10) # same as before
#R> [1] 625 100
best_f4(xyz=5, abc=10) 
#R> [1] 10000    25
# different from before because the names are more important than the position
best_f4(xyz=5, 10) # a mix between name and position 
#R> [1] 10000    25
```

### Default values

A function can be defined with default values for their arguments.  
R will use the values provided in the call; if one is missing, R will use the default value.


```r

best_f4 <- function(abc, xyz=2){
  c(abc^3, xyz^4)
}
best_f4(5) 
#R> [1] 125  16

best_f5 <- function(a, tada){
  if (tada==TRUE){
    plot(a)
  } else {
    sum(a)
  }
}


best_f5(5:28, tada=FALSE)
#R> [1] 396

best_f6 <- function(a, tada=TRUE){
  if (tada==TRUE){
    plot(a)
  } else {
    sum(a)
  }
}

best_f6(1:3, tada=FALSE)
#R> [1] 6
```













<!--chapter:end:23-functions.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# Loops (avoid them) {#loops}



## Introduction to loops with two examples

Whenever you learn about R (e.g in a book or tutorial), the advice given on loops is always:

1. Learn about and try to get a clear understanding of loops, due to the fact that they provide you with an understanding of the data that you’re manipulating.

2. After you have managed to get a clear understanding of loops, get rid of them or try to avoid them whilst using R for data science.

According to the R base manual, among the control flow commands, the loop constructs are:
- for
- while
- repeat
- break (additional clause)
- next (additional clause)

Loops allow to iterate a set of functions / lines of code over a predefined list of elements.  
They are common in many languages but are not highly regarded in R because:

  - they do not represent an efficient way of producing a result,
  - functionals, functions that return a vector such as the `apply` family, are preferred.
    
This section serves as a short introduction to the functionals because it helps understand the structure of the problem (Given by two examples):  

## A silly example of loops (Bad R Coding)

Suppose our gains at a game over the week are, in euros:

```r
gains <- c(5, 2,-10,0,-2,15,1)
gains
#R> [1]   5   2 -10   0  -2  15   1
```

Now, suppose we want to transform each gain into dollars, i.e., we must multiply each gain by 1.30. An intuitive way would be to take each gain _separately_ and multiply it 1.12. Let's do it by hand:


```r
gains_d <-numeric(length(gains)) # create a numeric vector of same length as gains
gains_d[1] <- gains[1]*1.12 
gains_d[2] <- gains[2]*1.12
gains_d[3] <- gains[3]*1.12
gains_d[4] <- gains[4]*1.12
gains_d[5] <- gains[5]*1.12
gains_d[6] <- gains[6]*1.12
gains_d[7] <- gains[7]*1.12
gains_d
#R> [1]   5.60   2.24 -11.20   0.00  -2.24  16.80   1.12
```

We recognize that the structure of each line of code: the first line is for the element 1 of the vectors, the second line for the second element of the vectors, etc.  
Doing a loop builds on that observation. But it asks the program to make the change between each line automatically.  
In the silly example, we want the program to evaluate a line with the value 1 and then, when it has finished, do the same line but with a 2 instead of a 1. And we want it to do it **for** the elements 1, 2, 3, 4, ..., 7.  
This is what a loop does!



```r
# create an empty numeric vector of same length as gains
gains_d2 <-numeric(length(gains)) 

# now the loop
# first for i=1, then i=2, then i=3, etc... until i=length(gains)
for (i in 1:length(gains)) {  
  gains_d2[i] <- gains[i]*1.12 
}
gains_d2
#R> [1]   5.60   2.24 -11.20   0.00  -2.24  16.80   1.12
```


## A good example of a loop

Suppose we want to know, every day, what is our cumulative gain until and including that day. This implies that we must to create another `cumulative_gains` with the same length as `gains`. 

Then, we could run the following loop.

```r
# create an empty vector
cumulative_gains <-numeric(length(gains)) 

cumulative_gains[1] <- gains[1]  
 
for (k in 2:length(gains)){
  cumulative_gains[k]<-cumulative_gains[k-1] + gains[k]
}
gains
#R> [1]   5   2 -10   0  -2  15   1
cumulative_gains
#R> [1]  5  7 -3 -3 -5 10 11
```


<!--chapter:end:24-loops.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# Simple plots {#splots}

The following chapter is an introduction for producing simple graphs with the R Programming Language. The package `ggplot2` described in Chapter \@ref(ggplot2) allows to make much richer and elegant plots. For every plot explained, an example will be given. In this chapter, we will only focus on line plots, bar graphs, and histograms (other examples such as boxplots, pie charts or dotcharts are only mentioned and not explained with own examples).

## Line plots

The simplest plot is a scatter plot of one variable plotted against an index (1, 2, 3, ...) on the horizontal axis.  
In order to (scatter) plot one vector against the other, it is compulsory that they are both numeric and have the same length.  
The following plots illustrate the creation of a line plot in incremental steps. In the steps, the following functions and arguments are introduced:  

- `plot` is the main function for the plot.




- `type` argument type gives how the vector should be rendered in the plot; the `type` of the plot is any of Table \@ref(tab:table-p-types). 


\begin{table}[t]

\caption{(\#tab:table-p-types)Plot types.}
\centering
\begin{tabular}{l|l}
\hline
Symbol & Description\\
\hline
p & Points\\
\hline
l & Lines\\
\hline
b & Both\\
\hline
c & The lines part alone of b\\
\hline
o & Both overplotted\\
\hline
s & Steps\\
\hline
h & Histogram like (vertical lines)\\
\hline
n & No plotting\\
\hline
\end{tabular}
\end{table}
  
Example 1:


```r
sales <- c(20, 18, 24, 36, 30)
date <- c(15, 16, 17, 18, 19)
# left
plot(sales)
# middle
plot(date, sales)
# right
plot(date, sales, type="l")
```

\begin{figure}

{\centering \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/simple-plots-1-1} \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/simple-plots-1-2} \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/simple-plots-1-3} 

}

\caption{Creating a simple line plot.}(\#fig:simple-plots-1)
\end{figure}

Example 2:


```r
tarsus <- readxl::read_excel("tarsus.xlsx")
# left
plot(tarsus$Weight)
```

![](MyR_files/figure-latex/unnamed-chunk-137-1.pdf)<!-- --> 

```r
# middle
plot(tarsus$TarsusLength, tarsus$Weight)
```

![](MyR_files/figure-latex/unnamed-chunk-137-2.pdf)<!-- --> 

```r
# right
plot(tarsus$TarsusLength, tarsus$Weight, type="l")
```

![](MyR_files/figure-latex/unnamed-chunk-137-3.pdf)<!-- --> 

We now add further customization with new functions and arguments.  

- `col` determines the color; see this [Rcolor.pdf online](http://www.stat.columbia.edu/~tzheng/files/Rcolor.pdf) for details.
- The `lty` argument refers to the type of line, to be chosen from the values shown in Figure \@ref(fig:line-types),
- `lines` adds the plot of a vector to a previously opened plot.
- `axis` is a function that changes the axis given in its first argument with 1, 2, 3, 4 referring to the bottom, left, top, and right axis, respectively.
- `at` simply states for what values of the axis the labels should correspond.
- `las` gives the orientation of the labels (e.g., `1=horizontal`).
- `xlab` and `ylab` are the x and y axes labels, respectively.
- `xlim` and `ylim` set a numerical limit for the x and y axes labels, respectively, notice that a vector of length 2 is necessary for each.


\begin{figure}

{\centering \includegraphics[width=0.5\linewidth]{MyR_files/figure-latex/line-types-1} 

}

\caption{Line types.}(\#fig:line-types)
\end{figure}




```r
sales2 <- c(12, 19, 22, 28, 32) 
# left
plot(date, sales, type="l", col="blue")
lines(date, sales2, type="b", col="red", lty=3)
# middle
s.range <- c(min(sales,sales2),max(sales,sales2))
plot(date, sales, type="l", col="blue", ylim=s.range)
lines(date, sales2, type="b", col="red", lty=3)
# right
plot(date, sales, type="l", col="blue",
     ylim=s.range,
     axes= FALSE, 
     xlab = "Day",
     ylab= "Sales")
lines(date, sales2, type="b", col="red", lty=3)
axis(1, at=date, lab=c("Mon","Tue","Wed","Thu","Fri"))
axis(2, las=1, at=seq(min(s.range),max(s.range),5)) 
```

\begin{figure}

{\centering \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/simple-plots-2-1} \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/simple-plots-2-2} \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/simple-plots-2-3} 

}

\caption{Custom a simple line plot.}(\#fig:simple-plots-2)
\end{figure}



We now add further elements such as a legend or a title.

- `legend` gives and places a legend; its first arguments are the location on the x and y axis respectively (this can be replaced by expressions such as `topleft`); the third is the legend itself, completed with colors and other formatting; notice that since the legend specifies two series, the formatting must also be given for each of them in vectors of length 2.
- `pch` determines the shape of the point in the plot, to be chosen from Figure \@ref(fig:point-types).
- `cex` gives the expanding factor of the text.
- `bty` specifies whether of not the legend should be in a box (default, "o") or not "n".
- `title` gives the title to the plot.


\begin{figure}

{\centering \includegraphics[width=0.5\linewidth]{MyR_files/figure-latex/point-types-1} 

}

\caption{Point types.}(\#fig:point-types)
\end{figure}




```r
plot(date, sales, type="l", col="blue", ylim=s.range,
      axes= FALSE, xlab = "Day", ylab= "Sales")
lines(date, sales2, type="b", col="red", lty=3)
axis(1, at=date, lab=c("Mon","Tue","Wed","Thu","Fri"))
axis(2, las=1, at=seq(min(s.range),max(s.range),5)) 
legend(date[1], s.range[2], c("Tom","Mark"), cex=1, 
   col=c("blue","red"), pch=c(NA,1), lty=c(1,3), bty="n")
title(main="Week Sales", col.main="black", font.main=2)
```

\begin{figure}

{\centering \includegraphics[width=0.5\linewidth]{MyR_files/figure-latex/simple-plots-3-1} 

}

\caption{Further customization of a simple line plot.}(\#fig:simple-plots-3)
\end{figure}


One can help but notice how cumbersome the coding of the graph is, in particular when one needs to retype the whole code for the same graph.



## Bar graphs and histograms


This subsection illustrates the creation of these graphs with a few commented examples.

- `barplot` takes a vector or a matrix as first argument. It is therefore important to double check how this latter is created.
- `density` applies to the colors and a single value would be recycled.
- `horiz` defaults to `FALSE` and gives the direction of the plot.
- `border` applies to the borders of the bars.
- `beside` forces side-by-side bars instead of stacking bars.

Advanced example of a bar plot with additional functions:


```r
barplot(sales,
        main="Week Sales - Tom",
        names.arg=c("Mon","Tue","Wed","Thu","Fri"),
        border="lightblue",
        col = "blue")
barplot(sales,
        main="Week Sales - Mark",
        names.arg=c("Mon","Tue","Wed","Thu","Fri"),
        border="red",
        col = "red",
        horiz = TRUE)

barplot(matrix(c(sales, sales2), ncol=5, byrow = TRUE),
        beside = TRUE,
        names.arg=c("Mon","Tue","Wed","Thu","Fri"),
        col=c("blue", "red"),
        density = 30, 
        main="Week Sales")
```

\begin{figure}

{\centering \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/bar-plots-1} \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/bar-plots-2} \includegraphics[width=0.25\linewidth]{MyR_files/figure-latex/bar-plots-3} 

}

\caption{Simple bar plots.}(\#fig:bar-plots)
\end{figure}

Simple example of a bar plot without additional functions:


```r
max.temp.germany <- c(20, 28, 36, 30, 39)

barplot(max.temp.germany)
```

![](MyR_files/figure-latex/unnamed-chunk-138-1.pdf)<!-- --> 


```r
# barchart with added parameters
barplot(max.temp.germany,
main = "Maximum Temperatures in Germany (July 2019)",
xlab = "Degree Celsius",
ylab = "Day",
names.arg = c("01.07.", "05.07.", "13.07", "18.07.", "20.07."),
col = "blue",
horiz = FALSE)
```

![](MyR_files/figure-latex/unnamed-chunk-139-1.pdf)<!-- --> 

Turning to histogram, the function and some arguments are the following.

- `hist` is the function to create an histogram from the values of a vector.
- `breaks` is the important argument as it controls the width of the bars.
- `freq` determines whether the frequency (default) of the density should be plotted.

Example histogram:


```r
hist(c(sales, sales2))

brks <- seq(min(s.range), max(s.range)+3, 5)
hist(c(sales, sales2),
    col=rev(heat.colors(length(brks))),
    breaks=brks,
    main="Histogram of Week Sales",
    las=1, cex.axis=0.8,
    freq=TRUE,
    xlab="Sales")
```

\begin{figure}

{\centering \includegraphics[width=0.35\linewidth]{MyR_files/figure-latex/hist-plots-1} \includegraphics[width=0.35\linewidth]{MyR_files/figure-latex/hist-plots-2} 

}

\caption{Simple histograms.}(\#fig:hist-plots)
\end{figure}

Basic histogram example including colors and labels:


```r
hist(iris$Sepal.Length, 
     breaks=30, 
     col="red", 
     xlab="Sepal Length", 
     main="Histogram Example with Colors and Labels")
```

![](MyR_files/figure-latex/unnamed-chunk-140-1.pdf)<!-- --> 

### Other plots

Other types of plots are called by the following functions.

- `pie` for the pie (round) charts.
- `boxplot` for the box-and-whisker plot.
- `dotchart` for the Cleveland dot plot.
- ...

<!--chapter:end:25-plots.Rmd-->

# Resampling

Resampling methods are a valuable and useful tool in statistics. They involve drawing samples from data or training sets and as the name already says, refitting a model on each sample, in order to obtain additional information about the fited model.

Two commonly used resampling methods that you may encounter are k-fold cross-validation and the bootstrap.

1. Bootstrap: Drawing samples from a dataset with replacement, where those instances not drawn into the data sample may be used for the test set.

2. k-fold Cross-Validation: A dataset is partitioned into k groups, where each group is given the opportunity of being used as a held out test set leaving the remaining groups as the training set.

## Replication Requirements

In order to expain what resampling is about, we will focus on various examples of bootstraps , which is part of the ISLR package in R. We can also use tidyverse packages, in order to manipulate and visualize the data. Important: We will use the boot package to illustrate resampling methods, which is the most important part of resampling.

Let us start with installing or using the required packages for resampling: 

Packages:

```{r
library(tidyverse)  # data manipulation and visualization
library(boot)       # resampling and bootstrapping
```

## Why Resampling?

Resampling methods are very easy to use and require only basic mathematical knowledge. They are methods that are fairly easy to understand and implement. They don't require deep technical skill, in order to select and interpret.

The resampling methods […] are easy to learn and easy to apply. They require no mathematics beyond introductory high-school algebra, et are applicable in an exceptionally broad range of subject areas.

— Page xiii, Resampling Methods: A Practical Guide to Data Analysis, 2005.

## Bootstrapping

Bootstrapping can be a very useful tool in statistics and is very easily implemented in R. Bootstrapping plays a role, when there is doubt that the distributional assumptions and asymptotic results are valid and accurate. It is a nonparametric method, which helps you compute estimated standard errors, confidence intervals and hypothesis testing.

The basic steps of bootstrapping:

1. Resample a given data set a specified number of times.
2. Calculate a specific statistic from each sample.
3. Find the standard deviation of the distribution of that statistic.

The following bootstrapping example is an example, where we are willing to obtain a standard error for the estimate of the median. 

We will therefore make use of the lapply, sapply functions in combination with the sample function. Hint: For more information about the lapply and sapply function please consult the help manuals.

### Sample function 

A major component of bootstrapping is being able to resample a given data set. In R, this is done by using the `sample function`:

Example sample function 

Step 1: Use sample to generate a permutation of the sequence 1:10


```r
sample(10)
#R>  [1]  8 10  4  5  1  7  6  9  2  3
```

Step 2: Bootstrap the sample


```r
sample(10, replace=T)
#R>  [1]  4  5  1 10  5 10  9  7 10  7
```

Step 3: boostrap sample with probabilities that favor numbers from 1 to 5


```r
bootstrap1 <- c(rep(.15, 5), rep(.05, 5))
bootstrap1
#R>  [1] 0.15 0.15 0.15 0.15 0.15 0.05 0.05 0.05 0.05 0.05
```


```r
sample(10, replace=T, prob=bootstrap1)
#R>  [1] 1 1 1 7 2 3 3 4 4 5
```

Step 4: Sample of size 5 from elements of a matrix, in order to create the data matrix


```r
matrix1 <- matrix( round(rnorm(25,5)), ncol=5)
matrix1
#R>      [,1] [,2] [,3] [,4] [,5]
#R> [1,]    5    3    5    5    5
#R> [2,]    6    4    5    4    4
#R> [3,]    6    4    6    6    7
#R> [4,]    4    3    4    5    6
#R> [5,]    6    5    4    6    5
```

Step 5: Save the sample of size 5 in the vector `vector1`


```r
vector1 <- matrix1[sample(25, 5)]
vector1
#R> [1] 5 5 6 5 5
```

Step 6: Sample the rows of the matrix, in order to create the data matrix


```r
matrix2 <- matrix( round(rnorm(40, 5)), ncol=5)
matrix2
#R>      [,1] [,2] [,3] [,4] [,5]
#R> [1,]    5    5    7    4    6
#R> [2,]    5    7    4    4    6
#R> [3,]    6    5    5    5    4
#R> [4,]    5    4    5    4    6
#R> [5,]    5    5    6    5    6
#R> [6,]    5    4    3    5    4
#R> [7,]    7    6    5    4    6
#R> [8,]    6    6    5    5    4
```

Step 7: Save the sample of rows in vector 2


```r
vector2 <- matrix2[sample(8, 3),  ]
vector2
#R>      [,1] [,2] [,3] [,4] [,5]
#R> [1,]    5    5    7    4    6
#R> [2,]    5    4    5    4    6
#R> [3,]    6    6    5    5    4
```

### A bootstrap example

Obtain 20 bootstrap samples and display the first of the bootstrap samples [1:10]


```r
data <- round(rnorm(100, 5, 3))
data[1:10] 
#R>  [1]  7  9  8  2 11  3  5  4  5  6
```


```r
resamples <- lapply(1:20, function(i) sample(data, replace = T))
resamples
#R> [[1]]
#R>   [1]  4  4  8  5  5  5  7  5  7  4  5  9  5  3  2  8  3  0  5  1  2  5  5
#R>  [24]  4  6  5  4  4  8  5  6  5  5  4  5  5  6  9  5  1  6  4  7  4  2  4
#R>  [47]  6  8  3  5  9  5  4  4  5  7  5  6  5  2  2  6  4  4  3  4  5  5  4
#R>  [70] 13  4  1  8  7  6  2  7  8  3  0  3  7  5  5  6  4  2  4  2  2  5 11
#R>  [93]  6  4  6  5  4 13  8  6
#R> 
#R> [[2]]
#R>   [1]  4  2  4  3  5  5  5  2  5  3  0  5  0  5  5  6  5  5  0  4  9  5  5
#R>  [24]  6  6  5  4  5  2  4  4  4  4  1  6  4  2  6  7  9  0  1  4  8  5  3
#R>  [47]  1  8  9  1  8  7  0  1  6  4  5  6  6  3  7  1  6  5 11  2 -1  8  0
#R>  [70]  5  5  8  5  5 10  7  5  5  9  8  9  5  2  6  2  4  5  4  7 10  4  4
#R>  [93]  7  6  4 10  5  4  9  8
#R> 
#R> [[3]]
#R>   [1]  3  4  7 -1  1  6  5  4  5  4  5  0  4  0  6  9  6  4  5  5  4  4  4
#R>  [24]  3  1  0  0  5  4  2  8  4  5  2  1  2  1  4  5  5  4  4  7  5  5  6
#R>  [47]  0  5  7  9  8  4  5  2  7  5  5  4  5  5  4  7  1  0  5  3  1  5  1
#R>  [70]  2  6 -1  4  7  5  4  6  4  1  3  1  5  7  7 10  2  5  3  4  5  8  4
#R>  [93]  9  5  7  6 11  8  9  1
#R> 
#R> [[4]]
#R>   [1]  6  4  5  2  5  4  5  8  1  1  4  5  7  7  9  0  6  8  9  1  3  2  1
#R>  [24]  2  4  5  7  5  2  4  4  9  5  2  6  6  5  4  5  2  5  4  1  5  9  1
#R>  [47]  2  5  3  1  4  5  2  5  4 13  4  5  4  3  8  1 10  8  3  7  6  6  6
#R>  [70]  5  2  9  5  6  9  1  8  9  6  0  8  2  2  7  9  5  5  5  1  5  4  4
#R>  [93]  1  9  2  8  3  3  4  3
#R> 
#R> [[5]]
#R>   [1]  3  3  0  2  1  9  0  4  5  1 -1  2  0  4  7  4 10  4  6  5  8  4  2
#R>  [24]  4  5 11 11  8  1  9  1  3  5  5  9  2  3  9  4  2  6  7  7  5  4  1
#R>  [47]  9  4  3  9  5  3  0  5 -1  4  9  2  1  6  4  6  6  2  1  5  7  4  5
#R>  [70] 13  4  5  5  7  9  3  5  2  5  4  4  5  6  8  5  6  4  4  1  6  3  5
#R>  [93]  3  5  2  5  9  6  4  4
#R> 
#R> [[6]]
#R>   [1]  8  5  6  2  5  9  1  1  8  2  4  5  5  4  1  6  5  8 10  3  1  4  6
#R>  [24]  7  7  5  4  4  4  2  0  5  4  2  0  1  1  6  9  5  2  6  7  5  4  8
#R>  [47]  8  9  7  4  4  4  8  5  7  0  9  4  2  5  7  2  5  9  8  5  4  0  4
#R>  [70]  1  1  5  5  5  9  5  3 13  1  5  4  5  2  2  4  6  4  5  7  5  4  7
#R>  [93]  8  6  5  4  5  4  4  3
#R> 
#R> [[7]]
#R>   [1]  7  7  6  5  5  9  7  8  4  4  5  5  2  1  0  1  4  6  5  4  6  1  1
#R>  [24]  2  5  6  5  5  8 11  7  0  6  3 11  3  2  4  6  5  4  5  1  8  2  2
#R>  [47]  8  1  3  6 10  9  3  5  5  6  3  3  4  0  8 -1  2  2  4  3  2  5  2
#R>  [70]  2  4  2  1 11  4  1  2  2  6 11  4  5  5  8  2  8  8  8  1  9  5 11
#R>  [93]  6  2  1  0  4  2  9  5
#R> 
#R> [[8]]
#R>   [1]  6  1  3  2  2  4  4  4  5  4  1  7  4  9  6 10  5  5  5  6  3  0  8
#R>  [24]  0  9  8  6  6  9  1  3  4  8  0  8  7  4  3 -1  3  5  9  5  1  4  8
#R>  [47]  3  2  8  4  5  5  4  7  8  5  2  6  8  5  6  4  0  4  5  5 11  2  5
#R>  [70]  2  7  2  4  6  4  1  5  9  2  6  7 10  7  5  1  5  8  7  5  8  5  0
#R>  [93]  1  5  5  6  6  2  9  5
#R> 
#R> [[9]]
#R>   [1]  6  5  5  4  9 13  6  6  6  2  5  9  1  7  3  9  5  4  6  5  8  6  2
#R>  [24]  7  3  7  7  3  9  4  7  5  6  8  5  8  3  0  5  4  3  5  6  5  1  2
#R>  [47]  4  3  7  6 13  8  0  8  5  3  2 11  4  1  4  4  2  4  4  1  5  5  7
#R>  [70]  3  6  9  5  4  1  5  5  2 13  0  4  9  7  2 -1  4  8  7 10  5  3  0
#R>  [93]  5  3  7  8  6  4  3  9
#R> 
#R> [[10]]
#R>   [1]  2  2  5  7  4  4  4  2  4  7  0  4  5  4  3  4  9  5  6  3  8  5  3
#R>  [24]  5  2  4  0  5  5  6  1  2  9  1  4  4  3  7  5  2  2  5  5  4  6  4
#R>  [47]  4  1  5  7 10  4  3  6  5 -1  8 11  5  5  3  1  2  3  6  4  7  4  3
#R>  [70]  3  7  3  7  6 -1  2  4  2  2  5  2  7  1  7  5  1  0  3  1  3  5  4
#R>  [93]  6  2  1  0  9  0  9  7
#R> 
#R> [[11]]
#R>   [1]  1  5  4  3  7  4  0  1  5  2  0  5  4  8  5  1  4  4  0  3  4  6  4
#R>  [24]  4  2  1  4  7  1 13  1  7  7  6  6  5  9  2  4  2  5  4  2  2  4  3
#R>  [47]  2  9  9  7  5  1  4  1 10  4  3  1  2  8  1  5  4  9  7  5  4  2  5
#R>  [70]  5  9  6  1  1  8  6  5  8  6  5  2  1  3 10  2  5  5  1  2  2  9  5
#R>  [93] 10 13  1  5  4  7  4  8
#R> 
#R> [[12]]
#R>   [1]  4  3  3  2  8  4  2  5  1 -1  9  2  4  7  9  5  0  5  1  5  3  2  8
#R>  [24]  5  7  2  8  1  4  0  1  5  5  2  6  5  1  6  4  3  2  0  6  5  4 -1
#R>  [47]  2  6  0  9  5  2  5  7  5  8  5 10  3  5  4  4  5 10  8 13  5 10  5
#R>  [70] 10  1  5  3  2  5  5  4  2  5  3  8  5  9  1  1  3  3  4  4 13  5  7
#R>  [93]  3  8  9  3  5  9  4  8
#R> 
#R> [[13]]
#R>   [1]  0  4  8  9  5  3  3  8  2 10  5  4  5  9  4 10 10  1  0  9  5  1  5
#R>  [24]  2  2  5  6  8  3  6  9  4  4  1  4  7  1  6  5  1 10  0  7  8  5  8
#R>  [47]  4  3  5  6  5  1  1  9  1 10  9  4  9  4  7  7  7  6 10  6  7  3  7
#R>  [70]  8  8  2  5  3  5  4  2  1  3  7  0  6  5  3  5  5  4  5  2  3  5 10
#R>  [93]  5  2  1  2  5  6  6  8
#R> 
#R> [[14]]
#R>   [1]  5  3  0  6  4  4  4  4  4  5  9  6  5  6  5  1  2  6  7 -1  6  5  3
#R>  [24]  9  4  1  9  4  3  5  7  5  8  3  6 11  5  5  3  6  6  5  4 11  4 13
#R>  [47]  1  5  4  4  4  5  4  8  5  3  6  5  6  6 13  5 13  1  2  1  6  6  1
#R>  [70]  9  6  1 10  5  3  8  5  4  9  7  6  4  2  4  4  7  5  4  5  3  0  8
#R>  [93]  1  8  7  0  4  8  0  5
#R> 
#R> [[15]]
#R>   [1] 10  5  3  9  5  8  9  5  5  5  7  9  7  2  9  4  4  4  3  5  3  2  3
#R>  [24]  3  5  5  2  5  5  3  1  3  4  5  4  5  5  6  9  2  2  2  6  5  3  6
#R>  [47]  3  3  7  1 10  6  3  8  3  7  5  5  6  2  5  2  5  0  5  7  8  7  3
#R>  [70]  4  5  2  8  2  5  5  6  1  1  4  9  5  5  5  4  6  2  0  2  3  5  6
#R>  [93]  4  5  9  5  5  5  1  3
#R> 
#R> [[16]]
#R>   [1]  2  8  0  6  8  4  5  4  5  4 13  7  8  5  6  5  7  4  0  0  4  9  3
#R>  [24]  6  1  4 13  7  5  1  7  0  2  0  2  7  8  2  5  2  4  5  3  2  3  5
#R>  [47]  8  4  2  5  6  7  8  8  5  7  4  2  7  8  7  5  1  1  8  4  6  5  4
#R>  [70]  4  3  5  2  1  5  1 10  2  3  5  4  6  1  3  3  4  9  4  4  0  4  0
#R>  [93]  8  7  4  5  2  4  5  1
#R> 
#R> [[17]]
#R>   [1]  5  2  7  4  5  7  6  0  4  6  0  2  3  5  1  2  7  5  1  9  7  2  9
#R>  [24]  0  9  4  5  6  1  5  0  6  4 -1  5  1 11  5  9  6  5  5  4  7  4  8
#R>  [47]  6  1  6  4  7  4  7  5  1  6  5  7  3  9  0  5  4  0  9  5  9  6  0
#R>  [70]  2  1  6  5  5  1  5  7  7  6  2  1  9  4  2 13  9  5 -1  7  1 10  8
#R>  [93] 10  2  5  8  5  5  5  1
#R> 
#R> [[18]]
#R>   [1]  7  7  3  4  9  2  2  1  0  6  9  2  4  6  5 10  2  5  3  3  6  4  2
#R>  [24]  4  4  6  9  6  4  6  7  4  5  4  5  5 11  4  8  2  3  4  4  4  9  6
#R>  [47]  1  5  1  0  9  5  5  7  4  4  8  8  6  5  1  7  9  7  9  5  4  4  1
#R>  [70] 10  1  1  1  3  8  2  3  7  5  1  6  4  6  7  0  3 -1  1  3  1  9  2
#R>  [93]  4  4  2  1  2  5  5  2
#R> 
#R> [[19]]
#R>   [1] 10  7  5  8  0  7  1  2  4  9  8  4  9  9  4  3  1  5  7  5  3  5  5
#R>  [24]  5  8  5  2  5  4  4  4  4  5  6  7  9  5  2  8  3  2  6  4  5  1  4
#R>  [47]  6  4  1  2  5  4  2  8 -1  5  4  0 13  2  2  1  5  6  8  2  5  6  1
#R>  [70]  2  4  5  1  4  7  8  4  5  3  3  8  8  4  8  4  4  2  6  3  1  3  5
#R>  [93]  2  5  7  1 13  6  7 13
#R> 
#R> [[20]]
#R>   [1]  5  8  5  6  4  4  0  2 10  2 10  7  1  6  6  8  9  1  4  5  9  7 10
#R>  [24]  5  0  5  5  2  8  5  5  2  9  2  8  9  1  7 -1  1  8  2  6  2  2 13
#R>  [47]  5  2  9  8  5  2  9  5  2  0  8  4  4  7  4  4 10  4  5  2  4 13  4
#R>  [70]  5  3  2  5  5  7  4  5  5  5  7  9  8  2  3  1  5  7  6  1  2  5  6
#R>  [93]  4  5  1  1  5  2  5  1
```

Calculate the median for each bootstrap sample 


```r
r.median <- sapply(resamples, median)
r.median
#R>  [1] 5.0 5.0 4.5 5.0 4.0 5.0 4.5 5.0 5.0 4.0 4.0 5.0 5.0 5.0 5.0 4.0 5.0
#R> [18] 4.0 5.0 5.0
```

Calculate the standard deviation of the distribution of medians


```r
sqrt(var(r.median))
#R> [1] 0.44129
```

Display a histogram of the distribution of the medians 


```r
hist(r.median)
```

![](MyR_files/figure-latex/unnamed-chunk-153-1.pdf)<!-- --> 

### Built in bootstrapping functions

R has numerous built in bootstrapping functions. Below, you will find an example of a bootstrapping function (others can be found in the bootstrap package):

We are making use of the "city" data included in the boot package.

Step 1: Make sure the boot package is installed using install.packages("boot") and obtain the data from the package


```r
library(boot)
data(city)
```

Step 2: Define the ratio function


```r
ratio <- function(d, w) sum(d$x * w)/sum(d$u * w)
```

Step 3: Use the boot function


```r
boot(city, ratio, R=999, stype="w")
#R> 
#R> ORDINARY NONPARAMETRIC BOOTSTRAP
#R> 
#R> 
#R> Call:
#R> boot(data = city, statistic = ratio, R = 999, stype = "w")
#R> 
#R> 
#R> Bootstrap Statistics :
#R>     original     bias    std. error
#R> t1* 1.520313 0.03782679   0.2131541
```

## Resampling Examples

Here is an additional resampling example, which we learned in the course of our semester.

### Creating many data sets


```r
# another resampling method: creating many data sets
library(boot)

degrees <- 1:10

loocv <- numeric()

for (i in degrees) {
  fit1 <- glm(mpg ~ poly(horsepower,i), data = Auto)
  
  loocv[i] <- cv.glm(Auto, fit1)$delta[1] %>% sqrt
  
}

plot(degrees, loocv, type = "b", col = "red" )
```

![](MyR_files/figure-latex/unnamed-chunk-157-1.pdf)<!-- --> 


```r
library(boot)

degrees <- 1:10
n.trys <- 12

m.k10 <- matrix(NA, length(degrees), n.trys)

for (s in 1:n.trys) {
  
  for (i in degrees) {
    fit1 <- glm(mpg ~ poly(horsepower,i), data = Auto)
    m.k10[i,s] <- cv.glm(Auto, fit1, K=10)$delta[1] %>% sqrt
    
    
  }
    
  
}
 plot(degrees, m.k10[,1], type = "l", col = "red", ylim = c(min(m.k10), max(m.k10)))   

for (s in 2:n.trys) {
  lines(degrees, m.k10[,s], col=s) 
  
}
```

![](MyR_files/figure-latex/unnamed-chunk-158-1.pdf)<!-- --> 

## Cross-Validation 

Definiton: Cross-validation is a resampling procedure used to evaluate machine learning models on a limited data sample.

Procedure has:

- `k` as a single parameter refering to the number of groups that a data sample is to be spit into

Therefore, the procedure is also known as the k-fold cross-validation, as mentioned in the first part of the chapter.

When you assign a specific value to k (e.g. k=10), it becomes a 10-fold cross-validation.

This approach divides the set of observations into k groups, or folds, of approximately equal size. Within that, the first fold is treated as a validation set, and the method is then fit on the remaining k − 1 folds.

### The Validation set Approach

The validation set approach randomly splits the data into two sets: 

- One set to train the model.
- Remaining other set to test the model.

The process:
1. Build the model on the training data set
2. Apply the model to the test data set to predict the outcome of new unseen observations
3. Quantify the prediction error as the mean squared difference between the observed and the predicted outcome values.

Example 1:

Step 1 of the process: Choose a different training set (Expectation: Obtain different errors as opposed to the first example).


```r
require(ISLR)
require(tidyverse)
set.seed (2)
train <- sample (392 ,196)
```

Step 2 of the process: Use the subset option in lm() to fit a linear regression.


```r
lm.fit = lm(mpg ~ horsepower , data = Auto, subset = train)
EMSE <- mean((Auto$mpg - predict(lm.fit, newdata = Auto))[-train]^2)
EMSE
#R> [1] 23.29559
```

Step 3 of the process: Use the poly() function to estimate the test error for the quadratic and cubic regressions.


```r
lm.fit2=lm(mpg ~ poly(horsepower ,2) ,data=Auto ,subset =train )
EMSE2 <- mean((Auto$mpg - predict(lm.fit2, newdata = Auto))[-train]^2)
EMSE2
#R> [1] 18.90124
```


```r
lm.fit3=lm(mpg ~ poly(horsepower ,3) ,data=Auto ,subset =train )
EMSE3 <- mean((Auto$mpg - predict(lm.fit3, newdata = Auto))[-train]^2)
EMSE3
#R> [1] 19.2574
```

Result: Using this split of the observations into a training set and a validation set, we find that the validation set error rates for the models with linear, quadratic, and cubic terms are 23.30, 18.90, and 19.26.

The next step is then to calculate the `Root Mean Squared Error`, where the model that produces the lowest test sample RMSE is the preferred model.

### k-fold Cross-Validation

The k-fold cross-validation method evaluates the model performance on different subset of the training data and then calculate the average prediction error rate. 

The algorithm is as follow:

1. Randomly split the data set into k-subsets (or k-fold) (for example 5 subsets)
2. Reserve one subset and train the model on all other subsets
3. Test the model on the reserved subset and record the prediction error
4. Repeat this process until each of the k subsets has served as the test set.
5. Compute the average of the k recorded errors. This is called the cross-validation error serving as the performance metric for the model.

How to choose the right k value?

- Lower value of K = More biased and therefore undesirable. 
- Higher value of K = :ess biased, but can suffer from large variability. 

In practice, one typically performs k-fold cross-validation using k = 5 or k = 10. 

These values have been shown empirically to yield test error rate estimates without excessively high bias and also without a very high variance.

Example (10-fold cross validation):

First of all: The package `caret` is needed for the k-fold cross-validation.


```r
require(caret)
#R> Loading required package: caret
#R> Loading required package: lattice
#R> 
#R> Attaching package: 'lattice'
#R> The following object is masked from 'package:boot':
#R> 
#R>     melanoma
#R> 
#R> Attaching package: 'caret'
#R> The following object is masked from 'package:purrr':
#R> 
#R>     lift
```

Step 1: Define training control


```r
set.seed(123) 
train.control <- trainControl(method = "cv", number = 10)
```

Step 2: Train the model


```r
model <- train(Fertility ~., data = swiss, method = "lm",
               trControl = train.control)
```

Step 3: Summarize the results


```r
print(model)
#R> Linear Regression 
#R> 
#R> 47 samples
#R>  5 predictor
#R> 
#R> No pre-processing
#R> Resampling: Cross-Validated (10 fold) 
#R> Summary of sample sizes: 43, 42, 42, 41, 43, 41, ... 
#R> Resampling results:
#R> 
#R>   RMSE      Rsquared   MAE     
#R>   7.379432  0.7512317  6.032731
#R> 
#R> Tuning parameter 'intercept' was held constant at a value of TRUE
```

<!--chapter:end:26-resampling.Rmd-->

# Trees

## Introduction

Recursive partitioning is a fundamental tool in data mining. It helps us explore the stucture of a set of data, while developing easy to visualize decision rules for predicting a categorical (classification tree) or continuous (regression tree) outcome. This section briefly describes CART modeling, conditional inference trees, and random forests.

Regression and classification trees can be generated through the rpart package.


```r
#load packages

require(data.tree)
#R> Loading required package: data.tree
require(randomForest)
require(rpart)

require(ISLR)
require(MASS)
require(tidyverse)
```

## Regression trees
Let`s look for a baseball salary example to illustrate data with a graph:


```r
require(ggplot2)
data("Hitters")

hist(Hitters$Salary)
```

![](MyR_files/figure-latex/unnamed-chunk-168-1.pdf)<!-- --> 

```r

Hitters$Salary <- log(Hitters$Salary)
hist(Hitters$Salary)

Hitters %>%
  mutate(Salary = log(Salary))
#R>     AtBat Hits HmRun Runs RBI Walks Years CAtBat CHits CHmRun CRuns CRBI
#R> 1     293   66     1   30  29    14     1    293    66      1    30   29
#R> 2     315   81     7   24  38    39    14   3449   835     69   321  414
#R> 3     479  130    18   66  72    76     3   1624   457     63   224  266
#R> 4     496  141    20   65  78    37    11   5628  1575    225   828  838
#R> 5     321   87    10   39  42    30     2    396   101     12    48   46
#R> 6     594  169     4   74  51    35    11   4408  1133     19   501  336
#R> 7     185   37     1   23   8    21     2    214    42      1    30    9
#R> 8     298   73     0   24  24     7     3    509   108      0    41   37
#R> 9     323   81     6   26  32     8     2    341    86      6    32   34
#R> 10    401   92    17   49  66    65    13   5206  1332    253   784  890
#R> 11    574  159    21  107  75    59    10   4631  1300     90   702  504
#R> 12    202   53     4   31  26    27     9   1876   467     15   192  186
#R> 13    418  113    13   48  61    47     4   1512   392     41   205  204
#R> 14    239   60     0   30  11    22     6   1941   510      4   309  103
#R> 15    196   43     7   29  27    30    13   3231   825     36   376  290
#R> 16    183   39     3   20  15    11     3    201    42      3    20   16
#R> 17    568  158    20   89  75    73    15   8068  2273    177  1045  993
#R> 18    190   46     2   24   8    15     5    479   102      5    65   23
#R> 19    407  104     6   57  43    65    12   5233  1478    100   643  658
#R> 20    127   32     8   16  22    14     8    727   180     24    67   82
#R> 21    413   92    16   72  48    65     1    413    92     16    72   48
#R> 22    426  109     3   55  43    62     1    426   109      3    55   43
#R> 23     22   10     1    4   2     1     6     84    26      2     9    9
#R> 24    472  116    16   60  62    74     6   1924   489     67   242  251
#R> 25    629  168    18   73 102    40    18   8424  2464    164  1008 1072
#R> 26    587  163     4   92  51    70     6   2695   747     17   442  198
#R> 27    324   73     4   32  18    22     7   1931   491     13   291  108
#R> 28    474  129    10   50  56    40    10   2331   604     61   246  327
#R> 29    550  152     6   92  37    81     5   2308   633     32   349  182
#R> 30    513  137    20   90  95    90    14   5201  1382    166   763  734
#R> 31    313   84     9   42  30    39    17   6890  1833    224  1033  864
#R> 32    419  108     6   55  36    22     3    591   149      8    80   46
#R> 33    517  141    27   70  87    52     9   3571   994    215   545  652
#R> 34    583  168    17   83  80    56     5   1646   452     44   219  208
#R> 35    204   49     6   23  25    12     7   1309   308     27   126  132
#R> 36    379  106    10   38  60    30    14   6207  1906    146   859  803
#R> 37    161   36     0   19  10    17     4   1053   244      3   156   86
#R> 38    268   60     5   24  25    15     2    350    78      5    34   29
#R> 39    346   98     5   31  53    30    16   5913  1615    235   784  901
#R> 40    241   61     1   34  12    14     1    241    61      1    34   12
#R> 41    181   41     1   15  21    33     2    232    50      4    20   29
#R> 42    216   54     0   21  18    15    18   7318  1926     46   796  627
#R> 43    200   57     6   23  14    14     9   2516   684     46   371  230
#R> 44    217   46     7   32  19     9     4    694   160     32    86   76
#R> 45    194   40     7   19  29    30    11   4183  1069     64   486  493
#R> 46    254   68     2   28  26    22     6    999   236     21   108  117
#R> 47    416  132     7   57  49    33     3    932   273     24   113  121
#R> 48    205   57     8   34  32     9     5    756   192     32   117  107
#R> 49    542  140    12   46  75    41    16   7099  2130    235   987 1089
#R> 50    526  146    13   71  70    84     6   2648   715     77   352  342
#R> 51    457  101    14   42  63    22    17   6521  1767    281  1003  977
#R> 52    214   53     2   30  29    23     2    226    59      2    32   32
#R> 53     19    7     0    1   2     1     4     41    13      1     3    4
#R> 54    591  168    19   80  72    39     9   4478  1307    113   634  563
#R> 55    403  101    12   45  53    39    12   5150  1429    166   747  666
#R> 56    405  102    18   49  85    20     6    950   231     29    99  138
#R> 57    244   58     9   28  25    35     4   1335   333     49   164  179
#R> 58    235   61     3   24  39    21    14   3926  1029     35   441  401
#R> 59    313   78     6   32  41    12    12   3742   968     35   409  321
#R> 60    627  177    25   98  81    70     6   3210   927    133   529  472
#R> 61    416  113    24   58  69    16     1    416   113     24    58   69
#R> 62    155   44     6   21  23    15    16   6631  1634     98   698  661
#R> 63    236   56     0   27  15    11     4   1115   270      1   116   64
#R> 64    216   53     1   31  15    22     4    926   210      9   118   69
#R> 65     24    3     0    1   0     2     3    159    28      0    20   12
#R> 66    585  139    31   93  94    62    17   7546  1982    315  1141 1179
#R> 67    191   37     4   12  17    14     4    773   163     16    61   74
#R> 68    199   53     5   29  22    21     3    514   120      8    57   40
#R> 69    521  142    20   67  86    45     4    815   205     22    99  103
#R> 70    419  113     1   44  27    44    12   4484  1231     32   612  344
#R> 71    311   81     3   42  30    26    17   8247  2198    100   950  909
#R> 72    138   31     8   18  21    38     3    244    53     12    33   32
#R> 73    512  131    26   69  96    52    14   5347  1397    221   712  815
#R> 74    507  122    29   78  85    91    18   7761  1947    347  1175 1152
#R> 75    529  137    26   86  97    97    15   6661  1785    291  1082  949
#R> 76    424  119     6   57  46    13     9   3651  1046     32   461  301
#R> 77    351   97     4   55  29    39     4   1258   353     16   196  110
#R> 78    195   55     5   24  33    30     8   1313   338     25   144  149
#R> 79    388  103    15   59  47    39     6   2174   555     80   285  274
#R> 80    339   96     4   37  29    23     4   1064   290     11   123  108
#R> 81    561  118    35   70  94    33    16   6677  1575    442   901 1210
#R> 82    255   70     7   49  35    43    15   6311  1661    154  1019  608
#R> 83    677  238    31  117 113    53     5   2223   737     93   349  401
#R> 84    227   46     7   23  20    12     5   1325   324     44   156  158
#R> 85    614  163    29   89  83    75    11   5017  1388    266   813  822
#R> 86    329   83     9   50  39    56     9   3828   948    145   575  528
#R> 87    637  174    31   89 116    56    14   6727  2024    247   978 1093
#R> 88    280   82    16   44  45    47     2    428   113     25    61   70
#R> 89    155   41    12   21  29    22    16   5409  1338    181   746  805
#R> 90    458  114    13   67  57    48     4   1350   298     28   160  123
#R> 91    314   83    13   39  46    16     5   1457   405     28   156  159
#R> 92    475  123    27   76  93    72     4   1810   471    108   292  343
#R> 93    317   78     7   35  35    32     1    317    78      7    35   35
#R> 94    511  138    25   76  96    61     3    592   164     28    87  110
#R> 95    278   69     3   24  21    29     8   2079   565     32   258  192
#R> 96    382  119    13   54  58    36    12   2133   594     41   287  294
#R> 97    565  148    24   90 104    77    14   7287  2083    305  1135 1234
#R> 98    277   71     2   27  29    14    15   5952  1647     60   753  596
#R> 99    415  115    27   97  71    68     3    711   184     45   156  119
#R> 100   424  110    15   70  47    36     7   2130   544     38   335  174
#R> 101   495  151    17   61  84    78    10   5624  1679    275   884 1015
#R> 102   524  132     9   69  47    54     2    972   260     14   123   92
#R> 103   233   49     2   41  23    18     8   1350   336      7   166  122
#R> 104   395  106    16   48  56    35    10   2303   571     86   266  323
#R> 105   397  114    23   67  67    53    13   5589  1632    241   906  926
#R> 106   210   37     8   15  19    15     6    994   244     36   107  114
#R> 107   420   95    23   55  58    37     3    646   139     31    77   77
#R> 108   566  154    22   76  84    43    14   6100  1583    131   743  693
#R> 109   641  198    31  101 108    41     5   2129   610     92   297  319
#R> 110   215   51     4   19  18    11     1    215    51      4    19   18
#R> 111   441  128    16   70  73    80    14   6675  2095    209  1072 1050
#R> 112   325   76    16   33  52    37     5   1506   351     71   195  219
#R> 113   490  125    24   81 105    62    13   6063  1646    271   847  999
#R> 114   574  152    31   91 101    64     3    985   260     53   148  173
#R> 115   284   64    14   30  42    24    18   7023  1925    348   986 1239
#R> 116   596  171    34   91 108    52     6   2862   728    107   361  401
#R> 117   472  118    12   63  54    30     4    793   187     14   102   80
#R> 118   283   77    14   45  47    26    16   6840  1910    259   915 1067
#R> 119   408   94     4   42  36    66     9   3573   866     59   429  365
#R> 120   327   85     3   30  44    20     8   2140   568     16   216  208
#R> 121   370   96    21   49  46    60    15   6986  1972    231  1070  955
#R> 122   354   77    16   36  55    41    20   8716  2172    384  1172 1267
#R> 123   539  139     5   93  58    69     5   1469   369     12   247  126
#R> 124   340   84    11   62  33    47     5   1516   376     42   284  141
#R> 125   510  126     2   42  44    35    11   5562  1578     44   703  519
#R> 126   315   59    16   45  36    58    13   4677  1051    268   681  782
#R> 127   282   78    13   37  51    29     5   1649   453     73   211  280
#R> 128   380  120     5   54  51    31     8   3118   900     92   444  419
#R> 129   584  158    15   70  84    42     5   2358   636     58   265  316
#R> 130   570  169    21   72  88    38     7   3754  1077    140   492  589
#R> 131   306  104    14   50  58    25     7   2954   822     55   313  377
#R> 132   220   54    10   30  39    31     5   1185   299     40   145  154
#R> 133   278   70     7   22  37    18    18   7186  2081    190   935 1088
#R> 134   445   99     1   46  24    29     4    618   129      1    72   31
#R> 135   143   39     5   18  30    15     9    639   151     16    80   97
#R> 136   185   40     4   23  11    18     3    524   125      7    58   37
#R> 137   589  170    40  107 108    69     6   2325   634    128   371  376
#R> 138   343  103     6   48  36    40    15   4338  1193     70   581  421
#R> 139   284   69     1   33  18    25     5   1407   361      6   139   98
#R> 140   438  103     2   65  32    71     2    440   103      2    67   32
#R> 141   600  144    33   85 117    65     2    696   173     38   101  130
#R> 142   663  200    29  108 121    32     4   1447   404     57   210  222
#R> 143   232   55     9   34  23    45    12   4405  1213    194   702  705
#R> 144   479  133    10   48  72    55    17   7472  2147    153   980 1032
#R> 145   209   45     0   38  19    42    10   3859   916     23   557  279
#R> 146   528  132    21   61  74    41     6   2641   671     97   273  383
#R> 147   160   39     8   18  31    22    14   2128   543     56   304  268
#R> 148   599  183    10   80  74    32     5   2482   715     27   330  326
#R> 149   497  136     7   58  38    26    11   3871  1066     40   450  367
#R> 150   210   70    13   32  51    28    15   4040  1130     97   544  462
#R> 151   225   61     5   32  26    26    11   1568   408     25   202  185
#R> 152   151   41     4   26  21    19     2    288    68      9    45   39
#R> 153   278   86     4   33  38    45     1    278    86      4    33   38
#R> 154   341   95     6   48  42    20    10   2964   808     81   379  428
#R> 155   537  147    23   58  88    47    10   2744   730     97   302  351
#R> 156   399  102     3   56  34    34     5    670   167      4    89   48
#R> 157   309   94     5   37  32    26    13   4618  1330     57   616  522
#R> 158   401  100     2   60  19    28     4    876   238      2   126   44
#R> 159   336   93     9   35  46    23    15   5779  1610    128   730  741
#R> 160   616  163    27   83 107    32     3   1437   377     65   181  227
#R> 161   219   47     8   24  26    17    12   1188   286     23   100  125
#R> 162   579  174     7   67  78    58     6   3053   880     32   366  337
#R> 163   165   39     2   13   9    16     3    196    44      2    18   10
#R> 164   618  200    20   98 110    62    13   7127  2163    351  1104 1289
#R> 165   257   66     5   31  26    32    14   3910   979     33   518  324
#R> 166   315   76    13   35  60    25     3    630   151     24    68   94
#R> 167   591  157    16   90  78    26     4   2020   541     52   310  226
#R> 168   404   92    11   54  49    18     6   1354   325     30   188  135
#R> 169   315   73     5   23  37    16     4    450   108      6    38   46
#R> 170   249   69     6   32  19    20     4    702   209     10    97   48
#R> 171   429   91    12   41  42    57    13   5590  1397     83   578  579
#R> 172   212   54    13   28  44    18     2    233    59     13    31   46
#R> 173   453  101     3   46  43    61     3    948   218      6    96   72
#R> 174   161   43     4   17  26    22     3    707   179     21    77   99
#R> 175   184   47     5   20  28    18    11   3327   890     74   419  382
#R> 176   591  184    20   83  79    38     5   1689   462     40   219  195
#R> 177   181   58     6   34  23    22     1    181    58      6    34   23
#R> 178   441  118    28   84  86    68     8   2723   750    126   433  420
#R> 179   490  150    21   69  58    35    14   6126  1839    121   983  707
#R> 180   551  171    13   94  83    94    13   6090  1840    128   969  900
#R> 181   550  147    29   85  91    71     6   2816   815    117   405  474
#R> 182   283   74     4   34  29    22    10   3919  1062     85   505  456
#R> 183   560  161    26   89  96    66     4   1789   470     65   233  260
#R> 184   328   91    12   51  43    33     2    342    94     12    51   44
#R> 185   586  159    12   72  79    53     9   3082   880     83   363  477
#R> 186   503  136     5   62  48    83    10   3423   970     20   408  303
#R> 187   344   85    24   69  64    88     7    911   214     64   150  156
#R> 188   680  223    31  119  96    34     3   1928   587     35   262  201
#R> 189   279   64     0   31  26    30     1    279    64      0    31   26
#R> 190   484  127    20   66  65    67     7   3006   844    116   436  458
#R> 191   431  127     8   77  45    58     2    667   187      9   117   64
#R> 192   283   70     8   33  37    27    12   4479  1222     94   557  483
#R> 193   491  141    11   77  47    37    15   4291  1240     84   615  430
#R> 194   199   52     9   26  28    21     6    805   191     30   113  119
#R> 195   589  149    21   89  86    64     7   3558   928    102   513  471
#R> 196   327   84    22   53  62    38    10   4273  1123    212   577  700
#R> 197   464  128    28   67  94    52    13   5829  1552    210   740  840
#R> 198   166   34     0   20  13    17     1    166    34      0    20   13
#R> 199   338   92    18   42  60    21     3    682   185     36    88  112
#R> 200   508  146     8   80  44    46     9   3148   915     41   571  289
#R> 201   584  157    20   95  73    63    10   4704  1320     93   724  522
#R> 202   216   54     2   27  25    33     1    216    54      2    27   25
#R> 203   625  179     4   94  60    65     5   1696   476     12   216  163
#R> 204   243   53     4   18  26    27     4    853   228     23   101  110
#R> 205   489  131    19   77  55    34     7   2051   549     62   300  263
#R> 206   209   56    12   22  36    19     2    216    58     12    24   37
#R> 207   407   93     8   47  30    30     2    969   230     14   121   69
#R> 208   490  148    14   64  78    49    13   3400  1000    113   445  491
#R> 209   209   59     6   20  37    27     4    884   209     14    66  106
#R> 210   442  131    18   68  77    33     6   1416   398     47   210  203
#R> 211   317   88     3   40  32    19     8   2543   715     28   269  270
#R> 212   288   65     8   30  36    27     9   2815   698     55   315  325
#R> 213   209   54     3   25  14    12     1    209    54      3    25   14
#R> 214   303   71     3   18  30    36     3    344    76      3    20   36
#R> 215   330   77    19   47  53    27     6   1928   516     90   247  288
#R> 216   504  120    28   71  71    54     3   1085   259     54   150  167
#R> 217   258   60     8   28  33    18     3    638   170     17    80   75
#R> 218    20    1     0    0   0     0     2     41     9      2     6    7
#R> 219   374   94     5   36  26    62     7   1968   519     26   181  199
#R> 220   211   43    10   26  35    39     3    498   116     14    59   55
#R> 221   299   75     6   38  23    26     3    580   160      8    71   33
#R> 222   576  167     8   89  49    57     4    822   232     19   132   83
#R> 223   381  110     9   61  45    32     7   3015   834     40   451  249
#R> 224   288   76     7   34  37    15     4   1644   408     16   198  120
#R> 225   369   93     9   43  42    49     5   1258   323     54   181  177
#R> 226   330   76    12   35  41    47     4   1367   326     55   167  198
#R> 227   547  137     2   58  47    12     2   1038   271      3   129   80
#R> 228   572  152    18  105  49    65     2    978   249     36   168   91
#R> 229   359   84     4   46  27    21    12   4992  1257     37   699  386
#R> 230   514  144     0   67  54    79     9   4739  1169     13   583  374
#R> 231   359   80    15   45  48    63     7   1493   359     61   176  202
#R> 232   526  163    12   88  50    77     4   1556   470     38   245  167
#R> 233   313   83     9   43  41    30    14   5885  1543    104   751  714
#R> 234   540  135    30   82  88    55     1    540   135     30    82   88
#R> 235   437  123     9   62  55    40     9   4139  1203     79   676  390
#R> 236   551  160    23   86  90    87     5   2235   602     75   278  328
#R> 237   237   52     0   15  25    30    24  14053  4256    160  2165 1314
#R> 238   236   56     6   41  19    21     5   1257   329     24   166  125
#R> 239   473  154     6   61  48    29     6   1966   566     29   250  252
#R> 240   309   72     0   33  31    26     5    354    82      0    41   32
#R> 241   271   77     5   35  29    33    12   4933  1358     48   630  435
#R> 242   357   96     7   50  45    39     5   1394   344     43   178  192
#R> 243   216   56     4   22  18    15    12   2796   665     43   266  304
#R> 244   256   70    13   42  36    44    16   7058  1845    312   965 1128
#R> 245   466  108    33   75  86    72     3    652   142     44   102  109
#R> 246   327   68    13   42  29    45    18   3949   939     78   438  380
#R> 247   462  119    16   49  65    37     7   2131   583     69   244  288
#R> 248   341  110     9   45  49    46     9   2331   658     50   249  322
#R> 249   608  160    28  130  74    89     8   4071  1182    103   862  417
#R> 250   419  101    18   65  58    92    20   9528  2510    548  1509 1659
#R> 251    33    6     0    2   4     7     1     33     6      0     2    4
#R> 252   376   82    21   42  60    35     5   1770   408    115   238  299
#R> 253   486  145    11   51  76    40    11   3967  1102     67   410  497
#R> 254   186   44     7   28  16    11     1    186    44      7    28   16
#R> 255   307   80     1   42  36    29     7   2421   656     18   379  198
#R> 256   246   76     5   35  39    13     6    912   234     12   102   96
#R> 257   205   52     8   31  27    17    12   5134  1323     56   643  445
#R> 258   348   90    11   50  45    43    10   2288   614     43   295  273
#R> 259   523  135     8   52  44    52     9   3368   895     39   377  284
#R> 260   312   68     2   32  22    24     1    312    68      2    32   22
#R> 261   496  119     8   57  33    21     7   3358   882     36   365  280
#R> 262   126   27     3    8  10     5     4    239    49      3    16   13
#R> 263   275   68     5   42  42    61     6    961   238     16   128  104
#R> 264   627  178    14   68  76    46     6   3146   902     74   494  345
#R> 265   394   86     1   38  28    36     4   1089   267      3    94   71
#R> 266   208   57     8   32  25    18     3    653   170     17    98   54
#R> 267   382  101    16   50  55    22     1    382   101     16    50   55
#R> 268   459  113    20   59  57    68    12   5348  1369    155   713  660
#R> 269   549  149     7   73  47    42     1    549   149      7    73   47
#R> 270   288   63     3   25  33    16    10   2682   667     38   315  259
#R> 271   303   84     4   35  32    23     2    312    87      4    39   32
#R> 272   522  163     9   82  46    62    13   7037  2019    153  1043  827
#R> 273   512  117    29   54  88    43     6   1750   412    100   204  276
#R> 274   220   66     5   20  28    13     3    290    80      5    27   31
#R> 275   522  140    16   73  77    60     4    730   185     22    93  106
#R> 276   461  112    18   54  54    35     2    680   160     24    76   75
#R> 277   581  145    17   66  68    21     2    831   210     21   106   86
#R> 278   530  159     3   82  50    47     6   1619   426     11   218  149
#R> 279   557  142    21   58  81    23    18   8759  2583    271  1138 1299
#R> 280   439   96     0   44  36    65     4    711   148      1    68   56
#R> 281   453  103     8   53  33    52     2    507   123      8    63   39
#R> 282   528  122     1   67  45    51     4   1716   403     12   211  146
#R> 283   633  210     6   91  56    59     6   3070   872     19   420  230
#R> 284    16    2     0    1   0     0     2     28     4      0     1    0
#R> 285   562  169    17   88  73    53     8   3181   841     61   450  342
#R> 286   281   76     3   42  25    20     8   2658   657     48   324  300
#R> 287   593  152    23   69  75    53     6   2765   686    133   369  384
#R> 288   687  213    10   91  65    27     4   1518   448     15   196  137
#R> 289   368  103     3   48  28    54     8   1897   493      9   207  162
#R> 290   263   70     1   26  23    30     4    888   220      9    83   82
#R> 291   642  211    14  107  59    52     5   2364   770     27   352  230
#R> 292   265   68     8   26  30    29     7   1337   339     32   135  163
#R> 293   289   63     7   36  41    44    17   7402  1954    195  1115  919
#R> 294   559  141     2   48  61    73     8   3162   874     16   421  349
#R> 295   520  120    17   53  44    21     4    927   227     22   106   80
#R> 296    19    4     1    2   3     1     1     19     4      1     2    3
#R> 297   205   43     2   24  17    20     7    854   219     12   105   99
#R> 298   193   47    10   21  29    24     6   1136   256     42   129  139
#R> 299   181   46     1   19  18    17     5    937   238      9    88   95
#R> 300   213   61     4   17  22     3    17   4061  1145     83   488  491
#R> 301   510  147    10   56  52    53     7   2872   821     63   307  340
#R> 302   578  138     1   56  59    34     3   1399   357      7   149  161
#R> 303   200   51     2   14  29    25    23   9778  2732    379  1272 1652
#R> 304   441  113     5   76  52    76     5   1546   397     17   226  149
#R> 305   172   42     3   17  14    15    10   4086  1150     57   579  363
#R> 306   580  194     9   91  62    78     8   3372  1028     48   604  314
#R> 307   127   32     4   14  25    12    19   8396  2402    242  1048 1348
#R> 308   279   69     4   35  31    32     4   1359   355     31   180  148
#R> 309   480  112    18   50  71    44     7   3031   771    110   338  406
#R> 310   600  139     0   94  29    60     2   1236   309      1   201   69
#R> 311   610  186    19  107  98    74     6   2728   753     69   399  366
#R> 312   360   81     5   37  44    37     7   2268   566     41   279  257
#R> 313   387  124     1   67  27    36     7   1775   506      6   272  125
#R> 314   580  207     8  107  71   105     5   2778   978     32   474  322
#R> 315   408  117    11   66  41    34     1    408   117     11    66   41
#R> 316   593  172    22   82 100    57     1    593   172     22    82  100
#R> 317   221   53     2   21  23    22     8   1063   283     15   107  124
#R> 318   497  127     7   65  48    37     5   2703   806     32   379  311
#R> 319   492  136     5   76  50    94    12   5511  1511     39   897  451
#R> 320   475  126     3   61  43    52     6   1700   433      7   217   93
#R> 321   573  144     9   85  60    78     8   3198   857     97   470  420
#R> 322   631  170     9   77  44    31    11   4908  1457     30   775  357
#R>     CWalks League Division PutOuts Assists Errors   Salary NewLeague
#R> 1       14      A        E     446      33     20       NA         A
#R> 2      375      N        W     632      43     10 1.818615         N
#R> 3      263      A        W     880      82     14 1.820312         A
#R> 4      354      N        E     200      11      3 1.826903         N
#R> 5       33      N        E     805      40      4 1.507702         N
#R> 6      194      A        W     282     421     25 1.890106         A
#R> 7       24      N        E      76     127      7 1.446565         A
#R> 8       12      A        W     121     283      9 1.527180         A
#R> 9        8      N        W     143     290     19 1.462674         N
#R> 10     866      A        E       0       0      0 1.946348         A
#R> 11     488      A        E     238     445     22 1.832313         A
#R> 12     161      N        W     304      45     11 1.830868         N
#R> 13     203      N        E     211      11      7 1.842123         N
#R> 14     207      A        E     121     151      6 1.879630         A
#R> 15     238      N        E      80      45      8 1.701222         N
#R> 16      11      A        W     118       0      0       NA         A
#R> 17     732      N        W     105     290     10 1.895047         N
#R> 18      39      A        W     102     177     16 1.641864         A
#R> 19     653      A        W     912      88      9       NA         A
#R> 20      56      N        W     202      22      2 1.590311         N
#R> 21      65      N        E     280       9      5 1.527180         N
#R> 22      62      A        W     361      22      2 1.557077         N
#R> 23       3      A        W     812      84     11       NA         A
#R> 24     240      N        W     518      55      3 1.855818         N
#R> 25     402      A        E    1067     157     14 1.895370         A
#R> 26     317      A        E     434       9      3 1.893093         A
#R> 27     180      N        E     222       3      3 1.881435         N
#R> 28     166      N        W     732      83     13 1.890106         N
#R> 29     308      N        W     262     329     16 1.862179         N
#R> 30     784      A        W     267       5      3 1.917275         A
#R> 31    1087      A        W     127     221      7       NA         A
#R> 32      31      N        W     226       7      4 1.547665         N
#R> 33     337      N        W    1378     102      8       NA         N
#R> 34     136      A        E     109     292     25 1.859036         A
#R> 35      66      A        W     419      46      5 1.741130         A
#R> 36     571      N        W      72     170     24 1.908837         N
#R> 37     107      A        E      70     149     12       NA         A
#R> 38      18      N        W     442      59      6 1.504035         N
#R> 39     560      A        E       0       0      0       NA         A
#R> 40      14      N        W     166     172     10       NA         N
#R> 41      45      A        E     326      29      5 1.437968         A
#R> 42     483      N        W     103      84      5       NA         N
#R> 43     195      N        W      69       1      1       NA         N
#R> 44      32      A        E     307      25      1 1.647303         A
#R> 45     608      A        E     325      22      2       NA         A
#R> 46     118      A        E     359      30      4 1.744023         A
#R> 47      80      N        W      73     177     18 1.680947         N
#R> 48      51      A        E      58       4      4 1.706821         A
#R> 49     431      A        E     697      61      9       NA         A
#R> 50     289      N        W     303       9      9 1.902583         N
#R> 51     619      A        W     389      39      4 1.913125         A
#R> 52      27      N        E     109       7      3 1.446565         N
#R> 53       4      A        E       0       0      0       NA         A
#R> 54     319      A        W      67     147      4 1.958696         A
#R> 55     526      A        E     316       6      5 1.874063         A
#R> 56      64      N        W     161      10      3 1.796461         N
#R> 57     194      N        W     142      14      2 1.762836         N
#R> 58     333      A        E     425      43      4       NA         A
#R> 59     170      N        W     106     206      7 1.797126         N
#R> 60     313      A        E     240     482     13 1.975172         A
#R> 61      16      A        E     203      70     10 1.504035         A
#R> 62     777      N        E      53      88      3 1.725757         N
#R> 63      57      A        W     125     199     13 1.693426         A
#R> 64     114      N        W      73     152     11 1.689376         N
#R> 65       9      A        W      80       4      0       NA         A
#R> 66     727      A        E       0       0      0 1.925192         A
#R> 67      52      N        E     391      38      8       NA         N
#R> 68      39      A        W     152       3      5 1.462674         A
#R> 69      78      A        E     107     242     23 1.537719         A
#R> 70     422      A        E     211       2      1       NA         A
#R> 71     690      N        W     153     223     10 1.752381         N
#R> 72      55      N        E     244      21      4       NA         N
#R> 73     548      A        W     119     216     12 1.908837         A
#R> 74    1380      A        E     808     108      2 1.837731         A
#R> 75     989      A        E     280      10      5 1.922607         A
#R> 76     112      A        E     224     286      8 1.908837         N
#R> 77     117      N        W     226       7      3 1.676556         A
#R> 78     153      N        E      83       2      1       NA         N
#R> 79     186      A        W     182       9      4 1.755065         A
#R> 80      55      A        W     104     213      9 1.725757         A
#R> 81     608      A        W     463      32      8       NA         A
#R> 82     820      N        E      51      54      8 1.809804         N
#R> 83     171      A        E    1377     100      6 2.026611         A
#R> 84      67      A        W      92       2      2       NA         A
#R> 85     617      N        W     303       6      6 2.021496         N
#R> 86     635      A        W     276       6      2 1.855818         A
#R> 87     495      N        W     278       9      9 1.938537         N
#R> 88      63      A        E     148       4      2 1.547665         A
#R> 89     875      A        W     165       9      1 1.715721         A
#R> 90     122      A        W     246     389     18 1.818615         A
#R> 91      76      A        W     533      40      4 1.802908         A
#R> 92     267      N        E     226      10      6 1.961025         N
#R> 93      32      A        E      45     122     26 1.446565         A
#R> 94      71      A        W     157       7      8 1.604774         A
#R> 95     162      N        W     142     210     10       NA         N
#R> 96     227      N        W      59     156      9 1.854509         N
#R> 97     791      A        E     292       9      5 2.018778         A
#R> 98     259      N        W     360      32      5       NA         N
#R> 99      99      N        W     274       2      7 1.741130         N
#R> 100    258      N        W     292       6      3 1.823647         N
#R> 101    709      A        E    1045      88     13 2.055138         A
#R> 102     90      A        E     212     327     20       NA         A
#R> 103    106      A        E     102     132     10 1.779506         A
#R> 104    248      A        E     709      41      7       NA         A
#R> 105    716      A        E     244       2      4       NA         A
#R> 106     53      A        E      40     115     15       NA         A
#R> 107     61      N        W     206      10      7       NA         N
#R> 108    300      A        W     316     439     10 1.890106         A
#R> 109    117      A        E     269      17     10 1.955722         A
#R> 110     11      A        E     116       5     12 1.446565         A
#R> 111    695      A        W      97     218     16 1.989684         A
#R> 112    214      N        W     726      87      3 1.783936         A
#R> 113    680      N        E     869      62      8 2.023265         N
#R> 114     95      N        W    1253     111     11 1.680947         N
#R> 115    666      N        E      96       4      4       NA         N
#R> 116    224      A        W     118     334     21 1.917275         A
#R> 117     50      A        W     228     377     26 1.618085         A
#R> 118    546      A        W     144       6      5 1.879630         A
#R> 119    410      N        W     282     487     19 1.837731         N
#R> 120     93      A        E      91     185     12 1.773769         A
#R> 121    921      N        E     137       5      9 1.886706         N
#R> 122   1057      N        W      83     174     16 1.667389         N
#R> 123    198      A        W     462       9      7 1.790336         A
#R> 124    219      N        E     185       8      4 1.790336         A
#R> 125    256      N        W     207     358     20 1.887564         N
#R> 126    697      A        W       0       0      0       NA         A
#R> 127    138      A        W     670      57      5 1.826903         A
#R> 128    240      A        W     237       8      1 1.855818         A
#R> 129    134      N        E     331      20      4 1.871190         N
#R> 130    263      A        W     295      15      5 1.925192         A
#R> 131    187      N        E     116     222     15 1.890106         N
#R> 132    128      N        E      50     136     20 1.739661         N
#R> 133    643      A        W       0       0      0 1.755065         A
#R> 134     48      A        W     278     415     16 1.497755         A
#R> 135     61      N        W     138      15      1 1.641864         N
#R> 136     47      N        E      97       2      2 1.504035         N
#R> 137    238      A        E     368      20      3 1.963027         A
#R> 138    325      A        E     211      56     13 1.802334         A
#R> 139    111      A        E     122     140      5       NA         N
#R> 140     71      A        W     276       7      9 1.527180         N
#R> 141     69      A        W     319       4     14 1.630406         A
#R> 142     68      A        E     241       8      6 1.708642         A
#R> 143    625      N        E     623      35      3 1.969922         N
#R> 144    854      N        W     237       5      4 1.894724         N
#R> 145    478      A        W     132     205      5       NA         A
#R> 146    226      N        E     885     105      8 1.933845         N
#R> 147    298      A        E      33       3      0 1.725757         A
#R> 148    158      A        E     231     374     18 1.895047         A
#R> 149    241      A        E     304     347     10 1.908837         A
#R> 150    551      A        E       0       0      0 1.774935         A
#R> 151    257      A        W     132       9      0       NA         A
#R> 152     35      A        W      28      56      2 1.515979         A
#R> 153     45      N        W     102       4      2 1.547665         N
#R> 154    221      N        W     158       4      5 1.527180         N
#R> 155    174      N        E      92     257     20 1.727367         N
#R> 156     54      A        W     211       9      3 1.477511         A
#R> 157    436      N        E     161       3      3 1.855818         N
#R> 158     55      N        E     193      11      4       NA         N
#R> 159    497      A        W       0       0      0       NA         A
#R> 160     82      A        W     110     308     15 1.667389         A
#R> 161     63      A        W     260      58      4       NA         A
#R> 162    218      N        E     280     479      5 1.869906         N
#R> 163     18      A        W     332      19      2 1.462674         N
#R> 164    564      A        E     330      16      8 2.052638         A
#R> 165    382      N        W      87     166     14 1.708642         A
#R> 166     55      N        E     498      39     13 1.618085         N
#R> 167     91      N        E     290     440     25 1.865857         N
#R> 168     63      A        E     222       5      5 1.741130         A
#R> 169     28      A        W     227      15      3 1.547665         A
#R> 170     44      N        E     103       8      2       NA         N
#R> 171    644      A        W     686      46      4 1.904401         N
#R> 172     20      A        E     243      23      5       NA         A
#R> 173     91      N        W     249     444     16 1.662599         N
#R> 174     76      A        W     300      12      2       NA         A
#R> 175    304      N        W      49       2      0 1.809804         N
#R> 176     82      N        W     303      12      5 1.863416         N
#R> 177     22      N        W      88       0      3 1.495181         N
#R> 178    309      A        E     190       2      2 1.969922         A
#R> 179    600      A        E      96       5      3 1.932645         N
#R> 180    917      N        E    1199     149      5 2.014308         N
#R> 181    319      A        W    1218     104     10 1.970990         A
#R> 182    283      N        W     145       5      7 1.887564         N
#R> 183    155      N        W     332       9      8 1.862179         N
#R> 184     33      N        E     145      59      8 1.574497         N
#R> 185    295      N        E     181      13      4 1.938767         N
#R> 186    414      N        W      65     258      8 1.884972         N
#R> 187    187      A        W       0       0      0 1.741130         A
#R> 188     91      A        W     429       8      6 1.774935         A
#R> 189     30      N        W     107     205     16 1.462674         N
#R> 190    377      N        E    1231      80      7 1.956722         N
#R> 191     88      N        E     283       8      3 1.669731         N
#R> 192    307      A        E     156       2      2 1.689376         A
#R> 193    340      A        E     239       8      2 1.834723         A
#R> 194     87      N        W     235      22      5 1.719140         N
#R> 195    351      A        E     371       6      6 1.897449         A
#R> 196    334      A        E     483      48      6 1.899808         N
#R> 197    452      A        W       0       0      0 1.852522         A
#R> 198     17      N        E      64     119      9       NA         N
#R> 199     50      A        E       0       0      0 1.604774         A
#R> 200    326      A        W     245       5      9       NA         A
#R> 201    576      A        E     276     421     11 1.798446         A
#R> 202     33      N        W     317      36      1 1.462674         N
#R> 203    166      A        E     303     450     14 1.849143         A
#R> 204     76      N        E     107       3      3       NA         N
#R> 205    153      A        W     310       9      9 1.896013         A
#R> 206     19      N        E     201       6      3 1.504035         N
#R> 207     68      N        W     172     317     25 1.611563         N
#R> 208    301      A        E       0       0      0 1.879630         N
#R> 209     92      N        E     415      35      3       NA         N
#R> 210    136      A        E     233       7      7 1.842123         A
#R> 211    118      A        W     220      16      4       NA         A
#R> 212    189      N        E     259      30     10 1.868253         A
#R> 213     12      A        W     102       6      3 1.439718         A
#R> 214     45      N        E     468      47      6 1.527180         N
#R> 215    161      N        W     149       8      6 1.872921         N
#R> 216    114      A        E     103     283     19 1.641864         A
#R> 217     36      A        W     358      32      8 1.593305         A
#R> 218      4      N        E      78     220      6 2.036355         N
#R> 219    288      N        W     756      64     15 1.913125         N
#R> 220     78      A        W     463      32      8 1.566007         A
#R> 221     44      N        E     212       1      2 1.597698         N
#R> 222     79      N        E     325      12      8 1.676556         N
#R> 223    168      N        E     228       7      5 1.899808         N
#R> 224    113      N        W     203       3      3 1.701222         N
#R> 225    157      A        E     149       1      6 1.767797         A
#R> 226    167      N        W     512      30      5       NA         N
#R> 227     24      A        W     261     459     22 1.641864         A
#R> 228    101      A        W     325      13      3 1.667389         A
#R> 229    387      N        W     151       8      5       NA         N
#R> 230    528      N        E     229     453     15 2.024252         N
#R> 231    175      N        W     682      93     13 1.879630         N
#R> 232    174      A        W     250      11      1 1.890106         A
#R> 233    535      N        W      58     141     23 1.809804         N
#R> 234     55      A        W     157       6     14 1.638510         A
#R> 235    364      A        E      82     170     15 1.965554         A
#R> 236    273      A        W    1224     115     11       NA         A
#R> 237   1566      N        W     523      43      6 1.890106         N
#R> 238    105      A        E     172       1      4 1.657661         A
#R> 239    178      A        E     846      84      9 1.850504         A
#R> 240     26      N        E     117     269     12 1.582588         N
#R> 241    403      A        W      62      90      3 1.809804         A
#R> 242    136      A        W     167       2      4 1.741130         A
#R> 243    198      A        E     391      44      4 1.708642         A
#R> 244    990      N        E      41     118      8 1.939683         A
#R> 245    102      A        E     286       8      8 1.680947         A
#R> 246    466      A        E     659      53      7 1.790336         A
#R> 247    150      A        E     866      65      6       NA         A
#R> 248    274      A        E     251       9      4 1.844974         A
#R> 249    708      A        E     426       4      6 2.004257         A
#R> 250   1342      A        W       0       0      0 1.822820         A
#R> 251      7      A        W     205       5      4       NA         A
#R> 252    157      A        W       0       0      0 1.800404         A
#R> 253    284      N        E      88     204     16 1.826903         A
#R> 254     11      N        W      99       3      1       NA         N
#R> 255    184      A        W     145       2      2       NA         A
#R> 256     80      A        E      44       0      1 1.708642         A
#R> 257    459      A        E     155       3      2 1.790336         A
#R> 258    269      A        E      60     176      6 1.809804         A
#R> 259    296      N        W     367     475     19 1.890106         N
#R> 260     24      A        E      86     150     15 1.446565         A
#R> 261    165      N        W     155     371     29 1.913125         N
#R> 262     14      N        E     190       2      9 1.657661         N
#R> 263    172      N        E     181       3      2 1.658661         N
#R> 264    242      N        E     309     492      5 1.888077         N
#R> 265     76      N        E     203     369     16 1.708642         N
#R> 266     62      N        E      42      94     13 1.597698         N
#R> 267     22      A        W     200       7      6 1.521667         A
#R> 268    735      A        W       0       0      0 1.888077         A
#R> 269     42      N        W     255     450     17 1.597698         N
#R> 270    204      A        W     135     257      7 1.763675         A
#R> 271     23      N        W     179       5      3       NA         N
#R> 272    535      A        E     352       9      1 1.932645         A
#R> 273    155      A        W    1236      98     18 1.527180         A
#R> 274     15      A        W     281      21      3 1.504035         A
#R> 275     86      N        E    1320     166     17 1.667389         N
#R> 276     49      A        W     111     226     11 1.590311         A
#R> 277     40      N        E     320     465     32 1.618085         N
#R> 278    163      A        W     196     354     15 1.818615         A
#R> 279    478      N        W    1160      53      7 1.985037         N
#R> 280     99      N        E     229     406     22 1.611563         N
#R> 281     58      A        W     289     407      6 1.537719         A
#R> 282    155      A        W     209     372     17 1.767797         A
#R> 283    274      N        W     367     432     16 1.504035         N
#R> 284      0      A        E     247       4      8       NA         A
#R> 285    373      A        E     351     442     17 1.836235         A
#R> 286    179      A        E     106     144      7 1.763675         A
#R> 287    321      A        W     315      10      6 1.923647         A
#R> 288     89      A        E     294     445     13 1.767797         A
#R> 289    198      N        W     209     246      3 1.755949         N
#R> 290     86      N        E      81     147      4 1.708642         N
#R> 291    193      N        W     337      19      4 1.888077         N
#R> 292    128      N        W      92       5      3 1.800404         A
#R> 293   1153      A        W     166     211      7       NA         A
#R> 294    359      N        E     352     414      9 1.921294         N
#R> 295     52      A        W      70     144     11 1.652566         A
#R> 296      1      N        W     692      70      8 1.920501         A
#R> 297     71      N        E     131       6      1 1.733127         N
#R> 298    106      A        W     299      13      5 1.704977         A
#R> 299    104      A        E      37      98      9       NA         A
#R> 300    244      A        W     178      45      4 1.697373         A
#R> 301    174      N        E     810      99     18 1.952675         N
#R> 302     87      N        E     133     371     20 1.624361         N
#R> 303    925      N        W     398      29      7       NA         N
#R> 304    191      A        W     160     290     11 1.800404         A
#R> 305    406      N        W      65       0      0 1.917275         N
#R> 306    469      N        E     270      13      6       NA         N
#R> 307    819      N        W     167      18      6 1.826903         N
#R> 308    158      N        E     133     173      9 1.727367         N
#R> 309    239      N        E      94     270     16 1.890106         N
#R> 310    110      N        E     300      12      9 1.624361         N
#R> 311    286      N        E    1182      96     13 1.969922         N
#R> 312    246      N        E     170     284      3 1.834723         N
#R> 313    194      N        E     186     290     17 1.842123         N
#R> 314    417      A        E     121     267     19 1.998470         A
#R> 315     34      N        W     942      72     11 1.566007         N
#R> 316     57      A        W    1222     139     15 1.630406         A
#R> 317    106      N        E     325      58      6       NA         N
#R> 318    138      N        E     325       9      3 1.879630         N
#R> 319    875      A        E     313     381     20 1.913125         A
#R> 320    146      A        W      37     113      7 1.783936         A
#R> 321    332      A        E    1314     131     12 1.926718         A
#R> 322    249      A        W     408       4      3 1.932645         A

hist(Hitters$Salary)
```

![](MyR_files/figure-latex/unnamed-chunk-168-2.pdf)<!-- --> 

```r

plot(Hitters$Years, Hitters$Hits, col = Hitters$Salary)
```

![](MyR_files/figure-latex/unnamed-chunk-168-3.pdf)<!-- --> 

```r


#another way

Hitters  %>%
  ggplot(aes(x=Years, y=Hits, col=Salary)) +
  geom_point()
```

![](MyR_files/figure-latex/unnamed-chunk-168-4.pdf)<!-- --> 

```r
#The salary level is shown by colour/shape from low (darker blue) to high (lighter blue)
```



A tree for this data (log) `Salary`... depending on `Years` and `Hits`:



```r
b.tree <- rpart(Salary ~ Years + Hits, data = Hitters)
plot(b.tree)
text(b.tree, pretty = 0)
```

![](MyR_files/figure-latex/unnamed-chunk-169-1.pdf)<!-- --> 

```r

plotcp(b.tree)
```

![](MyR_files/figure-latex/unnamed-chunk-169-2.pdf)<!-- --> 

```r

min.of.cp <- b.tree$cptable[which.min(b.tree$cptable[, "xerror"]), "CP"]

prune.b.tree <- prune(b.tree, cp = 0,071)
plot(prune.b.tree)
text(prune.b.tree, pretty = 0)
```

![](MyR_files/figure-latex/unnamed-chunk-169-3.pdf)<!-- --> 
Decision treers are typically are drawn upside down, because than the leaves are at the bottom of the tree.
The points along the tree where the predictor space is split are referred to as internal nodes. 
In the example hitters tree, the two internal nodes are indicated by the text Years < 3.5 and Hits < 117.5.

## Classification trees

The classification trees are very similar to the regression trees. But there is a difference in the purpose for. 
classification trees are used to predict that every observation belongs to the most commonly occuring class of training obervations in the region to which it belongs. Recursive binary splitting is used to grow a classification tree.

Here an example of a classification tree with another data set:


```r
library(rpart)
data("kyphosis")

#grow tree
fit <- rpart(Kyphosis ~ Age + Number + Start,
   method="class", data=kyphosis)

printcp(fit) # display the results 
#R> 
#R> Classification tree:
#R> rpart(formula = Kyphosis ~ Age + Number + Start, data = kyphosis, 
#R>     method = "class")
#R> 
#R> Variables actually used in tree construction:
#R> [1] Age   Start
#R> 
#R> Root node error: 17/81 = 0.20988
#R> 
#R> n= 81 
#R> 
#R>         CP nsplit rel error xerror    xstd
#R> 1 0.176471      0   1.00000 1.0000 0.21559
#R> 2 0.019608      1   0.82353 1.0588 0.22010
#R> 3 0.010000      4   0.76471 1.0588 0.22010
plotcp(fit) # visualize cross-validation results 
```

![](MyR_files/figure-latex/unnamed-chunk-170-1.pdf)<!-- --> 

```r
summary(fit) # detailed summary of splits
#R> Call:
#R> rpart(formula = Kyphosis ~ Age + Number + Start, data = kyphosis, 
#R>     method = "class")
#R>   n= 81 
#R> 
#R>           CP nsplit rel error   xerror      xstd
#R> 1 0.17647059      0 1.0000000 1.000000 0.2155872
#R> 2 0.01960784      1 0.8235294 1.058824 0.2200975
#R> 3 0.01000000      4 0.7647059 1.058824 0.2200975
#R> 
#R> Variable importance
#R>  Start    Age Number 
#R>     64     24     12 
#R> 
#R> Node number 1: 81 observations,    complexity param=0.1764706
#R>   predicted class=absent   expected loss=0.2098765  P(node) =1
#R>     class counts:    64    17
#R>    probabilities: 0.790 0.210 
#R>   left son=2 (62 obs) right son=3 (19 obs)
#R>   Primary splits:
#R>       Start  < 8.5  to the right, improve=6.762330, (0 missing)
#R>       Number < 5.5  to the left,  improve=2.866795, (0 missing)
#R>       Age    < 39.5 to the left,  improve=2.250212, (0 missing)
#R>   Surrogate splits:
#R>       Number < 6.5  to the left,  agree=0.802, adj=0.158, (0 split)
#R> 
#R> Node number 2: 62 observations,    complexity param=0.01960784
#R>   predicted class=absent   expected loss=0.09677419  P(node) =0.7654321
#R>     class counts:    56     6
#R>    probabilities: 0.903 0.097 
#R>   left son=4 (29 obs) right son=5 (33 obs)
#R>   Primary splits:
#R>       Start  < 14.5 to the right, improve=1.0205280, (0 missing)
#R>       Age    < 55   to the left,  improve=0.6848635, (0 missing)
#R>       Number < 4.5  to the left,  improve=0.2975332, (0 missing)
#R>   Surrogate splits:
#R>       Number < 3.5  to the left,  agree=0.645, adj=0.241, (0 split)
#R>       Age    < 16   to the left,  agree=0.597, adj=0.138, (0 split)
#R> 
#R> Node number 3: 19 observations
#R>   predicted class=present  expected loss=0.4210526  P(node) =0.2345679
#R>     class counts:     8    11
#R>    probabilities: 0.421 0.579 
#R> 
#R> Node number 4: 29 observations
#R>   predicted class=absent   expected loss=0  P(node) =0.3580247
#R>     class counts:    29     0
#R>    probabilities: 1.000 0.000 
#R> 
#R> Node number 5: 33 observations,    complexity param=0.01960784
#R>   predicted class=absent   expected loss=0.1818182  P(node) =0.4074074
#R>     class counts:    27     6
#R>    probabilities: 0.818 0.182 
#R>   left son=10 (12 obs) right son=11 (21 obs)
#R>   Primary splits:
#R>       Age    < 55   to the left,  improve=1.2467530, (0 missing)
#R>       Start  < 12.5 to the right, improve=0.2887701, (0 missing)
#R>       Number < 3.5  to the right, improve=0.1753247, (0 missing)
#R>   Surrogate splits:
#R>       Start  < 9.5  to the left,  agree=0.758, adj=0.333, (0 split)
#R>       Number < 5.5  to the right, agree=0.697, adj=0.167, (0 split)
#R> 
#R> Node number 10: 12 observations
#R>   predicted class=absent   expected loss=0  P(node) =0.1481481
#R>     class counts:    12     0
#R>    probabilities: 1.000 0.000 
#R> 
#R> Node number 11: 21 observations,    complexity param=0.01960784
#R>   predicted class=absent   expected loss=0.2857143  P(node) =0.2592593
#R>     class counts:    15     6
#R>    probabilities: 0.714 0.286 
#R>   left son=22 (14 obs) right son=23 (7 obs)
#R>   Primary splits:
#R>       Age    < 111  to the right, improve=1.71428600, (0 missing)
#R>       Start  < 12.5 to the right, improve=0.79365080, (0 missing)
#R>       Number < 3.5  to the right, improve=0.07142857, (0 missing)
#R> 
#R> Node number 22: 14 observations
#R>   predicted class=absent   expected loss=0.1428571  P(node) =0.1728395
#R>     class counts:    12     2
#R>    probabilities: 0.857 0.143 
#R> 
#R> Node number 23: 7 observations
#R>   predicted class=present  expected loss=0.4285714  P(node) =0.08641975
#R>     class counts:     3     4
#R>    probabilities: 0.429 0.571

#plot tree
plot(fit, uniform=TRUE, 
   main="Classification Tree for Kyphosis")
text(fit, use.n=TRUE, all=TRUE, cex=.8)
```

![](MyR_files/figure-latex/unnamed-chunk-170-2.pdf)<!-- --> 

```r

#prune the tree
pfit<- prune(fit, cp=   fit$cptable[which.min(fit$cptable[,"xerror"]),"CP"])
```

>> Command, if you want to plot the pruned tree:

```{r
plot(pfit, uniform=TRUE, 
   main="Pruned Classification Tree for Kyphosis")
text(pfit, use.n=TRUE, all=TRUE, cex=.8)
```

## Avoiding over-fitting of trees with Bagging

Bagging runs with package `randomForest` with the reason for reducing variance of statistical methods.


```r
library(randomForest)
data_frame(Boston)
boston_bag = randomForest(medv ~ ., data = Boston, mtry = 18, #mtry is number of predictors
                          importance = TRUE, ntrees = 500)
boston_bag
```


## Random Forest

Random forests improve predictive accuracy by generating a large number of bootstrapped trees (based on random samples of variables), classifying a case using each tree in this new "forest", and deciding a final predicted outcome by combining the results across all of the trees (an average in regression, a majority vote in classification). Breiman and Cutler's random forest approach is implimented via the randomForest package.

Here is an example:


```r
p <- length(names(Hitters)) -1

Hitters <- Hitters %>%
  na.omit(Hitters)
hit.bag <- randomForest(Salary ~ ., data = Hitters, 
                        mtry = p , importance = TRUE, ntrees = 500)
hit.bag
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = p,      importance = TRUE, ntrees = 500) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 19
#R> 
#R>           Mean of squared residuals: 0.1889228
#R>                     % Var explained: 76.01

hit.rf <- randomForest(Salary ~ ., data = Hitters, mtry = 
                         round(sqrt(p),0) , importance = TRUE, ntrees = 1000)
hit.rf
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = round(sqrt(p),      0), importance = TRUE, ntrees = 1000) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 4
#R> 
#R>           Mean of squared residuals: 0.1770242
#R>                     % Var explained: 77.53

hit.rf2 <- randomForest(Salary ~ ., data = Hitters, mtry = 
                          round(p/2,0) , importance = TRUE, ntrees = 1000)
hit.rf
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = round(sqrt(p),      0), importance = TRUE, ntrees = 1000) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 4
#R> 
#R>           Mean of squared residuals: 0.1770242
#R>                     % Var explained: 77.53


#what`s the best?
hit.bag
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = p,      importance = TRUE, ntrees = 500) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 19
#R> 
#R>           Mean of squared residuals: 0.1889228
#R>                     % Var explained: 76.01
hit.rf2
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = round(p/2,      0), importance = TRUE, ntrees = 1000) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 10
#R> 
#R>           Mean of squared residuals: 0.1844676
#R>                     % Var explained: 76.58
hit.rf
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = round(sqrt(p),      0), importance = TRUE, ntrees = 1000) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 4
#R> 
#R>           Mean of squared residuals: 0.1770242
#R>                     % Var explained: 77.53

train.index <- sample(1:nrow(Hitters), ceiling(nrow(Hitters)/2))

thit.bag <- randomForest(Salary ~ ., data = Hitters[train.index,], 
                         mtry = p , importance = TRUE, ntrees = 500)
hit.bag
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = p,      importance = TRUE, ntrees = 500) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 19
#R> 
#R>           Mean of squared residuals: 0.1889228
#R>                     % Var explained: 76.01

thit.rf <- randomForest(Salary ~ ., data = Hitters[train.index,], 
                        mtry = round(sqrt(p),0) , importance = TRUE, ntrees = 1000)
hit.rf
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = round(sqrt(p),      0), importance = TRUE, ntrees = 1000) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 4
#R> 
#R>           Mean of squared residuals: 0.1770242
#R>                     % Var explained: 77.53

thit.rf2 <- randomForest(Salary ~ ., data = Hitters[train.index,], 
                         mtry = round(p/2,0) , importance = TRUE, ntrees = 1000)
hit.rf
#R> 
#R> Call:
#R>  randomForest(formula = Salary ~ ., data = Hitters, mtry = round(sqrt(p),      0), importance = TRUE, ntrees = 1000) 
#R>                Type of random forest: regression
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 4
#R> 
#R>           Mean of squared residuals: 0.1770242
#R>                     % Var explained: 77.53

pre.thit.bag <- predict(thit.bag, newdata = Hitters[-train.index,])

pre.thit.rf <- predict(thit.rf, newdata = Hitters[-train.index,])

pre.thit.rf2 <- predict(thit.rf2, newdata = Hitters[-train.index,])

sqrt(mean( (pre.thit.bag- Hitters[-train.index, "Salary"])^2, na.rm = TRUE))
#R> [1] 0.410636
```

Another short example of random forest with our data set from classification trees:


```r
library(randomForest)
fit <- randomForest(Kyphosis ~ Age + Number + Start,   data=kyphosis)
print(fit) # view results 
#R> 
#R> Call:
#R>  randomForest(formula = Kyphosis ~ Age + Number + Start, data = kyphosis) 
#R>                Type of random forest: classification
#R>                      Number of trees: 500
#R> No. of variables tried at each split: 1
#R> 
#R>         OOB estimate of  error rate: 23.46%
#R> Confusion matrix:
#R>         absent present class.error
#R> absent      59       5   0.0781250
#R> present     14       3   0.8235294
importance(fit) # importance of each predictor
#R>        MeanDecreaseGini
#R> Age            8.627366
#R> Number         5.394290
#R> Start          9.820930
```

<!--chapter:end:27-Trees.Rmd-->

# Overview {#overview}

This chapter aims at providing an overview of some of the main issues addressed in a data science project. Because time is limited, however, these notes will only cover a selected set of topics.  
Actually, this constraint makes this overview even more important because it builds the framework where to place the future techniques learned in or outside this course.

## Universal scope

Data science addresses a very large set of issues. This latter has been expanding in the last decades thanks to the availability of computing power, data sets, new software and theoretical developments.  
Here is a very short list of cases handled by data science (sources: @esl, @isl and @isln).

## Statistical learning

The original postulate is that there exist a relationship between a _response_ \(Y\) variable and, **jointly** a set \(X\) of variables ( _independent variables_, _predictors_, _explanatory variables_).


```r
require(gridExtra)
require(tidyverse)
advertising <- read_csv("Advertising.csv")
advertising
#R> # A tibble: 200 x 5
#R>       X1    TV radio newspaper sales
#R>    <dbl> <dbl> <dbl>     <dbl> <dbl>
#R>  1     1 230.   37.8      69.2  22.1
#R>  2     2  44.5  39.3      45.1  10.4
#R>  3     3  17.2  45.9      69.3   9.3
#R>  4     4 152.   41.3      58.5  18.5
#R>  5     5 181.   10.8      58.4  12.9
#R>  6     6   8.7  48.9      75     7.2
#R>  7     7  57.5  32.8      23.5  11.8
#R>  8     8 120.   19.6      11.6  13.2
#R>  9     9   8.6   2.1       1     4.8
#R> 10    10 200.    2.6      21.2  10.6
#R> # ... with 190 more rows

p1 <- advertising %>% ggplot(
	mapping= aes(x=TV, y= sales)
	) +
	geom_point() +
	geom_smooth(method='lm', se = FALSE)

p2 <- advertising %>% ggplot(
	mapping= aes(x=radio, y= sales)
	) +
	geom_point() +
  geom_smooth(method='lm', se = FALSE)

p3 <- advertising %>% ggplot(
	mapping= aes(x=newspaper, y= sales)
	) +
	geom_point() +
  geom_smooth(method='lm', se = FALSE)

grid.arrange(p1, p2, p3, ncol=3)
```


\includegraphics[width=1\linewidth]{MyR_files/figure-latex/unnamed-chunk-174-1} 

```r

# require(GGally)
# ggpairs(advertising)
```


Then, the general form of the relationship between these variables is as follows.
\[Y=f(X) + \varepsilon \]
where \(\varepsilon\) captures various sources of error.  
We will denote by \(n\) the number of observations, i.e., the number of tuples containing a value of response and a value for each predictor. Also, \(p\) is the number of predictors.   
It is useful to see the different objects of the equation above.
\[\left( \begin{array}{l} y_1 \\ y_2 \\ \vdots \\ y_n \end{array}\right) =f\left( \begin{array}{llll} x_{11} & x_{12} & \dots & x_{1p} \\
x_{21} & x_{22} & \dots & x_{2p} \\
\vdots & \vdots & \ddots & \vdots \\
x_{n1} & x_{n2} & \dots & x_{np} \end{array}\right) 
+
\left( \begin{array}{l} \varepsilon_1 \\ \varepsilon_2 \\ \vdots \\ \varepsilon_n \end{array}\right)
\] 


The **goal of statistical learning is to estimate** (learn, determine, guess,...)  \(f()\).  
Figure \@ref(fig:plot-simf12-book) illustrates the data learning process by plotting \(Y\) for the values of \(X\), a unique vector (left) along with the errors measured as the difference between the observations and the true function (right). Notice that the true function is known in this case because the data is simulated.  
The different techniques explored here are designed to come as close as possible to the true, blue line.  

## Use of statistical learning

There are two main reasons one would want to estimate \(f()\).  

### Prediction

In many occasions, the independent variables are known but the response is not. Therefore, \(f()\) can be used to _predict_ these values. These predictions are noted by
\[\hat{Y}=\hat{f}(X)\]
where \(\hat{f}\) is the estimated function for \(f()\).

### Inference

The estimated \(\hat{f}()\) is also used to answer questions about the relationship between the independent variables and the response variables, such as:

  - which predictors contributes the response,
  - how much each predictor contributes to the response,
  - what is the form of the relationship.

This use of statistical learning is not the main interest of these notes (see Section \@ref(aiwhy)).     

## Classification setting

In classification problems, one cannot calculate the MSE. Instead, the common measure to assess accuracy if the **error rate**, the proportion or miss-classified observations, defined in the training set as
\[\frac{1}{n}\sum_i^n I\big(y_i\neq\hat{y}_i\big)\]
Similarly, in the test data, we can calculate
\[\text{Ave}\big(I(y_i\neq\hat{y}_i)\big)\] 


### Bayes classifier

It can be shown that the error rate in the test data is minimized by a classifier that assigns the observation to the class  for which it has the highest probability of belonging.  
This classifier is called _Bayes classifier_ and is based on the conditional probabilities for each \(j\) 
\[Pr(Y=j \vert X=x_0)\]
The problem is that, unless the data is simulated (as below), these probabilities are not known.
Figure \@ref(fig:plot-bayesc01) illustrates a simulated case and draws the contours given by the Bayes classifier. 

### K-nearest neighbors 

As a feasible solution, one could try to estimate the conditional probabilities. Some techniques attempt precisely that.  
Here, we quickly introduce a very simple non-parametric method, _K-nearest neighbors_. As it names indicates, the probability of a class is estimaded by an averaging of the \(K\) closest observations. Formely

\[Pr(Y=j \vert X=x_0)= \frac{1}{K}\sum_{i \in N(x_0)}I(y_i=j) \]









<!--chapter:end:28-overview.Rmd-->

---
title: "Linear Regression"
output: html_document
---

# Linear Regression

Let's start with a general defintion of what linear regression is and what it is used for:

In general, linear regression is a linear approach to modeling the relationship between a scalar response and one or more explanatory variables. In other words, linear regression is a useful tool to predict the value of an outcome variable Y based on one or more input predictor variables X. 

Objective: The objective is therefore to establish a linear relationship (mathematical formula) between the predictor variable(s) and the response variable, in order to be able to use this formula to estimate the value of the response variable Y, when only the predictor (Xs) variables or values are known.

The above mentioned mathematical equation can be generalized as follows:

\[Y=\beta_0 + \beta_1X_1 + \beta_2X_2 + \dots + \beta_pX_p + \varepsilon\]

β1 is the intercept
β2 is the slope

Collectively, they are called regression coefficients. 

ϵ is the error term (also descriped as the part of Y the regression model is unable to explain)

Example Problem:

For this analysis, we will use the cars dataset that comes with R by default. cars is a standard built-in dataset, that makes it convenient to demonstrate linear regression in a simple and easy to understand fashion. You can access this dataset simply by typing in cars in your R console. You will find that it consists of 50 observations(rows) and 2 variables (columns) – dist and speed. Lets print out the first six observations here..



```r
require(tidyverse)
advertising <- read_csv("Advertising.csv")
advertising
#R> # A tibble: 200 x 5
#R>       X1    TV radio newspaper sales
#R>    <dbl> <dbl> <dbl>     <dbl> <dbl>
#R>  1     1 230.   37.8      69.2  22.1
#R>  2     2  44.5  39.3      45.1  10.4
#R>  3     3  17.2  45.9      69.3   9.3
#R>  4     4 152.   41.3      58.5  18.5
#R>  5     5 181.   10.8      58.4  12.9
#R>  6     6   8.7  48.9      75     7.2
#R>  7     7  57.5  32.8      23.5  11.8
#R>  8     8 120.   19.6      11.6  13.2
#R>  9     9   8.6   2.1       1     4.8
#R> 10    10 200.    2.6      21.2  10.6
#R> # ... with 190 more rows

advertising <- read_csv("Advertising.csv")
advertising
#R> # A tibble: 200 x 5
#R>       X1    TV radio newspaper sales
#R>    <dbl> <dbl> <dbl>     <dbl> <dbl>
#R>  1     1 230.   37.8      69.2  22.1
#R>  2     2  44.5  39.3      45.1  10.4
#R>  3     3  17.2  45.9      69.3   9.3
#R>  4     4 152.   41.3      58.5  18.5
#R>  5     5 181.   10.8      58.4  12.9
#R>  6     6   8.7  48.9      75     7.2
#R>  7     7  57.5  32.8      23.5  11.8
#R>  8     8 120.   19.6      11.6  13.2
#R>  9     9   8.6   2.1       1     4.8
#R> 10    10 200.    2.6      21.2  10.6
#R> # ... with 190 more rows
```

Before we begin building the regression model, it is a good practice to analyze and understand the variables. The graphical analysis and correlation study below will help with this.

## Graphical Analysis

The aim of this exercise is to build a simple regression model that we can use to predict Distance (dist) by establishing a statistically significant linear relationship with Speed (speed). But before jumping in to the syntax, lets try to understand these variables graphically. Typically, for each of the independent variables (predictors), the following plots are drawn to visualize the following behavior:

Scatter plot: Visualize the linear relationship between the predictor and response.


```r
scatter.smooth(x=advertising$sales, y=advertising$TV, main="Sales ~ TV")  # scatterplot
```

![](MyR_files/figure-latex/unnamed-chunk-176-1.pdf)<!-- --> 

Box plot: To spot any outlier observations in the variable. 

Generally, any datapoint that lies outside the 1.5 * interquartile-range (1.5 * IQR) is considered an outlier, where, IQR is calculated as the distance between the 25th percentile and 75th percentile values for that variable.


```r
par(mfrow=c(1, 2))  # divide graph area in 2 columns
boxplot(advertising$sales, main="Sales", sub=paste("Outlier rows: ", boxplot.stats(advertising$sales)$out))  # box plot for 'Sales'
boxplot(advertising$TV, main="TV", sub=paste("Outlier rows: ", boxplot.stats(advertising$TV)$out))  # box plot for 'TV'
```

![](MyR_files/figure-latex/unnamed-chunk-177-1.pdf)<!-- --> 

Density plot: To see the distribution of the predictor variable. 


```r
library(e1071)
par(mfrow=c(1, 2))  # divide graph area in 2 columns
plot(density(advertising$sales), 
     main="Density Plot: Sales", ylab="Frequency", sub=paste("Skewness:", round(e1071::skewness(advertising$sales), 2)))  # density plot for 'Sales'
polygon(density(advertising$sales), col="red")
plot(density(advertising$TV), main="Density Plot: TV", 
     ylab="Frequency", sub=paste("Skewness:", 
      round(e1071::skewness(advertising$TV), 2)))  # density plot for 'TV'
polygon(density(advertising$TV), col="blue")
```

![](MyR_files/figure-latex/unnamed-chunk-178-1.pdf)<!-- --> 

Correlation:

Correlation is a statistical measure that suggests the level of linear dependence between two variables, that occur in pair – just like what we have here in sales and TV. 

High correlation = Correlation close to 1

Inverse relationship = Correlation close to -1

Weak correlation = Correlation close to 0


```r
cor(advertising$sales, advertising$TV)  # calculate correlation between sales and TV 
#R> [1] 0.7822244
```

## Simple linear regression

After applying a graphical analysis, we will now move over to a simple linear regression and apply the data from above.

This section therefore builds around the example of the simple linear regression of _sales_ on the amount of _TV_ advertising in the _Advertising_ data set.  
To fix ideas, the linear model estimated here is
\[\text{sales} = \beta_0 + \beta_1\times \text{TV}  + \varepsilon\]

The **estimation** of the model is carried with the function `lm` from the built-in `stats` package. The result of the estimation is an object to assigned to a name.


```r
estimation.mod <- lm(sales ~ TV, data = advertising)
```

The content of this linear regression object is better described with the function `summary`.


```r
summary(estimation.mod)
#R> 
#R> Call:
#R> lm(formula = sales ~ TV, data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -8.3860 -1.9545 -0.1913  2.0671  7.2124 
#R> 
#R> Coefficients:
#R>             Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept) 7.032594   0.457843   15.36   <2e-16 ***
#R> TV          0.047537   0.002691   17.67   <2e-16 ***
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 3.259 on 198 degrees of freedom
#R> Multiple R-squared:  0.6119,	Adjusted R-squared:  0.6099 
#R> F-statistic: 312.1 on 1 and 198 DF,  p-value: < 2.2e-16
names(estimation.mod)
#R>  [1] "coefficients"  "residuals"     "effects"       "rank"         
#R>  [5] "fitted.values" "assign"        "qr"            "df.residual"  
#R>  [9] "xlevels"       "call"          "terms"         "model"

estimation.mod$fitted.values
#R>         1         2         3         4         5         6         7 
#R> 17.970775  9.147974  7.850224 14.234395 15.627218  7.446162  9.765950 
#R>         8         9        10        11        12        13        14 
#R> 12.746498  7.441409 16.530414 10.174765 17.238710  8.163966 11.667416 
#R>        15        16        17        18        19        20        21 
#R> 16.734822 16.321253 10.255578 20.409404 10.322129 14.034741 17.414596 
#R>        22        23        24        25        26        27        28 
#R> 18.317792  7.660077 17.885209  9.994126 19.529976 13.825579 18.446141 
#R>        29        30        31        32        33        34        35 
#R> 18.859710 10.388680 20.956076 12.399480 11.653155 19.658325 11.581850 
#R>        36        37        38        39        40        41        42 
#R> 20.851495 19.720123 10.583581  9.081423 17.870948 16.658763 15.446579 
#R>        43        44        45        46        47        48        49 
#R> 20.989351 16.867924  8.225763 15.356259 11.296630 18.436634 17.832918 
#R>        50        51        52        53        54        55        56 
#R> 10.212795 16.530414 11.805272 17.319523 15.712784 19.520469 16.487631 
#R>        57        58        59        60        61        62        63 
#R>  7.379611 13.507084 17.053317 17.048564  9.575804 19.453918 18.408112 
#R>        64        65        66        67        68        69        70 
#R> 11.914607 13.264647 10.312622  8.529998 13.654448 18.317792 17.338537 
#R>        71        72        73        74        75        76        77 
#R> 16.497139 12.252117  8.306576 13.183835 17.176913  7.835963  8.339851 
#R>        78        79        80        81        82        83        84 
#R> 12.760759  7.289291 12.546844 10.664393 18.431880 10.612103 10.284100 
#R>        85        86        87        88        89        90        91 
#R> 17.181666 16.216672 10.659639 12.294900 11.230079 12.252117 13.416764 
#R>        92        93        94        95        96        97        98 
#R>  8.392141 17.381320 18.959537 12.138029 14.795327 16.425834 15.822118 
#R>        99       100       101       102       103       104       105 
#R> 20.803958 13.459547 17.604742 21.122454 20.352360 15.964728 18.355821 
#R>       106       107       108       109       110       111       112 
#R> 13.587896  8.221010 11.329906  7.655324 19.173452 17.766367 18.522200 
#R>       113       114       115       116       117       118       119 
#R> 15.384781 16.996273 10.749959 10.602595 13.649694 10.664393 13.007949 
#R>       120       121       122       123       124       125       126 
#R>  7.954804 13.749521  7.926282 17.680801 12.884354 17.942253 11.177789 
#R>       127       128       129       130       131       132       133 
#R>  7.403379 10.845032 17.504915  9.865777  7.065869 19.639311  7.431901 
#R>       134       135       136       137       138       139       140 
#R> 17.481147  8.786696  9.328613  8.249532 20.043372  9.076669 15.822118 
#R>       141       142       143       144       145       146       147 
#R> 10.521783 16.240441 17.514423 12.004926 11.605618 13.701984 18.446141 
#R>       148       149       150       151       152       153       154 
#R> 18.593505  8.838986  9.157481 20.376129 12.784527 16.425834 15.175620 
#R>       155       156       157       158       159       160       161 
#R> 15.959975  7.227494 11.496284 14.153582  7.588772 13.293169 15.232664 
#R>       162       163       164       165       166       167       168 
#R> 11.106484 15.988497 14.804834 12.603888 18.179936  7.883499 16.863171 
#R>       169       170       171       172       173       174       175 
#R> 17.271986 20.547260  9.409426 14.852371  7.964312 15.037764 17.604742 
#R>       176       177       178       179       180       181       182 
#R> 20.195489 18.840695 15.123330 20.185982 14.904661 14.476831 17.419349 
#R>       183       184       185       186       187       188       189 
#R>  9.704153 20.704131 19.097393 16.777605 13.663955 16.116846 20.628073 
#R>       190       191       192       193       194       195       196 
#R>  7.921529  8.910291 10.621610  7.850224 14.961705 14.148829  8.848493 
#R>       197       198       199       200 
#R> 11.510545 15.446579 20.513985 18.065848

names(summary(estimation.mod))
#R>  [1] "call"          "terms"         "residuals"     "coefficients" 
#R>  [5] "aliased"       "sigma"         "df"            "r.squared"    
#R>  [9] "adj.r.squared" "fstatistic"    "cov.unscaled"
summary(estimation.mod)$r.squared
#R> [1] 0.6118751
summary(estimation.mod)$df
#R> [1]   2 198   2
```


```r
# tidyverse alternative
advertising %>%
  mutate(y.hat1 = estimation.mod$fitted.values,
         y.hat2 <- predict(estimation.mod),
         y.hat3 <- estimation.mod$coefficients[1] + 
           estimation.mod$coefficients[2]*TV)
#R> # A tibble: 200 x 8
#R>       X1    TV radio newspaper sales y.hat1 `y.hat2 <- predi~ `... <- NULL`
#R>    <dbl> <dbl> <dbl>     <dbl> <dbl>  <dbl>             <dbl>         <dbl>
#R>  1     1 230.   37.8      69.2  22.1  18.0              18.0          18.0 
#R>  2     2  44.5  39.3      45.1  10.4   9.15              9.15          9.15
#R>  3     3  17.2  45.9      69.3   9.3   7.85              7.85          7.85
#R>  4     4 152.   41.3      58.5  18.5  14.2              14.2          14.2 
#R>  5     5 181.   10.8      58.4  12.9  15.6              15.6          15.6 
#R>  6     6   8.7  48.9      75     7.2   7.45              7.45          7.45
#R>  7     7  57.5  32.8      23.5  11.8   9.77              9.77          9.77
#R>  8     8 120.   19.6      11.6  13.2  12.7              12.7          12.7 
#R>  9     9   8.6   2.1       1     4.8   7.44              7.44          7.44
#R> 10    10 200.    2.6      21.2  10.6  16.5              16.5          16.5 
#R> # ... with 190 more rows

advertising
#R> # A tibble: 200 x 5
#R>       X1    TV radio newspaper sales
#R>    <dbl> <dbl> <dbl>     <dbl> <dbl>
#R>  1     1 230.   37.8      69.2  22.1
#R>  2     2  44.5  39.3      45.1  10.4
#R>  3     3  17.2  45.9      69.3   9.3
#R>  4     4 152.   41.3      58.5  18.5
#R>  5     5 181.   10.8      58.4  12.9
#R>  6     6   8.7  48.9      75     7.2
#R>  7     7  57.5  32.8      23.5  11.8
#R>  8     8 120.   19.6      11.6  13.2
#R>  9     9   8.6   2.1       1     4.8
#R> 10    10 200.    2.6      21.2  10.6
#R> # ... with 190 more rows
advertising$TV
#R>   [1] 230.1  44.5  17.2 151.5 180.8   8.7  57.5 120.2   8.6 199.8  66.1
#R>  [12] 214.7  23.8  97.5 204.1 195.4  67.8 281.4  69.2 147.3 218.4 237.4
#R>  [23]  13.2 228.3  62.3 262.9 142.9 240.1 248.8  70.6 292.9 112.9  97.2
#R>  [34] 265.6  95.7 290.7 266.9  74.7  43.1 228.0 202.5 177.0 293.6 206.9
#R>  [45]  25.1 175.1  89.7 239.9 227.2  66.9 199.8 100.4 216.4 182.6 262.7
#R>  [56] 198.9   7.3 136.2 210.8 210.7  53.5 261.3 239.3 102.7 131.1  69.0
#R>  [67]  31.5 139.3 237.4 216.8 199.1 109.8  26.8 129.4 213.4  16.9  27.5
#R>  [78] 120.5   5.4 116.0  76.4 239.8  75.3  68.4 213.5 193.2  76.3 110.7
#R>  [89]  88.3 109.8 134.3  28.6 217.7 250.9 107.4 163.3 197.6 184.9 289.7
#R> [100] 135.2 222.4 296.4 280.2 187.9 238.2 137.9  25.0  90.4  13.1 255.4
#R> [111] 225.8 241.7 175.7 209.6  78.2  75.1 139.2  76.4 125.7  19.4 141.3
#R> [122]  18.8 224.0 123.1 229.5  87.2   7.8  80.2 220.3  59.6   0.7 265.2
#R> [133]   8.4 219.8  36.9  48.3  25.6 273.7  43.0 184.9  73.4 193.7 220.5
#R> [144] 104.6  96.2 140.3 240.1 243.2  38.0  44.7 280.7 121.0 197.6 171.3
#R> [155] 187.8   4.1  93.9 149.8  11.7 131.7 172.5  85.7 188.4 163.5 117.2
#R> [166] 234.5  17.9 206.8 215.4 284.3  50.0 164.5  19.6 168.4 222.4 276.9
#R> [177] 248.4 170.2 276.7 165.6 156.6 218.5  56.2 287.6 253.8 205.0 139.5
#R> [188] 191.1 286.0  18.7  39.5  75.5  17.2 166.8 149.7  38.2  94.2 177.0
#R> [199] 283.6 232.1
advertising$y.hat1 <- estimation.mod$fitted.values
advertising$y.hat2 <- predict(estimation.mod)
advertising$y.hat3 <- estimation.mod$coefficients[1] + estimation.mod$coefficients[2]*advertising$TV


advertising
#R> # A tibble: 200 x 8
#R>       X1    TV radio newspaper sales y.hat1 y.hat2 y.hat3
#R>    <dbl> <dbl> <dbl>     <dbl> <dbl>  <dbl>  <dbl>  <dbl>
#R>  1     1 230.   37.8      69.2  22.1  18.0   18.0   18.0 
#R>  2     2  44.5  39.3      45.1  10.4   9.15   9.15   9.15
#R>  3     3  17.2  45.9      69.3   9.3   7.85   7.85   7.85
#R>  4     4 152.   41.3      58.5  18.5  14.2   14.2   14.2 
#R>  5     5 181.   10.8      58.4  12.9  15.6   15.6   15.6 
#R>  6     6   8.7  48.9      75     7.2   7.45   7.45   7.45
#R>  7     7  57.5  32.8      23.5  11.8   9.77   9.77   9.77
#R>  8     8 120.   19.6      11.6  13.2  12.7   12.7   12.7 
#R>  9     9   8.6   2.1       1     4.8   7.44   7.44   7.44
#R> 10    10 200.    2.6      21.2  10.6  16.5   16.5   16.5 
#R> # ... with 190 more rows

plot(advertising$TV, advertising$sales)
lines(advertising$TV, advertising$y.hat2, col="blue")
lines(advertising$TV, advertising$y.hat1, col="red")
```

![](MyR_files/figure-latex/unnamed-chunk-182-1.pdf)<!-- --> 

Let's now have a look at the **errors/ residuals** of our prediction.

```r
advertising$residuals <- advertising$sales - advertising$y.hat2

sum(advertising$residuals)
#R> [1] -1.029399e-12
```

Prediction of sales: We can now use the model to predict for data that not in the training data.


```r
# predict sales for TV=400, 500, 600...

# brute force way, very tedious in general
sales_tv_400 <- estimation.mod$coefficients[1] + 
  estimation.mod$coefficients[2]*400
sales_tv_400
#R> (Intercept) 
#R>    26.04725

# 'predict' way
# step 1: create a data.frame for the new X data
# step 2: predict with newdata= newdata

my.boss.question <- data.frame(TV=c(400, 500, 600))
my.boss.question
#R>    TV
#R> 1 400
#R> 2 500
#R> 3 600

sales_tv_boss <- predict(estimation.mod, newdata = my.boss.question ) 
sales_tv_boss
#R>        1        2        3 
#R> 26.04725 30.80091 35.55458
```


This last call alone provides a variety of statistics given in the package of `isln`.
Notice that parts of this regression object can be accessed through sub-setting of the object and used, once we know under what name they are stored, which we obtain by the next call (see `?lm` for the value of the function, i.e., what the function returns).


```r
names(estimation.mod)
#R>  [1] "coefficients"  "residuals"     "effects"       "rank"         
#R>  [5] "fitted.values" "assign"        "qr"            "df.residual"  
#R>  [9] "xlevels"       "call"          "terms"         "model"
# estimation.mod %>% names
```

Alternatively, and somehow more surprising, all the numbers given by the `summary` function can also be accessed in the same fashion:


```r
estimation.mod %>% summary %>% names
#R>  [1] "call"          "terms"         "residuals"     "coefficients" 
#R>  [5] "aliased"       "sigma"         "df"            "r.squared"    
#R>  [9] "adj.r.squared" "fstatistic"    "cov.unscaled"
```

As an example, the following table can be built by inline R-code (`isln`), with calls such as `summary(estimation.mod)$fstatistic[1]`, possibly with rounding as well.

| Quantity | Value |
|:--|:--|
| Residual Standard Error | 3.26 |
| \(R^2\) | 0.612 |
| \(F\)-statistic | 312.1 |

Table: Results for simple linear regression (Advertising)


As for the **confidence interval** of \(\beta_1\) (`isln`), i.e., the random interval in which, under repeated sampling, the true parameter would fall \(95\%\) of the time, we type the code below.


```r
c.i.beta1 <- c(summary(estimation.mod)$coefficients[2,1] -
                 2 * summary(estimation.mod)$coefficients[2,2],
               summary(estimation.mod)$coefficients[2,1] +
                 2 * summary(estimation.mod)$coefficients[2,2])
c.i.beta1 %>% round(3)
#R> [1] 0.042 0.053
```

One of the main reasons the simple linear regression is exposed is its graphical appeal. In particular, the _ordinary least squares_ criterion can be visualized with a graph of the residuals with respect to the fit.  
This visualization builds on the regression fit which we obtain first below in two alternative ways.  

1. The **fitted line** can be obtained with the fitted values of the model given by the `lm` function, i.e., `.$fitted.values`.


```r
tibble(advertising$TV, advertising$sales, estimation.mod$fitted.values)
#R> # A tibble: 200 x 3
#R>    `advertising$TV` `advertising$sales` `estimation.mod$fitted.values`
#R>               <dbl>               <dbl>                          <dbl>
#R>  1            230.                 22.1                          18.0 
#R>  2             44.5                10.4                           9.15
#R>  3             17.2                 9.3                           7.85
#R>  4            152.                 18.5                          14.2 
#R>  5            181.                 12.9                          15.6 
#R>  6              8.7                 7.2                           7.45
#R>  7             57.5                11.8                           9.77
#R>  8            120.                 13.2                          12.7 
#R>  9              8.6                 4.8                           7.44
#R> 10            200.                 10.6                          16.5 
#R> # ... with 190 more rows
```

Digging into the details, these fitted values  are simply obtained thanks to the estimated parameters using the \(X\) values (_TV_, in this case). 


```r
manually.fitted <- estimation.mod$coefficients[1] + 
  estimation.mod$coefficients[2] * advertising$TV
all.equal(as.vector(estimation.mod$fitted.values), 
          manually.fitted)
#R> [1] TRUE
```

2. The second approach uses the function `predict` from the built-in `stats` package. The function is a bit versatile as its behavior depends on which type of objects it is fed with.  
Applied to a `lm` object, it will, by default, return **predictions** for each of the \(X\) values  used to fit the model. 


```r
all.equal(as.vector(estimation.mod$fitted.values), 
          manually.fitted, predict(estimation.mod))
#R> [1] TRUE
```

Thanks to the fitted/predicted value, we can calculate the values above about the quality of the fit. Here are a few lines of code to manually calculate these statistics.


```r
## R2
TSS <- sum((advertising$sales - mean(advertising$sales))^2)
TSS
#R> [1] 5417.149

RSS <- sum((advertising$sales -  predict(estimation.mod))^2)
RSS
#R> [1] 2102.531

R2 <- 1 - RSS/TSS
R2 %>% round(3)
#R> [1] 0.612

## RSE
n <- length(advertising$sales)
p <- length(estimation.mod$coefficients) - 1
RSE <- sqrt(RSS /(n - p - 1))
RSE %>% round(2)
#R> [1] 3.26
# notice that this is more or less the sd of the errors
sd(advertising$sales -  predict(estimation.mod)) %>% round(2)
#R> [1] 3.25

## F-statistic
F <- (TSS - RSS)/p * (RSS/(n-p-1))^(-1)
F %>% round(1)
#R> [1] 312.1
```

We can now turn to the **graph** of the fit.  
As much as possible, we want to use `ggplot` for our graphs. In this case, we must first add the predicted/fitted values to the data frame. There are various, though similar ways to achieve that first step, including one with `geom_smooth`.


```r

advertising <- advertising %>%
	mutate(fit_TV= estimation.mod$fitted.values)
	# mutate(fit_TV= predict(estimation.mod))
	# mutate(fit_TV = predict(lm(sales ~ TV), interval = "confidence")[,"fit"])
         

p1 <- advertising %>% ggplot(
	mapping= aes(x=TV, y= sales)
	) +
	geom_point(size=1, shape=21) +
	#geom_smooth(method='lm', se = TRUE) + # another alternative for the fit
	geom_line(aes(y=fit_TV), color ="blue", size =1) +
	geom_segment(aes(x = TV, y = sales, xend = TV, yend = fit_TV, colour = "red")) +
	theme(legend.position = "none")
p1
```


\includegraphics[width=1\linewidth]{MyR_files/figure-latex/unnamed-chunk-192-1} 

## Multiple linear regression

The treatment of the multiple linear regression is similar to the part above. The differences include:

* The command for the `lm` function;
* No graphical representation;
* The often tedious interpretation of the coefficients.

We proceed by estimating 

\[\text{sales} = \beta_0 + \beta_1\times \text{TV} + \beta_2\times \text{radio} + \beta_3\times \text{newspaper}  + \varepsilon\]



```r
estimation.mod2 <- lm(sales ~ TV + radio + newspaper, data = advertising)
```

Importantly, the `+` sign does not mean that the regression is on the sum of the variables. 

Instead, the expression should be read "regression of sales on TV _plus on_ radio _plus on_ newspaper".


```r
summary(estimation.mod2)
#R> 
#R> Call:
#R> lm(formula = sales ~ TV + radio + newspaper, data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -8.8277 -0.8908  0.2418  1.1893  2.8292 
#R> 
#R> Coefficients:
#R>              Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)  2.938889   0.311908   9.422   <2e-16 ***
#R> TV           0.045765   0.001395  32.809   <2e-16 ***
#R> radio        0.188530   0.008611  21.893   <2e-16 ***
#R> newspaper   -0.001037   0.005871  -0.177     0.86    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 1.686 on 196 degrees of freedom
#R> Multiple R-squared:  0.8972,	Adjusted R-squared:  0.8956 
#R> F-statistic: 570.3 on 3 and 196 DF,  p-value: < 2.2e-16
```

For the interpretation of the coefficients, the correlations between the predictors is often useful.


```r
advertising %>% {cor(.[,c("TV", "radio", "newspaper")])} %>% round(4)
#R>               TV  radio newspaper
#R> TV        1.0000 0.0548    0.0566
#R> radio     0.0548 1.0000    0.3541
#R> newspaper 0.0566 0.3541    1.0000
```

## Categorical regressors

The predictors of the model need not be numeric variables. They can also be factors.

In order to closely follow `isln`, we now load another data set, `Credit` from the package `ISLR`.


```r
require(ISLR)
data("Credit")
str(Credit)
#R> 'data.frame':	400 obs. of  12 variables:
#R>  $ ID       : int  1 2 3 4 5 6 7 8 9 10 ...
#R>  $ Income   : num  14.9 106 104.6 148.9 55.9 ...
#R>  $ Limit    : int  3606 6645 7075 9504 4897 8047 3388 7114 3300 6819 ...
#R>  $ Rating   : int  283 483 514 681 357 569 259 512 266 491 ...
#R>  $ Cards    : int  2 3 4 3 2 4 2 2 5 3 ...
#R>  $ Age      : int  34 82 71 36 68 77 37 87 66 41 ...
#R>  $ Education: int  11 15 11 11 16 10 12 9 13 19 ...
#R>  $ Gender   : Factor w/ 2 levels " Male","Female": 1 2 1 2 1 1 2 1 2 2 ...
#R>  $ Student  : Factor w/ 2 levels "No","Yes": 1 2 1 1 1 1 1 1 1 2 ...
#R>  $ Married  : Factor w/ 2 levels "No","Yes": 2 2 1 1 2 1 1 1 1 2 ...
#R>  $ Ethnicity: Factor w/ 3 levels "African American",..: 3 2 2 2 3 3 1 2 3 1 ...
#R>  $ Balance  : int  333 903 580 964 331 1151 203 872 279 1350 ...
```

The scatter plots for each pair of variables is a useful visualization.


```r
require(GGally)
ggpairs(Credit[,c("Balance", "Age", "Cards", "Education",
                  "Income", "Limit", "Rating")])
```


\includegraphics[width=1\linewidth]{MyR_files/figure-latex/unnamed-chunk-197-1} 

The key element in this section is the qualitatitive / categorical predictors, also called factor variables.   
In the `Credit` data set, variables such `gender` or `student` are factors.  

We illustrate here how these variables can be used in a linear regression.


```r
model.credit <- lm(Balance ~ Gender, data = Credit)
summary(model.credit)
#R> 
#R> Call:
#R> lm(formula = Balance ~ Gender, data = Credit)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -529.54 -455.35  -60.17  334.71 1489.20 
#R> 
#R> Coefficients:
#R>              Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)    509.80      33.13  15.389   <2e-16 ***
#R> GenderFemale    19.73      46.05   0.429    0.669    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 460.2 on 398 degrees of freedom
#R> Multiple R-squared:  0.0004611,	Adjusted R-squared:  -0.00205 
#R> F-statistic: 0.1836 on 1 and 398 DF,  p-value: 0.6685
```

This seems to work seemlessly. There is a detail, however that must be brought into the light.  
`R` has automatically created a dummy variable. This may or may not be the intended choice.  
The exact choice can be examined with the following call.


```r
contrasts(Credit$Gender)
#R>        Female
#R>  Male       0
#R> Female      1
```
We see that the variable `GenderFemale` (read in the upper part of the table) shown in the summary of the model takes the value \(0\) if the individual is Male and \(1\) if the individual is Female.   
With multiple factors in the variable, the reading of the table must be well understood.


```r
contrasts(Credit$Ethnicity)
#R>                  Asian Caucasian
#R> African American     0         0
#R> Asian                1         0
#R> Caucasian            0         1
```

These values are used in the next model.


```r
model.credit2 <- lm(Balance ~ Ethnicity, data = Credit)
summary(model.credit2)
#R> 
#R> Call:
#R> lm(formula = Balance ~ Ethnicity, data = Credit)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -531.00 -457.08  -63.25  339.25 1480.50 
#R> 
#R> Coefficients:
#R>                    Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)          531.00      46.32  11.464   <2e-16 ***
#R> EthnicityAsian       -18.69      65.02  -0.287    0.774    
#R> EthnicityCaucasian   -12.50      56.68  -0.221    0.826    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 460.9 on 397 degrees of freedom
#R> Multiple R-squared:  0.0002188,	Adjusted R-squared:  -0.004818 
#R> F-statistic: 0.04344 on 2 and 397 DF,  p-value: 0.9575
```

Notice that these dummy values are created in alphabetical order. Hence, the first will always server as reference.  
This behavior can be changed thanks to the `relevel` function.


```r
Credit$Ethnicity <- relevel(Credit$Ethnicity, ref = "Caucasian")
contrasts(Credit$Ethnicity)
#R>                  African American Asian
#R> Caucasian                       0     0
#R> African American                1     0
#R> Asian                           0     1
```


## Interactions terms

Notice that the \(\beta\)'s represent the average effect of a one unit change in the predictor on the response.  
The assumption of a constant effect on the response, i.e., constant \(\beta_i\), is often difficult to sustain. For instance, in case of synergies of the advertising media, the effect of one particular media depends on how much of the other media are already been run.  
Interactions terms constitute a variation of the linear regression whose aim is precisely to allow for non-constant effects of variables on the response.  
The interaction between variables are built with the `:` symbol. For instance, the result in @isln, Chap. 3, slide 37 is obtained through the following call.


```r
model.interaction1 <- lm(sales ~ TV + radio + TV:radio, data = advertising)
summary(model.interaction1) 
#R> 
#R> Call:
#R> lm(formula = sales ~ TV + radio + TV:radio, data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -6.3366 -0.4028  0.1831  0.5948  1.5246 
#R> 
#R> Coefficients:
#R>              Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept) 6.750e+00  2.479e-01  27.233   <2e-16 ***
#R> TV          1.910e-02  1.504e-03  12.699   <2e-16 ***
#R> radio       2.886e-02  8.905e-03   3.241   0.0014 ** 
#R> TV:radio    1.086e-03  5.242e-05  20.727   <2e-16 ***
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 0.9435 on 196 degrees of freedom
#R> Multiple R-squared:  0.9678,	Adjusted R-squared:  0.9673 
#R> F-statistic:  1963 on 3 and 196 DF,  p-value: < 2.2e-16

## alternatively, use the cross *
lm(sales ~ TV*radio, data = advertising)
#R> 
#R> Call:
#R> lm(formula = sales ~ TV * radio, data = advertising)
#R> 
#R> Coefficients:
#R> (Intercept)           TV        radio     TV:radio  
#R>    6.750220     0.019101     0.028860     0.001086
```

Interactions can be done between quantitative and categorical variables. This case is actually the very easy to interpret and even visualize, despite the multiple variables.



```r
model.interaction2 <- lm(Balance ~  Income + Student, data = Credit)
summary(model.interaction2) 
#R> 
#R> Call:
#R> lm(formula = Balance ~ Income + Student, data = Credit)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -762.37 -331.38  -45.04  323.60  818.28 
#R> 
#R> Coefficients:
#R>             Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept) 211.1430    32.4572   6.505 2.34e-10 ***
#R> Income        5.9843     0.5566  10.751  < 2e-16 ***
#R> StudentYes  382.6705    65.3108   5.859 9.78e-09 ***
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 391.8 on 397 degrees of freedom
#R> Multiple R-squared:  0.2775,	Adjusted R-squared:  0.2738 
#R> F-statistic: 76.22 on 2 and 397 DF,  p-value: < 2.2e-16
model.interaction3 <- lm(Balance ~  Income + Student + Income:Student, data = Credit)
summary(model.interaction3) 
#R> 
#R> Call:
#R> lm(formula = Balance ~ Income + Student + Income:Student, data = Credit)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -773.39 -325.70  -41.13  321.65  814.04 
#R> 
#R> Coefficients:
#R>                   Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)       200.6232    33.6984   5.953 5.79e-09 ***
#R> Income              6.2182     0.5921  10.502  < 2e-16 ***
#R> StudentYes        476.6758   104.3512   4.568 6.59e-06 ***
#R> Income:StudentYes  -1.9992     1.7313  -1.155    0.249    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 391.6 on 396 degrees of freedom
#R> Multiple R-squared:  0.2799,	Adjusted R-squared:  0.2744 
#R> F-statistic:  51.3 on 3 and 396 DF,  p-value: < 2.2e-16


y.hat4 <- predict(model.interaction2)

plot(Credit$Income, Credit$Balance)
lines(Credit$Income, y.hat4, col="red")
```

![](MyR_files/figure-latex/unnamed-chunk-204-1.pdf)<!-- --> 

```r

s.data <- Credit
s.data$Student <- "Yes"

n.data <- Credit
n.data$Student <- "No"

y.hat5 <- predict(model.interaction2, newdata = s.data)

y.hat6 <- predict(model.interaction2, newdata = n.data)

plot(Credit$Income, Credit$Balance)
lines(Credit$Income, y.hat5, col="red")
lines(Credit$Income, y.hat6, col="black")
```

![](MyR_files/figure-latex/unnamed-chunk-204-2.pdf)<!-- --> 

```r
Credit
#R>      ID  Income Limit Rating Cards Age Education Gender Student Married
#R> 1     1  14.891  3606    283     2  34        11   Male      No     Yes
#R> 2     2 106.025  6645    483     3  82        15 Female     Yes     Yes
#R> 3     3 104.593  7075    514     4  71        11   Male      No      No
#R> 4     4 148.924  9504    681     3  36        11 Female      No      No
#R> 5     5  55.882  4897    357     2  68        16   Male      No     Yes
#R> 6     6  80.180  8047    569     4  77        10   Male      No      No
#R> 7     7  20.996  3388    259     2  37        12 Female      No      No
#R> 8     8  71.408  7114    512     2  87         9   Male      No      No
#R> 9     9  15.125  3300    266     5  66        13 Female      No      No
#R> 10   10  71.061  6819    491     3  41        19 Female     Yes     Yes
#R> 11   11  63.095  8117    589     4  30        14   Male      No     Yes
#R> 12   12  15.045  1311    138     3  64        16   Male      No      No
#R> 13   13  80.616  5308    394     1  57         7 Female      No     Yes
#R> 14   14  43.682  6922    511     1  49         9   Male      No     Yes
#R> 15   15  19.144  3291    269     2  75        13 Female      No      No
#R> 16   16  20.089  2525    200     3  57        15 Female      No     Yes
#R> 17   17  53.598  3714    286     3  73        17 Female      No     Yes
#R> 18   18  36.496  4378    339     3  69        15 Female      No     Yes
#R> 19   19  49.570  6384    448     1  28         9 Female      No     Yes
#R> 20   20  42.079  6626    479     2  44         9   Male      No      No
#R> 21   21  17.700  2860    235     4  63        16 Female      No      No
#R> 22   22  37.348  6378    458     1  72        17 Female      No      No
#R> 23   23  20.103  2631    213     3  61        10   Male      No     Yes
#R> 24   24  64.027  5179    398     5  48         8   Male      No     Yes
#R> 25   25  10.742  1757    156     3  57        15 Female      No      No
#R> 26   26  14.090  4323    326     5  25        16 Female      No     Yes
#R> 27   27  42.471  3625    289     6  44        12 Female     Yes      No
#R> 28   28  32.793  4534    333     2  44        16   Male      No      No
#R> 29   29 186.634 13414    949     2  41        14 Female      No     Yes
#R> 30   30  26.813  5611    411     4  55        16 Female      No      No
#R> 31   31  34.142  5666    413     4  47         5 Female      No     Yes
#R> 32   32  28.941  2733    210     5  43        16   Male      No     Yes
#R> 33   33 134.181  7838    563     2  48        13 Female      No      No
#R> 34   34  31.367  1829    162     4  30        10   Male      No     Yes
#R> 35   35  20.150  2646    199     2  25        14 Female      No     Yes
#R> 36   36  23.350  2558    220     3  49        12 Female     Yes      No
#R> 37   37  62.413  6457    455     2  71        11 Female      No     Yes
#R> 38   38  30.007  6481    462     2  69         9 Female      No     Yes
#R> 39   39  11.795  3899    300     4  25        10 Female      No      No
#R> 40   40  13.647  3461    264     4  47        14   Male      No     Yes
#R> 41   41  34.950  3327    253     3  54        14 Female      No      No
#R> 42   42 113.659  7659    538     2  66        15   Male     Yes     Yes
#R> 43   43  44.158  4763    351     2  66        13 Female      No     Yes
#R> 44   44  36.929  6257    445     1  24        14 Female      No     Yes
#R> 45   45  31.861  6375    469     3  25        16 Female      No     Yes
#R> 46   46  77.380  7569    564     3  50        12 Female      No     Yes
#R> 47   47  19.531  5043    376     2  64        16 Female     Yes     Yes
#R> 48   48  44.646  4431    320     2  49        15   Male     Yes     Yes
#R> 49   49  44.522  2252    205     6  72        15   Male      No     Yes
#R> 50   50  43.479  4569    354     4  49        13   Male     Yes     Yes
#R> 51   51  36.362  5183    376     3  49        15   Male      No     Yes
#R> 52   52  39.705  3969    301     2  27        20   Male      No     Yes
#R> 53   53  44.205  5441    394     1  32        12   Male      No     Yes
#R> 54   54  16.304  5466    413     4  66        10   Male      No     Yes
#R> 55   55  15.333  1499    138     2  47         9 Female      No     Yes
#R> 56   56  32.916  1786    154     2  60         8 Female      No     Yes
#R> 57   57  57.100  4742    372     7  79        18 Female      No     Yes
#R> 58   58  76.273  4779    367     4  65        14 Female      No     Yes
#R> 59   59  10.354  3480    281     2  70        17   Male      No     Yes
#R> 60   60  51.872  5294    390     4  81        17 Female      No      No
#R> 61   61  35.510  5198    364     2  35        20 Female      No      No
#R> 62   62  21.238  3089    254     3  59        10 Female      No      No
#R> 63   63  30.682  1671    160     2  77         7 Female      No      No
#R> 64   64  14.132  2998    251     4  75        17   Male      No      No
#R> 65   65  32.164  2937    223     2  79        15 Female      No     Yes
#R> 66   66  12.000  4160    320     4  28        14 Female      No     Yes
#R> 67   67 113.829  9704    694     4  38        13 Female      No     Yes
#R> 68   68  11.187  5099    380     4  69        16 Female      No      No
#R> 69   69  27.847  5619    418     2  78        15 Female      No     Yes
#R> 70   70  49.502  6819    505     4  55        14   Male      No     Yes
#R> 71   71  24.889  3954    318     4  75        12   Male      No     Yes
#R> 72   72  58.781  7402    538     2  81        12 Female      No     Yes
#R> 73   73  22.939  4923    355     1  47        18 Female      No     Yes
#R> 74   74  23.989  4523    338     4  31        15   Male      No      No
#R> 75   75  16.103  5390    418     4  45        10 Female      No     Yes
#R> 76   76  33.017  3180    224     2  28        16   Male      No     Yes
#R> 77   77  30.622  3293    251     1  68        16   Male     Yes      No
#R> 78   78  20.936  3254    253     1  30        15 Female      No      No
#R> 79   79 110.968  6662    468     3  45        11 Female      No     Yes
#R> 80   80  15.354  2101    171     2  65        14   Male      No      No
#R> 81   81  27.369  3449    288     3  40         9 Female      No     Yes
#R> 82   82  53.480  4263    317     1  83        15   Male      No      No
#R> 83   83  23.672  4433    344     3  63        11   Male      No      No
#R> 84   84  19.225  1433    122     3  38        14 Female      No      No
#R> 85   85  43.540  2906    232     4  69        11   Male      No      No
#R> 86   86 152.298 12066    828     4  41        12 Female      No     Yes
#R> 87   87  55.367  6340    448     1  33        15   Male      No     Yes
#R> 88   88  11.741  2271    182     4  59        12 Female      No      No
#R> 89   89  15.560  4307    352     4  57         8   Male      No     Yes
#R> 90   90  59.530  7518    543     3  52         9 Female      No      No
#R> 91   91  20.191  5767    431     4  42        16   Male      No     Yes
#R> 92   92  48.498  6040    456     3  47        16   Male      No     Yes
#R> 93   93  30.733  2832    249     4  51        13   Male      No      No
#R> 94   94  16.479  5435    388     2  26        16   Male      No      No
#R> 95   95  38.009  3075    245     3  45        15 Female      No      No
#R> 96   96  14.084   855    120     5  46        17 Female      No     Yes
#R> 97   97  14.312  5382    367     1  59        17   Male     Yes      No
#R> 98   98  26.067  3388    266     4  74        17 Female      No     Yes
#R> 99   99  36.295  2963    241     2  68        14 Female     Yes      No
#R> 100 100  83.851  8494    607     5  47        18   Male      No      No
#R> 101 101  21.153  3736    256     1  41        11   Male      No      No
#R> 102 102  17.976  2433    190     3  70        16 Female     Yes      No
#R> 103 103  68.713  7582    531     2  56        16   Male     Yes      No
#R> 104 104 146.183  9540    682     6  66        15   Male      No      No
#R> 105 105  15.846  4768    365     4  53        12 Female      No      No
#R> 106 106  12.031  3182    259     2  58        18 Female      No     Yes
#R> 107 107  16.819  1337    115     2  74        15   Male      No     Yes
#R> 108 108  39.110  3189    263     3  72        12   Male      No      No
#R> 109 109 107.986  6033    449     4  64        14   Male      No     Yes
#R> 110 110  13.561  3261    279     5  37        19   Male      No     Yes
#R> 111 111  34.537  3271    250     3  57        17 Female      No     Yes
#R> 112 112  28.575  2959    231     2  60        11 Female      No      No
#R> 113 113  46.007  6637    491     4  42        14   Male      No     Yes
#R> 114 114  69.251  6386    474     4  30        12 Female      No     Yes
#R> 115 115  16.482  3326    268     4  41        15   Male      No      No
#R> 116 116  40.442  4828    369     5  81         8 Female      No      No
#R> 117 117  35.177  2117    186     3  62        16 Female      No      No
#R> 118 118  91.362  9113    626     1  47        17   Male      No     Yes
#R> 119 119  27.039  2161    173     3  40        17 Female      No      No
#R> 120 120  23.012  1410    137     3  81        16   Male      No      No
#R> 121 121  27.241  1402    128     2  67        15 Female      No     Yes
#R> 122 122 148.080  8157    599     2  83        13   Male      No     Yes
#R> 123 123  62.602  7056    481     1  84        11 Female      No      No
#R> 124 124  11.808  1300    117     3  77        14 Female      No      No
#R> 125 125  29.564  2529    192     1  30        12 Female      No     Yes
#R> 126 126  27.578  2531    195     1  34        15 Female      No     Yes
#R> 127 127  26.427  5533    433     5  50        15 Female     Yes     Yes
#R> 128 128  57.202  3411    259     3  72        11 Female      No      No
#R> 129 129 123.299  8376    610     2  89        17   Male     Yes      No
#R> 130 130  18.145  3461    279     3  56        15   Male      No     Yes
#R> 131 131  23.793  3821    281     4  56        12 Female     Yes     Yes
#R> 132 132  10.726  1568    162     5  46        19   Male      No     Yes
#R> 133 133  23.283  5443    407     4  49        13   Male      No     Yes
#R> 134 134  21.455  5829    427     4  80        12 Female      No     Yes
#R> 135 135  34.664  5835    452     3  77        15 Female      No     Yes
#R> 136 136  44.473  3500    257     3  81        16 Female      No      No
#R> 137 137  54.663  4116    314     2  70         8 Female      No      No
#R> 138 138  36.355  3613    278     4  35         9   Male      No     Yes
#R> 139 139  21.374  2073    175     2  74        11 Female      No     Yes
#R> 140 140 107.841 10384    728     3  87         7   Male      No      No
#R> 141 141  39.831  6045    459     3  32        12 Female     Yes     Yes
#R> 142 142  91.876  6754    483     2  33        10   Male      No     Yes
#R> 143 143 103.893  7416    549     3  84        17   Male      No      No
#R> 144 144  19.636  4896    387     3  64        10 Female      No      No
#R> 145 145  17.392  2748    228     3  32        14   Male      No     Yes
#R> 146 146  19.529  4673    341     2  51        14   Male      No      No
#R> 147 147  17.055  5110    371     3  55        15 Female      No     Yes
#R> 148 148  23.857  1501    150     3  56        16   Male      No     Yes
#R> 149 149  15.184  2420    192     2  69        11 Female      No     Yes
#R> 150 150  13.444   886    121     5  44        10   Male      No     Yes
#R> 151 151  63.931  5728    435     3  28        14 Female      No     Yes
#R> 152 152  35.864  4831    353     3  66        13 Female      No     Yes
#R> 153 153  41.419  2120    184     4  24        11 Female     Yes      No
#R> 154 154  92.112  4612    344     3  32        17   Male      No      No
#R> 155 155  55.056  3155    235     2  31        16   Male      No     Yes
#R> 156 156  19.537  1362    143     4  34         9 Female      No     Yes
#R> 157 157  31.811  4284    338     5  75        13 Female      No     Yes
#R> 158 158  56.256  5521    406     2  72        16 Female     Yes     Yes
#R> 159 159  42.357  5550    406     2  83        12 Female      No     Yes
#R> 160 160  53.319  3000    235     3  53        13   Male      No      No
#R> 161 161  12.238  4865    381     5  67        11 Female      No      No
#R> 162 162  31.353  1705    160     3  81        14   Male      No     Yes
#R> 163 163  63.809  7530    515     1  56        12   Male      No     Yes
#R> 164 164  13.676  2330    203     5  80        16 Female      No      No
#R> 165 165  76.782  5977    429     4  44        12   Male      No     Yes
#R> 166 166  25.383  4527    367     4  46        11   Male      No     Yes
#R> 167 167  35.691  2880    214     2  35        15   Male      No      No
#R> 168 168  29.403  2327    178     1  37        14 Female      No     Yes
#R> 169 169  27.470  2820    219     1  32        11 Female      No     Yes
#R> 170 170  27.330  6179    459     4  36        12 Female      No     Yes
#R> 171 171  34.772  2021    167     3  57         9   Male      No      No
#R> 172 172  36.934  4270    299     1  63         9 Female      No     Yes
#R> 173 173  76.348  4697    344     4  60        18   Male      No      No
#R> 174 174  14.887  4745    339     3  58        12   Male      No     Yes
#R> 175 175 121.834 10673    750     3  54        16   Male      No      No
#R> 176 176  30.132  2168    206     3  52        17   Male      No      No
#R> 177 177  24.050  2607    221     4  32        18   Male      No     Yes
#R> 178 178  22.379  3965    292     2  34        14 Female      No     Yes
#R> 179 179  28.316  4391    316     2  29        10 Female      No      No
#R> 180 180  58.026  7499    560     5  67        11 Female      No      No
#R> 181 181  10.635  3584    294     5  69        16   Male      No     Yes
#R> 182 182  46.102  5180    382     3  81        12   Male      No     Yes
#R> 183 183  58.929  6420    459     2  66         9 Female      No     Yes
#R> 184 184  80.861  4090    335     3  29        15 Female      No     Yes
#R> 185 185 158.889 11589    805     1  62        17 Female      No     Yes
#R> 186 186  30.420  4442    316     1  30        14 Female      No      No
#R> 187 187  36.472  3806    309     2  52        13   Male      No      No
#R> 188 188  23.365  2179    167     2  75        15   Male      No      No
#R> 189 189  83.869  7667    554     2  83        11   Male      No      No
#R> 190 190  58.351  4411    326     2  85        16 Female      No     Yes
#R> 191 191  55.187  5352    385     4  50        17 Female      No     Yes
#R> 192 192 124.290  9560    701     3  52        17 Female     Yes      No
#R> 193 193  28.508  3933    287     4  56        14   Male      No     Yes
#R> 194 194 130.209 10088    730     7  39        19 Female      No     Yes
#R> 195 195  30.406  2120    181     2  79        14   Male      No     Yes
#R> 196 196  23.883  5384    398     2  73        16 Female      No     Yes
#R> 197 197  93.039  7398    517     1  67        12   Male      No     Yes
#R> 198 198  50.699  3977    304     2  84        17 Female      No      No
#R> 199 199  27.349  2000    169     4  51        16 Female      No     Yes
#R> 200 200  10.403  4159    310     3  43         7   Male      No     Yes
#R> 201 201  23.949  5343    383     2  40        18   Male      No     Yes
#R> 202 202  73.914  7333    529     6  67        15 Female      No     Yes
#R> 203 203  21.038  1448    145     2  58        13 Female      No     Yes
#R> 204 204  68.206  6784    499     5  40        16 Female     Yes      No
#R> 205 205  57.337  5310    392     2  45         7 Female      No      No
#R> 206 206  10.793  3878    321     8  29        13   Male      No      No
#R> 207 207  23.450  2450    180     2  78        13   Male      No      No
#R> 208 208  10.842  4391    358     5  37        10 Female     Yes     Yes
#R> 209 209  51.345  4327    320     3  46        15   Male      No      No
#R> 210 210 151.947  9156    642     2  91        11 Female      No     Yes
#R> 211 211  24.543  3206    243     2  62        12 Female      No     Yes
#R> 212 212  29.567  5309    397     3  25        15   Male      No      No
#R> 213 213  39.145  4351    323     2  66        13   Male      No     Yes
#R> 214 214  39.422  5245    383     2  44        19   Male      No      No
#R> 215 215  34.909  5289    410     2  62        16 Female      No     Yes
#R> 216 216  41.025  4229    337     3  79        19 Female      No     Yes
#R> 217 217  15.476  2762    215     3  60        18   Male      No      No
#R> 218 218  12.456  5395    392     3  65        14   Male      No     Yes
#R> 219 219  10.627  1647    149     2  71        10 Female     Yes     Yes
#R> 220 220  38.954  5222    370     4  76        13 Female      No      No
#R> 221 221  44.847  5765    437     3  53        13 Female     Yes      No
#R> 222 222  98.515  8760    633     5  78        11 Female      No      No
#R> 223 223  33.437  6207    451     4  44         9   Male     Yes      No
#R> 224 224  27.512  4613    344     5  72        17   Male      No     Yes
#R> 225 225 121.709  7818    584     4  50         6   Male      No     Yes
#R> 226 226  15.079  5673    411     4  28        15 Female      No     Yes
#R> 227 227  59.879  6906    527     6  78        15 Female      No      No
#R> 228 228  66.989  5614    430     3  47        14 Female      No     Yes
#R> 229 229  69.165  4668    341     2  34        11 Female      No      No
#R> 230 230  69.943  7555    547     3  76         9   Male      No     Yes
#R> 231 231  33.214  5137    387     3  59         9   Male      No      No
#R> 232 232  25.124  4776    378     4  29        12   Male      No     Yes
#R> 233 233  15.741  4788    360     1  39        14   Male      No     Yes
#R> 234 234  11.603  2278    187     3  71        11   Male      No     Yes
#R> 235 235  69.656  8244    579     3  41        14   Male      No     Yes
#R> 236 236  10.503  2923    232     3  25        18 Female      No     Yes
#R> 237 237  42.529  4986    369     2  37        11   Male      No     Yes
#R> 238 238  60.579  5149    388     5  38        15   Male      No     Yes
#R> 239 239  26.532  2910    236     6  58        19 Female      No     Yes
#R> 240 240  27.952  3557    263     1  35        13 Female      No     Yes
#R> 241 241  29.705  3351    262     5  71        14 Female      No     Yes
#R> 242 242  15.602   906    103     2  36        11   Male      No     Yes
#R> 243 243  20.918  1233    128     3  47        18 Female     Yes     Yes
#R> 244 244  58.165  6617    460     1  56        12 Female      No     Yes
#R> 245 245  22.561  1787    147     4  66        15 Female      No      No
#R> 246 246  34.509  2001    189     5  80        18 Female      No     Yes
#R> 247 247  19.588  3211    265     4  59        14 Female      No      No
#R> 248 248  36.364  2220    188     3  50        19   Male      No      No
#R> 249 249  15.717   905     93     1  38        16   Male     Yes     Yes
#R> 250 250  22.574  1551    134     3  43        13 Female     Yes     Yes
#R> 251 251  10.363  2430    191     2  47        18 Female      No     Yes
#R> 252 252  28.474  3202    267     5  66        12   Male      No     Yes
#R> 253 253  72.945  8603    621     3  64         8 Female      No      No
#R> 254 254  85.425  5182    402     6  60        12   Male      No     Yes
#R> 255 255  36.508  6386    469     4  79         6 Female      No     Yes
#R> 256 256  58.063  4221    304     3  50         8   Male      No      No
#R> 257 257  25.936  1774    135     2  71        14 Female      No      No
#R> 258 258  15.629  2493    186     1  60        14   Male      No     Yes
#R> 259 259  41.400  2561    215     2  36        14   Male      No     Yes
#R> 260 260  33.657  6196    450     6  55         9 Female      No      No
#R> 261 261  67.937  5184    383     4  63        12   Male      No     Yes
#R> 262 262 180.379  9310    665     3  67         8 Female     Yes     Yes
#R> 263 263  10.588  4049    296     1  66        13 Female      No     Yes
#R> 264 264  29.725  3536    270     2  52        15 Female      No      No
#R> 265 265  27.999  5107    380     1  55        10   Male      No     Yes
#R> 266 266  40.885  5013    379     3  46        13 Female      No     Yes
#R> 267 267  88.830  4952    360     4  86        16 Female      No     Yes
#R> 268 268  29.638  5833    433     3  29        15 Female      No     Yes
#R> 269 269  25.988  1349    142     4  82        12   Male      No      No
#R> 270 270  39.055  5565    410     4  48        18 Female      No     Yes
#R> 271 271  15.866  3085    217     1  39        13   Male      No      No
#R> 272 272  44.978  4866    347     1  30        10 Female      No      No
#R> 273 273  30.413  3690    299     2  25        15 Female     Yes      No
#R> 274 274  16.751  4706    353     6  48        14   Male     Yes      No
#R> 275 275  30.550  5869    439     5  81         9 Female      No      No
#R> 276 276 163.329  8732    636     3  50        14   Male      No     Yes
#R> 277 277  23.106  3476    257     2  50        15 Female      No      No
#R> 278 278  41.532  5000    353     2  50        12   Male      No     Yes
#R> 279 279 128.040  6982    518     2  78        11 Female      No     Yes
#R> 280 280  54.319  3063    248     3  59         8 Female     Yes      No
#R> 281 281  53.401  5319    377     3  35        12 Female      No      No
#R> 282 282  36.142  1852    183     3  33        13 Female      No      No
#R> 283 283  63.534  8100    581     2  50        17 Female      No     Yes
#R> 284 284  49.927  6396    485     3  75        17 Female      No     Yes
#R> 285 285  14.711  2047    167     2  67         6   Male      No     Yes
#R> 286 286  18.967  1626    156     2  41        11 Female      No     Yes
#R> 287 287  18.036  1552    142     2  48        15 Female      No      No
#R> 288 288  60.449  3098    272     4  69         8   Male      No     Yes
#R> 289 289  16.711  5274    387     3  42        16 Female      No     Yes
#R> 290 290  10.852  3907    296     2  30         9   Male      No      No
#R> 291 291  26.370  3235    268     5  78        11   Male      No     Yes
#R> 292 292  24.088  3665    287     4  56        13 Female      No     Yes
#R> 293 293  51.532  5096    380     2  31        15   Male      No     Yes
#R> 294 294 140.672 11200    817     7  46         9   Male      No     Yes
#R> 295 295  42.915  2532    205     4  42        13   Male      No     Yes
#R> 296 296  27.272  1389    149     5  67        10 Female      No     Yes
#R> 297 297  65.896  5140    370     1  49        17 Female      No     Yes
#R> 298 298  55.054  4381    321     3  74        17   Male      No     Yes
#R> 299 299  20.791  2672    204     1  70        18 Female      No      No
#R> 300 300  24.919  5051    372     3  76        11 Female      No     Yes
#R> 301 301  21.786  4632    355     1  50        17   Male      No     Yes
#R> 302 302  31.335  3526    289     3  38         7 Female      No      No
#R> 303 303  59.855  4964    365     1  46        13 Female      No     Yes
#R> 304 304  44.061  4970    352     1  79        11   Male      No     Yes
#R> 305 305  82.706  7506    536     2  64        13 Female      No     Yes
#R> 306 306  24.460  1924    165     2  50        14 Female      No     Yes
#R> 307 307  45.120  3762    287     3  80         8   Male      No     Yes
#R> 308 308  75.406  3874    298     3  41        14 Female      No     Yes
#R> 309 309  14.956  4640    332     2  33         6   Male      No      No
#R> 310 310  75.257  7010    494     3  34        18 Female      No     Yes
#R> 311 311  33.694  4891    369     1  52        16   Male     Yes      No
#R> 312 312  23.375  5429    396     3  57        15 Female      No     Yes
#R> 313 313  27.825  5227    386     6  63        11   Male      No     Yes
#R> 314 314  92.386  7685    534     2  75        18 Female      No     Yes
#R> 315 315 115.520  9272    656     2  69        14   Male      No      No
#R> 316 316  14.479  3907    296     3  43        16   Male      No     Yes
#R> 317 317  52.179  7306    522     2  57        14   Male      No      No
#R> 318 318  68.462  4712    340     2  71        16   Male      No     Yes
#R> 319 319  18.951  1485    129     3  82        13 Female      No      No
#R> 320 320  27.590  2586    229     5  54        16   Male      No     Yes
#R> 321 321  16.279  1160    126     3  78        13   Male     Yes     Yes
#R> 322 322  25.078  3096    236     2  27        15 Female      No     Yes
#R> 323 323  27.229  3484    282     6  51        11   Male      No      No
#R> 324 324 182.728 13913    982     4  98        17   Male      No     Yes
#R> 325 325  31.029  2863    223     2  66        17   Male     Yes     Yes
#R> 326 326  17.765  5072    364     1  66        12 Female      No     Yes
#R> 327 327 125.480 10230    721     3  82        16   Male      No     Yes
#R> 328 328  49.166  6662    508     3  68        14 Female      No      No
#R> 329 329  41.192  3673    297     3  54        16 Female      No     Yes
#R> 330 330  94.193  7576    527     2  44        16 Female      No     Yes
#R> 331 331  20.405  4543    329     2  72        17   Male     Yes      No
#R> 332 332  12.581  3976    291     2  48        16   Male      No     Yes
#R> 333 333  62.328  5228    377     3  83        15   Male      No      No
#R> 334 334  21.011  3402    261     2  68        17   Male      No     Yes
#R> 335 335  24.230  4756    351     2  64        15 Female      No     Yes
#R> 336 336  24.314  3409    270     2  23         7 Female      No     Yes
#R> 337 337  32.856  5884    438     4  68        13   Male      No      No
#R> 338 338  12.414   855    119     3  32        12   Male      No     Yes
#R> 339 339  41.365  5303    377     1  45        14   Male      No      No
#R> 340 340 149.316 10278    707     1  80        16   Male      No      No
#R> 341 341  27.794  3807    301     4  35         8 Female      No     Yes
#R> 342 342  13.234  3922    299     2  77        17 Female      No     Yes
#R> 343 343  14.595  2955    260     5  37         9   Male      No     Yes
#R> 344 344  10.735  3746    280     2  44        17 Female      No     Yes
#R> 345 345  48.218  5199    401     7  39        10   Male      No     Yes
#R> 346 346  30.012  1511    137     2  33        17   Male      No     Yes
#R> 347 347  21.551  5380    420     5  51        18   Male      No     Yes
#R> 348 348 160.231 10748    754     2  69        17   Male      No      No
#R> 349 349  13.433  1134    112     3  70        14   Male      No     Yes
#R> 350 350  48.577  5145    389     3  71        13 Female      No     Yes
#R> 351 351  30.002  1561    155     4  70        13 Female      No     Yes
#R> 352 352  61.620  5140    374     1  71         9   Male      No     Yes
#R> 353 353 104.483  7140    507     2  41        14   Male      No     Yes
#R> 354 354  41.868  4716    342     2  47        18   Male      No      No
#R> 355 355  12.068  3873    292     1  44        18 Female      No     Yes
#R> 356 356 180.682 11966    832     2  58         8 Female      No     Yes
#R> 357 357  34.480  6090    442     3  36        14   Male      No      No
#R> 358 358  39.609  2539    188     1  40        14   Male      No     Yes
#R> 359 359  30.111  4336    339     1  81        18   Male      No     Yes
#R> 360 360  12.335  4471    344     3  79        12   Male      No     Yes
#R> 361 361  53.566  5891    434     4  82        10 Female      No      No
#R> 362 362  53.217  4943    362     2  46        16 Female      No     Yes
#R> 363 363  26.162  5101    382     3  62        19 Female      No      No
#R> 364 364  64.173  6127    433     1  80        10   Male      No     Yes
#R> 365 365 128.669  9824    685     3  67        16   Male      No     Yes
#R> 366 366 113.772  6442    489     4  69        15   Male     Yes     Yes
#R> 367 367  61.069  7871    564     3  56        14   Male      No     Yes
#R> 368 368  23.793  3615    263     2  70        14   Male      No      No
#R> 369 369  89.000  5759    440     3  37         6 Female      No      No
#R> 370 370  71.682  8028    599     3  57        16   Male      No     Yes
#R> 371 371  35.610  6135    466     4  40        12   Male      No      No
#R> 372 372  39.116  2150    173     4  75        15   Male      No      No
#R> 373 373  19.782  3782    293     2  46        16 Female     Yes      No
#R> 374 374  55.412  5354    383     2  37        16 Female     Yes     Yes
#R> 375 375  29.400  4840    368     3  76        18 Female      No     Yes
#R> 376 376  20.974  5673    413     5  44        16 Female      No     Yes
#R> 377 377  87.625  7167    515     2  46        10 Female      No      No
#R> 378 378  28.144  1567    142     3  51        10   Male      No     Yes
#R> 379 379  19.349  4941    366     1  33        19   Male      No     Yes
#R> 380 380  53.308  2860    214     1  84        10   Male      No     Yes
#R> 381 381 115.123  7760    538     3  83        14 Female      No      No
#R> 382 382 101.788  8029    574     2  84        11   Male      No     Yes
#R> 383 383  24.824  5495    409     1  33         9   Male     Yes      No
#R> 384 384  14.292  3274    282     9  64         9   Male      No     Yes
#R> 385 385  20.088  1870    180     3  76        16   Male      No      No
#R> 386 386  26.400  5640    398     3  58        15 Female      No      No
#R> 387 387  19.253  3683    287     4  57        10   Male      No      No
#R> 388 388  16.529  1357    126     3  62         9   Male      No      No
#R> 389 389  37.878  6827    482     2  80        13 Female      No      No
#R> 390 390  83.948  7100    503     2  44        18   Male      No      No
#R> 391 391 135.118 10578    747     3  81        15 Female      No     Yes
#R> 392 392  73.327  6555    472     2  43        15 Female      No      No
#R> 393 393  25.974  2308    196     2  24        10   Male      No      No
#R> 394 394  17.316  1335    138     2  65        13   Male      No      No
#R> 395 395  49.794  5758    410     4  40         8   Male      No      No
#R> 396 396  12.096  4100    307     3  32        13   Male      No     Yes
#R> 397 397  13.364  3838    296     5  65        17   Male      No      No
#R> 398 398  57.872  4171    321     5  67        12 Female      No     Yes
#R> 399 399  37.728  2525    192     1  44        13   Male      No     Yes
#R> 400 400  18.701  5524    415     5  64         7 Female      No      No
#R>            Ethnicity Balance
#R> 1          Caucasian     333
#R> 2              Asian     903
#R> 3              Asian     580
#R> 4              Asian     964
#R> 5          Caucasian     331
#R> 6          Caucasian    1151
#R> 7   African American     203
#R> 8              Asian     872
#R> 9          Caucasian     279
#R> 10  African American    1350
#R> 11         Caucasian    1407
#R> 12         Caucasian       0
#R> 13             Asian     204
#R> 14         Caucasian    1081
#R> 15  African American     148
#R> 16  African American       0
#R> 17  African American       0
#R> 18             Asian     368
#R> 19             Asian     891
#R> 20             Asian    1048
#R> 21             Asian      89
#R> 22         Caucasian     968
#R> 23  African American       0
#R> 24  African American     411
#R> 25         Caucasian       0
#R> 26  African American     671
#R> 27         Caucasian     654
#R> 28  African American     467
#R> 29  African American    1809
#R> 30         Caucasian     915
#R> 31         Caucasian     863
#R> 32             Asian       0
#R> 33         Caucasian     526
#R> 34         Caucasian       0
#R> 35             Asian       0
#R> 36         Caucasian     419
#R> 37         Caucasian     762
#R> 38         Caucasian    1093
#R> 39         Caucasian     531
#R> 40         Caucasian     344
#R> 41  African American      50
#R> 42  African American    1155
#R> 43             Asian     385
#R> 44             Asian     976
#R> 45         Caucasian    1120
#R> 46         Caucasian     997
#R> 47             Asian    1241
#R> 48         Caucasian     797
#R> 49             Asian       0
#R> 50  African American     902
#R> 51  African American     654
#R> 52  African American     211
#R> 53         Caucasian     607
#R> 54             Asian     957
#R> 55             Asian       0
#R> 56             Asian       0
#R> 57             Asian     379
#R> 58         Caucasian     133
#R> 59         Caucasian     333
#R> 60         Caucasian     531
#R> 61             Asian     631
#R> 62         Caucasian     108
#R> 63         Caucasian       0
#R> 64         Caucasian     133
#R> 65  African American       0
#R> 66         Caucasian     602
#R> 67             Asian    1388
#R> 68  African American     889
#R> 69         Caucasian     822
#R> 70         Caucasian    1084
#R> 71         Caucasian     357
#R> 72             Asian    1103
#R> 73             Asian     663
#R> 74         Caucasian     601
#R> 75         Caucasian     945
#R> 76  African American      29
#R> 77         Caucasian     532
#R> 78             Asian     145
#R> 79         Caucasian     391
#R> 80             Asian       0
#R> 81         Caucasian     162
#R> 82         Caucasian      99
#R> 83         Caucasian     503
#R> 84         Caucasian       0
#R> 85         Caucasian       0
#R> 86             Asian    1779
#R> 87         Caucasian     815
#R> 88             Asian       0
#R> 89  African American     579
#R> 90  African American    1176
#R> 91  African American    1023
#R> 92         Caucasian     812
#R> 93         Caucasian       0
#R> 94  African American     937
#R> 95  African American       0
#R> 96  African American       0
#R> 97             Asian    1380
#R> 98  African American     155
#R> 99  African American     375
#R> 100        Caucasian    1311
#R> 101        Caucasian     298
#R> 102        Caucasian     431
#R> 103        Caucasian    1587
#R> 104        Caucasian    1050
#R> 105        Caucasian     745
#R> 106        Caucasian     210
#R> 107            Asian       0
#R> 108            Asian       0
#R> 109        Caucasian     227
#R> 110            Asian     297
#R> 111            Asian      47
#R> 112 African American       0
#R> 113        Caucasian    1046
#R> 114            Asian     768
#R> 115        Caucasian     271
#R> 116 African American     510
#R> 117        Caucasian       0
#R> 118            Asian    1341
#R> 119        Caucasian       0
#R> 120        Caucasian       0
#R> 121            Asian       0
#R> 122        Caucasian     454
#R> 123        Caucasian     904
#R> 124 African American       0
#R> 125        Caucasian       0
#R> 126        Caucasian       0
#R> 127            Asian    1404
#R> 128        Caucasian       0
#R> 129 African American    1259
#R> 130 African American     255
#R> 131 African American     868
#R> 132            Asian       0
#R> 133 African American     912
#R> 134 African American    1018
#R> 135 African American     835
#R> 136 African American       8
#R> 137 African American      75
#R> 138            Asian     187
#R> 139        Caucasian       0
#R> 140 African American    1597
#R> 141 African American    1425
#R> 142        Caucasian     605
#R> 143            Asian     669
#R> 144 African American     710
#R> 145        Caucasian      68
#R> 146            Asian     642
#R> 147        Caucasian     805
#R> 148        Caucasian       0
#R> 149        Caucasian       0
#R> 150            Asian       0
#R> 151 African American     581
#R> 152        Caucasian     534
#R> 153        Caucasian     156
#R> 154        Caucasian       0
#R> 155 African American       0
#R> 156            Asian       0
#R> 157        Caucasian     429
#R> 158        Caucasian    1020
#R> 159            Asian     653
#R> 160            Asian       0
#R> 161        Caucasian     836
#R> 162        Caucasian       0
#R> 163        Caucasian    1086
#R> 164 African American       0
#R> 165            Asian     548
#R> 166        Caucasian     570
#R> 167 African American       0
#R> 168        Caucasian       0
#R> 169            Asian       0
#R> 170        Caucasian    1099
#R> 171            Asian       0
#R> 172        Caucasian     283
#R> 173            Asian     108
#R> 174 African American     724
#R> 175 African American    1573
#R> 176        Caucasian       0
#R> 177        Caucasian       0
#R> 178            Asian     384
#R> 179        Caucasian     453
#R> 180        Caucasian    1237
#R> 181            Asian     423
#R> 182 African American     516
#R> 183 African American     789
#R> 184            Asian       0
#R> 185        Caucasian    1448
#R> 186 African American     450
#R> 187 African American     188
#R> 188            Asian       0
#R> 189 African American     930
#R> 190        Caucasian     126
#R> 191        Caucasian     538
#R> 192            Asian    1687
#R> 193            Asian     336
#R> 194        Caucasian    1426
#R> 195 African American       0
#R> 196 African American     802
#R> 197 African American     749
#R> 198 African American      69
#R> 199 African American       0
#R> 200            Asian     571
#R> 201 African American     829
#R> 202        Caucasian    1048
#R> 203        Caucasian       0
#R> 204 African American    1411
#R> 205        Caucasian     456
#R> 206        Caucasian     638
#R> 207        Caucasian       0
#R> 208        Caucasian    1216
#R> 209 African American     230
#R> 210 African American     732
#R> 211        Caucasian      95
#R> 212        Caucasian     799
#R> 213        Caucasian     308
#R> 214 African American     637
#R> 215        Caucasian     681
#R> 216        Caucasian     246
#R> 217            Asian      52
#R> 218        Caucasian     955
#R> 219            Asian     195
#R> 220        Caucasian     653
#R> 221            Asian    1246
#R> 222 African American    1230
#R> 223        Caucasian    1549
#R> 224            Asian     573
#R> 225        Caucasian     701
#R> 226            Asian    1075
#R> 227        Caucasian    1032
#R> 228        Caucasian     482
#R> 229 African American     156
#R> 230            Asian    1058
#R> 231 African American     661
#R> 232        Caucasian     657
#R> 233            Asian     689
#R> 234        Caucasian       0
#R> 235 African American    1329
#R> 236 African American     191
#R> 237            Asian     489
#R> 238            Asian     443
#R> 239        Caucasian      52
#R> 240            Asian     163
#R> 241            Asian     148
#R> 242 African American       0
#R> 243            Asian      16
#R> 244        Caucasian     856
#R> 245        Caucasian       0
#R> 246 African American       0
#R> 247            Asian     199
#R> 248        Caucasian       0
#R> 249        Caucasian       0
#R> 250        Caucasian      98
#R> 251            Asian       0
#R> 252        Caucasian     132
#R> 253        Caucasian    1355
#R> 254 African American     218
#R> 255        Caucasian    1048
#R> 256 African American     118
#R> 257            Asian       0
#R> 258            Asian       0
#R> 259        Caucasian       0
#R> 260        Caucasian    1092
#R> 261            Asian     345
#R> 262            Asian    1050
#R> 263        Caucasian     465
#R> 264 African American     133
#R> 265        Caucasian     651
#R> 266 African American     549
#R> 267        Caucasian      15
#R> 268            Asian     942
#R> 269        Caucasian       0
#R> 270        Caucasian     772
#R> 271        Caucasian     136
#R> 272        Caucasian     436
#R> 273            Asian     728
#R> 274            Asian    1255
#R> 275 African American     967
#R> 276        Caucasian     529
#R> 277        Caucasian     209
#R> 278        Caucasian     531
#R> 279        Caucasian     250
#R> 280        Caucasian     269
#R> 281 African American     541
#R> 282 African American       0
#R> 283        Caucasian    1298
#R> 284        Caucasian     890
#R> 285        Caucasian       0
#R> 286            Asian       0
#R> 287        Caucasian       0
#R> 288        Caucasian       0
#R> 289            Asian     863
#R> 290        Caucasian     485
#R> 291            Asian     159
#R> 292        Caucasian     309
#R> 293        Caucasian     481
#R> 294 African American    1677
#R> 295            Asian       0
#R> 296        Caucasian       0
#R> 297        Caucasian     293
#R> 298            Asian     188
#R> 299 African American       0
#R> 300 African American     711
#R> 301        Caucasian     580
#R> 302        Caucasian     172
#R> 303        Caucasian     295
#R> 304 African American     414
#R> 305            Asian     905
#R> 306            Asian       0
#R> 307        Caucasian      70
#R> 308            Asian       0
#R> 309            Asian     681
#R> 310        Caucasian     885
#R> 311 African American    1036
#R> 312        Caucasian     844
#R> 313        Caucasian     823
#R> 314            Asian     843
#R> 315 African American    1140
#R> 316        Caucasian     463
#R> 317            Asian    1142
#R> 318        Caucasian     136
#R> 319        Caucasian       0
#R> 320 African American       0
#R> 321 African American       5
#R> 322        Caucasian      81
#R> 323        Caucasian     265
#R> 324        Caucasian    1999
#R> 325            Asian     415
#R> 326        Caucasian     732
#R> 327        Caucasian    1361
#R> 328            Asian     984
#R> 329        Caucasian     121
#R> 330        Caucasian     846
#R> 331            Asian    1054
#R> 332        Caucasian     474
#R> 333        Caucasian     380
#R> 334 African American     182
#R> 335        Caucasian     594
#R> 336        Caucasian     194
#R> 337        Caucasian     926
#R> 338 African American       0
#R> 339        Caucasian     606
#R> 340 African American    1107
#R> 341 African American     320
#R> 342        Caucasian     426
#R> 343 African American     204
#R> 344        Caucasian     410
#R> 345            Asian     633
#R> 346        Caucasian       0
#R> 347            Asian     907
#R> 348        Caucasian    1192
#R> 349        Caucasian       0
#R> 350            Asian     503
#R> 351        Caucasian       0
#R> 352        Caucasian     302
#R> 353 African American     583
#R> 354        Caucasian     425
#R> 355            Asian     413
#R> 356 African American    1405
#R> 357        Caucasian     962
#R> 358            Asian       0
#R> 359        Caucasian     347
#R> 360 African American     611
#R> 361        Caucasian     712
#R> 362            Asian     382
#R> 363 African American     710
#R> 364        Caucasian     578
#R> 365            Asian    1243
#R> 366        Caucasian     790
#R> 367        Caucasian    1264
#R> 368 African American     216
#R> 369        Caucasian     345
#R> 370        Caucasian    1208
#R> 371        Caucasian     992
#R> 372        Caucasian       0
#R> 373        Caucasian     840
#R> 374        Caucasian    1003
#R> 375        Caucasian     588
#R> 376        Caucasian    1000
#R> 377 African American     767
#R> 378        Caucasian       0
#R> 379        Caucasian     717
#R> 380        Caucasian       0
#R> 381 African American     661
#R> 382        Caucasian     849
#R> 383        Caucasian    1352
#R> 384        Caucasian     382
#R> 385 African American       0
#R> 386            Asian     905
#R> 387 African American     371
#R> 388            Asian       0
#R> 389        Caucasian    1129
#R> 390        Caucasian     806
#R> 391            Asian    1393
#R> 392        Caucasian     721
#R> 393            Asian       0
#R> 394 African American       0
#R> 395        Caucasian     734
#R> 396        Caucasian     560
#R> 397 African American     480
#R> 398        Caucasian     138
#R> 399        Caucasian       0
#R> 400            Asian     966
```

We can plot these different models.


```r
s.data <- Credit
s.data$Student <- "Yes"

ns.data <- Credit
ns.data$Student <- "No"

cols <- c("Student"="red", "Yes" ="red", "Not student"="black", "No"="black")
p1 <- Credit %>%
	mutate(fit.student = predict(model.interaction2, newdata = s.data),
		fit.not.student = predict(model.interaction2, newdata = ns.data)) %>%
	ggplot(aes(x=Income, y=Balance)) +
  geom_point(aes(x=Income, y=Balance, color=Student)) +
  geom_line(aes(y=fit.student, color="Student")) +
  geom_line(aes(y=fit.not.student, color="Not student")) +
  scale_colour_manual(values=cols) +
  theme(legend.position = "none")

p2 <- Credit %>%
	mutate(fit.student = predict(model.interaction3, newdata = s.data),
	       fit.not.student = predict(model.interaction3, newdata = ns.data)) %>%
  ggplot(aes(x=Income, y=Balance)) +
  geom_point(aes(x=Income, y=Balance, color=Student)) +
  geom_line(aes(y=fit.student, color="Student")) +
  geom_line(aes(y=fit.not.student, color="Not student")) +
  scale_colour_manual(values=cols) +
  theme(legend.position = c(50, 1000),
          legend.direction = "horizontal")
require(gridExtra)
grid.arrange(p1, p2, ncol=2)
```

\begin{figure}
\includegraphics[width=1\linewidth]{MyR_files/figure-latex/unnamed-chunk-205-1} \caption{Fits of models without (left) and with (right) interactions terms of Income and Student for Students (red) and not Students (black).}(\#fig:unnamed-chunk-205)
\end{figure}

## Polynomials of degree n {#polyn}

Another very useful extension of the linear model is to include powers of variables in order to capture non-linear effects. This seems to be a contradiction in terms, but a possible answer could be that the model is still linear in the coefficients.  

To fix ideas, here is an example of fitting a quadratic model.

\[\text{mpg} = \beta_0 + \beta_{1}\times \text{horsepower} + \beta_{2}\times \text{horsepower}^2 + \varepsilon\]

This model can be estimated in the `Auto` data set of the `ISLR` package.


```r
require(ISLR)
data("Auto")
model.pd1 <- lm(mpg ~ horsepower, data = Auto)
summary(model.pd1)
#R> 
#R> Call:
#R> lm(formula = mpg ~ horsepower, data = Auto)
#R> 
#R> Residuals:
#R>      Min       1Q   Median       3Q      Max 
#R> -13.5710  -3.2592  -0.3435   2.7630  16.9240 
#R> 
#R> Coefficients:
#R>              Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept) 39.935861   0.717499   55.66   <2e-16 ***
#R> horsepower  -0.157845   0.006446  -24.49   <2e-16 ***
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 4.906 on 390 degrees of freedom
#R> Multiple R-squared:  0.6059,	Adjusted R-squared:  0.6049 
#R> F-statistic: 599.7 on 1 and 390 DF,  p-value: < 2.2e-16
model.pd2 <- lm(mpg ~ horsepower + I(horsepower^2), data = Auto)
summary(model.pd2) 
#R> 
#R> Call:
#R> lm(formula = mpg ~ horsepower + I(horsepower^2), data = Auto)
#R> 
#R> Residuals:
#R>      Min       1Q   Median       3Q      Max 
#R> -14.7135  -2.5943  -0.0859   2.2868  15.8961 
#R> 
#R> Coefficients:
#R>                   Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)     56.9000997  1.8004268   31.60   <2e-16 ***
#R> horsepower      -0.4661896  0.0311246  -14.98   <2e-16 ***
#R> I(horsepower^2)  0.0012305  0.0001221   10.08   <2e-16 ***
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 4.374 on 389 degrees of freedom
#R> Multiple R-squared:  0.6876,	Adjusted R-squared:  0.686 
#R> F-statistic:   428 on 2 and 389 DF,  p-value: < 2.2e-16
```
Notice the use of the `I` function which, in a formula, inhibits the interpretation of operators such as `+` and `^` as formula operators but, instead, makes them be used as arithmetical operators.  

For higher degrees of polynomial, it can become cumbersome to write all the degrees. That is where the function `poly` is handy.


```r
require(ISLR)
data("Auto")
model.pd5 <- lm(mpg ~ poly(horsepower, 5), data = Auto)
model.pd9 <- lm(mpg ~ poly(horsepower, 9), data = Auto)
```

Again, the advantage of the linear regression with a single predictor is the visualization of its fits, as illustrated below.


```r
Auto <- Auto %>%
	mutate(fit1 = predict(model.pd1),
	fit2 = predict(model.pd2),
	fit5 = predict(model.pd5),
	fit9 = predict(model.pd9))

cols <- c("Deg.1", "Deg.2", "Deg.5", "Deg.9")
Auto %>% 
	ggplot(aes(x=horsepower, y=mpg)) +
	geom_point() +
	geom_line(aes(y=fit1, color="Deg.1"), size =2) +
	geom_line(aes(y=fit2, color="Deg.2"), size =2) +
	geom_line(aes(y=fit5, color="Deg.5"), size =2) +
  geom_line(aes(y=fit9, color="Deg.9"), size =2) +
	theme(legend.title = element_blank(), 
		legend.position = "bottom", 
		legend.direction = "horizontal")
```

\begin{figure}
\includegraphics[width=1\linewidth]{MyR_files/figure-latex/unnamed-chunk-208-1} \caption{Fits of mpg for various degrees of the polynomial of horsepower.}(\#fig:unnamed-chunk-208)
\end{figure}



```r
fita1 <- lm(sales ~ TV + radio + newspaper, data=advertising )
summary(fita1)
#R> 
#R> Call:
#R> lm(formula = sales ~ TV + radio + newspaper, data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -8.8277 -0.8908  0.2418  1.1893  2.8292 
#R> 
#R> Coefficients:
#R>              Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)  2.938889   0.311908   9.422   <2e-16 ***
#R> TV           0.045765   0.001395  32.809   <2e-16 ***
#R> radio        0.188530   0.008611  21.893   <2e-16 ***
#R> newspaper   -0.001037   0.005871  -0.177     0.86    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 1.686 on 196 degrees of freedom
#R> Multiple R-squared:  0.8972,	Adjusted R-squared:  0.8956 
#R> F-statistic: 570.3 on 3 and 196 DF,  p-value: < 2.2e-16

fita2 <- lm(sales ~ poly(TV,5) + radio + newspaper , data=advertising )
summary(fita2)
#R> 
#R> Call:
#R> lm(formula = sales ~ poly(TV, 5) + radio + newspaper, data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -4.7146 -0.7626  0.0771  0.7641  3.9479 
#R> 
#R> Coefficients:
#R>                Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)   9.492e+00  2.068e-01  45.888  < 2e-16 ***
#R> poly(TV, 5)1  5.534e+01  1.400e+00  39.536  < 2e-16 ***
#R> poly(TV, 5)2 -1.037e+01  1.406e+00  -7.377 4.73e-12 ***
#R> poly(TV, 5)3  7.380e+00  1.403e+00   5.261 3.81e-07 ***
#R> poly(TV, 5)4 -3.627e+00  1.397e+00  -2.596   0.0102 *  
#R> poly(TV, 5)5  3.119e+00  1.402e+00   2.225   0.0272 *  
#R> radio         1.961e-01  7.196e-03  27.247  < 2e-16 ***
#R> newspaper    -9.927e-04  4.886e-03  -0.203   0.8392    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 1.396 on 192 degrees of freedom
#R> Multiple R-squared:  0.9309,	Adjusted R-squared:  0.9284 
#R> F-statistic: 369.4 on 7 and 192 DF,  p-value: < 2.2e-16

fita3 <- lm(sales ~ poly(TV,5) + poly(radio,3) + poly(newspaper,6) , data=advertising )
summary(fita3)
#R> 
#R> Call:
#R> lm(formula = sales ~ poly(TV, 5) + poly(radio, 3) + poly(newspaper, 
#R>     6), data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -4.3885 -0.7860  0.1327  0.8392  3.5109 
#R> 
#R> Coefficients:
#R>                      Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)          14.02250    0.09858 142.251  < 2e-16 ***
#R> poly(TV, 5)1         55.36886    1.40715  39.348  < 2e-16 ***
#R> poly(TV, 5)2        -10.57519    1.44722  -7.307 7.91e-12 ***
#R> poly(TV, 5)3          7.67566    1.42764   5.376 2.27e-07 ***
#R> poly(TV, 5)4         -3.41418    1.46292  -2.334   0.0207 *  
#R> poly(TV, 5)5          3.40874    1.42291   2.396   0.0176 *  
#R> poly(radio, 3)1      41.07485    1.57040  26.156  < 2e-16 ***
#R> poly(radio, 3)2       1.67469    1.40486   1.192   0.2348    
#R> poly(radio, 3)3      -0.77950    1.43343  -0.544   0.5872    
#R> poly(newspaper, 6)1  -0.49881    1.51667  -0.329   0.7426    
#R> poly(newspaper, 6)2  -1.62406    1.43837  -1.129   0.2603    
#R> poly(newspaper, 6)3  -1.21464    1.47339  -0.824   0.4108    
#R> poly(newspaper, 6)4   1.41833    1.42002   0.999   0.3192    
#R> poly(newspaper, 6)5  -1.62507    1.44128  -1.128   0.2610    
#R> poly(newspaper, 6)6   1.86592    1.44978   1.287   0.1997    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 1.394 on 185 degrees of freedom
#R> Multiple R-squared:  0.9336,	Adjusted R-squared:  0.9286 
#R> F-statistic: 185.9 on 14 and 185 DF,  p-value: < 2.2e-16

fita4 <- lm(sales ~ TV + radio + newspaper + TV:radio, data=advertising )
summary(fita4)
#R> 
#R> Call:
#R> lm(formula = sales ~ TV + radio + newspaper + TV:radio, data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -6.2929 -0.3983  0.1811  0.5957  1.5009 
#R> 
#R> Coefficients:
#R>              Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept) 6.728e+00  2.533e-01  26.561  < 2e-16 ***
#R> TV          1.907e-02  1.509e-03  12.633  < 2e-16 ***
#R> radio       2.799e-02  9.141e-03   3.062  0.00251 ** 
#R> newspaper   1.444e-03  3.295e-03   0.438  0.66169    
#R> TV:radio    1.087e-03  5.256e-05  20.686  < 2e-16 ***
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 0.9455 on 195 degrees of freedom
#R> Multiple R-squared:  0.9678,	Adjusted R-squared:  0.9672 
#R> F-statistic:  1466 on 4 and 195 DF,  p-value: < 2.2e-16

fita5 <- lm(sales ~ TV*radio*newspaper, data=advertising )
summary(fita5)
#R> 
#R> Call:
#R> lm(formula = sales ~ TV * radio * newspaper, data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -5.8955 -0.3883  0.1938  0.5865  1.5240 
#R> 
#R> Coefficients:
#R>                      Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)         6.556e+00  4.655e-01  14.083  < 2e-16 ***
#R> TV                  1.971e-02  2.719e-03   7.250 9.95e-12 ***
#R> radio               1.962e-02  1.639e-02   1.197    0.233    
#R> newspaper           1.311e-02  1.721e-02   0.761    0.447    
#R> TV:radio            1.162e-03  9.753e-05  11.909  < 2e-16 ***
#R> TV:newspaper       -5.545e-05  9.326e-05  -0.595    0.553    
#R> radio:newspaper     9.063e-06  4.831e-04   0.019    0.985    
#R> TV:radio:newspaper -7.610e-07  2.700e-06  -0.282    0.778    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 0.9406 on 192 degrees of freedom
#R> Multiple R-squared:  0.9686,	Adjusted R-squared:  0.9675 
#R> F-statistic: 847.3 on 7 and 192 DF,  p-value: < 2.2e-16

fita6 <- lm(sales ~ poly(TV,2)*poly(radio,2)*poly(newspaper,2), data=advertising )
summary(fita6)
#R> 
#R> Call:
#R> lm(formula = sales ~ poly(TV, 2) * poly(radio, 2) * poly(newspaper, 
#R>     2), data = advertising)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -3.9725 -0.2858 -0.0204  0.3599  1.5506 
#R> 
#R> Coefficients:
#R>                                                   Estimate Std. Error
#R> (Intercept)                                        13.8835     0.0703
#R> poly(TV, 2)1                                       54.2030     1.0438
#R> poly(TV, 2)2                                      -11.6034     1.1108
#R> poly(radio, 2)1                                    41.0018     1.0644
#R> poly(radio, 2)2                                    -0.1182     0.8191
#R> poly(newspaper, 2)1                                -0.9759     1.6684
#R> poly(newspaper, 2)2                                -1.1251     1.3658
#R> poly(TV, 2)1:poly(radio, 2)1                      260.7218    15.4199
#R> poly(TV, 2)2:poly(radio, 2)1                        1.0911    17.1214
#R> poly(TV, 2)1:poly(radio, 2)2                       10.0864    11.6822
#R> poly(TV, 2)2:poly(radio, 2)2                      -18.5441    12.6479
#R> poly(TV, 2)1:poly(newspaper, 2)1                    5.4960    24.8771
#R> poly(TV, 2)2:poly(newspaper, 2)1                  -20.1420    27.7030
#R> poly(TV, 2)1:poly(newspaper, 2)2                   31.5107    19.6835
#R> poly(TV, 2)2:poly(newspaper, 2)2                  -39.2877    22.2611
#R> poly(radio, 2)1:poly(newspaper, 2)1                33.4157    24.2185
#R> poly(radio, 2)2:poly(newspaper, 2)1                -1.6575    16.9091
#R> poly(radio, 2)1:poly(newspaper, 2)2                21.2605    18.8661
#R> poly(radio, 2)2:poly(newspaper, 2)2                -7.4744    16.5449
#R> poly(TV, 2)1:poly(radio, 2)1:poly(newspaper, 2)1 -341.4466   359.3642
#R> poly(TV, 2)2:poly(radio, 2)1:poly(newspaper, 2)1  730.7858   397.7077
#R> poly(TV, 2)1:poly(radio, 2)2:poly(newspaper, 2)1  310.4246   215.8568
#R> poly(TV, 2)2:poly(radio, 2)2:poly(newspaper, 2)1 -160.2951   238.1557
#R> poly(TV, 2)1:poly(radio, 2)1:poly(newspaper, 2)2 -188.3401   264.0924
#R> poly(TV, 2)2:poly(radio, 2)1:poly(newspaper, 2)2  400.4017   303.3395
#R> poly(TV, 2)1:poly(radio, 2)2:poly(newspaper, 2)2  291.4037   187.8892
#R> poly(TV, 2)2:poly(radio, 2)2:poly(newspaper, 2)2 -139.3321   233.1617
#R>                                                  t value Pr(>|t|)    
#R> (Intercept)                                      197.479   <2e-16 ***
#R> poly(TV, 2)1                                      51.928   <2e-16 ***
#R> poly(TV, 2)2                                     -10.446   <2e-16 ***
#R> poly(radio, 2)1                                   38.519   <2e-16 ***
#R> poly(radio, 2)2                                   -0.144   0.8854    
#R> poly(newspaper, 2)1                               -0.585   0.5593    
#R> poly(newspaper, 2)2                               -0.824   0.4112    
#R> poly(TV, 2)1:poly(radio, 2)1                      16.908   <2e-16 ***
#R> poly(TV, 2)2:poly(radio, 2)1                       0.064   0.9493    
#R> poly(TV, 2)1:poly(radio, 2)2                       0.863   0.3891    
#R> poly(TV, 2)2:poly(radio, 2)2                      -1.466   0.1444    
#R> poly(TV, 2)1:poly(newspaper, 2)1                   0.221   0.8254    
#R> poly(TV, 2)2:poly(newspaper, 2)1                  -0.727   0.4682    
#R> poly(TV, 2)1:poly(newspaper, 2)2                   1.601   0.1112    
#R> poly(TV, 2)2:poly(newspaper, 2)2                  -1.765   0.0794 .  
#R> poly(radio, 2)1:poly(newspaper, 2)1                1.380   0.1694    
#R> poly(radio, 2)2:poly(newspaper, 2)1               -0.098   0.9220    
#R> poly(radio, 2)1:poly(newspaper, 2)2                1.127   0.2613    
#R> poly(radio, 2)2:poly(newspaper, 2)2               -0.452   0.6520    
#R> poly(TV, 2)1:poly(radio, 2)1:poly(newspaper, 2)1  -0.950   0.3434    
#R> poly(TV, 2)2:poly(radio, 2)1:poly(newspaper, 2)1   1.837   0.0679 .  
#R> poly(TV, 2)1:poly(radio, 2)2:poly(newspaper, 2)1   1.438   0.1522    
#R> poly(TV, 2)2:poly(radio, 2)2:poly(newspaper, 2)1  -0.673   0.5018    
#R> poly(TV, 2)1:poly(radio, 2)1:poly(newspaper, 2)2  -0.713   0.4767    
#R> poly(TV, 2)2:poly(radio, 2)1:poly(newspaper, 2)2   1.320   0.1886    
#R> poly(TV, 2)1:poly(radio, 2)2:poly(newspaper, 2)2   1.551   0.1227    
#R> poly(TV, 2)2:poly(radio, 2)2:poly(newspaper, 2)2  -0.598   0.5509    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 0.6169 on 173 degrees of freedom
#R> Multiple R-squared:  0.9878,	Adjusted R-squared:  0.986 
#R> F-statistic: 540.8 on 26 and 173 DF,  p-value: < 2.2e-16

length(fita6$coefficients)
#R> [1] 27
```



<!--chapter:end:29-linear_regression.Rmd-->

---
output:
  pdf_document: default
  html_document: default
---
# Scoping {#scoping}


## Introduction Part 

In general, a function and its sub-functions create their own environment where the function was created. The lexical scoping that is used by R sometimes changes towards dynamic scoping. Nevertheless, in our book we mainly focus on lexical scoping. The set of rules, that describes scoping looks for the value of a name such as a code that contains `myv <- 12` and by writing `myv` which means that R retrieves 12 from an environment. 

Typically, a function is defined in the global environment, so that the values of free variables are just found in the user’s workspace. This behavior is logical for most people and is usually the “right thing” to do. However, in R you can have functions defined inside other functions (languages like C don’t let you do this). Now things get interesting—in this case the environment in which a function is defined is the body of another function!



```r
mean <- function(x) {
  x+1
}
mean(1:10)
#R>  [1]  2  3  4  5  6  7  8  9 10 11

rm(mean)

mean(1:10)
#R> [1] 5.5
```


## Rule 1: name masking  

R will check one level up in the partent if a name is not defined in a function:


```r
a <- 15

f <- function(){
  b <- 5
  a + b # same as return(a + b)
}

f()
#R> [1] 20

c <- 9
g <- function() {
  d <- 2
  h <- function() {
    e <- 7
    c + 4*d + e
  }
  h()
}

g()
#R> [1] 24



c <- 9
d <- 2
g <- function() {
  d <- 2
  h <- function() {
    e <- 7
    c + 4*d + e
  }
  h()
}
 g()
#R> [1] 24
```



## Rule 2: new start

After a function has been called, a new environment was created so that the function does not know that it has been called before. 


```r
a 
#R> [1] 15
z <- function() {
  if (exists("a")) { 
    a <- a + 3
    a
  } else {
    a <- 11 
    a
  } 
}
z()
#R> [1] 18

z()
#R> [1] 18
z()
#R> [1] 18

a <- 4
# gives this output because when the function z looks for 'a', NOW, it finds it in the parent 
z() 
#R> [1] 7


l <- function() {
  a <- 5 
  # 'a' is defined in the environment, so no look into the parent required
  if (exists("a")) { 
    a <- a + 3
    a
  } else {
    a <- 11 
    a
  } 
}
l()
#R> [1] 8
```

## Rule 3: dynamic lookup

In case of a change in the environment in between calls, the values and the outcome of the function will be different. If it is possible, this type of error should be avoided


```r
v <- function() a^3 #like we had in a chapter before it works also with exponents
a <- 4
v() 
#R> [1] 64
# needs a value for 'a' because it does not define one within its environment; 
# therefore, u() looks up to, in this case, the global environment
a <- 6
v()
#R> [1] 216
```

## Functions inside functions

Here is an example of a function that returns another function as its return value. Remember, in R functions are treated like any other object and so this is perfectly valid:


```r
m.power <- function(pow){
  m.exp <- function(b){ b^pow }
  m.exp # return the m.exp function
}
```

A function always preserves the environment in which it has been created and therefore R can create many functions with that function. 




```r

mycube <- m.power(3) #m.power() function is a kind of “constructor function” that can be used to construct other functions.
mycube(9)
#R> [1] 729

mysquare <- m.power(2)
mysquare(7)
#R> [1] 49

# ls(environment(m.power)) gives the global environment
ls(environment(mycube)) 
#R> [1] "m.exp" "pow"

w <- function(k){
  q <- 6
  k*q
}

z <- function() w(2) # z is itself a function that inherits the environment of w
# but z, here, is forced to use 2 as an argument 

z()
#R> [1] 12
```


## Examples


The following example illustrates lexical scoping.

```r
yy <- 10

ff <- function(xx){
  yy <- 2
  yy^2 + gg(xx)
}

gg <- function(xx){
  xx*yy
}

ff(3) 
#R> [1] 34
```


In order to find out what `g(2)` produces after a set of commands it is important to keep the environment in which the function has been created in mind since it provides information about the correct bindings, also called parents. 


```r
a <- 1
b <- 2
f <- function(x){
  a*x + b
}
g <- function(x){
  a <- 2
  b <- 1
  f(x)
}

g(2)
#R> [1] 4
```

Compare to `g(2)` here.


```r
a <- 1
b <- 2
f <- function(a,b){
  return( function(x) {a*x + b})
}
g <- f(2,1)
g(2)
#R> [1] 5
```


## Lexical vs Dynamic Scoping

We can use the following example to demonstrate the difference between lexical and dynamic scoping rules:


```r

y <- 10
 
f <- function(x) {
         y <- 2
         y^2 + g(x)
 }
 
 g <- function(x) { 
         x*y
 }
 
f(3)
#R> [1] 34
```

With lexical scoping the value of y in the function g is looked up in the environment in which the function was defined, in this case the global environment, so the value of y is 10. With dynamic scoping, the value of y is looked up in the environment from which the function was called (sometimes referred to as the calling environment). In R the calling environment is known as the parent frame. In this case, the value of y would be 2.

When a function is defined in the global environment and is subsequently called from the global environment, then the defining environment and the calling environment are the same. This can sometimes give the appearance of dynamic scoping.

Consider this example:

```{r
 g <- function(x) { 
         a <- 3
         x+a+y   
         ## 'y' is a free variable
 }
 
g(2) Error in g(2): object 'y' not found
y <- 3
g(2)
[1] 8
```
Here, y is defined in the global environment, which also happens to be where the function g() is defined.

There are numerous other languages that support lexical scoping, including_

-Scheme
-Perl
-Python
-Common Lisp (all languages converge to Lisp, right?)

Lexical scoping in R has consequences beyond how free variables are looked up. In particular, it’s the reason that all objects must be stored in memory in R. This is because all functions must carry a pointer to their respective defining environments, which could be anywhere. In the S language (R’s close cousin), free variables are always looked up in the global workspace, so everything can be stored on the disk because the “defining environment” of all functions is the same.

<!--chapter:end:30-scoping.Rmd-->

# Introduction to accuracy assessment


## (Root) Mean square error {#rmse}

This chapter provides an introduction to the task of assessing the accuracy of a fit when the response variable is numeric.  
The most common metric used to assess the quality of a fit is the mean square error (MSE) -- or the root thereof, the **root mean square error** (RMSE). We shall use this latter.   
This metric is simply compiled by taking the root of the average of the squares of the deviations between the predicted values and the observed values.
\[\text{RMSE}(\hat{f}, data) = \sqrt{\frac{1}{n}\sum_{i=1}^n \big(y_i -\hat{f}(X_i)\big)^2}\]

Obviously, the lower the MSE, the most accurate the fit.  
Both \(y_i\) and \(\hat{f}(X_i)\) are vectors. We can write a function to calculate the MSE for any given vector of observed values and predicted values.


```r
# a function for calculating the RMSE from two vectors
c.rmse <- function(observed, predicted){
	(observed - predicted)^2 %>%
    mean %>%
    sqrt %>%
    round(3)
}

# c.rmse <- function(observed, predicted){
# 	round(sqrt(mean((observed - predicted)^2)),3) 
# }
```

As a illustration, we can calculate the RMSE error of the different fits of Section \@ref(polyn) to which we had an extra one.


```r
require(ISLR)
data("Auto")

# estimate the models
model.pd1 <- lm(mpg ~ horsepower, data = Auto)
model.pd2 <- lm(mpg ~ horsepower + I(horsepower^2), data = Auto)
model.pd5 <- lm(mpg ~ poly(horsepower, 5), data = Auto)  # number in blue is the respective polynom
model.pd9 <- lm(mpg ~ poly(horsepower, 9), data = Auto)




models.rmse <- tibble(
            model = paste0("model.pd",c(1,2,5,9)),
						RMSE= c(
						  c.rmse(Auto$mpg,predict(model.pd1)),
							c.rmse(Auto$mpg,predict(model.pd2)),
							c.rmse(Auto$mpg,predict(model.pd5)),
							c.rmse(Auto$mpg,predict(model.pd9))
							)
					)
models.rmse
#R> # A tibble: 4 x 2
#R>   model      RMSE
#R>   <chr>     <dbl>
#R> 1 model.pd1  4.89
#R> 2 model.pd2  4.36
#R> 3 model.pd5  4.29
#R> 4 model.pd9  4.25
```

## Over-fitting

The example above illustrates an important aspect in the context of predictions: the RMSE error calculated on the data that was used to estimate the model decreases with the complexity of the estimated model, for instance as measure by the number of coefficients in the linear model.   


```r
# a function for calculating the number of estimated coefficients in lm
n.coef <- function(model){
	model %>%
    coefficients %>%
    length %>%
    {. - 1}
}

length(model.pd5$coefficients) -1
#R> [1] 5

n.coef(model.pd5)
#R> [1] 5

models.rmse$n.coef <- c(n.coef(model.pd1),
                        n.coef(model.pd2),
                        n.coef(model.pd5),
                        n.coef(model.pd9))
```

Now we plot to see the different polynoms with the respective RMSE:


```r
models.rmse %>%
  ggplot(aes(x=n.coef, y= RMSE)) +
  geom_line(color = "dodgerblue") + 
  geom_point(color = "dodgerblue") +
  scale_x_continuous(breaks = c(1,2,5,9) )
```

\begin{figure}
\includegraphics[width=1\linewidth]{MyR_files/figure-latex/unnamed-chunk-223-1} \caption{RMSE for various numbers of coefficients in the linear model.}(\#fig:unnamed-chunk-223)
\end{figure}

```r

# alternatively
# plot(models.rmse$n.coef, models.rmse$RMSE, type="b", col = "dodgerblue")
```

What should become apparent there is always a way to improve the accuracy of the fit when calculating the RMSE using the data that was used to estimate the model. This is a very general conclusion illustrated above by adding terms of a polynomial in the linear model.  

## Train versus test data

In order to avoid over-fitting, one could assess how the model fits the data by calculating the RMSE on data never seen in the estimation of the model. This data is called **test data**.  
Test data may or may not appear naturally in a given context. If it is not, a common strategy is to randomly select a part of the data that will not be used to estimate the model but simply to assess its accuracy. This division is referred to as the train-test split of the data.  
This implies that the RMSE must now be calcultated for two sets of predictions.  
\[\text{RMSE}_\text{train}(\hat{f}, \text{train data}) = \sqrt{\frac{1}{n_{\text{train}}}\sum_{i\in \text{train}} \big(y_i -\hat{f}(X_i)\big)^2}\]
\[\text{RMSE}_\text{test}(\hat{f}, \text{test data}) = \sqrt{\frac{1}{n_{\text{test}}}\sum_{i \in \text{test}} \big(y_i -\hat{f}(X_i)\big)^2}\]

How this works, will be illustrated in the solution to the final task of the project (Section: \@ref(solution_final_task) . This is a good example of how the whole process of calculating the RMSE works.

<!--chapter:end:31-intro_accuracy.Rmd-->

---
title: "Final Project"
output: html_document
---

# Final Task

This document provides the instructions for the final project that students must present for this class.

In short

In this project, you must provide:
• your best vector of predictions of length 140 x 7 = 980, necessarily called our.predictions,
• a fully reproducible Rmd file giving and explaining all the steps and R code used to obtain that vector.

A train.data is provided for you to estimate and select relevant models. There are 7 different responses to be estimated. Models may (should) vary for each response.
Based on these models, the predictions are made on test.data for which you have the predictors but not the responses.

Your vector of predictions will be evaluated with the root mean square error criterion both for the overall performance and for each individual response.

## Data

The file project_data.Rdata contains two data frames, train.data and test.data. These names are self-explanatory. Their dimensions are the following:

```{r
dim(train.data)
## [1] 200 18
dim(test.data)
## [1] 140 11
```

The data used in this problem comes from a study on water quality. Samples were taken from sites on different rivers where the quantities of eight chemical substances were recorded: the maximum pH value (mxPH), the minimum oxygen value (mnO2) as well as the mean values of chloride (Cl), nitrates (NO3), ammonium (NH4), orthophosphate (oPO4), phosphate (PO4) and chlorophyll (Chla). Further information for each observation includes three categorical variables: the season when the sample was taken (season), the river size (size) and the flow velocity (speed). In total, that are 11 predictors for the frequency of 7 plants. In the train.data, these plants are note a1 to a7.
The test.data has the same structure but does not contain the frequencies for each of the 7 plants. Your goal is precisely to estimate them for the 140 observations. Data summaries and visualizations can help you gain insights into the data.

## Some specifics

### Models and their selection

Because there are 7 responses to estimate, you can/should use 7 models. Available techniques include linear models, trees, random forests, etc. . . For every model that you try, provide a short description. Of course, you do not need to describe sub-versions such as yet another polynomial. However, you cannot simply present only your chosen model. The process of selection must also be described. This include parameter selection such as the degree of
polynomial or the size of the tree. Importantly, it also includes methods to evaluate the models (crossvalidation). Your 980 predictions must be stacked into a vector so that they can be compared with the actual values and evaluated with the root mean square error.
Your scored on the quality of the predictions will be determined by comparing your RMSE with mine.

### NA’s

Both data frames contain NA’s. To deal with them, there are various options:
• remove the observations with NA’s,
• fill the blanks,
• use a mix of these two.

Of course, whatever method is chosen in the train data, must similarly be used in the test data. Recall, however, that the test data must never be used in the estimation process.
In this particular case, it is acceptable to delete train observations that seem too noisy to be useful in the estimation.

train.data %>% is.na %>% rowSums %>% table

>> .
>> 0 1 2 6
>> 184 7 7 2

As for the missing values in some variables, you can fill them with an appropriate choice. Here, you have many options. These range from the simplest (and least accurate) such as replacing with the mean of the variable, to the most sophisticated such as replacing each missing value with the prediction of a complex model. Intermediate solutions include exploiting correlations between variables. No matter what option you take, you must be clear about your choice.

test.data %>% complete.cases %>% table

>> .
>> FALSE TRUE
>> 18 122

Recall that the test data also contains missing values. Hence, your predictions will start by filling them by using the same approach that you used with the train data.

<!--chapter:end:32-Final_Task.Rmd-->

---
title: "Solution"
output: html_document
---

# Solution to the final task 

This part of the book focuses on the final task of our group project in Data Science at Hochschule Fresenius (the final task is described in the previous chapter). 

To understand the process of finding solution, we will divide this chapter into two parts:

1. Trial and error 

2. Model used for the solution of the final task

The first part ("Trial and error") focuses on the first steps of finding a solution for the final task, which was the attempt to use multiple linear regressions, in order to analyze the data and find the "best" predictions. It is therefore the first "failure" of finding a solution.

The second part ("Model used for the solution of the final task") focuses on a multiple linear regression model to cross-validation we have found and used as a solution to the problem. This model is therefore our solution to the problem, which is relevant for the project.

## Trial and error 

### First attempt

Our first attempt was to make use of the interaction terms of linear regressions, since interactions can be done between quantitative and categorical variables. We therefore thought it would be very easy to interpret and even visualize, despite the multiple variables given in the task.

Here the example:

Before starting, let's load the required data:


```r
load("project_data (1).Rdata")
```

Step 1: Define the data set (Use train.data).


```r
train.dt <- lm(a1 ~ mxPH + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
```


```r
summary(train.dt)
#R> 
#R> Call:
#R> lm(formula = a1 ~ mxPH + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, 
#R>     data = train.data)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -32.884 -12.096  -2.628   7.171  68.436 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)   
#R> (Intercept) 64.0594094 26.2377683   2.441  0.01561 * 
#R> mxPH        -3.9524146  3.2635549  -1.211  0.22748   
#R> Cl          -0.0559842  0.0324522  -1.725  0.08625 . 
#R> NO3         -1.4925146  0.5185500  -2.878  0.00449 **
#R> NH4          0.0015551  0.0009702   1.603  0.11075   
#R> oPO4         0.0022141  0.0369305   0.060  0.95226   
#R> PO4         -0.0591881  0.0276658  -2.139  0.03377 * 
#R> Chla        -0.0965602  0.0798308  -1.210  0.22806   
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 17.64 on 177 degrees of freedom
#R>   (15 observations deleted due to missingness)
#R> Multiple R-squared:  0.3042,	Adjusted R-squared:  0.2767 
#R> F-statistic: 11.06 on 7 and 177 DF,  p-value: 1.446e-11
```

Step 2: Get rid of the NA's.


```r
is.na(train.data)
#R>        season  size speed  mxPH  mnO2    Cl   NO3   NH4  oPO4   PO4  Chla
#R>   [1,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [2,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [3,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [4,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [5,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [6,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [7,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [8,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [9,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [10,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [11,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [12,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [13,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [14,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [15,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [16,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [17,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [18,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [19,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [20,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [21,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [22,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [23,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [24,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [25,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [26,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [27,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [28,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE FALSE
#R>  [29,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [30,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [31,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [32,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [33,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [34,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [35,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [36,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [37,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [38,]  FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [39,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [40,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [41,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [42,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [43,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [44,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [45,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [46,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [47,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [48,]  FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [49,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [50,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [51,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [52,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [53,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [54,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [55,]  FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE
#R>  [56,]  FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE
#R>  [57,]  FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE
#R>  [58,]  FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE
#R>  [59,]  FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE
#R>  [60,]  FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE
#R>  [61,]  FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE
#R>  [62,]  FALSE FALSE FALSE FALSE  TRUE  TRUE  TRUE  TRUE  TRUE FALSE  TRUE
#R>  [63,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE
#R>  [64,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [65,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [66,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [67,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [68,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [69,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [70,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [71,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [72,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [73,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [74,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [75,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [76,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [77,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [78,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [79,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [80,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [81,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [82,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [83,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [84,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [85,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [86,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [87,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [88,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [89,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [90,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [91,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [92,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [93,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [94,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [95,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [96,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [97,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [98,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [99,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [100,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [101,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [102,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [103,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [104,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [105,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [106,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [107,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [108,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [109,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [110,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [111,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [112,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [113,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [114,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [115,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [116,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE
#R> [117,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [118,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [119,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [120,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [121,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [122,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [123,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [124,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [125,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [126,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [127,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [128,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [129,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [130,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [131,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [132,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [133,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [134,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [135,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [136,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [137,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [138,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [139,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [140,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [141,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [142,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [143,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [144,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [145,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [146,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [147,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [148,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [149,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [150,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [151,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [152,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [153,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [154,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [155,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [156,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [157,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [158,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [159,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [160,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [161,]  FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE FALSE
#R> [162,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [163,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [164,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [165,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [166,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [167,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [168,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [169,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [170,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [171,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [172,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [173,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [174,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [175,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [176,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [177,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [178,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [179,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [180,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [181,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [182,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [183,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [184,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE  TRUE
#R> [185,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [186,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [187,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [188,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [189,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [190,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [191,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [192,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [193,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [194,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [195,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [196,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [197,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [198,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [199,]  FALSE FALSE FALSE FALSE FALSE  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE
#R> [200,]  FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>           a1    a2    a3    a4    a5    a6    a7
#R>   [1,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [2,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [3,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [4,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [5,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [6,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [7,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [8,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>   [9,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [10,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [11,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [12,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [13,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [14,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [15,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [16,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [17,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [18,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [19,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [20,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [21,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [22,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [23,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [24,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [25,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [26,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [27,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [28,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [29,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [30,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [31,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [32,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [33,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [34,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [35,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [36,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [37,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [38,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [39,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [40,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [41,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [42,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [43,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [44,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [45,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [46,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [47,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [48,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [49,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [50,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [51,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [52,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [53,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [54,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [55,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [56,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [57,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [58,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [59,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [60,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [61,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [62,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [63,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [64,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [65,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [66,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [67,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [68,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [69,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [70,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [71,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [72,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [73,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [74,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [75,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [76,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [77,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [78,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [79,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [80,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [81,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [82,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [83,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [84,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [85,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [86,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [87,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [88,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [89,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [90,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [91,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [92,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [93,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [94,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [95,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [96,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [97,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [98,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R>  [99,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [100,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [101,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [102,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [103,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [104,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [105,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [106,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [107,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [108,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [109,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [110,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [111,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [112,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [113,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [114,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [115,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [116,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [117,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [118,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [119,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [120,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [121,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [122,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [123,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [124,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [125,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [126,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [127,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [128,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [129,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [130,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [131,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [132,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [133,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [134,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [135,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [136,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [137,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [138,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [139,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [140,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [141,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [142,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [143,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [144,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [145,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [146,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [147,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [148,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [149,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [150,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [151,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [152,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [153,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [154,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [155,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [156,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [157,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [158,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [159,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [160,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [161,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [162,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [163,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [164,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [165,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [166,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [167,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [168,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [169,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [170,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [171,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [172,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [173,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [174,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [175,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [176,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [177,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [178,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [179,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [180,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [181,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [182,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [183,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [184,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [185,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [186,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [187,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [188,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [189,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [190,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [191,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [192,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [193,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [194,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [195,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [196,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [197,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [198,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [199,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
#R> [200,] FALSE FALSE FALSE FALSE FALSE FALSE FALSE
na.omit(train.data)
#R>     season   size  speed  mxPH  mnO2      Cl    NO3       NH4    oPO4
#R> 1   winter  small medium 8.000  9.80  60.800  6.238   578.000 105.000
#R> 2   spring  small medium 8.350  8.00  57.750  1.288   370.000 428.750
#R> 3   autumn  small medium 8.100 11.40  40.020  5.330   346.667 125.667
#R> 4   spring  small medium 8.070  4.80  77.364  2.302    98.182  61.182
#R> 5   autumn  small medium 8.060  9.00  55.350 10.416   233.700  58.222
#R> 6   winter  small   high 8.250 13.10  65.750  9.248   430.000  18.250
#R> 7   summer  small   high 8.150 10.30  73.250  1.535   110.000  61.250
#R> 8   autumn  small   high 8.050 10.60  59.067  4.990   205.667  44.667
#R> 9   winter  small medium 8.700  3.40  21.950  0.886   102.750  36.300
#R> 10  winter  small   high 7.930  9.90   8.000  1.390     5.800  27.250
#R> 11  spring  small   high 7.700 10.20   8.000  1.527    21.571  12.750
#R> 12  summer  small   high 7.450 11.70   8.690  1.588    18.429  10.667
#R> 13  winter  small   high 7.740  9.60   5.000  1.223    27.286  12.000
#R> 14  summer  small   high 7.720 11.80   6.300  1.470     8.000  16.000
#R> 15  winter  small   high 7.900  9.60   3.000  1.448    46.200  13.000
#R> 16  autumn  small   high 7.550 11.50   4.700  1.320    14.750   4.250
#R> 17  winter  small   high 7.780 12.00   7.000  1.420    34.333  18.667
#R> 18  spring  small   high 7.610  9.80   7.000  1.443    31.333  20.000
#R> 19  summer  small   high 7.350 10.40   7.000  1.718    49.000  41.500
#R> 20  spring  small medium 7.790  3.20  64.000  2.822  8777.600 564.600
#R> 21  winter  small medium 7.830 10.70  88.000  4.825  1729.000 467.500
#R> 22  spring  small   high 7.200  9.20   0.800  0.642    81.000  15.600
#R> 23  autumn  small   high 7.750 10.30  32.920  2.942    42.000  16.000
#R> 24  winter  small   high 7.620  8.50  11.867  1.715   208.333   3.000
#R> 25  spring  small   high 7.840  9.40  10.975  1.510    12.500   3.000
#R> 26  summer  small   high 7.770 10.70  12.536  3.976    58.500   9.000
#R> 27  winter  small   high 7.090  8.40  10.500  1.572    28.000   4.000
#R> 29  winter  small   high 8.000  9.80  16.000  0.730    20.000  26.000
#R> 30  spring  small   high 7.200 11.30   9.000  0.230   120.000  12.000
#R> 31  autumn  small   high 7.400 12.50  13.000  3.330    60.000  72.000
#R> 32  winter  small   high 8.100 10.30  26.000  3.780    60.000 246.000
#R> 33  summer  small   high 7.800 11.30  20.083  3.020    49.500  53.000
#R> 34  autumn  small medium 8.400  9.90  34.500  2.818  3515.000  20.000
#R> 35  winter  small medium 8.270  7.80  29.200  0.050  6400.000   7.400
#R> 36  summer  small medium 8.660  8.40  30.523  3.444  1911.000  58.875
#R> 37  winter  small   high 8.300 10.90   1.170  0.735    13.500   1.625
#R> 39  winter  small medium 8.300  8.90  20.625  3.414   228.750 196.620
#R> 40  spring  small medium 8.100 10.50  22.286  4.071   178.570 182.420
#R> 41  winter  small medium 8.000  5.50  77.000  6.096   122.850 143.710
#R> 42  summer  small medium 8.150  7.10  54.190  3.829   647.570  59.429
#R> 43  winter  small   high 8.300  7.70  50.000  8.543    76.000 264.900
#R> 44  spring  small   high 8.300  8.80  54.143  7.830    51.429 276.850
#R> 45  winter  small   high 8.400 13.40  69.750  4.555    37.500  10.000
#R> 46  spring  small   high 8.300 12.50  87.000  4.870    22.500  27.000
#R> 47  autumn  small   high 8.000 12.10  66.300  4.535    39.000  16.000
#R> 49  spring  small medium 7.600  9.60  15.000  3.020    40.000  27.000
#R> 50  autumn  small medium 7.290 11.21  17.750  3.070    35.000  13.000
#R> 51  winter  small medium 7.600 10.20  32.300  4.508   192.500  12.750
#R> 52  summer  small medium 8.000  7.90  27.233  1.651    28.333   7.300
#R> 53  winter  small   high 7.900 11.00   6.167  1.172    18.333   7.750
#R> 54  spring  small   high 7.900  9.00   5.273  0.910    33.636   9.000
#R> 64  spring  small   high 7.570 10.80   4.575  1.203    27.500   2.000
#R> 65  summer  small   high 7.190 11.70   4.326  1.474   160.000   2.500
#R> 66  winter  small   high 7.440 10.10   2.933  0.770    15.000   1.333
#R> 67  spring  small   high 7.140  9.80   3.275  0.923    15.000   1.250
#R> 68  summer  small   high 7.000 12.10   3.136  1.208    16.200   1.800
#R> 69  winter  small medium 7.500  1.50  32.400  0.921  1386.250 220.750
#R> 70  spring  small medium 7.500  1.80  29.775  1.051  2082.850 209.857
#R> 71  summer  small medium 7.800  7.10  32.540  1.720  2167.370 151.125
#R> 72  autumn medium medium 8.500  8.10  38.125  3.850   225.000  45.000
#R> 73  summer medium medium 7.925 10.20  34.037  9.080   109.000  55.000
#R> 74  winter medium medium 8.100  8.10 136.000  3.773   245.000 136.750
#R> 75  spring medium medium 8.200  6.80 129.375  3.316   271.250 100.000
#R> 76  spring medium   high 9.100  9.40  35.750  5.164    32.500  85.500
#R> 77  autumn medium medium 8.100  9.80  29.500  1.287   224.286  25.167
#R> 78  winter medium medium 8.000  5.90  27.400  0.735   133.636  36.000
#R> 79  spring medium medium 8.000  3.30  26.760  0.658   165.000  37.375
#R> 80  winter medium   high 7.500  9.20  11.000  3.310   101.000  26.600
#R> 81  spring medium   high 7.400  9.80  11.000  3.235   255.000  38.750
#R> 82  autumn medium   high 7.300 11.70  10.400  4.930   130.000  10.800
#R> 83  winter medium   high 7.400  8.90  13.500  5.442   123.333  27.667
#R> 84  summer medium   high 7.400 11.17  12.146  6.188    89.600  32.000
#R> 85  autumn medium medium 7.500 10.80  31.000  4.408   737.500 111.250
#R> 86  winter medium medium 7.600  6.00  53.000  3.734   914.000 137.600
#R> 87  summer medium medium 7.400 10.77  36.248  3.730   429.200  57.600
#R> 88  winter medium medium 7.800  3.60  48.667  4.030  5738.330 412.333
#R> 89  summer medium medium 7.600  9.70  53.102  7.160  4073.330 282.167
#R> 90  winter medium medium 8.500  8.60 125.600  3.778   124.167 197.833
#R> 91  spring medium medium 8.700  9.40 173.750  3.318   101.250 267.750
#R> 92  summer medium medium 8.100 10.70  94.405  4.698   153.000 191.750
#R> 93  winter medium   high 8.800  8.50  53.333  5.132    96.667 120.500
#R> 94  spring medium   high 7.800 10.50  70.000  2.443    98.333 144.667
#R> 95  summer medium   high 7.900 11.80  63.510  4.940   137.000 159.500
#R> 96  autumn medium    low 8.500 10.50  56.717  0.330   215.714  23.000
#R> 97  winter medium    low 9.100  5.40  61.050  0.308   105.556 104.222
#R> 98  spring medium    low 8.900  4.50  57.750  0.267   155.000  97.333
#R> 99  winter medium   high 7.900  6.30 101.875  3.978   153.750  51.750
#R> 100 summer medium   high 7.800  8.20  85.982  6.200   421.667  31.333
#R> 101 winter medium medium 7.700  7.10  63.625  3.140   122.500  28.625
#R> 102 spring medium medium 7.800  6.50  82.111  2.603   215.556  12.889
#R> 103 winter medium    low 7.700  5.30  65.333  2.899   371.111  51.111
#R> 104 summer medium    low 7.500  8.80  58.331  8.688   758.750 104.500
#R> 105 autumn medium    low 7.600 10.00  49.625  5.456   308.750  38.625
#R> 106 winter medium    low 8.700  7.40  47.778  2.316    38.111  24.667
#R> 107 summer medium    low 7.700 11.10  47.229  8.759   239.000  54.000
#R> 108 autumn medium   high 8.300 11.10  41.500  4.665   931.833  39.000
#R> 109 winter medium   high 8.430  6.00  40.167  2.670   723.667  60.833
#R> 110 summer medium   high 8.160 11.10  32.056  5.694   461.875  71.000
#R> 111 winter medium   high 8.700  9.80   5.889  1.534    51.111   9.667
#R> 112 spring medium   high 8.200 11.30   7.250  1.875    25.000   6.500
#R> 113 summer medium   high 8.500 11.80   7.838  1.732   206.538   8.692
#R> 114 spring medium medium 7.800  6.00  53.425  0.381   118.571  37.857
#R> 115 summer medium medium 8.000  9.70  57.848  0.461   217.750  37.000
#R> 117 summer medium   high 8.600 11.62   1.549  0.445    25.833  16.833
#R> 118 autumn medium medium 8.300 11.60   5.830  0.701    12.727   3.545
#R> 119 spring medium    low 8.400  5.30  74.667  3.900   131.667 261.600
#R> 120 summer medium    low 8.200  6.60 131.400  4.188    92.000 238.200
#R> 121 winter medium medium 8.200  9.40  45.273  7.195   345.455 144.000
#R> 122 spring medium medium 8.100  7.10  42.636  5.078    56.364 166.727
#R> 123 summer medium medium 8.100  9.00  48.429  6.640   128.571 181.000
#R> 124 winter medium   high 7.400 10.70  11.818  2.163   170.909  36.909
#R> 125 spring medium   high 8.300  9.70  10.556  1.921    65.556  61.556
#R> 126 summer medium   high 8.600 10.70  12.000  2.231    43.750  62.625
#R> 127 winter medium medium 9.100 11.60  31.091  5.099   246.364  55.000
#R> 128 spring medium medium 9.000  6.90  28.333  2.954    76.667 102.333
#R> 129 summer medium medium 8.300 10.00  30.125  3.726   102.500  75.875
#R> 130 winter medium   high 8.500 10.10  10.936  1.335   236.000  34.636
#R> 131 spring medium   high 8.300  7.70  10.078  1.212   103.333  48.667
#R> 132 summer medium   high 7.300 10.50  11.088  1.374    92.375  48.625
#R> 133 winter medium medium 7.900  9.80 194.750  6.513  3466.660  23.000
#R> 134 spring medium medium 7.900  8.30 391.500  6.045   380.000 173.000
#R> 135 autumn medium medium 8.000 11.90 130.670  6.540   196.000  75.000
#R> 136 spring medium medium 8.000  9.20  39.000  4.860   120.000 187.000
#R> 137 autumn medium medium 8.100 11.70  35.660  5.130    46.500  49.000
#R> 138 winter medium    low 8.430  9.90  37.600  0.826   124.000  32.500
#R> 139 summer medium    low 8.100  6.20  39.000  0.673   112.857  60.000
#R> 140 winter medium medium 7.900 11.20  49.900  9.773   505.000  67.500
#R> 141 summer medium medium 8.100  6.20  51.113  5.099   175.000 132.500
#R> 142 spring medium   high 7.800  9.50   8.300  1.670    34.000  16.800
#R> 143 autumn medium   high 7.900 10.50  10.207  2.304   132.250  10.583
#R> 144 winter medium    low 8.000  4.50  79.077  8.984   920.000  70.000
#R> 145 spring medium    low 7.600  6.30  81.333  9.715   196.667  77.333
#R> 146 autumn medium    low 7.800  6.50  64.093  7.740  1990.160  47.500
#R> 147 winter medium   high 8.220  8.10  41.250  1.415   172.500  46.667
#R> 148 autumn medium   high 8.300  9.90  40.226  1.587   235.000  33.800
#R> 149 winter medium   high 8.470  9.00  46.167  2.102    84.667  48.000
#R> 150 spring medium   high 8.400  4.90  47.000  0.536    91.833 109.000
#R> 151 autumn medium   high 8.870 11.00  41.163  2.273    54.750  39.000
#R> 152 summer medium   high 7.700  4.40  53.000  2.310    90.000  22.200
#R> 153 autumn medium   high 7.300 11.80  44.205 45.650 24064.000  44.000
#R> 154 spring medium medium 7.900  6.00 127.833  2.680   176.667  27.500
#R> 155 autumn medium medium 7.800 10.53 100.830  5.410   486.500  24.000
#R> 156 spring  large    low 7.800  3.20  94.000  4.908  1131.660 175.667
#R> 157 summer  large    low 7.600  4.90  69.000  3.685  1495.000 234.500
#R> 158 spring  large    low 8.600  3.60  50.000  0.376   134.000  54.100
#R> 159 autumn  large    low 8.400 10.60  19.220  1.655    96.833  20.667
#R> 160 winter  large    low 8.300 11.50  26.000  1.870    62.500  30.750
#R> 162 spring  large    low 9.500  5.70  44.000  0.102   146.667 151.333
#R> 163 summer  large    low 8.800  8.80  43.000  0.130   103.333 180.667
#R> 164 autumn  large    low 8.840 12.90  43.090  0.846    52.200   8.600
#R> 165 winter  large   high 7.300  9.90  16.000  4.820   101.667  14.667
#R> 166 autumn  large   high 7.400 10.68  22.350  5.414   244.600  66.400
#R> 167 spring  large    low 9.100  4.30  82.857  0.860   137.273 102.364
#R> 168 autumn  large    low 8.530 11.10  63.292  1.726   227.600  84.300
#R> 169 winter  large    low 8.560  8.70  43.970  4.053   643.000 221.900
#R> 170 autumn  large    low 8.060  8.30  38.902  3.678   627.273 205.636
#R> 171 winter  large medium 8.240  6.10  95.367  3.561  1168.000 236.400
#R> 172 summer  large medium 7.910  6.20 151.833  3.923  1081.660 346.167
#R> 173 winter  large medium 8.210  9.30 104.818  3.908   124.364  82.222
#R> 174 spring  large medium 8.500  7.30  71.444  2.512    66.667  64.389
#R> 175 spring  large medium 8.600 10.60 208.364  4.459   197.909  87.333
#R> 176 winter  large medium 9.060  6.35 187.183  3.351    54.778 159.167
#R> 177 autumn  large   high 8.700 10.70   4.545  0.941    32.727  16.000
#R> 178 spring  large   high 8.100 10.70   3.500  1.013    12.500  12.750
#R> 179 summer  large   high 8.400 10.29   5.326  0.996    53.846   7.667
#R> 180 spring  large medium 8.600 10.10   2.111  0.663    11.111   3.222
#R> 181 summer  large medium 8.200  9.50   2.200  0.672    10.000   3.800
#R> 182 winter  large medium 8.500 10.50   2.750  0.758    10.500   4.000
#R> 183 summer  large medium 8.300 10.00   3.860  0.866    32.000   6.000
#R> 185 summer  large   high 8.100 10.20   7.613  0.699    32.500  26.625
#R> 186 winter  large    low 8.700 10.80  39.109  6.225   161.818 104.727
#R> 187 winter  large    low 8.700 11.70  22.455  3.765    88.182  41.300
#R> 188 summer  large    low 8.400  8.20  23.250  2.805    43.750  51.125
#R> 189 autumn  large    low 8.550 11.00  22.320  3.140    82.100  45.900
#R> 190 spring  large medium 8.500  7.60  12.778  1.873    17.778  50.889
#R> 191 autumn  large medium 8.700 11.40  15.541  2.323   103.000  34.500
#R> 192 winter  large medium 8.400 10.50  12.182  1.519    65.455  19.727
#R> 193 spring  large medium 8.200  8.20   7.333  1.003    37.778  19.111
#R> 194 autumn  large medium 8.580 11.10  23.825  3.617    72.600  51.111
#R> 195 summer  large medium 8.500  7.90  12.444  2.586    96.667  19.111
#R> 196 autumn  large medium 8.400  8.40  17.375  3.833    83.750  53.625
#R> 197 spring  large medium 8.300 10.60  14.320  3.200   125.333  35.333
#R> 198 autumn  large medium 8.200  7.00 139.989  2.978    60.110  78.333
#R> 200 summer  large medium 8.500  6.70  82.852  2.800    27.069  64.000
#R>         PO4    Chla   a1   a2   a3   a4   a5   a6   a7
#R> 1   170.000  50.000  0.0  0.0  0.0  0.0 34.2  8.3  0.0
#R> 2   558.750   1.300  1.4  7.6  4.8  1.9  6.7  0.0  2.1
#R> 3   187.057  15.600  3.3 53.6  1.9  0.0  0.0  0.0  9.7
#R> 4   138.700   1.400  3.1 41.0 18.9  0.0  1.4  0.0  1.4
#R> 5    97.580  10.500  9.2  2.9  7.5  0.0  7.5  4.1  1.0
#R> 6    56.667  28.400 15.1 14.6  1.4  0.0 22.5 12.6  2.9
#R> 7   111.750   3.200  2.4  1.2  3.2  3.9  5.8  6.8  0.0
#R> 8    77.434   6.900 18.2  1.6  0.0  0.0  5.5  8.7  0.0
#R> 9    71.000   5.544 25.4  5.4  2.5  0.0  0.0  0.0  0.0
#R> 10   46.600   0.800 17.0  0.0  0.0  2.9  0.0  0.0  1.7
#R> 11   20.750   0.800 16.6  0.0  0.0  0.0  1.2  0.0  6.0
#R> 12   19.000   0.600 32.1  0.0  0.0  0.0  0.0  0.0  1.5
#R> 13   17.000  41.000 43.5  0.0  2.1  0.0  1.2  0.0  2.1
#R> 14   15.000   0.500 31.1  1.0  3.4  0.0  1.9  0.0  4.1
#R> 15   61.600   0.300 52.2  5.0  7.8  0.0  4.0  0.0  0.0
#R> 16   98.250   1.100 69.9  0.0  1.7  0.0  0.0  0.0  0.0
#R> 17   50.000   1.100 46.2  0.0  0.0  1.2  0.0  0.0  0.0
#R> 18   57.833   0.400 31.8  0.0  3.1  4.8  7.7  1.4  7.2
#R> 19   61.500   0.800 50.6  0.0  9.9  4.3  3.6  8.2  2.2
#R> 20  771.600   4.500  0.0  0.0  0.0 44.6  0.0  0.0  1.4
#R> 21  586.000  16.000  0.0  0.0  0.0  6.8  6.1  0.0  0.0
#R> 22   18.000   0.500 15.5  0.0  0.0  2.3  0.0  0.0  0.0
#R> 23   40.000   7.600 23.2  0.0  0.0  0.0 27.6 11.1  0.0
#R> 24   27.500   1.700 74.2  0.0  0.0  3.7  0.0  0.0  0.0
#R> 25   11.500   1.500 13.0  8.6  1.2  3.5  1.2  1.6  1.9
#R> 26   44.136   3.000  4.1  0.0  0.0  0.0  9.2 10.1  0.0
#R> 27   13.600   0.500 29.7  0.0  0.0  4.9  0.0  0.0  0.0
#R> 29   45.000   0.800 17.1  0.0 19.6  0.0  0.0  0.0  2.5
#R> 30   19.000   0.500 33.9  1.0 14.6  0.0  0.0  0.0  0.0
#R> 31  142.000   4.900  3.4 16.0  1.2  0.0 15.3 15.8  0.0
#R> 32  304.000   2.800  6.9 17.1 20.2  0.0  4.0  0.0  2.9
#R> 33  130.750   5.800  0.0  8.0  1.9  0.0 11.2 42.7  1.2
#R> 34   47.000   2.300 13.6  9.1  0.0  0.0  1.4  0.0  0.0
#R> 35   23.000   0.900  5.3 40.7  3.3  0.0  0.0  0.0  1.9
#R> 36   84.460   3.600 18.3 12.4  1.0  0.0  0.0  0.0  1.0
#R> 37    3.000   0.200 66.0  0.0  0.0  0.0  0.0  0.0  0.0
#R> 39  253.250  12.320  2.0 38.5  4.1  2.2  0.0  0.0 10.2
#R> 40  255.280   8.957  2.2  2.7  1.0  3.7  2.7  0.0  0.0
#R> 41  296.000   3.700  0.0  5.9 10.6  1.7  0.0  0.0  7.1
#R> 42  175.046  13.200  0.0  0.0  0.0  5.7 11.3 17.0  1.6
#R> 43  344.600  22.500  0.0 40.9  7.5  0.0  2.4  1.5  0.0
#R> 44  326.857  11.840  4.1  3.1  0.0  0.0 19.7 17.0  0.0
#R> 45   40.667   3.900 51.8  4.1  0.0  0.0  3.1  5.5  0.0
#R> 46   43.500   3.300 29.5  1.0  2.7  3.2  2.9  9.6  0.0
#R> 47   39.000   0.800 54.4  3.4  1.2  0.0 18.7  2.0  0.0
#R> 49  121.000   2.800 89.8  0.0  0.0  0.0  0.0  0.0  0.0
#R> 50   20.812  12.100 24.8  7.4  0.0  2.5 10.6 17.1  3.2
#R> 51   49.333   7.900  0.0  0.0  0.0  4.6  1.2  0.0  3.9
#R> 52   22.900   4.500 39.1  0.0  1.2  2.2  5.4  1.5  3.2
#R> 53   11.800   0.500 81.9  0.0  0.0  0.0  0.0  0.0  0.0
#R> 54   11.818   0.800 54.0  0.0  0.0  2.4  0.0  0.0  0.0
#R> 64    6.750   1.000 20.3  4.3  5.5  0.0  0.0  0.0  1.4
#R> 65    7.200   0.300 15.8  1.7  7.8  0.0  0.0  2.4  1.4
#R> 66    6.000   0.600 55.5  0.0  1.7  1.4  0.0  0.0  0.0
#R> 67   10.750   2.500 10.3  0.0 42.8  2.2  0.0  0.0  0.0
#R> 68    2.500   0.500 64.2  0.0  3.0  0.0  0.0  0.0  0.0
#R> 69  351.600  10.000  0.0  0.0  1.5  7.6  0.0  0.0  6.1
#R> 70  313.600   1.000  1.9  4.9  2.6  3.0  0.0  0.0  1.9
#R> 71  279.066  13.100 25.5  3.9  1.0 11.0  0.0  0.0 12.5
#R> 72  152.333   5.200 11.3  1.7  2.0  2.2 13.3 10.6  0.0
#R> 73   58.623  11.600  4.4  4.0  3.3  0.0 11.7 21.4  1.2
#R> 74  249.250  20.870  1.9  5.8 24.8  4.6  9.5  5.1  1.2
#R> 75  233.500  13.000  1.6  8.0 17.6  3.7 11.5  7.0  0.0
#R> 76  215.500  18.370  2.2  9.6  5.0  1.0  8.6  7.9  2.2
#R> 77  102.333   3.600 64.9  1.0  0.0  1.0  2.9  1.4  1.0
#R> 78  105.727   3.000 15.1  7.3 23.2  3.4  4.1  0.0  0.0
#R> 79  111.375   3.000 14.4  0.0 11.8 11.3  5.5  0.0  0.0
#R> 80  108.000   1.300  6.7  0.0  5.4  3.4  4.9  6.9 10.8
#R> 81   56.667   2.000 10.8  0.0  0.0  4.6  6.5  2.2  1.4
#R> 82   60.000   4.300  1.2  0.0  1.7  0.0  7.5 17.7 14.4
#R> 83  104.000  21.000 12.6  4.3 21.9  1.0  2.4  3.3 22.1
#R> 84   69.930   3.100 14.7  4.1  1.0  0.0  7.7  8.5 31.2
#R> 85  214.000   2.900  3.3  0.0  0.0  5.0  1.9  6.2 25.6
#R> 86  254.600   4.300  0.0  0.0  0.0  4.6  9.0 13.1 30.1
#R> 87  169.001   3.200  2.8  0.0  0.0  2.6  5.2 13.2 16.7
#R> 88  607.167   4.300  0.0  0.0  2.6  2.4  5.0  0.0  2.4
#R> 89  624.733   6.800  0.0  0.0  0.0  1.0 35.6  9.9  0.0
#R> 90  303.333  40.000  0.0 15.2  8.8  0.0  8.6  5.1  2.7
#R> 91  391.750   3.500  0.0  5.5  3.3  0.0 20.8 12.4  0.0
#R> 92  265.250   7.300  0.0  2.1  1.6  0.0 20.8 32.9  0.0
#R> 93  232.833  31.000  1.2  5.6  6.3  1.7  1.2  0.0  1.0
#R> 94  244.000   9.000  0.0  3.1  3.5  1.6  8.2  9.9  0.0
#R> 95  218.000   6.500  0.0  5.2  0.0  0.0 28.8 20.4  1.0
#R> 96  138.500  20.829  5.7  0.0  0.0  4.4 12.4  8.3  7.8
#R> 97  239.000  72.478  3.6 31.9  2.4  0.0  0.0  0.0  2.2
#R> 98  235.667  98.817  1.2 16.2  0.0  0.0  0.0  0.0  1.0
#R> 99  205.875   2.000  4.0  2.1 35.1  6.8  7.3  0.0  0.0
#R> 100 211.667  21.900  5.9  3.4  1.0  1.2 17.8 49.4  1.0
#R> 101 186.500  30.000 16.5  2.1 19.5  3.5  5.3  1.2  3.2
#R> 102 154.125   5.200  7.0  0.0 13.5  4.3  8.7  0.0  4.3
#R> 103 183.667  17.200 58.7  0.0 11.5  6.6  0.0  0.0  0.0
#R> 104 292.625   3.000  8.7  0.0  3.0  5.3  9.4 33.2  0.0
#R> 105 285.714  75.000 17.0 21.6  1.6  1.4 10.2  3.6  1.1
#R> 106 201.778   3.000 12.3  5.4  1.9  0.0  1.4  0.0  1.9
#R> 107 275.143  65.700  8.8 19.6  4.7  0.0  0.0  0.0  2.7
#R> 108 124.200  13.100 23.7 13.7  0.0  1.7  6.4  2.6  0.0
#R> 109 141.833  25.000  0.0  6.4  7.3 12.7  0.0  0.0  4.2
#R> 110 132.546  15.000  3.6 38.8  0.0  0.0  1.2  0.0  2.4
#R> 111  17.333   1.000 64.3  1.5  8.0  0.0  0.0  0.0  0.0
#R> 112  26.000   0.300 46.6  0.0  2.5  0.0  0.0  0.0  0.0
#R> 113  16.662   2.100 24.0  0.0  1.0  0.0  0.0  0.0  0.0
#R> 114 102.571   1.200  3.7  1.4  1.1  2.1  3.2  6.4  0.0
#R> 115  86.997   3.000 18.1 14.5  0.0  0.0 11.5 22.3  0.0
#R> 117  18.293   1.400 43.7  0.0  1.2  0.0  0.0  4.7  0.0
#R> 118  13.200   3.200 86.6  0.0  0.0  0.0  0.0  0.0  0.0
#R> 119 432.909  24.917  1.9 12.7 25.9  0.0  0.0  0.0  6.8
#R> 120 320.400   6.800  1.2  1.9 22.9  0.0  8.1  0.0  0.0
#R> 121 287.000   9.882  1.4 18.4  0.0  0.0 20.0 29.5  0.0
#R> 122 262.727  17.200  1.6  8.9  6.6  0.0  9.2  1.6  1.4
#R> 123 222.286   6.429  3.3 11.6  7.0  0.0 17.9  4.7  0.0
#R> 124 122.000   5.555 14.6  0.0  0.0  1.9 22.1 12.7  1.4
#R> 125 127.222   5.233  1.7  0.0 10.3  2.6  8.9  6.7  0.0
#R> 126  89.625   2.150  3.3  0.0  0.0  1.9 34.3  7.1  6.0
#R> 127 284.000  88.255  0.0 36.6  4.1  0.0  1.2 16.7  6.1
#R> 128 277.333 110.456  0.0 16.4 10.1  0.0  0.0  0.0  6.6
#R> 129 177.625  50.225  1.5 32.8  1.0  4.1  0.0 15.8  2.4
#R> 130  72.900  11.100  4.2  0.0  1.4  1.9 16.2  0.0  1.4
#R> 131  82.444   2.000  4.1  0.0 25.3  2.1  8.0  0.0 18.6
#R> 132  66.750   3.300  1.2  0.0  2.3  0.0 44.4  7.5  1.9
#R> 133 173.750  15.300  0.0  0.0  1.0  0.0  9.0 64.6  0.0
#R> 134 317.000   5.500  2.4  1.7  4.2  8.3  1.7  0.0  2.4
#R> 135  84.000   4.500  7.8  8.7  2.1  0.0 14.9 22.9  2.4
#R> 136 213.000   2.000 10.3 26.5  6.1  0.0  5.6  1.5  2.2
#R> 137  88.500   2.500  1.5 72.6  0.0  0.0  3.4  6.8  3.4
#R> 138 115.000  11.700  9.2  2.9  2.0  1.3  2.5  0.0  0.0
#R> 139  98.143   2.000 28.1  0.0  0.0  4.0  1.2  0.0  0.0
#R> 140 143.750   5.450  2.1  2.6  0.0  0.0 15.0 15.7  0.0
#R> 141 197.143   6.400  1.4 15.7  1.4  0.0  3.5  0.0  1.6
#R> 142  35.200   1.000 19.0  0.0 22.0  5.0  1.1  5.4  0.0
#R> 143  23.485   2.000 42.5  0.0  2.2  1.0  0.0  0.0  0.0
#R> 144 200.231  19.400  2.5  1.4  1.4  6.2  4.1  1.8  3.9
#R> 145 147.833   3.000  4.4 11.2  6.8  0.0  1.0  0.0 31.6
#R> 146 276.000   8.100  6.5  4.1  0.0  7.7  9.9 18.2  7.0
#R> 147 123.333  30.400 39.7 12.7  0.0  1.1  2.7  0.0  1.6
#R> 148  75.207  23.800 32.8 28.0  2.0  3.5  1.0  0.0  1.5
#R> 149 116.200   7.300 12.2 16.0  1.0  1.4  1.9  1.2  0.0
#R> 150 188.667  32.000  1.9 25.4 21.7  0.0  0.0  1.0  0.0
#R> 151  72.696  22.700  0.0  5.6  1.2  0.0  8.0  2.7  0.0
#R> 152 116.200  16.000  0.0  0.0  0.0  1.2  5.7 32.1  0.0
#R> 153  34.000  53.100  2.2  0.0  0.0  1.2  5.9 77.6  0.0
#R> 154  76.333   2.100  3.4 21.5 14.0  1.8  3.9  0.0  0.0
#R> 155  58.374  27.500  2.8  1.9  0.0  1.2 19.0  4.5  0.0
#R> 156 361.000  28.567 24.8 10.4  0.0  6.9  0.0  0.0  2.7
#R> 157 236.000  22.500 32.5 12.0  0.0  5.0  0.0  0.0  1.9
#R> 158 125.800  26.800  0.0 28.0  0.0  0.0  0.0  0.0 15.1
#R> 159  54.916  20.600  0.0 11.3  1.8  0.0  2.5  0.0  1.4
#R> 160  75.333  34.750  0.0 20.1  0.0  0.0  0.0  0.0  0.0
#R> 162 252.500  93.683 12.3 21.7  3.9  0.0  0.0  0.0  3.9
#R> 163 269.667  92.667  7.2 28.2  0.0  0.0  0.0  0.0  3.3
#R> 164  46.438  81.540  3.4 21.5  0.0  0.0  0.0  0.0  2.7
#R> 165  85.000   2.000  0.0  0.0  0.0  2.4  0.0 17.8  3.6
#R> 166 171.272   3.800  1.1  0.0  1.4  0.0  6.6 42.1  5.2
#R> 167 232.900  54.367  0.0  6.0  2.9  0.0  0.0  0.0  2.9
#R> 168 146.452  21.220  1.4 14.7  2.5  0.0  0.0  0.0  2.0
#R> 169 246.667  14.700 12.5  2.1  0.0  1.2  6.4  4.5  1.7
#R> 170 219.909   6.209  0.0  0.0  0.0  0.0  8.6 52.5  0.0
#R> 171 272.222  20.578  2.5 13.2  0.0  2.0  7.4 17.2  0.0
#R> 172 388.167   5.083  1.7 12.0  4.9  2.7  0.0  5.9  1.7
#R> 173 167.900   5.609  1.4  4.6 10.8  2.2  5.5 42.4  0.0
#R> 174 137.778   9.384  0.0  3.8 16.0  4.0  0.0  0.0  3.3
#R> 175 194.100  27.618  0.0  1.2  0.0  0.0 11.3 11.5  0.0
#R> 176 221.278  20.800  0.0 21.1  3.7  0.0  0.0  0.0  1.9
#R> 177  21.300   1.100 39.7  0.0 12.9  0.0  0.0  0.0  0.0
#R> 178  11.000   0.600 37.3  9.7 13.6  0.0  2.2  0.0  1.2
#R> 179  14.354   0.800 52.4  7.5  9.4  0.0  1.4  1.9  0.0
#R> 180   7.000   1.300 48.3  2.0  0.0  0.0  0.0  0.0  0.0
#R> 181   6.200   0.800 50.4  3.8  0.0  0.0  0.0  0.0  0.0
#R> 182   7.654   4.000 56.8  5.0  0.0  0.0  0.0  0.0  0.0
#R> 183  16.000   2.860 17.3  6.7 19.7  0.0  0.0  0.0  0.0
#R> 185  52.875   2.000 18.1  1.7  2.0  0.0  1.7  5.9  0.0
#R> 186 228.364  46.075  1.1  3.9  2.1  0.0  3.9  4.6  2.3
#R> 187  85.400  17.491  0.0  4.7  0.0  0.0  2.6  2.6  0.0
#R> 188  87.125  14.775  0.0 12.0  1.7  0.0  2.7  0.0  0.0
#R> 189 101.455  18.330  1.7  7.0  1.2  0.0  4.8  3.1  0.0
#R> 190 127.000  24.556  0.0  0.0 10.2  1.7  1.2  0.0  5.5
#R> 191  81.558   5.620  7.6  0.0  1.2  0.0 15.9 31.8  5.9
#R> 192  50.455   8.155  2.9  4.6  1.0  0.0  6.6 16.6  0.0
#R> 193 120.889   5.111  2.2 12.7  8.8  0.0  0.0  0.0  1.2
#R> 194  91.111  22.900  3.8 22.0  2.9  0.0  3.1  5.5  0.0
#R> 195  61.444   6.167 18.9 13.2  5.0  0.0  6.1  0.0  0.0
#R> 196  79.750   2.338 12.7 21.7  5.6  0.0  1.0  0.0  0.0
#R> 197  75.904   4.667 18.0  7.0  1.7  0.0  4.8 10.3  1.0
#R> 198 140.220  31.738  0.0 15.9  2.4  1.0  0.0  0.0  0.0
#R> 200 140.517  18.300  2.4 10.5  9.0  7.8  0.0  0.0  5.8
```


```r
require(dplyr)
na.omit(train.data) %>% {cor(.[,c("mxPH", "Cl", "NO3", "NH4", "oPO4", "PO4", "Chla")])} %>% round(2)
#R>       mxPH   Cl   NO3   NH4 oPO4  PO4 Chla
#R> mxPH  1.00 0.15 -0.17 -0.15 0.09 0.10 0.43
#R> Cl    0.15 1.00  0.21  0.07 0.38 0.45 0.14
#R> NO3  -0.17 0.21  1.00  0.72 0.13 0.16 0.15
#R> NH4  -0.15 0.07  0.72  1.00 0.22 0.20 0.09
#R> oPO4  0.09 0.38  0.13  0.22 1.00 0.91 0.11
#R> PO4   0.10 0.45  0.16  0.20 0.91 1.00 0.25
#R> Chla  0.43 0.14  0.15  0.09 0.11 0.25 1.00
```


Step 3: Plot the first part dataset given (Data = train.data), which focuses on a1.


```r
train.int1 <- lm(a1 ~ mxPH + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
summary(train.int1) 
#R> 
#R> Call:
#R> lm(formula = a1 ~ mxPH + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, 
#R>     data = train.data)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -32.884 -12.096  -2.628   7.171  68.436 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)   
#R> (Intercept) 64.0594094 26.2377683   2.441  0.01561 * 
#R> mxPH        -3.9524146  3.2635549  -1.211  0.22748   
#R> Cl          -0.0559842  0.0324522  -1.725  0.08625 . 
#R> NO3         -1.4925146  0.5185500  -2.878  0.00449 **
#R> NH4          0.0015551  0.0009702   1.603  0.11075   
#R> oPO4         0.0022141  0.0369305   0.060  0.95226   
#R> PO4         -0.0591881  0.0276658  -2.139  0.03377 * 
#R> Chla        -0.0965602  0.0798308  -1.210  0.22806   
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 17.64 on 177 degrees of freedom
#R>   (15 observations deleted due to missingness)
#R> Multiple R-squared:  0.3042,	Adjusted R-squared:  0.2767 
#R> F-statistic: 11.06 on 7 and 177 DF,  p-value: 1.446e-11
plot(train.int1)
```

![](MyR_files/figure-latex/unnamed-chunk-229-1.pdf)<!-- --> ![](MyR_files/figure-latex/unnamed-chunk-229-2.pdf)<!-- --> ![](MyR_files/figure-latex/unnamed-chunk-229-3.pdf)<!-- --> ![](MyR_files/figure-latex/unnamed-chunk-229-4.pdf)<!-- --> 

Step 4: Plot the remaining parts of the dataset, which focuses on a2-a6.


```r
pred1 <- predict(train.int1)

plot(train.data$mxPH, train.data$a1)


t.data <- train.data
t.data$mxPH <- "Yes"

n.data <- train.data
n.data$mxPH <- "No"

pred1.1 <- predict(train.int1, data = t.data)

pred1.2 <- predict(train.int1, data = n.data)

plot(train.data$mxPH, train.data$a1)
lines(train.data$mxPH, train.data$a1, col="red")
lines(train.data$mxPH, train.data$a1, col="black")
```

![](MyR_files/figure-latex/unnamed-chunk-230-1.pdf)<!-- --> 

```r
train.data
#R>     season   size  speed  mxPH  mnO2      Cl    NO3       NH4    oPO4
#R> 1   winter  small medium 8.000  9.80  60.800  6.238   578.000 105.000
#R> 2   spring  small medium 8.350  8.00  57.750  1.288   370.000 428.750
#R> 3   autumn  small medium 8.100 11.40  40.020  5.330   346.667 125.667
#R> 4   spring  small medium 8.070  4.80  77.364  2.302    98.182  61.182
#R> 5   autumn  small medium 8.060  9.00  55.350 10.416   233.700  58.222
#R> 6   winter  small   high 8.250 13.10  65.750  9.248   430.000  18.250
#R> 7   summer  small   high 8.150 10.30  73.250  1.535   110.000  61.250
#R> 8   autumn  small   high 8.050 10.60  59.067  4.990   205.667  44.667
#R> 9   winter  small medium 8.700  3.40  21.950  0.886   102.750  36.300
#R> 10  winter  small   high 7.930  9.90   8.000  1.390     5.800  27.250
#R> 11  spring  small   high 7.700 10.20   8.000  1.527    21.571  12.750
#R> 12  summer  small   high 7.450 11.70   8.690  1.588    18.429  10.667
#R> 13  winter  small   high 7.740  9.60   5.000  1.223    27.286  12.000
#R> 14  summer  small   high 7.720 11.80   6.300  1.470     8.000  16.000
#R> 15  winter  small   high 7.900  9.60   3.000  1.448    46.200  13.000
#R> 16  autumn  small   high 7.550 11.50   4.700  1.320    14.750   4.250
#R> 17  winter  small   high 7.780 12.00   7.000  1.420    34.333  18.667
#R> 18  spring  small   high 7.610  9.80   7.000  1.443    31.333  20.000
#R> 19  summer  small   high 7.350 10.40   7.000  1.718    49.000  41.500
#R> 20  spring  small medium 7.790  3.20  64.000  2.822  8777.600 564.600
#R> 21  winter  small medium 7.830 10.70  88.000  4.825  1729.000 467.500
#R> 22  spring  small   high 7.200  9.20   0.800  0.642    81.000  15.600
#R> 23  autumn  small   high 7.750 10.30  32.920  2.942    42.000  16.000
#R> 24  winter  small   high 7.620  8.50  11.867  1.715   208.333   3.000
#R> 25  spring  small   high 7.840  9.40  10.975  1.510    12.500   3.000
#R> 26  summer  small   high 7.770 10.70  12.536  3.976    58.500   9.000
#R> 27  winter  small   high 7.090  8.40  10.500  1.572    28.000   4.000
#R> 28  autumn  small   high 6.800 11.10   9.000  0.630    20.000   4.000
#R> 29  winter  small   high 8.000  9.80  16.000  0.730    20.000  26.000
#R> 30  spring  small   high 7.200 11.30   9.000  0.230   120.000  12.000
#R> 31  autumn  small   high 7.400 12.50  13.000  3.330    60.000  72.000
#R> 32  winter  small   high 8.100 10.30  26.000  3.780    60.000 246.000
#R> 33  summer  small   high 7.800 11.30  20.083  3.020    49.500  53.000
#R> 34  autumn  small medium 8.400  9.90  34.500  2.818  3515.000  20.000
#R> 35  winter  small medium 8.270  7.80  29.200  0.050  6400.000   7.400
#R> 36  summer  small medium 8.660  8.40  30.523  3.444  1911.000  58.875
#R> 37  winter  small   high 8.300 10.90   1.170  0.735    13.500   1.625
#R> 38  spring  small   high 8.000    NA   1.450  0.810    10.000   2.500
#R> 39  winter  small medium 8.300  8.90  20.625  3.414   228.750 196.620
#R> 40  spring  small medium 8.100 10.50  22.286  4.071   178.570 182.420
#R> 41  winter  small medium 8.000  5.50  77.000  6.096   122.850 143.710
#R> 42  summer  small medium 8.150  7.10  54.190  3.829   647.570  59.429
#R> 43  winter  small   high 8.300  7.70  50.000  8.543    76.000 264.900
#R> 44  spring  small   high 8.300  8.80  54.143  7.830    51.429 276.850
#R> 45  winter  small   high 8.400 13.40  69.750  4.555    37.500  10.000
#R> 46  spring  small   high 8.300 12.50  87.000  4.870    22.500  27.000
#R> 47  autumn  small   high 8.000 12.10  66.300  4.535    39.000  16.000
#R> 48  winter  small    low    NA 12.60   9.000  0.230    10.000   5.000
#R> 49  spring  small medium 7.600  9.60  15.000  3.020    40.000  27.000
#R> 50  autumn  small medium 7.290 11.21  17.750  3.070    35.000  13.000
#R> 51  winter  small medium 7.600 10.20  32.300  4.508   192.500  12.750
#R> 52  summer  small medium 8.000  7.90  27.233  1.651    28.333   7.300
#R> 53  winter  small   high 7.900 11.00   6.167  1.172    18.333   7.750
#R> 54  spring  small   high 7.900  9.00   5.273  0.910    33.636   9.000
#R> 55  winter  small   high 6.600 10.80      NA  3.245    10.000   1.000
#R> 56  spring  small medium 5.600 11.80      NA  2.220     5.000   1.000
#R> 57  autumn  small medium 5.700 10.80      NA  2.550    10.000   1.000
#R> 58  spring  small   high 6.600  9.50      NA  1.320    20.000   1.000
#R> 59  summer  small   high 6.600 10.80      NA  2.640    10.000   2.000
#R> 60  autumn  small medium 6.600 11.30      NA  4.170    10.000   1.000
#R> 61  spring  small medium 6.500 10.40      NA  5.970    10.000   2.000
#R> 62  summer  small medium 6.400    NA      NA     NA        NA      NA
#R> 63  autumn  small   high 7.830 11.70   4.083  1.328    18.000   3.333
#R> 64  spring  small   high 7.570 10.80   4.575  1.203    27.500   2.000
#R> 65  summer  small   high 7.190 11.70   4.326  1.474   160.000   2.500
#R> 66  winter  small   high 7.440 10.10   2.933  0.770    15.000   1.333
#R> 67  spring  small   high 7.140  9.80   3.275  0.923    15.000   1.250
#R> 68  summer  small   high 7.000 12.10   3.136  1.208    16.200   1.800
#R> 69  winter  small medium 7.500  1.50  32.400  0.921  1386.250 220.750
#R> 70  spring  small medium 7.500  1.80  29.775  1.051  2082.850 209.857
#R> 71  summer  small medium 7.800  7.10  32.540  1.720  2167.370 151.125
#R> 72  autumn medium medium 8.500  8.10  38.125  3.850   225.000  45.000
#R> 73  summer medium medium 7.925 10.20  34.037  9.080   109.000  55.000
#R> 74  winter medium medium 8.100  8.10 136.000  3.773   245.000 136.750
#R> 75  spring medium medium 8.200  6.80 129.375  3.316   271.250 100.000
#R> 76  spring medium   high 9.100  9.40  35.750  5.164    32.500  85.500
#R> 77  autumn medium medium 8.100  9.80  29.500  1.287   224.286  25.167
#R> 78  winter medium medium 8.000  5.90  27.400  0.735   133.636  36.000
#R> 79  spring medium medium 8.000  3.30  26.760  0.658   165.000  37.375
#R> 80  winter medium   high 7.500  9.20  11.000  3.310   101.000  26.600
#R> 81  spring medium   high 7.400  9.80  11.000  3.235   255.000  38.750
#R> 82  autumn medium   high 7.300 11.70  10.400  4.930   130.000  10.800
#R> 83  winter medium   high 7.400  8.90  13.500  5.442   123.333  27.667
#R> 84  summer medium   high 7.400 11.17  12.146  6.188    89.600  32.000
#R> 85  autumn medium medium 7.500 10.80  31.000  4.408   737.500 111.250
#R> 86  winter medium medium 7.600  6.00  53.000  3.734   914.000 137.600
#R> 87  summer medium medium 7.400 10.77  36.248  3.730   429.200  57.600
#R> 88  winter medium medium 7.800  3.60  48.667  4.030  5738.330 412.333
#R> 89  summer medium medium 7.600  9.70  53.102  7.160  4073.330 282.167
#R> 90  winter medium medium 8.500  8.60 125.600  3.778   124.167 197.833
#R> 91  spring medium medium 8.700  9.40 173.750  3.318   101.250 267.750
#R> 92  summer medium medium 8.100 10.70  94.405  4.698   153.000 191.750
#R> 93  winter medium   high 8.800  8.50  53.333  5.132    96.667 120.500
#R> 94  spring medium   high 7.800 10.50  70.000  2.443    98.333 144.667
#R> 95  summer medium   high 7.900 11.80  63.510  4.940   137.000 159.500
#R> 96  autumn medium    low 8.500 10.50  56.717  0.330   215.714  23.000
#R> 97  winter medium    low 9.100  5.40  61.050  0.308   105.556 104.222
#R> 98  spring medium    low 8.900  4.50  57.750  0.267   155.000  97.333
#R> 99  winter medium   high 7.900  6.30 101.875  3.978   153.750  51.750
#R> 100 summer medium   high 7.800  8.20  85.982  6.200   421.667  31.333
#R> 101 winter medium medium 7.700  7.10  63.625  3.140   122.500  28.625
#R> 102 spring medium medium 7.800  6.50  82.111  2.603   215.556  12.889
#R> 103 winter medium    low 7.700  5.30  65.333  2.899   371.111  51.111
#R> 104 summer medium    low 7.500  8.80  58.331  8.688   758.750 104.500
#R> 105 autumn medium    low 7.600 10.00  49.625  5.456   308.750  38.625
#R> 106 winter medium    low 8.700  7.40  47.778  2.316    38.111  24.667
#R> 107 summer medium    low 7.700 11.10  47.229  8.759   239.000  54.000
#R> 108 autumn medium   high 8.300 11.10  41.500  4.665   931.833  39.000
#R> 109 winter medium   high 8.430  6.00  40.167  2.670   723.667  60.833
#R> 110 summer medium   high 8.160 11.10  32.056  5.694   461.875  71.000
#R> 111 winter medium   high 8.700  9.80   5.889  1.534    51.111   9.667
#R> 112 spring medium   high 8.200 11.30   7.250  1.875    25.000   6.500
#R> 113 summer medium   high 8.500 11.80   7.838  1.732   206.538   8.692
#R> 114 spring medium medium 7.800  6.00  53.425  0.381   118.571  37.857
#R> 115 summer medium medium 8.000  9.70  57.848  0.461   217.750  37.000
#R> 116 winter medium   high 9.700 10.80   0.222  0.406    10.000  22.444
#R> 117 summer medium   high 8.600 11.62   1.549  0.445    25.833  16.833
#R> 118 autumn medium medium 8.300 11.60   5.830  0.701    12.727   3.545
#R> 119 spring medium    low 8.400  5.30  74.667  3.900   131.667 261.600
#R> 120 summer medium    low 8.200  6.60 131.400  4.188    92.000 238.200
#R> 121 winter medium medium 8.200  9.40  45.273  7.195   345.455 144.000
#R> 122 spring medium medium 8.100  7.10  42.636  5.078    56.364 166.727
#R> 123 summer medium medium 8.100  9.00  48.429  6.640   128.571 181.000
#R> 124 winter medium   high 7.400 10.70  11.818  2.163   170.909  36.909
#R> 125 spring medium   high 8.300  9.70  10.556  1.921    65.556  61.556
#R> 126 summer medium   high 8.600 10.70  12.000  2.231    43.750  62.625
#R> 127 winter medium medium 9.100 11.60  31.091  5.099   246.364  55.000
#R> 128 spring medium medium 9.000  6.90  28.333  2.954    76.667 102.333
#R> 129 summer medium medium 8.300 10.00  30.125  3.726   102.500  75.875
#R> 130 winter medium   high 8.500 10.10  10.936  1.335   236.000  34.636
#R> 131 spring medium   high 8.300  7.70  10.078  1.212   103.333  48.667
#R> 132 summer medium   high 7.300 10.50  11.088  1.374    92.375  48.625
#R> 133 winter medium medium 7.900  9.80 194.750  6.513  3466.660  23.000
#R> 134 spring medium medium 7.900  8.30 391.500  6.045   380.000 173.000
#R> 135 autumn medium medium 8.000 11.90 130.670  6.540   196.000  75.000
#R> 136 spring medium medium 8.000  9.20  39.000  4.860   120.000 187.000
#R> 137 autumn medium medium 8.100 11.70  35.660  5.130    46.500  49.000
#R> 138 winter medium    low 8.430  9.90  37.600  0.826   124.000  32.500
#R> 139 summer medium    low 8.100  6.20  39.000  0.673   112.857  60.000
#R> 140 winter medium medium 7.900 11.20  49.900  9.773   505.000  67.500
#R> 141 summer medium medium 8.100  6.20  51.113  5.099   175.000 132.500
#R> 142 spring medium   high 7.800  9.50   8.300  1.670    34.000  16.800
#R> 143 autumn medium   high 7.900 10.50  10.207  2.304   132.250  10.583
#R> 144 winter medium    low 8.000  4.50  79.077  8.984   920.000  70.000
#R> 145 spring medium    low 7.600  6.30  81.333  9.715   196.667  77.333
#R> 146 autumn medium    low 7.800  6.50  64.093  7.740  1990.160  47.500
#R> 147 winter medium   high 8.220  8.10  41.250  1.415   172.500  46.667
#R> 148 autumn medium   high 8.300  9.90  40.226  1.587   235.000  33.800
#R> 149 winter medium   high 8.470  9.00  46.167  2.102    84.667  48.000
#R> 150 spring medium   high 8.400  4.90  47.000  0.536    91.833 109.000
#R> 151 autumn medium   high 8.870 11.00  41.163  2.273    54.750  39.000
#R> 152 summer medium   high 7.700  4.40  53.000  2.310    90.000  22.200
#R> 153 autumn medium   high 7.300 11.80  44.205 45.650 24064.000  44.000
#R> 154 spring medium medium 7.900  6.00 127.833  2.680   176.667  27.500
#R> 155 autumn medium medium 7.800 10.53 100.830  5.410   486.500  24.000
#R> 156 spring  large    low 7.800  3.20  94.000  4.908  1131.660 175.667
#R> 157 summer  large    low 7.600  4.90  69.000  3.685  1495.000 234.500
#R> 158 spring  large    low 8.600  3.60  50.000  0.376   134.000  54.100
#R> 159 autumn  large    low 8.400 10.60  19.220  1.655    96.833  20.667
#R> 160 winter  large    low 8.300 11.50  26.000  1.870    62.500  30.750
#R> 161 spring  large    low 9.000  5.80      NA  0.900   142.000 102.000
#R> 162 spring  large    low 9.500  5.70  44.000  0.102   146.667 151.333
#R> 163 summer  large    low 8.800  8.80  43.000  0.130   103.333 180.667
#R> 164 autumn  large    low 8.840 12.90  43.090  0.846    52.200   8.600
#R> 165 winter  large   high 7.300  9.90  16.000  4.820   101.667  14.667
#R> 166 autumn  large   high 7.400 10.68  22.350  5.414   244.600  66.400
#R> 167 spring  large    low 9.100  4.30  82.857  0.860   137.273 102.364
#R> 168 autumn  large    low 8.530 11.10  63.292  1.726   227.600  84.300
#R> 169 winter  large    low 8.560  8.70  43.970  4.053   643.000 221.900
#R> 170 autumn  large    low 8.060  8.30  38.902  3.678   627.273 205.636
#R> 171 winter  large medium 8.240  6.10  95.367  3.561  1168.000 236.400
#R> 172 summer  large medium 7.910  6.20 151.833  3.923  1081.660 346.167
#R> 173 winter  large medium 8.210  9.30 104.818  3.908   124.364  82.222
#R> 174 spring  large medium 8.500  7.30  71.444  2.512    66.667  64.389
#R> 175 spring  large medium 8.600 10.60 208.364  4.459   197.909  87.333
#R> 176 winter  large medium 9.060  6.35 187.183  3.351    54.778 159.167
#R> 177 autumn  large   high 8.700 10.70   4.545  0.941    32.727  16.000
#R> 178 spring  large   high 8.100 10.70   3.500  1.013    12.500  12.750
#R> 179 summer  large   high 8.400 10.29   5.326  0.996    53.846   7.667
#R> 180 spring  large medium 8.600 10.10   2.111  0.663    11.111   3.222
#R> 181 summer  large medium 8.200  9.50   2.200  0.672    10.000   3.800
#R> 182 winter  large medium 8.500 10.50   2.750  0.758    10.500   4.000
#R> 183 summer  large medium 8.300 10.00   3.860  0.866    32.000   6.000
#R> 184 winter  large   high 8.000 10.90   9.055  0.825    40.000  21.083
#R> 185 summer  large   high 8.100 10.20   7.613  0.699    32.500  26.625
#R> 186 winter  large    low 8.700 10.80  39.109  6.225   161.818 104.727
#R> 187 winter  large    low 8.700 11.70  22.455  3.765    88.182  41.300
#R> 188 summer  large    low 8.400  8.20  23.250  2.805    43.750  51.125
#R> 189 autumn  large    low 8.550 11.00  22.320  3.140    82.100  45.900
#R> 190 spring  large medium 8.500  7.60  12.778  1.873    17.778  50.889
#R> 191 autumn  large medium 8.700 11.40  15.541  2.323   103.000  34.500
#R> 192 winter  large medium 8.400 10.50  12.182  1.519    65.455  19.727
#R> 193 spring  large medium 8.200  8.20   7.333  1.003    37.778  19.111
#R> 194 autumn  large medium 8.580 11.10  23.825  3.617    72.600  51.111
#R> 195 summer  large medium 8.500  7.90  12.444  2.586    96.667  19.111
#R> 196 autumn  large medium 8.400  8.40  17.375  3.833    83.750  53.625
#R> 197 spring  large medium 8.300 10.60  14.320  3.200   125.333  35.333
#R> 198 autumn  large medium 8.200  7.00 139.989  2.978    60.110  78.333
#R> 199 winter  large medium 8.000  7.60      NA     NA        NA      NA
#R> 200 summer  large medium 8.500  6.70  82.852  2.800    27.069  64.000
#R>         PO4    Chla   a1   a2   a3   a4   a5   a6   a7
#R> 1   170.000  50.000  0.0  0.0  0.0  0.0 34.2  8.3  0.0
#R> 2   558.750   1.300  1.4  7.6  4.8  1.9  6.7  0.0  2.1
#R> 3   187.057  15.600  3.3 53.6  1.9  0.0  0.0  0.0  9.7
#R> 4   138.700   1.400  3.1 41.0 18.9  0.0  1.4  0.0  1.4
#R> 5    97.580  10.500  9.2  2.9  7.5  0.0  7.5  4.1  1.0
#R> 6    56.667  28.400 15.1 14.6  1.4  0.0 22.5 12.6  2.9
#R> 7   111.750   3.200  2.4  1.2  3.2  3.9  5.8  6.8  0.0
#R> 8    77.434   6.900 18.2  1.6  0.0  0.0  5.5  8.7  0.0
#R> 9    71.000   5.544 25.4  5.4  2.5  0.0  0.0  0.0  0.0
#R> 10   46.600   0.800 17.0  0.0  0.0  2.9  0.0  0.0  1.7
#R> 11   20.750   0.800 16.6  0.0  0.0  0.0  1.2  0.0  6.0
#R> 12   19.000   0.600 32.1  0.0  0.0  0.0  0.0  0.0  1.5
#R> 13   17.000  41.000 43.5  0.0  2.1  0.0  1.2  0.0  2.1
#R> 14   15.000   0.500 31.1  1.0  3.4  0.0  1.9  0.0  4.1
#R> 15   61.600   0.300 52.2  5.0  7.8  0.0  4.0  0.0  0.0
#R> 16   98.250   1.100 69.9  0.0  1.7  0.0  0.0  0.0  0.0
#R> 17   50.000   1.100 46.2  0.0  0.0  1.2  0.0  0.0  0.0
#R> 18   57.833   0.400 31.8  0.0  3.1  4.8  7.7  1.4  7.2
#R> 19   61.500   0.800 50.6  0.0  9.9  4.3  3.6  8.2  2.2
#R> 20  771.600   4.500  0.0  0.0  0.0 44.6  0.0  0.0  1.4
#R> 21  586.000  16.000  0.0  0.0  0.0  6.8  6.1  0.0  0.0
#R> 22   18.000   0.500 15.5  0.0  0.0  2.3  0.0  0.0  0.0
#R> 23   40.000   7.600 23.2  0.0  0.0  0.0 27.6 11.1  0.0
#R> 24   27.500   1.700 74.2  0.0  0.0  3.7  0.0  0.0  0.0
#R> 25   11.500   1.500 13.0  8.6  1.2  3.5  1.2  1.6  1.9
#R> 26   44.136   3.000  4.1  0.0  0.0  0.0  9.2 10.1  0.0
#R> 27   13.600   0.500 29.7  0.0  0.0  4.9  0.0  0.0  0.0
#R> 28       NA   2.700 30.3  1.9  0.0  0.0  2.1  1.4  2.1
#R> 29   45.000   0.800 17.1  0.0 19.6  0.0  0.0  0.0  2.5
#R> 30   19.000   0.500 33.9  1.0 14.6  0.0  0.0  0.0  0.0
#R> 31  142.000   4.900  3.4 16.0  1.2  0.0 15.3 15.8  0.0
#R> 32  304.000   2.800  6.9 17.1 20.2  0.0  4.0  0.0  2.9
#R> 33  130.750   5.800  0.0  8.0  1.9  0.0 11.2 42.7  1.2
#R> 34   47.000   2.300 13.6  9.1  0.0  0.0  1.4  0.0  0.0
#R> 35   23.000   0.900  5.3 40.7  3.3  0.0  0.0  0.0  1.9
#R> 36   84.460   3.600 18.3 12.4  1.0  0.0  0.0  0.0  1.0
#R> 37    3.000   0.200 66.0  0.0  0.0  0.0  0.0  0.0  0.0
#R> 38    3.000   0.300 75.8  0.0  0.0  0.0  0.0  0.0  0.0
#R> 39  253.250  12.320  2.0 38.5  4.1  2.2  0.0  0.0 10.2
#R> 40  255.280   8.957  2.2  2.7  1.0  3.7  2.7  0.0  0.0
#R> 41  296.000   3.700  0.0  5.9 10.6  1.7  0.0  0.0  7.1
#R> 42  175.046  13.200  0.0  0.0  0.0  5.7 11.3 17.0  1.6
#R> 43  344.600  22.500  0.0 40.9  7.5  0.0  2.4  1.5  0.0
#R> 44  326.857  11.840  4.1  3.1  0.0  0.0 19.7 17.0  0.0
#R> 45   40.667   3.900 51.8  4.1  0.0  0.0  3.1  5.5  0.0
#R> 46   43.500   3.300 29.5  1.0  2.7  3.2  2.9  9.6  0.0
#R> 47   39.000   0.800 54.4  3.4  1.2  0.0 18.7  2.0  0.0
#R> 48    6.000   1.100 35.5  0.0  0.0  0.0  0.0  0.0  0.0
#R> 49  121.000   2.800 89.8  0.0  0.0  0.0  0.0  0.0  0.0
#R> 50   20.812  12.100 24.8  7.4  0.0  2.5 10.6 17.1  3.2
#R> 51   49.333   7.900  0.0  0.0  0.0  4.6  1.2  0.0  3.9
#R> 52   22.900   4.500 39.1  0.0  1.2  2.2  5.4  1.5  3.2
#R> 53   11.800   0.500 81.9  0.0  0.0  0.0  0.0  0.0  0.0
#R> 54   11.818   0.800 54.0  0.0  0.0  2.4  0.0  0.0  0.0
#R> 55    6.500      NA 24.3  0.0  0.0  0.0  0.0  0.0  0.0
#R> 56    1.000      NA 82.7  0.0  0.0  0.0  0.0  0.0  0.0
#R> 57    4.000      NA 16.8  4.6  3.9 11.5  0.0  0.0  0.0
#R> 58    6.000      NA 46.8  0.0  0.0 28.8  0.0  0.0  0.0
#R> 59   11.000      NA 46.9  0.0  0.0 13.4  0.0  0.0  0.0
#R> 60    6.000      NA 47.1  0.0  0.0  0.0  0.0  1.2  0.0
#R> 61   14.000      NA 66.9  0.0  0.0  0.0  0.0  0.0  0.0
#R> 62   14.000      NA 19.4  0.0  0.0  2.0  0.0  3.9  1.7
#R> 63    6.667      NA 14.4  0.0  0.0  0.0  0.0  0.0  0.0
#R> 64    6.750   1.000 20.3  4.3  5.5  0.0  0.0  0.0  1.4
#R> 65    7.200   0.300 15.8  1.7  7.8  0.0  0.0  2.4  1.4
#R> 66    6.000   0.600 55.5  0.0  1.7  1.4  0.0  0.0  0.0
#R> 67   10.750   2.500 10.3  0.0 42.8  2.2  0.0  0.0  0.0
#R> 68    2.500   0.500 64.2  0.0  3.0  0.0  0.0  0.0  0.0
#R> 69  351.600  10.000  0.0  0.0  1.5  7.6  0.0  0.0  6.1
#R> 70  313.600   1.000  1.9  4.9  2.6  3.0  0.0  0.0  1.9
#R> 71  279.066  13.100 25.5  3.9  1.0 11.0  0.0  0.0 12.5
#R> 72  152.333   5.200 11.3  1.7  2.0  2.2 13.3 10.6  0.0
#R> 73   58.623  11.600  4.4  4.0  3.3  0.0 11.7 21.4  1.2
#R> 74  249.250  20.870  1.9  5.8 24.8  4.6  9.5  5.1  1.2
#R> 75  233.500  13.000  1.6  8.0 17.6  3.7 11.5  7.0  0.0
#R> 76  215.500  18.370  2.2  9.6  5.0  1.0  8.6  7.9  2.2
#R> 77  102.333   3.600 64.9  1.0  0.0  1.0  2.9  1.4  1.0
#R> 78  105.727   3.000 15.1  7.3 23.2  3.4  4.1  0.0  0.0
#R> 79  111.375   3.000 14.4  0.0 11.8 11.3  5.5  0.0  0.0
#R> 80  108.000   1.300  6.7  0.0  5.4  3.4  4.9  6.9 10.8
#R> 81   56.667   2.000 10.8  0.0  0.0  4.6  6.5  2.2  1.4
#R> 82   60.000   4.300  1.2  0.0  1.7  0.0  7.5 17.7 14.4
#R> 83  104.000  21.000 12.6  4.3 21.9  1.0  2.4  3.3 22.1
#R> 84   69.930   3.100 14.7  4.1  1.0  0.0  7.7  8.5 31.2
#R> 85  214.000   2.900  3.3  0.0  0.0  5.0  1.9  6.2 25.6
#R> 86  254.600   4.300  0.0  0.0  0.0  4.6  9.0 13.1 30.1
#R> 87  169.001   3.200  2.8  0.0  0.0  2.6  5.2 13.2 16.7
#R> 88  607.167   4.300  0.0  0.0  2.6  2.4  5.0  0.0  2.4
#R> 89  624.733   6.800  0.0  0.0  0.0  1.0 35.6  9.9  0.0
#R> 90  303.333  40.000  0.0 15.2  8.8  0.0  8.6  5.1  2.7
#R> 91  391.750   3.500  0.0  5.5  3.3  0.0 20.8 12.4  0.0
#R> 92  265.250   7.300  0.0  2.1  1.6  0.0 20.8 32.9  0.0
#R> 93  232.833  31.000  1.2  5.6  6.3  1.7  1.2  0.0  1.0
#R> 94  244.000   9.000  0.0  3.1  3.5  1.6  8.2  9.9  0.0
#R> 95  218.000   6.500  0.0  5.2  0.0  0.0 28.8 20.4  1.0
#R> 96  138.500  20.829  5.7  0.0  0.0  4.4 12.4  8.3  7.8
#R> 97  239.000  72.478  3.6 31.9  2.4  0.0  0.0  0.0  2.2
#R> 98  235.667  98.817  1.2 16.2  0.0  0.0  0.0  0.0  1.0
#R> 99  205.875   2.000  4.0  2.1 35.1  6.8  7.3  0.0  0.0
#R> 100 211.667  21.900  5.9  3.4  1.0  1.2 17.8 49.4  1.0
#R> 101 186.500  30.000 16.5  2.1 19.5  3.5  5.3  1.2  3.2
#R> 102 154.125   5.200  7.0  0.0 13.5  4.3  8.7  0.0  4.3
#R> 103 183.667  17.200 58.7  0.0 11.5  6.6  0.0  0.0  0.0
#R> 104 292.625   3.000  8.7  0.0  3.0  5.3  9.4 33.2  0.0
#R> 105 285.714  75.000 17.0 21.6  1.6  1.4 10.2  3.6  1.1
#R> 106 201.778   3.000 12.3  5.4  1.9  0.0  1.4  0.0  1.9
#R> 107 275.143  65.700  8.8 19.6  4.7  0.0  0.0  0.0  2.7
#R> 108 124.200  13.100 23.7 13.7  0.0  1.7  6.4  2.6  0.0
#R> 109 141.833  25.000  0.0  6.4  7.3 12.7  0.0  0.0  4.2
#R> 110 132.546  15.000  3.6 38.8  0.0  0.0  1.2  0.0  2.4
#R> 111  17.333   1.000 64.3  1.5  8.0  0.0  0.0  0.0  0.0
#R> 112  26.000   0.300 46.6  0.0  2.5  0.0  0.0  0.0  0.0
#R> 113  16.662   2.100 24.0  0.0  1.0  0.0  0.0  0.0  0.0
#R> 114 102.571   1.200  3.7  1.4  1.1  2.1  3.2  6.4  0.0
#R> 115  86.997   3.000 18.1 14.5  0.0  0.0 11.5 22.3  0.0
#R> 116  10.111      NA 41.0  1.5  0.0  0.0  0.0  0.0  0.0
#R> 117  18.293   1.400 43.7  0.0  1.2  0.0  0.0  4.7  0.0
#R> 118  13.200   3.200 86.6  0.0  0.0  0.0  0.0  0.0  0.0
#R> 119 432.909  24.917  1.9 12.7 25.9  0.0  0.0  0.0  6.8
#R> 120 320.400   6.800  1.2  1.9 22.9  0.0  8.1  0.0  0.0
#R> 121 287.000   9.882  1.4 18.4  0.0  0.0 20.0 29.5  0.0
#R> 122 262.727  17.200  1.6  8.9  6.6  0.0  9.2  1.6  1.4
#R> 123 222.286   6.429  3.3 11.6  7.0  0.0 17.9  4.7  0.0
#R> 124 122.000   5.555 14.6  0.0  0.0  1.9 22.1 12.7  1.4
#R> 125 127.222   5.233  1.7  0.0 10.3  2.6  8.9  6.7  0.0
#R> 126  89.625   2.150  3.3  0.0  0.0  1.9 34.3  7.1  6.0
#R> 127 284.000  88.255  0.0 36.6  4.1  0.0  1.2 16.7  6.1
#R> 128 277.333 110.456  0.0 16.4 10.1  0.0  0.0  0.0  6.6
#R> 129 177.625  50.225  1.5 32.8  1.0  4.1  0.0 15.8  2.4
#R> 130  72.900  11.100  4.2  0.0  1.4  1.9 16.2  0.0  1.4
#R> 131  82.444   2.000  4.1  0.0 25.3  2.1  8.0  0.0 18.6
#R> 132  66.750   3.300  1.2  0.0  2.3  0.0 44.4  7.5  1.9
#R> 133 173.750  15.300  0.0  0.0  1.0  0.0  9.0 64.6  0.0
#R> 134 317.000   5.500  2.4  1.7  4.2  8.3  1.7  0.0  2.4
#R> 135  84.000   4.500  7.8  8.7  2.1  0.0 14.9 22.9  2.4
#R> 136 213.000   2.000 10.3 26.5  6.1  0.0  5.6  1.5  2.2
#R> 137  88.500   2.500  1.5 72.6  0.0  0.0  3.4  6.8  3.4
#R> 138 115.000  11.700  9.2  2.9  2.0  1.3  2.5  0.0  0.0
#R> 139  98.143   2.000 28.1  0.0  0.0  4.0  1.2  0.0  0.0
#R> 140 143.750   5.450  2.1  2.6  0.0  0.0 15.0 15.7  0.0
#R> 141 197.143   6.400  1.4 15.7  1.4  0.0  3.5  0.0  1.6
#R> 142  35.200   1.000 19.0  0.0 22.0  5.0  1.1  5.4  0.0
#R> 143  23.485   2.000 42.5  0.0  2.2  1.0  0.0  0.0  0.0
#R> 144 200.231  19.400  2.5  1.4  1.4  6.2  4.1  1.8  3.9
#R> 145 147.833   3.000  4.4 11.2  6.8  0.0  1.0  0.0 31.6
#R> 146 276.000   8.100  6.5  4.1  0.0  7.7  9.9 18.2  7.0
#R> 147 123.333  30.400 39.7 12.7  0.0  1.1  2.7  0.0  1.6
#R> 148  75.207  23.800 32.8 28.0  2.0  3.5  1.0  0.0  1.5
#R> 149 116.200   7.300 12.2 16.0  1.0  1.4  1.9  1.2  0.0
#R> 150 188.667  32.000  1.9 25.4 21.7  0.0  0.0  1.0  0.0
#R> 151  72.696  22.700  0.0  5.6  1.2  0.0  8.0  2.7  0.0
#R> 152 116.200  16.000  0.0  0.0  0.0  1.2  5.7 32.1  0.0
#R> 153  34.000  53.100  2.2  0.0  0.0  1.2  5.9 77.6  0.0
#R> 154  76.333   2.100  3.4 21.5 14.0  1.8  3.9  0.0  0.0
#R> 155  58.374  27.500  2.8  1.9  0.0  1.2 19.0  4.5  0.0
#R> 156 361.000  28.567 24.8 10.4  0.0  6.9  0.0  0.0  2.7
#R> 157 236.000  22.500 32.5 12.0  0.0  5.0  0.0  0.0  1.9
#R> 158 125.800  26.800  0.0 28.0  0.0  0.0  0.0  0.0 15.1
#R> 159  54.916  20.600  0.0 11.3  1.8  0.0  2.5  0.0  1.4
#R> 160  75.333  34.750  0.0 20.1  0.0  0.0  0.0  0.0  0.0
#R> 161 186.000  68.050  1.7 20.6  1.5  2.2  0.0  0.0  0.0
#R> 162 252.500  93.683 12.3 21.7  3.9  0.0  0.0  0.0  3.9
#R> 163 269.667  92.667  7.2 28.2  0.0  0.0  0.0  0.0  3.3
#R> 164  46.438  81.540  3.4 21.5  0.0  0.0  0.0  0.0  2.7
#R> 165  85.000   2.000  0.0  0.0  0.0  2.4  0.0 17.8  3.6
#R> 166 171.272   3.800  1.1  0.0  1.4  0.0  6.6 42.1  5.2
#R> 167 232.900  54.367  0.0  6.0  2.9  0.0  0.0  0.0  2.9
#R> 168 146.452  21.220  1.4 14.7  2.5  0.0  0.0  0.0  2.0
#R> 169 246.667  14.700 12.5  2.1  0.0  1.2  6.4  4.5  1.7
#R> 170 219.909   6.209  0.0  0.0  0.0  0.0  8.6 52.5  0.0
#R> 171 272.222  20.578  2.5 13.2  0.0  2.0  7.4 17.2  0.0
#R> 172 388.167   5.083  1.7 12.0  4.9  2.7  0.0  5.9  1.7
#R> 173 167.900   5.609  1.4  4.6 10.8  2.2  5.5 42.4  0.0
#R> 174 137.778   9.384  0.0  3.8 16.0  4.0  0.0  0.0  3.3
#R> 175 194.100  27.618  0.0  1.2  0.0  0.0 11.3 11.5  0.0
#R> 176 221.278  20.800  0.0 21.1  3.7  0.0  0.0  0.0  1.9
#R> 177  21.300   1.100 39.7  0.0 12.9  0.0  0.0  0.0  0.0
#R> 178  11.000   0.600 37.3  9.7 13.6  0.0  2.2  0.0  1.2
#R> 179  14.354   0.800 52.4  7.5  9.4  0.0  1.4  1.9  0.0
#R> 180   7.000   1.300 48.3  2.0  0.0  0.0  0.0  0.0  0.0
#R> 181   6.200   0.800 50.4  3.8  0.0  0.0  0.0  0.0  0.0
#R> 182   7.654   4.000 56.8  5.0  0.0  0.0  0.0  0.0  0.0
#R> 183  16.000   2.860 17.3  6.7 19.7  0.0  0.0  0.0  0.0
#R> 184  56.091      NA 16.8 19.6  4.0  0.0  0.0  0.0  0.0
#R> 185  52.875   2.000 18.1  1.7  2.0  0.0  1.7  5.9  0.0
#R> 186 228.364  46.075  1.1  3.9  2.1  0.0  3.9  4.6  2.3
#R> 187  85.400  17.491  0.0  4.7  0.0  0.0  2.6  2.6  0.0
#R> 188  87.125  14.775  0.0 12.0  1.7  0.0  2.7  0.0  0.0
#R> 189 101.455  18.330  1.7  7.0  1.2  0.0  4.8  3.1  0.0
#R> 190 127.000  24.556  0.0  0.0 10.2  1.7  1.2  0.0  5.5
#R> 191  81.558   5.620  7.6  0.0  1.2  0.0 15.9 31.8  5.9
#R> 192  50.455   8.155  2.9  4.6  1.0  0.0  6.6 16.6  0.0
#R> 193 120.889   5.111  2.2 12.7  8.8  0.0  0.0  0.0  1.2
#R> 194  91.111  22.900  3.8 22.0  2.9  0.0  3.1  5.5  0.0
#R> 195  61.444   6.167 18.9 13.2  5.0  0.0  6.1  0.0  0.0
#R> 196  79.750   2.338 12.7 21.7  5.6  0.0  1.0  0.0  0.0
#R> 197  75.904   4.667 18.0  7.0  1.7  0.0  4.8 10.3  1.0
#R> 198 140.220  31.738  0.0 15.9  2.4  1.0  0.0  0.0  0.0
#R> 199      NA      NA  0.0 12.5  3.7  1.0  0.0  0.0  4.9
#R> 200 140.517  18.300  2.4 10.5  9.0  7.8  0.0  0.0  5.8
```

This was the final step of our first attempt to find the solution to the problem, yet we didn't know how to proceed from here.

### Second attempt

Our second attempt was to make use of ploynomials with regards to linear regressions. We started by defining the dataset and then tried to find the right degree n. This also didn't work, which is why we made use of other models, in order to find the solution to the problem.

## Model used for the solution of the final task (#THE SOLUTION)

As mentioned before, in order to find the solution to the final task of our project, we decided to make use of a multiple linear regression model to cross validation.

### Solution: Multiple linear regression model to cross validation

Step 1: The first step of using the model is to load the two datasets given, as well as the liabraries needed (train.data & test.data).


```r
library(tidyverse)
library(caret)
library(dplyr)
train.data
#R>     season   size  speed  mxPH  mnO2      Cl    NO3       NH4    oPO4
#R> 1   winter  small medium 8.000  9.80  60.800  6.238   578.000 105.000
#R> 2   spring  small medium 8.350  8.00  57.750  1.288   370.000 428.750
#R> 3   autumn  small medium 8.100 11.40  40.020  5.330   346.667 125.667
#R> 4   spring  small medium 8.070  4.80  77.364  2.302    98.182  61.182
#R> 5   autumn  small medium 8.060  9.00  55.350 10.416   233.700  58.222
#R> 6   winter  small   high 8.250 13.10  65.750  9.248   430.000  18.250
#R> 7   summer  small   high 8.150 10.30  73.250  1.535   110.000  61.250
#R> 8   autumn  small   high 8.050 10.60  59.067  4.990   205.667  44.667
#R> 9   winter  small medium 8.700  3.40  21.950  0.886   102.750  36.300
#R> 10  winter  small   high 7.930  9.90   8.000  1.390     5.800  27.250
#R> 11  spring  small   high 7.700 10.20   8.000  1.527    21.571  12.750
#R> 12  summer  small   high 7.450 11.70   8.690  1.588    18.429  10.667
#R> 13  winter  small   high 7.740  9.60   5.000  1.223    27.286  12.000
#R> 14  summer  small   high 7.720 11.80   6.300  1.470     8.000  16.000
#R> 15  winter  small   high 7.900  9.60   3.000  1.448    46.200  13.000
#R> 16  autumn  small   high 7.550 11.50   4.700  1.320    14.750   4.250
#R> 17  winter  small   high 7.780 12.00   7.000  1.420    34.333  18.667
#R> 18  spring  small   high 7.610  9.80   7.000  1.443    31.333  20.000
#R> 19  summer  small   high 7.350 10.40   7.000  1.718    49.000  41.500
#R> 20  spring  small medium 7.790  3.20  64.000  2.822  8777.600 564.600
#R> 21  winter  small medium 7.830 10.70  88.000  4.825  1729.000 467.500
#R> 22  spring  small   high 7.200  9.20   0.800  0.642    81.000  15.600
#R> 23  autumn  small   high 7.750 10.30  32.920  2.942    42.000  16.000
#R> 24  winter  small   high 7.620  8.50  11.867  1.715   208.333   3.000
#R> 25  spring  small   high 7.840  9.40  10.975  1.510    12.500   3.000
#R> 26  summer  small   high 7.770 10.70  12.536  3.976    58.500   9.000
#R> 27  winter  small   high 7.090  8.40  10.500  1.572    28.000   4.000
#R> 28  autumn  small   high 6.800 11.10   9.000  0.630    20.000   4.000
#R> 29  winter  small   high 8.000  9.80  16.000  0.730    20.000  26.000
#R> 30  spring  small   high 7.200 11.30   9.000  0.230   120.000  12.000
#R> 31  autumn  small   high 7.400 12.50  13.000  3.330    60.000  72.000
#R> 32  winter  small   high 8.100 10.30  26.000  3.780    60.000 246.000
#R> 33  summer  small   high 7.800 11.30  20.083  3.020    49.500  53.000
#R> 34  autumn  small medium 8.400  9.90  34.500  2.818  3515.000  20.000
#R> 35  winter  small medium 8.270  7.80  29.200  0.050  6400.000   7.400
#R> 36  summer  small medium 8.660  8.40  30.523  3.444  1911.000  58.875
#R> 37  winter  small   high 8.300 10.90   1.170  0.735    13.500   1.625
#R> 38  spring  small   high 8.000    NA   1.450  0.810    10.000   2.500
#R> 39  winter  small medium 8.300  8.90  20.625  3.414   228.750 196.620
#R> 40  spring  small medium 8.100 10.50  22.286  4.071   178.570 182.420
#R> 41  winter  small medium 8.000  5.50  77.000  6.096   122.850 143.710
#R> 42  summer  small medium 8.150  7.10  54.190  3.829   647.570  59.429
#R> 43  winter  small   high 8.300  7.70  50.000  8.543    76.000 264.900
#R> 44  spring  small   high 8.300  8.80  54.143  7.830    51.429 276.850
#R> 45  winter  small   high 8.400 13.40  69.750  4.555    37.500  10.000
#R> 46  spring  small   high 8.300 12.50  87.000  4.870    22.500  27.000
#R> 47  autumn  small   high 8.000 12.10  66.300  4.535    39.000  16.000
#R> 48  winter  small    low    NA 12.60   9.000  0.230    10.000   5.000
#R> 49  spring  small medium 7.600  9.60  15.000  3.020    40.000  27.000
#R> 50  autumn  small medium 7.290 11.21  17.750  3.070    35.000  13.000
#R> 51  winter  small medium 7.600 10.20  32.300  4.508   192.500  12.750
#R> 52  summer  small medium 8.000  7.90  27.233  1.651    28.333   7.300
#R> 53  winter  small   high 7.900 11.00   6.167  1.172    18.333   7.750
#R> 54  spring  small   high 7.900  9.00   5.273  0.910    33.636   9.000
#R> 55  winter  small   high 6.600 10.80      NA  3.245    10.000   1.000
#R> 56  spring  small medium 5.600 11.80      NA  2.220     5.000   1.000
#R> 57  autumn  small medium 5.700 10.80      NA  2.550    10.000   1.000
#R> 58  spring  small   high 6.600  9.50      NA  1.320    20.000   1.000
#R> 59  summer  small   high 6.600 10.80      NA  2.640    10.000   2.000
#R> 60  autumn  small medium 6.600 11.30      NA  4.170    10.000   1.000
#R> 61  spring  small medium 6.500 10.40      NA  5.970    10.000   2.000
#R> 62  summer  small medium 6.400    NA      NA     NA        NA      NA
#R> 63  autumn  small   high 7.830 11.70   4.083  1.328    18.000   3.333
#R> 64  spring  small   high 7.570 10.80   4.575  1.203    27.500   2.000
#R> 65  summer  small   high 7.190 11.70   4.326  1.474   160.000   2.500
#R> 66  winter  small   high 7.440 10.10   2.933  0.770    15.000   1.333
#R> 67  spring  small   high 7.140  9.80   3.275  0.923    15.000   1.250
#R> 68  summer  small   high 7.000 12.10   3.136  1.208    16.200   1.800
#R> 69  winter  small medium 7.500  1.50  32.400  0.921  1386.250 220.750
#R> 70  spring  small medium 7.500  1.80  29.775  1.051  2082.850 209.857
#R> 71  summer  small medium 7.800  7.10  32.540  1.720  2167.370 151.125
#R> 72  autumn medium medium 8.500  8.10  38.125  3.850   225.000  45.000
#R> 73  summer medium medium 7.925 10.20  34.037  9.080   109.000  55.000
#R> 74  winter medium medium 8.100  8.10 136.000  3.773   245.000 136.750
#R> 75  spring medium medium 8.200  6.80 129.375  3.316   271.250 100.000
#R> 76  spring medium   high 9.100  9.40  35.750  5.164    32.500  85.500
#R> 77  autumn medium medium 8.100  9.80  29.500  1.287   224.286  25.167
#R> 78  winter medium medium 8.000  5.90  27.400  0.735   133.636  36.000
#R> 79  spring medium medium 8.000  3.30  26.760  0.658   165.000  37.375
#R> 80  winter medium   high 7.500  9.20  11.000  3.310   101.000  26.600
#R> 81  spring medium   high 7.400  9.80  11.000  3.235   255.000  38.750
#R> 82  autumn medium   high 7.300 11.70  10.400  4.930   130.000  10.800
#R> 83  winter medium   high 7.400  8.90  13.500  5.442   123.333  27.667
#R> 84  summer medium   high 7.400 11.17  12.146  6.188    89.600  32.000
#R> 85  autumn medium medium 7.500 10.80  31.000  4.408   737.500 111.250
#R> 86  winter medium medium 7.600  6.00  53.000  3.734   914.000 137.600
#R> 87  summer medium medium 7.400 10.77  36.248  3.730   429.200  57.600
#R> 88  winter medium medium 7.800  3.60  48.667  4.030  5738.330 412.333
#R> 89  summer medium medium 7.600  9.70  53.102  7.160  4073.330 282.167
#R> 90  winter medium medium 8.500  8.60 125.600  3.778   124.167 197.833
#R> 91  spring medium medium 8.700  9.40 173.750  3.318   101.250 267.750
#R> 92  summer medium medium 8.100 10.70  94.405  4.698   153.000 191.750
#R> 93  winter medium   high 8.800  8.50  53.333  5.132    96.667 120.500
#R> 94  spring medium   high 7.800 10.50  70.000  2.443    98.333 144.667
#R> 95  summer medium   high 7.900 11.80  63.510  4.940   137.000 159.500
#R> 96  autumn medium    low 8.500 10.50  56.717  0.330   215.714  23.000
#R> 97  winter medium    low 9.100  5.40  61.050  0.308   105.556 104.222
#R> 98  spring medium    low 8.900  4.50  57.750  0.267   155.000  97.333
#R> 99  winter medium   high 7.900  6.30 101.875  3.978   153.750  51.750
#R> 100 summer medium   high 7.800  8.20  85.982  6.200   421.667  31.333
#R> 101 winter medium medium 7.700  7.10  63.625  3.140   122.500  28.625
#R> 102 spring medium medium 7.800  6.50  82.111  2.603   215.556  12.889
#R> 103 winter medium    low 7.700  5.30  65.333  2.899   371.111  51.111
#R> 104 summer medium    low 7.500  8.80  58.331  8.688   758.750 104.500
#R> 105 autumn medium    low 7.600 10.00  49.625  5.456   308.750  38.625
#R> 106 winter medium    low 8.700  7.40  47.778  2.316    38.111  24.667
#R> 107 summer medium    low 7.700 11.10  47.229  8.759   239.000  54.000
#R> 108 autumn medium   high 8.300 11.10  41.500  4.665   931.833  39.000
#R> 109 winter medium   high 8.430  6.00  40.167  2.670   723.667  60.833
#R> 110 summer medium   high 8.160 11.10  32.056  5.694   461.875  71.000
#R> 111 winter medium   high 8.700  9.80   5.889  1.534    51.111   9.667
#R> 112 spring medium   high 8.200 11.30   7.250  1.875    25.000   6.500
#R> 113 summer medium   high 8.500 11.80   7.838  1.732   206.538   8.692
#R> 114 spring medium medium 7.800  6.00  53.425  0.381   118.571  37.857
#R> 115 summer medium medium 8.000  9.70  57.848  0.461   217.750  37.000
#R> 116 winter medium   high 9.700 10.80   0.222  0.406    10.000  22.444
#R> 117 summer medium   high 8.600 11.62   1.549  0.445    25.833  16.833
#R> 118 autumn medium medium 8.300 11.60   5.830  0.701    12.727   3.545
#R> 119 spring medium    low 8.400  5.30  74.667  3.900   131.667 261.600
#R> 120 summer medium    low 8.200  6.60 131.400  4.188    92.000 238.200
#R> 121 winter medium medium 8.200  9.40  45.273  7.195   345.455 144.000
#R> 122 spring medium medium 8.100  7.10  42.636  5.078    56.364 166.727
#R> 123 summer medium medium 8.100  9.00  48.429  6.640   128.571 181.000
#R> 124 winter medium   high 7.400 10.70  11.818  2.163   170.909  36.909
#R> 125 spring medium   high 8.300  9.70  10.556  1.921    65.556  61.556
#R> 126 summer medium   high 8.600 10.70  12.000  2.231    43.750  62.625
#R> 127 winter medium medium 9.100 11.60  31.091  5.099   246.364  55.000
#R> 128 spring medium medium 9.000  6.90  28.333  2.954    76.667 102.333
#R> 129 summer medium medium 8.300 10.00  30.125  3.726   102.500  75.875
#R> 130 winter medium   high 8.500 10.10  10.936  1.335   236.000  34.636
#R> 131 spring medium   high 8.300  7.70  10.078  1.212   103.333  48.667
#R> 132 summer medium   high 7.300 10.50  11.088  1.374    92.375  48.625
#R> 133 winter medium medium 7.900  9.80 194.750  6.513  3466.660  23.000
#R> 134 spring medium medium 7.900  8.30 391.500  6.045   380.000 173.000
#R> 135 autumn medium medium 8.000 11.90 130.670  6.540   196.000  75.000
#R> 136 spring medium medium 8.000  9.20  39.000  4.860   120.000 187.000
#R> 137 autumn medium medium 8.100 11.70  35.660  5.130    46.500  49.000
#R> 138 winter medium    low 8.430  9.90  37.600  0.826   124.000  32.500
#R> 139 summer medium    low 8.100  6.20  39.000  0.673   112.857  60.000
#R> 140 winter medium medium 7.900 11.20  49.900  9.773   505.000  67.500
#R> 141 summer medium medium 8.100  6.20  51.113  5.099   175.000 132.500
#R> 142 spring medium   high 7.800  9.50   8.300  1.670    34.000  16.800
#R> 143 autumn medium   high 7.900 10.50  10.207  2.304   132.250  10.583
#R> 144 winter medium    low 8.000  4.50  79.077  8.984   920.000  70.000
#R> 145 spring medium    low 7.600  6.30  81.333  9.715   196.667  77.333
#R> 146 autumn medium    low 7.800  6.50  64.093  7.740  1990.160  47.500
#R> 147 winter medium   high 8.220  8.10  41.250  1.415   172.500  46.667
#R> 148 autumn medium   high 8.300  9.90  40.226  1.587   235.000  33.800
#R> 149 winter medium   high 8.470  9.00  46.167  2.102    84.667  48.000
#R> 150 spring medium   high 8.400  4.90  47.000  0.536    91.833 109.000
#R> 151 autumn medium   high 8.870 11.00  41.163  2.273    54.750  39.000
#R> 152 summer medium   high 7.700  4.40  53.000  2.310    90.000  22.200
#R> 153 autumn medium   high 7.300 11.80  44.205 45.650 24064.000  44.000
#R> 154 spring medium medium 7.900  6.00 127.833  2.680   176.667  27.500
#R> 155 autumn medium medium 7.800 10.53 100.830  5.410   486.500  24.000
#R> 156 spring  large    low 7.800  3.20  94.000  4.908  1131.660 175.667
#R> 157 summer  large    low 7.600  4.90  69.000  3.685  1495.000 234.500
#R> 158 spring  large    low 8.600  3.60  50.000  0.376   134.000  54.100
#R> 159 autumn  large    low 8.400 10.60  19.220  1.655    96.833  20.667
#R> 160 winter  large    low 8.300 11.50  26.000  1.870    62.500  30.750
#R> 161 spring  large    low 9.000  5.80      NA  0.900   142.000 102.000
#R> 162 spring  large    low 9.500  5.70  44.000  0.102   146.667 151.333
#R> 163 summer  large    low 8.800  8.80  43.000  0.130   103.333 180.667
#R> 164 autumn  large    low 8.840 12.90  43.090  0.846    52.200   8.600
#R> 165 winter  large   high 7.300  9.90  16.000  4.820   101.667  14.667
#R> 166 autumn  large   high 7.400 10.68  22.350  5.414   244.600  66.400
#R> 167 spring  large    low 9.100  4.30  82.857  0.860   137.273 102.364
#R> 168 autumn  large    low 8.530 11.10  63.292  1.726   227.600  84.300
#R> 169 winter  large    low 8.560  8.70  43.970  4.053   643.000 221.900
#R> 170 autumn  large    low 8.060  8.30  38.902  3.678   627.273 205.636
#R> 171 winter  large medium 8.240  6.10  95.367  3.561  1168.000 236.400
#R> 172 summer  large medium 7.910  6.20 151.833  3.923  1081.660 346.167
#R> 173 winter  large medium 8.210  9.30 104.818  3.908   124.364  82.222
#R> 174 spring  large medium 8.500  7.30  71.444  2.512    66.667  64.389
#R> 175 spring  large medium 8.600 10.60 208.364  4.459   197.909  87.333
#R> 176 winter  large medium 9.060  6.35 187.183  3.351    54.778 159.167
#R> 177 autumn  large   high 8.700 10.70   4.545  0.941    32.727  16.000
#R> 178 spring  large   high 8.100 10.70   3.500  1.013    12.500  12.750
#R> 179 summer  large   high 8.400 10.29   5.326  0.996    53.846   7.667
#R> 180 spring  large medium 8.600 10.10   2.111  0.663    11.111   3.222
#R> 181 summer  large medium 8.200  9.50   2.200  0.672    10.000   3.800
#R> 182 winter  large medium 8.500 10.50   2.750  0.758    10.500   4.000
#R> 183 summer  large medium 8.300 10.00   3.860  0.866    32.000   6.000
#R> 184 winter  large   high 8.000 10.90   9.055  0.825    40.000  21.083
#R> 185 summer  large   high 8.100 10.20   7.613  0.699    32.500  26.625
#R> 186 winter  large    low 8.700 10.80  39.109  6.225   161.818 104.727
#R> 187 winter  large    low 8.700 11.70  22.455  3.765    88.182  41.300
#R> 188 summer  large    low 8.400  8.20  23.250  2.805    43.750  51.125
#R> 189 autumn  large    low 8.550 11.00  22.320  3.140    82.100  45.900
#R> 190 spring  large medium 8.500  7.60  12.778  1.873    17.778  50.889
#R> 191 autumn  large medium 8.700 11.40  15.541  2.323   103.000  34.500
#R> 192 winter  large medium 8.400 10.50  12.182  1.519    65.455  19.727
#R> 193 spring  large medium 8.200  8.20   7.333  1.003    37.778  19.111
#R> 194 autumn  large medium 8.580 11.10  23.825  3.617    72.600  51.111
#R> 195 summer  large medium 8.500  7.90  12.444  2.586    96.667  19.111
#R> 196 autumn  large medium 8.400  8.40  17.375  3.833    83.750  53.625
#R> 197 spring  large medium 8.300 10.60  14.320  3.200   125.333  35.333
#R> 198 autumn  large medium 8.200  7.00 139.989  2.978    60.110  78.333
#R> 199 winter  large medium 8.000  7.60      NA     NA        NA      NA
#R> 200 summer  large medium 8.500  6.70  82.852  2.800    27.069  64.000
#R>         PO4    Chla   a1   a2   a3   a4   a5   a6   a7
#R> 1   170.000  50.000  0.0  0.0  0.0  0.0 34.2  8.3  0.0
#R> 2   558.750   1.300  1.4  7.6  4.8  1.9  6.7  0.0  2.1
#R> 3   187.057  15.600  3.3 53.6  1.9  0.0  0.0  0.0  9.7
#R> 4   138.700   1.400  3.1 41.0 18.9  0.0  1.4  0.0  1.4
#R> 5    97.580  10.500  9.2  2.9  7.5  0.0  7.5  4.1  1.0
#R> 6    56.667  28.400 15.1 14.6  1.4  0.0 22.5 12.6  2.9
#R> 7   111.750   3.200  2.4  1.2  3.2  3.9  5.8  6.8  0.0
#R> 8    77.434   6.900 18.2  1.6  0.0  0.0  5.5  8.7  0.0
#R> 9    71.000   5.544 25.4  5.4  2.5  0.0  0.0  0.0  0.0
#R> 10   46.600   0.800 17.0  0.0  0.0  2.9  0.0  0.0  1.7
#R> 11   20.750   0.800 16.6  0.0  0.0  0.0  1.2  0.0  6.0
#R> 12   19.000   0.600 32.1  0.0  0.0  0.0  0.0  0.0  1.5
#R> 13   17.000  41.000 43.5  0.0  2.1  0.0  1.2  0.0  2.1
#R> 14   15.000   0.500 31.1  1.0  3.4  0.0  1.9  0.0  4.1
#R> 15   61.600   0.300 52.2  5.0  7.8  0.0  4.0  0.0  0.0
#R> 16   98.250   1.100 69.9  0.0  1.7  0.0  0.0  0.0  0.0
#R> 17   50.000   1.100 46.2  0.0  0.0  1.2  0.0  0.0  0.0
#R> 18   57.833   0.400 31.8  0.0  3.1  4.8  7.7  1.4  7.2
#R> 19   61.500   0.800 50.6  0.0  9.9  4.3  3.6  8.2  2.2
#R> 20  771.600   4.500  0.0  0.0  0.0 44.6  0.0  0.0  1.4
#R> 21  586.000  16.000  0.0  0.0  0.0  6.8  6.1  0.0  0.0
#R> 22   18.000   0.500 15.5  0.0  0.0  2.3  0.0  0.0  0.0
#R> 23   40.000   7.600 23.2  0.0  0.0  0.0 27.6 11.1  0.0
#R> 24   27.500   1.700 74.2  0.0  0.0  3.7  0.0  0.0  0.0
#R> 25   11.500   1.500 13.0  8.6  1.2  3.5  1.2  1.6  1.9
#R> 26   44.136   3.000  4.1  0.0  0.0  0.0  9.2 10.1  0.0
#R> 27   13.600   0.500 29.7  0.0  0.0  4.9  0.0  0.0  0.0
#R> 28       NA   2.700 30.3  1.9  0.0  0.0  2.1  1.4  2.1
#R> 29   45.000   0.800 17.1  0.0 19.6  0.0  0.0  0.0  2.5
#R> 30   19.000   0.500 33.9  1.0 14.6  0.0  0.0  0.0  0.0
#R> 31  142.000   4.900  3.4 16.0  1.2  0.0 15.3 15.8  0.0
#R> 32  304.000   2.800  6.9 17.1 20.2  0.0  4.0  0.0  2.9
#R> 33  130.750   5.800  0.0  8.0  1.9  0.0 11.2 42.7  1.2
#R> 34   47.000   2.300 13.6  9.1  0.0  0.0  1.4  0.0  0.0
#R> 35   23.000   0.900  5.3 40.7  3.3  0.0  0.0  0.0  1.9
#R> 36   84.460   3.600 18.3 12.4  1.0  0.0  0.0  0.0  1.0
#R> 37    3.000   0.200 66.0  0.0  0.0  0.0  0.0  0.0  0.0
#R> 38    3.000   0.300 75.8  0.0  0.0  0.0  0.0  0.0  0.0
#R> 39  253.250  12.320  2.0 38.5  4.1  2.2  0.0  0.0 10.2
#R> 40  255.280   8.957  2.2  2.7  1.0  3.7  2.7  0.0  0.0
#R> 41  296.000   3.700  0.0  5.9 10.6  1.7  0.0  0.0  7.1
#R> 42  175.046  13.200  0.0  0.0  0.0  5.7 11.3 17.0  1.6
#R> 43  344.600  22.500  0.0 40.9  7.5  0.0  2.4  1.5  0.0
#R> 44  326.857  11.840  4.1  3.1  0.0  0.0 19.7 17.0  0.0
#R> 45   40.667   3.900 51.8  4.1  0.0  0.0  3.1  5.5  0.0
#R> 46   43.500   3.300 29.5  1.0  2.7  3.2  2.9  9.6  0.0
#R> 47   39.000   0.800 54.4  3.4  1.2  0.0 18.7  2.0  0.0
#R> 48    6.000   1.100 35.5  0.0  0.0  0.0  0.0  0.0  0.0
#R> 49  121.000   2.800 89.8  0.0  0.0  0.0  0.0  0.0  0.0
#R> 50   20.812  12.100 24.8  7.4  0.0  2.5 10.6 17.1  3.2
#R> 51   49.333   7.900  0.0  0.0  0.0  4.6  1.2  0.0  3.9
#R> 52   22.900   4.500 39.1  0.0  1.2  2.2  5.4  1.5  3.2
#R> 53   11.800   0.500 81.9  0.0  0.0  0.0  0.0  0.0  0.0
#R> 54   11.818   0.800 54.0  0.0  0.0  2.4  0.0  0.0  0.0
#R> 55    6.500      NA 24.3  0.0  0.0  0.0  0.0  0.0  0.0
#R> 56    1.000      NA 82.7  0.0  0.0  0.0  0.0  0.0  0.0
#R> 57    4.000      NA 16.8  4.6  3.9 11.5  0.0  0.0  0.0
#R> 58    6.000      NA 46.8  0.0  0.0 28.8  0.0  0.0  0.0
#R> 59   11.000      NA 46.9  0.0  0.0 13.4  0.0  0.0  0.0
#R> 60    6.000      NA 47.1  0.0  0.0  0.0  0.0  1.2  0.0
#R> 61   14.000      NA 66.9  0.0  0.0  0.0  0.0  0.0  0.0
#R> 62   14.000      NA 19.4  0.0  0.0  2.0  0.0  3.9  1.7
#R> 63    6.667      NA 14.4  0.0  0.0  0.0  0.0  0.0  0.0
#R> 64    6.750   1.000 20.3  4.3  5.5  0.0  0.0  0.0  1.4
#R> 65    7.200   0.300 15.8  1.7  7.8  0.0  0.0  2.4  1.4
#R> 66    6.000   0.600 55.5  0.0  1.7  1.4  0.0  0.0  0.0
#R> 67   10.750   2.500 10.3  0.0 42.8  2.2  0.0  0.0  0.0
#R> 68    2.500   0.500 64.2  0.0  3.0  0.0  0.0  0.0  0.0
#R> 69  351.600  10.000  0.0  0.0  1.5  7.6  0.0  0.0  6.1
#R> 70  313.600   1.000  1.9  4.9  2.6  3.0  0.0  0.0  1.9
#R> 71  279.066  13.100 25.5  3.9  1.0 11.0  0.0  0.0 12.5
#R> 72  152.333   5.200 11.3  1.7  2.0  2.2 13.3 10.6  0.0
#R> 73   58.623  11.600  4.4  4.0  3.3  0.0 11.7 21.4  1.2
#R> 74  249.250  20.870  1.9  5.8 24.8  4.6  9.5  5.1  1.2
#R> 75  233.500  13.000  1.6  8.0 17.6  3.7 11.5  7.0  0.0
#R> 76  215.500  18.370  2.2  9.6  5.0  1.0  8.6  7.9  2.2
#R> 77  102.333   3.600 64.9  1.0  0.0  1.0  2.9  1.4  1.0
#R> 78  105.727   3.000 15.1  7.3 23.2  3.4  4.1  0.0  0.0
#R> 79  111.375   3.000 14.4  0.0 11.8 11.3  5.5  0.0  0.0
#R> 80  108.000   1.300  6.7  0.0  5.4  3.4  4.9  6.9 10.8
#R> 81   56.667   2.000 10.8  0.0  0.0  4.6  6.5  2.2  1.4
#R> 82   60.000   4.300  1.2  0.0  1.7  0.0  7.5 17.7 14.4
#R> 83  104.000  21.000 12.6  4.3 21.9  1.0  2.4  3.3 22.1
#R> 84   69.930   3.100 14.7  4.1  1.0  0.0  7.7  8.5 31.2
#R> 85  214.000   2.900  3.3  0.0  0.0  5.0  1.9  6.2 25.6
#R> 86  254.600   4.300  0.0  0.0  0.0  4.6  9.0 13.1 30.1
#R> 87  169.001   3.200  2.8  0.0  0.0  2.6  5.2 13.2 16.7
#R> 88  607.167   4.300  0.0  0.0  2.6  2.4  5.0  0.0  2.4
#R> 89  624.733   6.800  0.0  0.0  0.0  1.0 35.6  9.9  0.0
#R> 90  303.333  40.000  0.0 15.2  8.8  0.0  8.6  5.1  2.7
#R> 91  391.750   3.500  0.0  5.5  3.3  0.0 20.8 12.4  0.0
#R> 92  265.250   7.300  0.0  2.1  1.6  0.0 20.8 32.9  0.0
#R> 93  232.833  31.000  1.2  5.6  6.3  1.7  1.2  0.0  1.0
#R> 94  244.000   9.000  0.0  3.1  3.5  1.6  8.2  9.9  0.0
#R> 95  218.000   6.500  0.0  5.2  0.0  0.0 28.8 20.4  1.0
#R> 96  138.500  20.829  5.7  0.0  0.0  4.4 12.4  8.3  7.8
#R> 97  239.000  72.478  3.6 31.9  2.4  0.0  0.0  0.0  2.2
#R> 98  235.667  98.817  1.2 16.2  0.0  0.0  0.0  0.0  1.0
#R> 99  205.875   2.000  4.0  2.1 35.1  6.8  7.3  0.0  0.0
#R> 100 211.667  21.900  5.9  3.4  1.0  1.2 17.8 49.4  1.0
#R> 101 186.500  30.000 16.5  2.1 19.5  3.5  5.3  1.2  3.2
#R> 102 154.125   5.200  7.0  0.0 13.5  4.3  8.7  0.0  4.3
#R> 103 183.667  17.200 58.7  0.0 11.5  6.6  0.0  0.0  0.0
#R> 104 292.625   3.000  8.7  0.0  3.0  5.3  9.4 33.2  0.0
#R> 105 285.714  75.000 17.0 21.6  1.6  1.4 10.2  3.6  1.1
#R> 106 201.778   3.000 12.3  5.4  1.9  0.0  1.4  0.0  1.9
#R> 107 275.143  65.700  8.8 19.6  4.7  0.0  0.0  0.0  2.7
#R> 108 124.200  13.100 23.7 13.7  0.0  1.7  6.4  2.6  0.0
#R> 109 141.833  25.000  0.0  6.4  7.3 12.7  0.0  0.0  4.2
#R> 110 132.546  15.000  3.6 38.8  0.0  0.0  1.2  0.0  2.4
#R> 111  17.333   1.000 64.3  1.5  8.0  0.0  0.0  0.0  0.0
#R> 112  26.000   0.300 46.6  0.0  2.5  0.0  0.0  0.0  0.0
#R> 113  16.662   2.100 24.0  0.0  1.0  0.0  0.0  0.0  0.0
#R> 114 102.571   1.200  3.7  1.4  1.1  2.1  3.2  6.4  0.0
#R> 115  86.997   3.000 18.1 14.5  0.0  0.0 11.5 22.3  0.0
#R> 116  10.111      NA 41.0  1.5  0.0  0.0  0.0  0.0  0.0
#R> 117  18.293   1.400 43.7  0.0  1.2  0.0  0.0  4.7  0.0
#R> 118  13.200   3.200 86.6  0.0  0.0  0.0  0.0  0.0  0.0
#R> 119 432.909  24.917  1.9 12.7 25.9  0.0  0.0  0.0  6.8
#R> 120 320.400   6.800  1.2  1.9 22.9  0.0  8.1  0.0  0.0
#R> 121 287.000   9.882  1.4 18.4  0.0  0.0 20.0 29.5  0.0
#R> 122 262.727  17.200  1.6  8.9  6.6  0.0  9.2  1.6  1.4
#R> 123 222.286   6.429  3.3 11.6  7.0  0.0 17.9  4.7  0.0
#R> 124 122.000   5.555 14.6  0.0  0.0  1.9 22.1 12.7  1.4
#R> 125 127.222   5.233  1.7  0.0 10.3  2.6  8.9  6.7  0.0
#R> 126  89.625   2.150  3.3  0.0  0.0  1.9 34.3  7.1  6.0
#R> 127 284.000  88.255  0.0 36.6  4.1  0.0  1.2 16.7  6.1
#R> 128 277.333 110.456  0.0 16.4 10.1  0.0  0.0  0.0  6.6
#R> 129 177.625  50.225  1.5 32.8  1.0  4.1  0.0 15.8  2.4
#R> 130  72.900  11.100  4.2  0.0  1.4  1.9 16.2  0.0  1.4
#R> 131  82.444   2.000  4.1  0.0 25.3  2.1  8.0  0.0 18.6
#R> 132  66.750   3.300  1.2  0.0  2.3  0.0 44.4  7.5  1.9
#R> 133 173.750  15.300  0.0  0.0  1.0  0.0  9.0 64.6  0.0
#R> 134 317.000   5.500  2.4  1.7  4.2  8.3  1.7  0.0  2.4
#R> 135  84.000   4.500  7.8  8.7  2.1  0.0 14.9 22.9  2.4
#R> 136 213.000   2.000 10.3 26.5  6.1  0.0  5.6  1.5  2.2
#R> 137  88.500   2.500  1.5 72.6  0.0  0.0  3.4  6.8  3.4
#R> 138 115.000  11.700  9.2  2.9  2.0  1.3  2.5  0.0  0.0
#R> 139  98.143   2.000 28.1  0.0  0.0  4.0  1.2  0.0  0.0
#R> 140 143.750   5.450  2.1  2.6  0.0  0.0 15.0 15.7  0.0
#R> 141 197.143   6.400  1.4 15.7  1.4  0.0  3.5  0.0  1.6
#R> 142  35.200   1.000 19.0  0.0 22.0  5.0  1.1  5.4  0.0
#R> 143  23.485   2.000 42.5  0.0  2.2  1.0  0.0  0.0  0.0
#R> 144 200.231  19.400  2.5  1.4  1.4  6.2  4.1  1.8  3.9
#R> 145 147.833   3.000  4.4 11.2  6.8  0.0  1.0  0.0 31.6
#R> 146 276.000   8.100  6.5  4.1  0.0  7.7  9.9 18.2  7.0
#R> 147 123.333  30.400 39.7 12.7  0.0  1.1  2.7  0.0  1.6
#R> 148  75.207  23.800 32.8 28.0  2.0  3.5  1.0  0.0  1.5
#R> 149 116.200   7.300 12.2 16.0  1.0  1.4  1.9  1.2  0.0
#R> 150 188.667  32.000  1.9 25.4 21.7  0.0  0.0  1.0  0.0
#R> 151  72.696  22.700  0.0  5.6  1.2  0.0  8.0  2.7  0.0
#R> 152 116.200  16.000  0.0  0.0  0.0  1.2  5.7 32.1  0.0
#R> 153  34.000  53.100  2.2  0.0  0.0  1.2  5.9 77.6  0.0
#R> 154  76.333   2.100  3.4 21.5 14.0  1.8  3.9  0.0  0.0
#R> 155  58.374  27.500  2.8  1.9  0.0  1.2 19.0  4.5  0.0
#R> 156 361.000  28.567 24.8 10.4  0.0  6.9  0.0  0.0  2.7
#R> 157 236.000  22.500 32.5 12.0  0.0  5.0  0.0  0.0  1.9
#R> 158 125.800  26.800  0.0 28.0  0.0  0.0  0.0  0.0 15.1
#R> 159  54.916  20.600  0.0 11.3  1.8  0.0  2.5  0.0  1.4
#R> 160  75.333  34.750  0.0 20.1  0.0  0.0  0.0  0.0  0.0
#R> 161 186.000  68.050  1.7 20.6  1.5  2.2  0.0  0.0  0.0
#R> 162 252.500  93.683 12.3 21.7  3.9  0.0  0.0  0.0  3.9
#R> 163 269.667  92.667  7.2 28.2  0.0  0.0  0.0  0.0  3.3
#R> 164  46.438  81.540  3.4 21.5  0.0  0.0  0.0  0.0  2.7
#R> 165  85.000   2.000  0.0  0.0  0.0  2.4  0.0 17.8  3.6
#R> 166 171.272   3.800  1.1  0.0  1.4  0.0  6.6 42.1  5.2
#R> 167 232.900  54.367  0.0  6.0  2.9  0.0  0.0  0.0  2.9
#R> 168 146.452  21.220  1.4 14.7  2.5  0.0  0.0  0.0  2.0
#R> 169 246.667  14.700 12.5  2.1  0.0  1.2  6.4  4.5  1.7
#R> 170 219.909   6.209  0.0  0.0  0.0  0.0  8.6 52.5  0.0
#R> 171 272.222  20.578  2.5 13.2  0.0  2.0  7.4 17.2  0.0
#R> 172 388.167   5.083  1.7 12.0  4.9  2.7  0.0  5.9  1.7
#R> 173 167.900   5.609  1.4  4.6 10.8  2.2  5.5 42.4  0.0
#R> 174 137.778   9.384  0.0  3.8 16.0  4.0  0.0  0.0  3.3
#R> 175 194.100  27.618  0.0  1.2  0.0  0.0 11.3 11.5  0.0
#R> 176 221.278  20.800  0.0 21.1  3.7  0.0  0.0  0.0  1.9
#R> 177  21.300   1.100 39.7  0.0 12.9  0.0  0.0  0.0  0.0
#R> 178  11.000   0.600 37.3  9.7 13.6  0.0  2.2  0.0  1.2
#R> 179  14.354   0.800 52.4  7.5  9.4  0.0  1.4  1.9  0.0
#R> 180   7.000   1.300 48.3  2.0  0.0  0.0  0.0  0.0  0.0
#R> 181   6.200   0.800 50.4  3.8  0.0  0.0  0.0  0.0  0.0
#R> 182   7.654   4.000 56.8  5.0  0.0  0.0  0.0  0.0  0.0
#R> 183  16.000   2.860 17.3  6.7 19.7  0.0  0.0  0.0  0.0
#R> 184  56.091      NA 16.8 19.6  4.0  0.0  0.0  0.0  0.0
#R> 185  52.875   2.000 18.1  1.7  2.0  0.0  1.7  5.9  0.0
#R> 186 228.364  46.075  1.1  3.9  2.1  0.0  3.9  4.6  2.3
#R> 187  85.400  17.491  0.0  4.7  0.0  0.0  2.6  2.6  0.0
#R> 188  87.125  14.775  0.0 12.0  1.7  0.0  2.7  0.0  0.0
#R> 189 101.455  18.330  1.7  7.0  1.2  0.0  4.8  3.1  0.0
#R> 190 127.000  24.556  0.0  0.0 10.2  1.7  1.2  0.0  5.5
#R> 191  81.558   5.620  7.6  0.0  1.2  0.0 15.9 31.8  5.9
#R> 192  50.455   8.155  2.9  4.6  1.0  0.0  6.6 16.6  0.0
#R> 193 120.889   5.111  2.2 12.7  8.8  0.0  0.0  0.0  1.2
#R> 194  91.111  22.900  3.8 22.0  2.9  0.0  3.1  5.5  0.0
#R> 195  61.444   6.167 18.9 13.2  5.0  0.0  6.1  0.0  0.0
#R> 196  79.750   2.338 12.7 21.7  5.6  0.0  1.0  0.0  0.0
#R> 197  75.904   4.667 18.0  7.0  1.7  0.0  4.8 10.3  1.0
#R> 198 140.220  31.738  0.0 15.9  2.4  1.0  0.0  0.0  0.0
#R> 199      NA      NA  0.0 12.5  3.7  1.0  0.0  0.0  4.9
#R> 200 140.517  18.300  2.4 10.5  9.0  7.8  0.0  0.0  5.8
test.data
#R>     season   size  speed mxPH  mnO2       Cl    NO3       NH4     oPO4
#R> 1   summer  small medium 7.95  5.70  57.3330  2.460   273.333  295.667
#R> 2   winter  small medium 7.98  8.80  59.3330  7.392   286.667   33.333
#R> 3   summer  small medium 8.00  7.20  80.0000  1.957   174.286   47.857
#R> 4   spring  small   high 8.35  8.40  68.0000  3.026   458.000   45.200
#R> 5   spring  small medium 8.10 13.20  19.0000  0.000   130.000    6.000
#R> 6   summer  small medium 8.37 12.10  12.8500  0.840    15.000    5.000
#R> 7   spring  small   high 7.31  9.90   6.0000  1.395    58.750    6.000
#R> 8   autumn  small   high 7.91 11.20   5.0000  1.383     6.000   24.333
#R> 9   summer  small   high 7.99 10.70   4.0000  1.368   117.000   17.250
#R> 10  autumn  small   high 7.82 11.50   8.1800  1.488    39.000   16.000
#R> 11  summer  small medium 7.90  6.00  63.0000  1.053 11160.600 1435.000
#R> 12  autumn  small medium 8.02  9.40  18.7400  1.598  6249.600  455.800
#R> 13  summer  small   high 6.60 10.80   4.0000  1.180    80.000    2.000
#R> 14  autumn  small   high 6.79  9.40  11.4200  1.966    42.000    3.000
#R> 15  summer  small   high 6.78 10.20  10.7040  1.460    46.000    3.000
#R> 16  summer  small   high 7.80 10.80  14.5680  1.228    61.250   34.500
#R> 17  spring  small   high 8.30 12.70  27.0000  4.040    10.000  363.000
#R> 18  spring  small medium 7.97  2.50  32.1250  1.034  7912.500  132.625
#R> 19  autumn  small   high 8.20 11.30   6.0000  1.560    10.000    2.000
#R> 20  summer  small   high 8.20 10.40   3.5770  0.788    10.583    1.667
#R> 21  autumn  small medium 8.10  6.40  21.2000  3.222    44.000   54.800
#R> 22  summer  small medium 8.54 12.83  22.5450  4.000   170.500   68.000
#R> 23  autumn  small medium 8.50  7.80  71.0000 11.020   500.000  121.000
#R> 24  spring  small medium 7.70  6.80  65.0000  1.833   782.500   77.250
#R> 25  autumn  small   high 8.40 10.50  50.6000 10.494   334.000  209.100
#R> 26  summer  small   high 8.50 11.50  57.2920 10.526   312.600  261.400
#R> 27  summer  small   high 8.10 12.20  66.0000  4.080    10.000   26.000
#R> 28  autumn  small    low 6.13 11.23   8.8700  0.620    36.000    3.000
#R> 29  winter  small medium   NA 12.10  18.0000  3.140    10.000   21.000
#R> 30  summer  small medium 7.20 10.40  18.0000  2.420    80.000   11.000
#R> 31  spring  small medium 7.90  8.60  27.6500  2.063    62.500    7.750
#R> 32  autumn  small medium 7.80  9.10  36.1240  5.974   169.000   13.091
#R> 33  summer  small   high 7.80  9.40   5.7140  0.807    22.143    6.000
#R> 34  autumn  small   high 7.80 11.35   5.3430  1.363    19.750    5.818
#R> 35  autumn  small   high 5.90 11.90       NA  1.880     5.000    1.000
#R> 36  winter  small   high 6.80  9.10       NA  0.780    10.000    1.000
#R> 37  summer  small medium 6.60  8.80       NA  0.950    20.000    1.000
#R> 38  winter  small   high 6.60 11.80       NA  2.210    10.000    1.000
#R> 39  winter  small medium 6.90  9.20       NA  2.210    10.000    2.000
#R> 40  winter  small   high 7.66 10.80   4.0000  0.997    15.000    1.500
#R> 41  autumn  small   high 7.60 10.50   3.0500  1.002    13.333    1.667
#R> 42  autumn  small medium 7.80  6.90  31.3750  0.933  2138.570  152.429
#R> 43  winter medium medium 8.00  7.00  37.0910  2.237   146.364   84.091
#R> 44  spring medium medium 8.20  7.80  37.6250  1.453   105.714   66.714
#R> 45  autumn medium medium 8.20 10.70 134.6670  4.504   617.778   49.444
#R> 46  summer medium medium 8.00  8.50 131.4690  3.454   792.000   63.100
#R> 47  autumn medium   high 8.90 10.50  34.8000  6.000   122.556   41.111
#R> 48  summer medium   high 8.20  9.20  30.0370  5.184   174.800   86.600
#R> 49  summer medium medium 7.80  8.80  29.0780  2.823   263.556   27.000
#R> 50  summer medium   high 7.50 10.80  10.3570  3.350   127.667   22.000
#R> 51  spring medium   high 7.40  9.00  13.7500  5.268    58.750   56.250
#R> 52  spring medium medium 7.50  8.90  55.8000  4.408   389.000  127.400
#R> 53  spring medium medium 7.80 10.40  49.0000  7.557  6433.330  170.667
#R> 54  autumn medium medium 9.10  8.00 101.2000  4.306   273.750  152.875
#R> 55  autumn medium   high 8.90  8.00  60.2000  4.033   306.471  136.000
#R> 56  summer medium    low 8.50 10.74  56.2920  0.694   264.800   43.400
#R> 57  autumn medium   high 8.30  8.60  75.0000  5.180   560.000   30.500
#R> 58  spring medium   high 7.80  6.30 136.6670  3.734   154.444   35.556
#R> 59  autumn medium medium 7.60  9.20  64.7780  6.164   720.000   21.778
#R> 60  summer medium medium 7.50  9.20  61.5570  7.035   558.333   24.500
#R> 61  autumn medium    low 7.50  8.60  57.5000  7.368   577.000   67.300
#R> 62  spring medium    low 7.70  4.80  88.9090  1.714   669.091   38.182
#R> 63  spring medium    low 7.90  7.20  55.2500  2.235    89.375   17.500
#R> 64  spring medium   high 8.06  2.20  39.0000  2.085   773.125   90.750
#R> 65  autumn medium   high 8.50  7.50   9.3000  1.557   260.000    9.600
#R> 66  autumn medium medium 8.20 10.40  63.3000  0.389   217.143   24.333
#R> 67  winter medium medium 8.00  4.80  58.7670  0.308    93.750   33.375
#R> 68  autumn medium   high 8.70 10.80   1.1180  0.534    26.364   14.818
#R> 69  spring medium   high 8.40 11.20   0.5000  0.320    10.000   21.600
#R> 70  winter medium    low 8.50  8.30  36.5830  5.632   440.833  149.000
#R> 71  autumn medium    low 8.30  8.80  64.7680  6.272   357.167  219.000
#R> 72  autumn medium medium 8.40 10.80  47.3040  7.773   258.909  145.091
#R> 73  autumn medium   high 7.90 11.90  11.8620  2.209   128.636   48.091
#R> 74  autumn medium medium 9.13 12.00  30.4960  4.971    99.600   64.600
#R> 75  autumn medium   high 7.40 11.40  12.0310  1.621   176.800   36.300
#R> 76  summer medium medium 8.30  8.90 271.5000  6.315   375.000  169.000
#R> 77  winter medium medium 8.20 10.40  41.0000  5.160   410.000   38.000
#R> 78  summer medium medium 8.20 11.20  36.0000  4.400    32.500  108.000
#R> 79  spring medium    low 8.17  6.30  37.3000  0.527    82.000   62.000
#R> 80  autumn medium    low 8.33 10.60  36.1560  1.137   119.444   92.889
#R> 81  spring medium medium 8.50  6.70  45.6090  4.411   160.000   88.364
#R> 82  autumn medium medium 8.10  9.10  47.2670  9.367   169.091   75.000
#R> 83  winter medium   high 8.20 11.90  12.2500  2.348   121.875   14.000
#R> 84  summer medium   high 8.10  9.40  11.0000  2.251    48.750   17.375
#R> 85  summer medium    low 7.80  7.90  87.0000 12.130   652.500   93.250
#R> 86  spring medium   high 8.26  5.00  44.8180  0.526    97.273  105.455
#R> 87  summer medium   high 8.11  6.60  49.8570  0.993   194.280   77.000
#R> 88  summer medium   high 7.87  1.80  49.2500  0.611   357.125  128.250
#R> 89  winter medium   high 7.20 10.10  49.5000  3.955    55.000   18.000
#R> 90  spring medium   high 7.80  8.30  51.5000  2.098    30.200   24.600
#R> 91  winter medium medium 7.90 11.30  82.5000  6.283   300.000   12.333
#R> 92  summer medium medium 8.00  8.80 176.2500  0.618   440.000   16.250
#R> 93  winter  large    low 7.70  9.30  66.0000  3.560   310.000   37.000
#R> 94  autumn  large    low 8.10  9.07  71.3900  2.904  1768.800   27.600
#R> 95  winter  large    low 8.70  5.40  48.0000  1.139   144.286   36.714
#R> 96  summer  large    low 7.90  5.30  48.0000  0.513   138.333   61.333
#R> 97  autumn  large    low 8.70 12.20  32.2300  1.887   233.500   17.500
#R> 98  winter  large    low 8.60  6.50  43.0000  0.668    95.000   10.500
#R> 99  spring  large   high 7.40  7.30  19.0000  4.390   120.000   74.857
#R> 100 summer  large   high 7.80 10.40  22.5000  4.720   178.750  116.500
#R> 101 winter  large    low 8.50  9.80  70.2500  1.644   285.000   68.714
#R> 102 spring  large    low 7.98  5.60  47.0600  3.088   357.000  311.400
#R> 103 summer  large    low 7.95  7.20  57.2860  3.746   425.714  291.143
#R> 104 spring  large medium 7.96  5.50 131.3640  3.313   810.900  311.455
#R> 105 autumn  large medium 8.03  7.83  83.0230  4.065  1222.810  240.545
#R> 106 winter  large medium 8.35  2.75  97.7330  3.681   137.444   91.000
#R> 107 summer  large medium 8.15 10.40 189.5670  5.011   162.944  135.778
#R> 108 winter  large   high 8.50 10.10   3.0000  0.851    37.778   10.778
#R> 109 winter  large medium 8.50 11.40   3.0000  0.774    10.909    3.727
#R> 110 spring  large medium 8.50  8.50   4.0250  0.825    23.636    5.583
#R> 111 autumn  large medium 8.40 11.43   4.9660  0.969    24.111    6.000
#R> 112 spring  large   high 8.20  9.90   6.4000  0.553    21.429   12.000
#R> 113 autumn  large   high 8.00 10.98   9.7000  0.874    67.700   26.600
#R> 114 autumn  large    low 8.30  8.90  42.0580  5.922   116.727  150.583
#R> 115 spring  large    low 8.70  6.80  16.8890  2.139    30.000   37.111
#R> 116 winter  large medium 8.60 10.40  15.1820  2.502   140.909   31.909
#R> 117 summer  large medium 8.00  9.10  15.3750  2.118    43.750   48.875
#R> 118 summer  large medium 8.20  9.50  17.8750  2.363    63.750   44.000
#R> 119 spring  large medium 8.50  9.60  16.5450  3.849   103.273   34.273
#R> 120 spring  large medium 8.04  9.30 130.2630  3.776   131.008   97.500
#R> 121 autumn  large medium 7.95  9.10  76.8860  3.461    93.827   68.333
#R> 122 summer  small   high 7.25  9.54       NA  0.642    85.000   14.600
#R> 123 autumn  small   high 7.64 10.30  34.2350  2.942    41.430   17.000
#R> 124 winter  small   high 7.92  8.50  10.8670  1.715   199.540    3.222
#R> 125 spring  small   high 7.62  9.40  11.0550  1.510    13.560    4.000
#R> 126 summer medium   high 7.75 10.70  15.5000  3.976    57.640   10.500
#R> 127 winter  small   high 7.08  8.40   9.4500  1.572    26.540    4.000
#R> 128 summer  small   high 6.92 11.10   9.1000  0.630    21.000    5.000
#R> 129 winter  small   high 8.10  9.80  14.3400  0.730    22.500   23.000
#R> 130 spring  small   high 7.20 11.30   8.9700  0.230   134.500   13.000
#R> 131 spring  large medium 8.61 10.10   3.5180  0.663    12.220    3.222
#R> 132 summer  large medium 8.22  9.50   2.3000  0.672     9.870    4.000
#R> 133 winter  large medium 8.53 10.50   3.0000  0.758    10.350    4.100
#R> 134 summer  large medium 8.40 10.00   3.5100  0.866    29.650    5.800
#R> 135 winter  large   high 8.10 10.90   9.0560  0.825    41.000   20.000
#R> 136 summer medium   high 8.12 10.20   7.6130  0.699    33.560   28.034
#R> 137 winter  large    low 8.43 10.80  35.6420  6.225   134.000  103.500
#R> 138 winter  large    low 8.70 11.70  21.4656  3.765    91.450   38.000
#R> 139 summer  large    low 8.10  8.20  26.5400  2.805    42.750   48.500
#R> 140 autumn  large    low 8.35 11.10  22.5600  3.140    76.200   41.000
#R>          PO4   Chla
#R> 1    380.000     NA
#R> 2    138.000  7.100
#R> 3    113.714  4.500
#R> 4    111.800  3.200
#R> 5     40.000  2.000
#R> 6     10.507 13.800
#R> 7     16.000  0.800
#R> 8     30.000 32.000
#R> 9     44.750  0.800
#R> 10   139.500  0.400
#R> 11  1690.000  4.500
#R> 12   690.600  2.000
#R> 13    59.000  0.600
#R> 14    15.000  0.600
#R> 15    13.714  0.700
#R> 16    62.000  1.100
#R> 17   482.000  6.000
#R> 18   164.620  1.000
#R> 19     5.000     NA
#R> 20     2.088  0.800
#R> 21   155.000 61.520
#R> 22   116.069 41.600
#R> 23        NA  7.100
#R> 24   340.000  9.000
#R> 25   276.667 20.720
#R> 26   299.400 23.500
#R> 27    70.000  1.800
#R> 28    14.741  2.100
#R> 29    41.000  4.800
#R> 30    44.000  2.500
#R> 31    30.000     NA
#R> 32    71.057  3.300
#R> 33    18.714  1.500
#R> 34     8.846  1.900
#R> 35     2.000     NA
#R> 36    14.000     NA
#R> 37     7.000     NA
#R> 38     4.000     NA
#R> 39    13.000     NA
#R> 40     7.333  1.000
#R> 41    10.833     NA
#R> 42   317.500 15.400
#R> 43   172.778  2.300
#R> 44   143.400  2.600
#R> 45   164.778 19.200
#R> 46   286.600  8.200
#R> 47   144.111 27.030
#R> 48   130.800  3.450
#R> 49    95.120 11.500
#R> 50    34.321  1.200
#R> 51    64.000  2.500
#R> 52   206.200  5.000
#R> 53   341.000  2.300
#R> 54   290.313 10.700
#R> 55   242.941 18.400
#R> 56   124.942 30.480
#R> 57   170.000 16.700
#R> 58   175.333  2.700
#R> 59   242.500 54.200
#R> 60   257.333 19.500
#R> 61   254.444 22.000
#R> 62   205.182  2.800
#R> 63   141.500 17.000
#R> 64   163.250 26.000
#R> 65    18.100  3.900
#R> 66   114.000  2.700
#R> 67   110.875  2.700
#R> 68    20.900  1.400
#R> 69    27.600  0.600
#R> 70   266.364 19.827
#R> 71   302.500  8.267
#R> 72   223.044 13.360
#R> 73    69.079  2.755
#R> 74   146.265 54.130
#R> 75    58.599 36.100
#R> 76   313.500  2.800
#R> 77    61.000  6.000
#R> 78   155.500  3.000
#R> 79   133.100  1.400
#R> 80   112.855 10.500
#R> 81   180.364 32.833
#R> 82   127.778  3.667
#R> 83    27.500  4.600
#R> 84    66.875  2.500
#R> 85   209.000  6.000
#R> 86   181.636 20.600
#R> 87   197.571 13.000
#R> 88   185.125  4.500
#R> 89   138.000 49.000
#R> 90   184.400 31.300
#R> 91    53.333 13.700
#R> 92    79.250  3.500
#R> 93        NA 17.350
#R> 94   123.060 41.540
#R> 95    66.833 22.017
#R> 96    89.167  4.000
#R> 97    66.167 39.333
#R> 98    74.667 63.500
#R> 99   166.286  5.300
#R> 100  201.000  2.700
#R> 101  132.000 16.028
#R> 102  342.300 18.530
#R> 103  330.000  4.714
#R> 104  349.818 20.470
#R> 105  269.091  6.809
#R> 106  155.556  2.744
#R> 107  219.278  2.859
#R> 108   23.889  0.500
#R> 109    8.091  3.600
#R> 110   31.091  2.400
#R> 111   18.167  2.133
#R> 112   76.286  1.300
#R> 113   51.034  2.200
#R> 114  220.723  6.700
#R> 115   85.444 23.033
#R> 116   77.700 15.318
#R> 117   86.500  8.125
#R> 118   77.000  8.463
#R> 119   63.400 14.682
#R> 120  152.966  6.150
#R> 121  146.049  3.950
#R> 122   19.450  0.460
#R> 123   41.567  7.430
#R> 124   27.200  1.900
#R> 125   12.650  1.456
#R> 126   43.169  3.120
#R> 127   13.600  0.675
#R> 128       NA  2.460
#R> 129   45.500  0.850
#R> 130   19.000     NA
#R> 131    7.000  1.300
#R> 132    6.123  0.800
#R> 133       NA  4.000
#R> 134   15.000  2.860
#R> 135   58.000     NA
#R> 136   49.658  2.200
#R> 137       NA 45.375
#R> 138   83.000 17.000
#R> 139   88.125 13.980
#R> 140   98.665 17.456
```

Step 2: The second step is to handle the NAs by filling blanks with column mean (for train.data & test.data).


```r
train.data <- train.data %>% mutate_all(~ifelse(is.na(.x), mean(.x, na.rm = TRUE), .x))
train.data$season <- as.factor(train.data$season)
train.data$size <- as.factor(train.data$size)
train.data$speed <- as.factor(train.data$speed)
```


```r
test.data <- test.data %>% mutate_all(~ifelse(is.na(.x), mean(.x, na.rm = TRUE), .x))
test.data$season <- as.factor(test.data$season)
test.data$size <- as.factor(test.data$size)
test.data$speed <- as.factor(test.data$speed)
```

Step 3: The third step of using the model is define in total 7 datasets for the AV's we have and therefore prepare the predictions. This also includes the calculation of the predicted values and the calculation of the RMSE.

1. Multiple linear regression model #1 


```r
modela1 <- lm(a1 ~ season + size + speed + mxPH + mnO2 + log(Cl) + NO3 + NH4 + log(oPO4) + log(PO4) + log(Chla), data = train.data)
summary(modela1)
#R> 
#R> Call:
#R> lm(formula = a1 ~ season + size + speed + mxPH + mnO2 + log(Cl) + 
#R>     NO3 + NH4 + log(oPO4) + log(PO4) + log(Chla), data = train.data)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -35.221  -8.481  -1.309   5.006  69.782 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)  
#R> (Intercept) 55.4555960 21.9297539   2.529   0.0123 *
#R> season2     -1.7606407  3.7387370  -0.471   0.6383  
#R> season3     -1.6620694  3.6549413  -0.455   0.6498  
#R> season4      0.3232167  3.4369950   0.094   0.9252  
#R> size2        4.3934694  3.2372792   1.357   0.1764  
#R> size3        7.7328727  3.7032113   2.088   0.0382 *
#R> speed2       5.3218219  4.1234163   1.291   0.1984  
#R> speed3       1.5409451  2.9266780   0.527   0.5992  
#R> mxPH         0.7470830  2.4740700   0.302   0.7630  
#R> mnO2        -0.3596363  0.6597621  -0.545   0.5863  
#R> log(Cl)     -1.9435729  1.5516159  -1.253   0.2119  
#R> NO3         -0.1294644  0.5253036  -0.246   0.8056  
#R> NH4         -0.0003348  0.0009050  -0.370   0.7119  
#R> log(oPO4)   -3.6735893  1.9889961  -1.847   0.0664 .
#R> log(PO4)    -5.2398109  2.3492656  -2.230   0.0269 *
#R> log(Chla)   -2.2068834  1.0726061  -2.057   0.0410 *
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 15.74 on 184 degrees of freedom
#R> Multiple R-squared:  0.4971,	Adjusted R-squared:  0.4561 
#R> F-statistic: 12.12 on 15 and 184 DF,  p-value: < 2.2e-16
```

>> Calculate predicted values


```r
preda1 <- predict.lm(modela1, test.data, na.action = na.pass)
```

>> Calculate RMSE


```r
RMSE <- function(pred, obs, dv){
  sqrt(mean((pred-obs)^2, na.rm=T))/sd(dv)
}

RMSEa1 <- RMSE(preda1, train.data$a1, train.data$a1)
#R> Warning in pred - obs: longer object length is not a multiple of shorter
#R> object length
```

2. Multiple linear regression model #2


```r
modela2 <- lm(a2 ~ season + size + speed + mxPH + mnO2 + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
summary(modela2)
#R> 
#R> Call:
#R> lm(formula = a2 ~ season + size + speed + mxPH + mnO2 + Cl + 
#R>     NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -17.145  -5.053  -1.802   2.135  61.704 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept) -2.770e+01  1.318e+01  -2.101  0.03700 *  
#R> season2     -3.731e+00  2.350e+00  -1.588  0.11407    
#R> season3     -2.720e+00  2.270e+00  -1.198  0.23239    
#R> season4     -3.154e+00  2.180e+00  -1.447  0.14950    
#R> size2        6.984e-01  2.122e+00   0.329  0.74246    
#R> size3        1.484e+00  2.337e+00   0.635  0.52624    
#R> speed2       9.094e-02  2.659e+00   0.034  0.97275    
#R> speed3       3.746e+00  1.827e+00   2.050  0.04176 *  
#R> mxPH         4.382e+00  1.471e+00   2.980  0.00327 ** 
#R> mnO2        -2.489e-01  3.984e-01  -0.625  0.53296    
#R> Cl          -1.500e-02  1.894e-02  -0.792  0.42959    
#R> NO3          3.166e-01  3.115e-01   1.017  0.31070    
#R> NH4         -9.033e-04  5.690e-04  -1.588  0.11411    
#R> oPO4         2.965e-02  2.179e-02   1.361  0.17532    
#R> PO4         -1.574e-02  1.657e-02  -0.950  0.34319    
#R> Chla         1.834e-01  4.372e-02   4.196 4.22e-05 ***
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 9.993 on 184 degrees of freedom
#R> Multiple R-squared:  0.2408,	Adjusted R-squared:  0.1789 
#R> F-statistic:  3.89 on 15 and 184 DF,  p-value: 4.822e-06
```

>> Calculate predicted values


```r
preda2 <- predict.lm(modela2, test.data, na.action = na.pass)
```

>> Calculate RMSE


```r
RMSEa2 <- RMSE(preda2, train.data$a2, train.data$a2)
#R> Warning in pred - obs: longer object length is not a multiple of shorter
#R> object length
```

3. Multiple linear regression model #3


```r
modela3 <- lm(a3 ~ season + size + speed + mxPH + mnO2 + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
summary(modela3)
#R> 
#R> Call:
#R> lm(formula = a3 ~ season + size + speed + mxPH + mnO2 + Cl + 
#R>     NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
#R> 
#R> Residuals:
#R>    Min     1Q Median     3Q    Max 
#R> -9.301 -3.655 -1.855  1.695 36.924 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)   
#R> (Intercept) 11.9848194  8.6734390   1.382  0.16871   
#R> season2      3.4468345  1.5458913   2.230  0.02698 * 
#R> season3      0.1899946  1.4932651   0.127  0.89889   
#R> season4      1.8507088  1.4339203   1.291  0.19844   
#R> size2        0.6176306  1.3961245   0.442  0.65873   
#R> size3       -1.7037368  1.5375856  -1.108  0.26928   
#R> speed2      -3.6157866  1.7494556  -2.067  0.04015 * 
#R> speed3      -1.8297644  1.2021705  -1.522  0.12971   
#R> mxPH        -0.0621544  0.9675642  -0.064  0.94885   
#R> mnO2        -0.7680247  0.2621231  -2.930  0.00382 **
#R> Cl           0.0040915  0.0124629   0.328  0.74306   
#R> NO3          0.1629201  0.2049364   0.795  0.42765   
#R> NH4         -0.0005812  0.0003743  -1.553  0.12226   
#R> oPO4        -0.0073644  0.0143363  -0.514  0.60809   
#R> PO4          0.0034608  0.0108999   0.318  0.75122   
#R> Chla        -0.0257943  0.0287611  -0.897  0.37097   
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 6.575 on 184 degrees of freedom
#R> Multiple R-squared:  0.1722,	Adjusted R-squared:  0.1047 
#R> F-statistic: 2.551 on 15 and 184 DF,  p-value: 0.001787
```

>> Calculate predicted values


```r
preda3 <- predict.lm(modela3, test.data, na.action = na.pass)
```

>> Calculate RMSE


```r
RMSEa3 <- RMSE(preda3, train.data$a3, train.data$a3)
#R> Warning in pred - obs: longer object length is not a multiple of shorter
#R> object length
```

4. Multiple linear regression model #4


```r
modela4 <- lm(a4 ~ season + size + speed + mxPH + mnO2 + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
summary(modela4)
#R> 
#R> Call:
#R> lm(formula = a4 ~ season + size + speed + mxPH + mnO2 + Cl + 
#R>     NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
#R> 
#R> Residuals:
#R>      Min       1Q   Median       3Q      Max 
#R> -10.1473  -1.7619  -0.1493   1.2065  26.0873 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept) 22.8036253  4.9473272   4.609 7.54e-06 ***
#R> season2      0.2055504  0.8817760   0.233   0.8159    
#R> season3     -0.3150422  0.8517580  -0.370   0.7119    
#R> season4     -0.3177135  0.8179078  -0.388   0.6981    
#R> size2        0.1700448  0.7963490   0.214   0.8311    
#R> size3        0.3720058  0.8770384   0.424   0.6719    
#R> speed2      -0.7081964  0.9978890  -0.710   0.4788    
#R> speed3      -0.7563638  0.6857177  -1.103   0.2715    
#R> mxPH        -2.2634348  0.5518984  -4.101 6.16e-05 ***
#R> mnO2        -0.3094343  0.1495149  -2.070   0.0399 *  
#R> Cl           0.0098658  0.0071088   1.388   0.1669    
#R> NO3         -0.4896526  0.1168957  -4.189 4.35e-05 ***
#R> NH4          0.0009765  0.0002135   4.573 8.80e-06 ***
#R> oPO4        -0.0014364  0.0081774  -0.176   0.8608    
#R> PO4          0.0097475  0.0062173   1.568   0.1186    
#R> Chla        -0.0046280  0.0164053  -0.282   0.7782    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 3.75 on 184 degrees of freedom
#R> Multiple R-squared:  0.3336,	Adjusted R-squared:  0.2792 
#R> F-statistic:  6.14 on 15 and 184 DF,  p-value: 2.26e-10
```

>> Calculate predicted values


```r
preda4 <- predict.lm(modela4, test.data, na.action = na.pass)
```

>> Calculate RMSE


```r
RMSEa4 <- RMSE(preda4, train.data$a4, train.data$a4)
#R> Warning in pred - obs: longer object length is not a multiple of shorter
#R> object length
```

5. Multiple linear regression model #5


```r
modela5 <- lm(a5 ~ season + size + speed + mxPH + mnO2 + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
summary(modela5)
#R> 
#R> Call:
#R> lm(formula = a5 ~ season + size + speed + mxPH + mnO2 + Cl + 
#R>     NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -11.759  -3.617  -1.014   1.844  36.411 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)   
#R> (Intercept) -1.104e+01  8.715e+00  -1.267  0.20689   
#R> season2     -1.843e+00  1.553e+00  -1.187  0.23682   
#R> season3      1.021e+00  1.500e+00   0.680  0.49710   
#R> season4     -1.678e+00  1.441e+00  -1.165  0.24569   
#R> size2        3.368e+00  1.403e+00   2.401  0.01734 * 
#R> size3        3.751e-01  1.545e+00   0.243  0.80842   
#R> speed2      -2.812e+00  1.758e+00  -1.600  0.11131   
#R> speed3      -4.426e-01  1.208e+00  -0.366  0.71445   
#R> mxPH         7.092e-01  9.721e-01   0.729  0.46663   
#R> mnO2         7.350e-01  2.634e-01   2.791  0.00581 **
#R> Cl           7.116e-03  1.252e-02   0.568  0.57052   
#R> NO3          5.009e-01  2.059e-01   2.432  0.01595 * 
#R> NH4         -7.961e-04  3.761e-04  -2.117  0.03562 * 
#R> oPO4        -6.821e-03  1.440e-02  -0.474  0.63641   
#R> PO4          2.285e-02  1.095e-02   2.087  0.03830 * 
#R> Chla        -4.338e-02  2.890e-02  -1.501  0.13501   
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 6.606 on 184 degrees of freedom
#R> Multiple R-squared:  0.281,	Adjusted R-squared:  0.2224 
#R> F-statistic: 4.795 on 15 and 184 DF,  p-value: 8.338e-08
```

>> Calculate predicted values


```r
preda5 <- predict.lm(modela5, test.data, na.action = na.pass)
```

>> Calculate RMSE


```r
RMSEa5 <- RMSE(preda5, train.data$a5, train.data$a5)
#R> Warning in pred - obs: longer object length is not a multiple of shorter
#R> object length
```

6. Multiple linear regression model #6


```r
modela6 <- lm(a6 ~ season + size + speed + mxPH + mnO2 + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
summary(modela6)
#R> 
#R> Call:
#R> lm(formula = a6 ~ season + size + speed + mxPH + mnO2 + Cl + 
#R>     NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -19.066  -5.315  -1.284   2.753  48.140 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)    
#R> (Intercept)  5.4254769 12.3762403   0.438  0.66163    
#R> season2     -2.9639800  2.2058520  -1.344  0.18070    
#R> season3      1.8429011  2.1307590   0.865  0.38822    
#R> season4     -1.4638663  2.0460792  -0.715  0.47524    
#R> size2       -3.3559100  1.9921478  -1.685  0.09377 .  
#R> size3       -6.2890064  2.1940004  -2.866  0.00463 ** 
#R> speed2      -4.5370568  2.4963204  -1.817  0.07077 .  
#R> speed3      -1.6597626  1.7153924  -0.968  0.33453    
#R> mxPH        -0.7712740  1.3806296  -0.559  0.57709    
#R> mnO2         0.6575173  0.3740267   1.758  0.08042 .  
#R> Cl           0.0285116  0.0177835   1.603  0.11059    
#R> NO3          1.2207440  0.2924264   4.175  4.6e-05 ***
#R> NH4          0.0007878  0.0005341   1.475  0.14194    
#R> oPO4        -0.0480160  0.0204567  -2.347  0.01998 *  
#R> PO4          0.0378528  0.0155532   2.434  0.01590 *  
#R> Chla        -0.0504584  0.0410396  -1.230  0.22045    
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 9.382 on 184 degrees of freedom
#R> Multiple R-squared:  0.4015,	Adjusted R-squared:  0.3527 
#R> F-statistic: 8.229 on 15 and 184 DF,  p-value: 3.682e-14
```

>> Calculate predicted values


```r
preda6 <- predict.lm(modela6, test.data, na.action = na.pass)
```

>> Calculate RMSE


```r
RMSEa6 <- RMSE(preda6, train.data$a6, train.data$a6)
#R> Warning in pred - obs: longer object length is not a multiple of shorter
#R> object length
```

7. Multiple linear regression model #7


```r
modela7 <- lm(a7 ~ season + size + speed + mxPH + mnO2 + Cl + NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
summary(modela7)
#R> 
#R> Call:
#R> lm(formula = a7 ~ season + size + speed + mxPH + mnO2 + Cl + 
#R>     NO3 + NH4 + oPO4 + PO4 + Chla, data = train.data)
#R> 
#R> Residuals:
#R>     Min      1Q  Median      3Q     Max 
#R> -6.7777 -2.4322 -1.2191  0.8332 26.4037 
#R> 
#R> Coefficients:
#R>               Estimate Std. Error t value Pr(>|t|)  
#R> (Intercept) 15.5568092  6.6565378   2.337   0.0205 *
#R> season2     -0.1213454  1.1864134  -0.102   0.9186  
#R> season3     -0.5275534  1.1460247  -0.460   0.6458  
#R> season4     -0.1865401  1.1004799  -0.170   0.8656  
#R> size2        1.2021358  1.0714730   1.122   0.2633  
#R> size3       -0.9444757  1.1800390  -0.800   0.4245  
#R> speed2       0.6752945  1.3426413   0.503   0.6156  
#R> speed3       0.4300397  0.9226206   0.466   0.6417  
#R> mxPH        -1.3422332  0.7425691  -1.808   0.0723 .
#R> mnO2        -0.3194371  0.2011696  -1.588   0.1140  
#R> Cl          -0.0229582  0.0095648  -2.400   0.0174 *
#R> NO3          0.3314091  0.1572810   2.107   0.0365 *
#R> NH4         -0.0006165  0.0002873  -2.146   0.0332 *
#R> oPO4        -0.0047316  0.0110026  -0.430   0.6677  
#R> PO4          0.0074985  0.0083653   0.896   0.3712  
#R> Chla        -0.0077729  0.0220731  -0.352   0.7251  
#R> ---
#R> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
#R> 
#R> Residual standard error: 5.046 on 184 degrees of freedom
#R> Multiple R-squared:  0.1153,	Adjusted R-squared:  0.04321 
#R> F-statistic: 1.599 on 15 and 184 DF,  p-value: 0.0774
```

>> Calculate predicted values


```r
preda7 <- predict.lm(modela7, test.data, na.action = na.pass)
```

>> Calculate RMSE


```r
RMSEa7 <- RMSE(preda7, train.data$a7, train.data$a7)
#R> Warning in pred - obs: longer object length is not a multiple of shorter
#R> object length
```

Step 3: Create table and find the solution.


```r
RMSE.table <- matrix(c(RMSEa1, RMSEa2, RMSEa3, RMSEa4, RMSEa5, RMSEa6, RMSEa7), ncol=1, byrow=TRUE)
colnames(RMSE.table) <- c("RMSE")
rownames(RMSE.table) <- c("Model a1:", "Model a2:", "Model a3:", "Model a4:", "Model a5:", "Model a6:", "Model a7:")
RMSE.table <- as.table(RMSE.table)
RMSE.table
#R>               RMSE
#R> Model a1: 1.224734
#R> Model a2: 1.083993
#R> Model a3: 1.048168
#R> Model a4: 1.324800
#R> Model a5: 1.170842
#R> Model a6: 1.061003
#R> Model a7: 1.031306
```

Our best vector of predictions, called `our.predictions`:


```r
our.predictions <- c(preda1, preda2, preda3, preda4, preda5, preda6, preda7)
our.predictions
#R>             1             2             3             4             5 
#R>   1.343549386  15.835459134  15.292943150  14.616999439  31.065779885 
#R>             6             7             8             9            10 
#R>  35.863443597  39.028342424  24.565259840  30.850603466  26.566619167 
#R>            11            12            13            14            15 
#R> -14.080769679   1.070207597  36.914630572  42.780493299  41.142725132 
#R>            16            17            18            19            20 
#R>  23.239819019  -1.849925275  13.800809748  45.274821672  56.087140567 
#R>            21            22            23            24            25 
#R>  11.886116174   9.563885798  10.752044673   6.302434315   0.811817744 
#R>            26            27            28            29            30 
#R>  -2.885272167  18.988350329  44.945060347  26.528220816  28.088923470 
#R>            31            32            33            34            35 
#R>  28.385278196  25.059575605  37.647850894  42.185623647  46.916634303 
#R>            36            37            38            39            40 
#R>  38.863743108  41.984479854  44.122415512  38.100272472  50.592576306 
#R>            41            42            43            44            45 
#R>  43.118294646   5.856596051  12.696312809  12.117842087   5.750736800 
#R>            46            47            48            49            50 
#R>   2.936249104   8.032200091   9.002853279  14.021279709  24.601900520 
#R>            51            52            53            54            55 
#R>  15.966485924   4.233116340  -0.257006612   2.266221585   1.776535200 
#R>            56            57            58            59            60 
#R>  11.295145696   8.028314880   9.173986914   5.712401003   5.528398722 
#R>            61            62            63            64            65 
#R>   7.351108028  14.719615567  15.889953264   5.220062999  32.392849815 
#R>            66            67            68            69            70 
#R>  16.856840434  18.225699275  35.596182367  34.093193241   6.748419083 
#R>            71            72            73            74            75 
#R>   4.780030243   2.853660772  17.678614004   6.332490701  13.734780532 
#R>            76            77            78            79            80 
#R>  -0.341622461  17.218795372   8.212535899  18.586354644  13.821899091 
#R>            81            82            83            84            85 
#R>   4.131782621  11.262469849  26.375886703  21.357185923   7.418481154 
#R>            86            87            88            89            90 
#R>   3.923227933   4.764851200   7.138533227   8.780030930   6.286318950 
#R>            91            92            93            94            95 
#R>  18.219076030  16.341878895   9.538375911   8.673219185  15.859980872 
#R>            96            97            98            99           100 
#R>  13.764064707  15.232571153  17.361107777   3.937800535   1.699455749 
#R>           101           102           103           104           105 
#R>   8.107258056  -3.151304250  -0.681174300  -9.421638967  -3.037144567 
#R>           106           107           108           109           110 
#R>   7.896347947  -1.817561994  32.406237333  38.716013375  29.449575228 
#R>           111           112           113           114           115 
#R>  32.465715771  20.154579796  18.533326619   4.806787021  13.785261101 
#R>           116           117           118           119           120 
#R>  12.794613711  10.157128542  10.737110819  11.491640197   0.710205164 
#R>           121           122           123           124           125 
#R>   6.078821979  32.499724801  23.565643670  38.423163924  39.651180267 
#R>           126           127           128           129           130 
#R>  23.390129528  43.300842965  24.724718255  29.596795147  28.244658933 
#R>           131           132           133           134           135 
#R>  40.427910384  42.254790433  23.736553693  32.484822892  15.917428070 
#R>           136           137           138           139           140 
#R>  22.090173931   4.555203340  14.145133238  11.919899127  12.522125590 
#R>             1             2             3             4             5 
#R>  12.720210582   8.466888402   7.794341235   4.247054105   5.524336592 
#R>             6             7             8             9            10 
#R>  11.053734280  -0.003898652  12.137610399   3.637703792   3.856672821 
#R>            11            12            13            14            15 
#R>  14.006537021   7.924206074  -3.217722194   1.577197123  -1.499755544 
#R>            16            17            18            19            20 
#R>   2.922590618   8.405103932   2.327168647   9.315749180   4.761148615 
#R>            21            22            23            24            25 
#R>  22.566448701  17.637005595  17.577533800   3.338497717  15.888963675 
#R>            26            27            28            29            30 
#R>  14.990459021   3.817368124  -1.782883593   7.893806896   4.291747291 
#R>            31            32            33            34            35 
#R>   8.252852220  10.520059807   3.215768154   5.857101138  -1.313035442 
#R>            36            37            38            39            40 
#R>  -0.368443056   3.166133456  -1.306601785   4.289465394   1.865241700 
#R>            41            42            43            44            45 
#R>   6.648356452  10.233906234   7.121641675   7.005694838  11.259324058 
#R>            46            47            48            49            50 
#R>   4.238037138  14.563536145   6.098666197   7.649773311   1.580982733 
#R>            51            52            53            54            55 
#R>   1.984925374   5.322287449   0.568232251  16.155919170  13.689950062 
#R>            56            57            58            59            60 
#R>   8.993951195   8.532387163  -0.335392959  14.860979013   5.655342147 
#R>            61            62            63            64            65 
#R>   6.791141671  -1.071428004   3.395328040   8.308628985   9.215618513 
#R>            66            67            68            69            70 
#R>   8.491417430   6.325267331   8.932583718   3.692857625   9.816366689 
#R>            71            72            73            74            75 
#R>  11.211371522  15.627261749   5.906382778  24.337493783   9.539560932 
#R>            76            77            78            79            80 
#R>   6.361367525   8.852865235   9.301150576   3.127481926   9.569347063 
#R>            81            82            83            84            85 
#R>  14.967663904  12.966026948   4.093249700   3.861173674   5.107688323 
#R>            86            87            88            89            90 
#R>   7.673703681   5.125363101   5.165476356   6.692992772   4.816867911 
#R>            91            92            93            94            95 
#R>   7.919045450   3.925316655   2.678836377  10.382734219   9.604462137 
#R>            96            97            98            99           100 
#R>   3.439002724  14.076534043  15.571745952   0.752382554   2.954890394 
#R>           101           102           103           104           105 
#R>   6.156180128   9.429311997   6.962454018  11.658147371  12.369472563 
#R>           106           107           108           109           110 
#R>   9.128122792   6.149037479   4.107426774   8.138488859   7.746153364 
#R>           111           112           113           114           115 
#R>  10.507272699   1.493821468   5.085104289   9.906779482   9.471425176 
#R>           116           117           118           119           120 
#R>  10.961683008   8.099134152   8.965093313  10.765074907   5.969677770 
#R>           121           122           123           124           125 
#R>   8.930600797   0.186185362   6.295138346   3.438069585   1.594235662 
#R>           126           127           128           129           130 
#R>   2.757717036  -0.073376442  -2.852803693   3.804880210   0.730472285 
#R>           131           132           133           134           135 
#R>   7.904136925   7.323908078   6.576763321   8.305158474   3.731256711 
#R>           136           137           138           139           140 
#R>   3.854840162  14.074905436   8.176970766   6.194230428   9.672416564 
#R>             1             2             3             4             5 
#R>   3.097733059   4.376855179   3.084193444   7.234070535   1.301620117 
#R>             6             7             8             9            10 
#R>  -1.347727557   5.878353866   0.529061399   1.935042055   1.570607997 
#R>            11            12            13            14            15 
#R>  -7.349935465  -3.579863831   2.102290292   2.996581324   2.478055940 
#R>            16            17            18            19            20 
#R>   1.847802559   3.061015325   4.751419495   1.082307016   2.085134428 
#R>            21            22            23            24            25 
#R>   2.164591838  -2.270541344   3.120442517   6.682431886   2.300455434 
#R>            26            27            28            29            30 
#R>   1.383046774   1.531017761  -2.249493325   0.955977324   0.634545194 
#R>            31            32            33            34            35 
#R>   4.975883586   2.064743639   2.890714426   1.250399813   0.959389281 
#R>            36            37            38            39            40 
#R>   4.764039580   1.514058740   2.901171872   3.073407886   3.519638943 
#R>            41            42            43            44            45 
#R>   1.651741959   1.283682164   7.100472496   7.986390020   2.681796951 
#R>            46            47            48            49            50 
#R>   4.893241098   4.532454281   5.808758722   3.978702340   4.471389973 
#R>            51            52            53            54            55 
#R>   9.300252690   7.284741923   3.304081179   4.622258100   5.994922534 
#R>            56            57            58            59            60 
#R>  -0.084173814   6.239849693  12.078982025   3.366135630   4.711373237 
#R>            61            62            63            64            65 
#R>   2.833294512   8.879236581   6.873261114  13.134613457   6.345912945 
#R>            66            67            68            69            70 
#R>   2.617422515   8.744063896   3.770383938   6.894648428   4.058608612 
#R>            71            72            73            74            75 
#R>   2.012260481   2.624158418   3.119443164   0.499890256   2.601891243 
#R>            76            77            78            79            80 
#R>   5.301274955   4.672910400   2.361801747   7.245880467   0.027263876 
#R>            81            82            83            84            85 
#R>   8.484252228   4.696699102   5.039243348   5.491966437   4.459239143 
#R>            86            87            88            89            90 
#R>  11.228926950   7.253633775  10.594463611   6.144620363   9.374483888 
#R>            91            92            93            94            95 
#R>   4.380892955   4.337249734   3.015350941  -0.212009753   5.222774903 
#R>            96            97            98            99           100 
#R>   3.950781683  -2.152467099   3.465751747   9.975838768   4.227726842 
#R>           101           102           103           104           105 
#R>   2.091779310   5.920478132   2.008758533   7.877920376   2.917789696 
#R>           106           107           108           109           110 
#R>  10.091817553   3.033547719   5.669534269   2.761699213   6.687085198 
#R>           111           112           113           114           115 
#R>   0.982277558   7.564472467   3.121384195   1.568880836   5.880990122 
#R>           116           117           118           119           120 
#R>   3.510425805   2.971177467   2.684363664   5.923595985   6.684277155 
#R>           121           122           123           124           125 
#R>   3.396143336   2.864093139   2.317882791   5.340620614   6.294993646 
#R>           126           127           128           129           130 
#R>   4.762168068   5.519879856   2.010251149   4.232384830   4.281851851 
#R>           131           132           133           134           135 
#R>   5.391963545   2.622159728   3.874673619   2.216350574   4.875780367 
#R>           136           137           138           139           140 
#R>   4.488078202   1.017577300   0.910076500   1.885711179  -0.526190688 
#R>             1             2             3             4             5 
#R>   5.202203064  -0.173473699   2.788884139   2.528709850   0.892884039 
#R>             6             7             8             9            10 
#R>  -0.823395938   3.349211389   1.293572896   1.356387288   2.642206169 
#R>            11            12            13            14            15 
#R>  27.761898620  12.930613095   4.689276348   4.228376355   3.920029243 
#R>            16            17            18            19            20 
#R>   2.015848231   3.111921533  12.758296805   0.418528604   0.756340609 
#R>            21            22            23            24            25 
#R>   1.926961905  -1.924060164  -2.332192509   6.761611458  -1.098766827 
#R>            26            27            28            29            30 
#R>  -1.786531239   0.051443296   5.066371218  -0.700048043   2.061643117 
#R>            31            32            33            34            35 
#R>   1.636212235   0.203412308   2.146815763   1.482438808   5.594008360 
#R>            36            37            38            39            40 
#R>   4.766090276   4.416206301   3.585626102   3.041052422   1.808739498 
#R>            41            42            43            44            45 
#R>   2.328849342   7.374988035   2.592301410   2.502001675   1.518950230 
#R>            46            47            48            49            50 
#R>   4.208817990  -1.674291872   0.314953821   1.521579501   1.224876287 
#R>            51            52            53            54            55 
#R>   1.789900964   3.268909269   7.683281289   0.862586590   1.359610474 
#R>            56            57            58            59            60 
#R>   0.876506653   1.812378566   4.891267597   2.574005580   2.170442638 
#R>            61            62            63            64            65 
#R>   2.433250965   6.180762181   3.175410466   5.714572301   1.141559234 
#R>            66            67            68            69            70 
#R>   2.148863580   3.847667596  -0.108844201   0.793941201   0.464531727 
#R>            71            72            73            74            75 
#R>   1.268391991  -1.320105773   1.162785014  -3.114586638   2.546296009 
#R>            76            77            78            79            80 
#R>   3.114519185  -1.088189874  -0.544408956   3.421204417   0.965702354 
#R>            81            82            83            84            85 
#R>   1.036025467  -1.766683501  -0.269656871   1.085381842  -0.717371424 
#R>            86            87            88            89            90 
#R>   4.739359175   4.210333249   6.423320917   2.931959137   4.083664313 
#R>            91            92            93            94            95 
#R>  -1.009014994   3.670613859   1.864021023   2.932264677   0.968450288 
#R>            96            97            98            99           100 
#R>   3.379243253  -1.311747192   0.909618942   3.644765490   1.480458060 
#R>           101           102           103           104           105 
#R>   0.786241057   4.610301832   3.481456253   5.867355358   3.717660098 
#R>           106           107           108           109           110 
#R>   2.647811766   1.571955548  -0.013714480  -1.319087109   0.326185130 
#R>           111           112           113           114           115 
#R>  -0.745767132   1.919246185   1.481473713   0.088346418   0.326458498 
#R>           116           117           118           119           120 
#R>  -1.251183139   0.701566409  -0.037828075  -1.076736684   2.063732518 
#R>           121           122           123           124           125 
#R>   1.699759572   3.837629504   1.979839895   2.015340678   2.718880217 
#R>           126           127           128           129           130 
#R>   0.459676833   3.706661884   4.861380975   1.704180858   3.810291244 
#R>           131           132           133           134           135 
#R>  -0.581059123  -0.059321817   0.132779733  -0.610787595   0.990006016 
#R>           136           137           138           139           140 
#R>   1.322512266  -2.253953437  -2.401230354   0.563946323  -0.657440122 
#R>             1             2             3             4             5 
#R>   7.351298400   5.858288748   4.368294201   3.331803926   3.315391384 
#R>             6             7             8             9            10 
#R>   4.852106207   0.938826427   3.033478679   5.379430653   7.169009680 
#R>            11            12            13            14            15 
#R>  20.654209539  10.034766994   4.840792369   2.390149280   3.696460004 
#R>            16            17            18            19            20 
#R>   5.631172841  13.200135547  -8.198439527   3.893639384   4.230473468 
#R>            21            22            23            24            25 
#R>   1.571717416   7.813655190   8.232138980   5.119457356  12.358985504 
#R>            26            27            28            29            30 
#R>  14.308597521   8.918594071  -0.303780288   4.045165957   4.763784708 
#R>            31            32            33            34            35 
#R>   0.306628121   5.620445577   3.547334007   3.995864358   3.054630679 
#R>            36            37            38            39            40 
#R>  -0.323646004   1.487298867   2.006723281   0.064699770   1.659326216 
#R>            41            42            43            44            45 
#R>   2.712574575   4.033052020   5.570643356   5.212570211  10.884663132 
#R>            46            47            48            49            50 
#R>  12.627167814  11.354478388  10.847722862   7.809354287   8.839733206 
#R>            51            52            53            54            55 
#R>   6.009437307   7.825525071   8.759853040  12.006928574  10.551716973 
#R>            56            57            58            59            60 
#R>   6.234474126  10.171685603   7.015395098  10.055754468  13.373447100 
#R>            61            62            63            64            65 
#R>   9.198500429   1.928102322   2.386708763   0.509450712   4.688431203 
#R>            66            67            68            69            70 
#R>   8.140942143   2.097625113   7.008001164   5.288836545   6.908826287 
#R>            71            72            73            74            75 
#R>  10.249867016  13.333764017   8.898363854  10.363091560   6.239011995 
#R>            76            77            78            79            80 
#R>  16.022032884   7.092980895  12.076125663   1.120645075   5.437500029 
#R>            81            82            83            84            85 
#R>   5.497426951  11.462733108   6.713387408   8.472254726  11.931175006 
#R>            86            87            88            89            90 
#R>   3.062015350   8.076328681   3.787638051   6.376072694   6.200031756 
#R>            91            92            93            94            95 
#R>   8.152912306   7.811353940   0.852107140  -0.063603045  -4.270582549 
#R>            96            97            98            99           100 
#R>  -1.397486588   1.961251867  -5.207038995   3.029752489   9.221607343 
#R>           101           102           103           104           105 
#R>   0.651513293   0.572933727   5.395987722   3.293534883   5.835387118 
#R>           106           107           108           109           110 
#R>   0.029054096  10.653706557   1.603785373   1.652079110  -0.057295647 
#R>           111           112           113           114           115 
#R>   3.660582807   2.120716675   4.047843022   5.475757448  -2.658205272 
#R>           116           117           118           119           120 
#R>   2.726776423   4.328272793   4.690184029   2.301304191   4.490779098 
#R>           121           122           123           124           125 
#R>   5.751659840   3.381391076   4.521402406   0.817986339   0.829352770 
#R>           126           127           128           129           130 
#R>   9.546747407  -0.058137056   6.729990769   1.902281829   0.841820758 
#R>           131           132           133           134           135 
#R>   0.634359695   2.775093719   3.882853517   3.461481150   2.193061759 
#R>           136           137           138           139           140 
#R>   7.831974302   2.061844506   2.106697755   1.577957586   3.119939405 
#R>             1             2             3             4             5 
#R>   1.416919972   9.850406020   4.470203950   3.149233743  -1.286126134 
#R>             6             7             8             9            10 
#R>   1.684935623  -0.758626798   0.588005656   4.553798196   7.239006547 
#R>            11            12            13            14            15 
#R>   3.887082629   9.034889431   6.714710404   3.232325584   4.920269207 
#R>            16            17            18            19            20 
#R>   4.662126176   4.343403304  -1.766033918   1.859239916   2.524001905 
#R>            21            22            23            24            25 
#R>   0.141562510   5.858354984  10.859674137   6.458982954  13.464996797 
#R>            26            27            28            29            30 
#R>  14.310291610  10.934500315  -1.398477872   2.472296140   5.146253698 
#R>            31            32            33            34            35 
#R>  -2.365517932   7.794615306   2.654192004   2.374743963   5.344762507 
#R>            36            37            38            39            40 
#R>   0.461055878   2.015494964   3.757742897   0.449712644   0.363870182 
#R>            41            42            43            44            45 
#R>   1.270116900   3.638126930   3.668374821   1.273352454  13.839699614 
#R>            46            47            48            49            50 
#R>  17.665255373  12.639514829  11.578516212   8.229633209   9.896710333 
#R>            51            52            53            54            55 
#R>   5.780549946   6.227346962  18.555570022  10.117734069   9.083866655 
#R>            56            57            58            59            60 
#R>   3.649646947  14.353480509  10.601891497  15.934874725  20.880649780 
#R>            61            62            63            64            65 
#R>  13.780899217   2.732306109   1.241734636  -0.887954501   2.843200298 
#R>            66            67            68            69            70 
#R>   6.384872080   0.515379155   3.174175197   0.381169566   5.163587962 
#R>            71            72            73            74            75 
#R>   7.219459888  12.875856293   7.103814605   7.977957052   4.972582525 
#R>            76            77            78            79            80 
#R>  21.059241026   7.432353961  10.264763531  -3.828422996  -0.127654996 
#R>            81            82            83            84            85 
#R>   3.034204777  14.112001824   5.553919225   8.516724903  19.487044645 
#R>            86            87            88            89            90 
#R>  -1.208501542   7.909242449   2.079885883   9.863093563   6.819827446 
#R>            91            92            93            94            95 
#R>  11.276647784  10.037863375   8.527967389   8.815635843  -1.206264246 
#R>            96            97            98            99           100 
#R>   2.455303479   5.286124603  -1.700158358   9.981906045  16.513187208 
#R>           101           102           103           104           105 
#R>   4.435221552  -2.085709039   6.149482644   3.961201995   9.305814762 
#R>           106           107           108           109           110 
#R>   6.438569087  19.447807163   5.562377500   4.226362881   1.763005593 
#R>           111           112           113           114           115 
#R>   6.437869056   5.766753721   8.415201150   9.645628091  -0.908018083 
#R>           116           117           118           119           120 
#R>   6.741348662   8.997714995   9.350005526   5.823187902   9.940667045 
#R>           121           122           123           124           125 
#R>  12.156531905   3.690020596   4.998779342   0.492641486  -1.141445747 
#R>           126           127           128           129           130 
#R>  11.284018579   0.233157595   8.728980128  -0.238273243  -1.772529627 
#R>           131           132           133           134           135 
#R>   1.765940615   6.408192262   8.354647775   7.030674588   6.854720419 
#R>           136           137           138           139           140 
#R>   5.875805703   6.593128092   6.146974111   6.391806154   7.168407807 
#R>             1             2             3             4             5 
#R>   2.718065903   3.066509919   0.772730616   0.358971497  -0.427982181 
#R>             6             7             8             9            10 
#R>  -0.662876232   1.890548983   0.618510280   0.479479988   1.691066427 
#R>            11            12            13            14            15 
#R>  -0.136099416   0.527457876   2.454312971   2.952953095   2.019130835 
#R>            16            17            18            19            20 
#R>   0.493310411   1.856539962  -1.249284066   0.311341313  -0.069623287 
#R>            21            22            23            24            25 
#R>   3.104635475  -0.118061955   3.239678091   3.160432453   3.017844874 
#R>            26            27            28            29            30 
#R>   1.808186445  -0.465817469   3.532116187   1.076138570   2.126488688 
#R>            31            32            33            34            35 
#R>   1.682726813   3.157606927   0.835542426   0.858206334   2.496240905 
#R>            36            37            38            39            40 
#R>   1.718464411   2.169453036   1.523360617   2.444022008   0.963816384 
#R>            41            42            43            44            45 
#R>   1.298291058   2.179062111   4.707916405   3.861689847   1.637163251 
#R>            46            47            48            49            50 
#R>   2.633217922   3.248925112   3.751149695   3.982579611   3.652386358 
#R>            51            52            53            54            55 
#R>   5.418426810   5.002374188   2.420768764   2.724468929   3.058289232 
#R>            56            57            58            59            60 
#R>   1.335933703   3.521447798   3.285869386   5.454956048   5.891972297 
#R>            61            62            63            64            65 
#R>   6.804826753   4.894857316   4.672557294   5.028039341   3.156362066 
#R>            66            67            68            69            70 
#R>   2.121022053   4.078862668   1.842370288   1.973644432   5.080429763 
#R>            71            72            73            74            75 
#R>   5.021915054   4.676847563   3.003473160   2.357406570   3.323882744 
#R>            76            77            78            79            80 
#R>  -0.164226024   3.420960309   3.320779301   4.295962092   2.665613121 
#R>            81            82            83            84            85 
#R>   4.513679097   5.899682845   2.290772071   3.219819047   6.613381275 
#R>            86            87            88            89            90 
#R>   3.741884045   3.318385280   4.691005039   4.391147053   4.034219217 
#R>            91            92            93            94            95 
#R>   3.027464962  -0.510172907   2.914902822   1.164898095   1.985992823 
#R>            96            97            98            99           100 
#R>   2.737947459   0.506625254   1.618253501   4.967252702   3.110161469 
#R>           101           102           103           104           105 
#R>   0.802498647   4.283056512   3.457954060   1.996872382   2.221427666 
#R>           106           107           108           109           110 
#R>   3.320145994  -0.614353371   1.049083509   0.945706946   2.095804056 
#R>           111           112           113           114           115 
#R>   1.344439729   1.794997544   1.576459974   4.064159585   2.849879797 
#R>           116           117           118           119           120 
#R>   1.641304564   2.490731117   2.055181734   2.421121485   0.921089086 
#R>           121           122           123           124           125 
#R>   2.474334245   0.600013949   1.404458028   1.449892244   1.563338911 
#R>           126           127           128           129           130 
#R>   3.587170452   2.604974181   2.206699257   0.547805353   0.999441581 
#R>           131           132           133           134           135 
#R>   1.241123415   1.576072419   2.134214702   1.241106003   1.310669546 
#R>           136           137           138           139           140 
#R>   2.332998104   2.612112508   1.639718632   2.829670971   2.364573898
```

Desciption of the solution for RMSE's:

Since the test.data has the same structure as the train.data but does not contain the frequencies for each of the 7 plants, our goal is precisely to estimate them for the 140 observations.

Within this solution, the lowest test sample RMSE is the preferred model. It produces the best `model fit`.

In this case, the best fit is therefore Model a7.

<!--chapter:end:33-Solution_Final_Task.Rmd-->

# (PART) Conclusion {-}


# Conclusion {#conclusion}

This brings us to the end of our book. It is built in the form of a tutorial and contains a variety of hints regarding the use of R in general and the use of R for data science or data analysis.

As mentioned before, the book itself is part of a university project in `Data Science` at Hochschule Fresenius in Cologne. The course itself was designed or intended to learn about the language R and how R can be used for `Data Science`. Please keep in mind that the entire project is a work-in-progress document and that it might contain "simple" errors, due to the fact that this is the first time we are working with R and data science. Since we are "first-time learners" of R and data science, we intended to pass on our knowledge and give the reader a basic understanding of R and how to make use of helpful and life-simplifying tools (e.g. for data science).

It was important for  us to get you started with R and data science, as well as all related machine learning and artificial intelligence tools. 

In our examples, we tried to give a simple understanding of the issue, as well as basic examples (and some advanced examples) for working with and presenting complex models. Our objective was and still is to demonstrate how R can be used to "read" data and convert it into data scientific output. Furthermore, we want to demonstrate how "easy" it can be to use R as a language for data science. When it comes to machine learning, we demonstrated the possible use of a variety of packages that support the use of machine learning with R. 

In case of any ambiguities, the authors are happy to support you and will try to give you valuable advice. 


<!--chapter:end:34-conclusion.Rmd-->



<!--chapter:end:35-references.Rmd-->

