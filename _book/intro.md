# Introduction {#intro}

The first part of this text is designed to help get you oriented to coursework in computational social science. Both [Introduction to Geographic Information Science (SOC 4650/5650)](https://slu-soc5650.github.io) and [Quantitative Analysis: Applied Inferential Statistics (SOC 4930/5050)](https://slu-soc5050.github.io) are focused on building students' capacities to address social science research questions using tools that have been the traditional domain of computer and information scientists. The growth and application of these tools in a variety of disciplines both inside and outside of the social sciences has come to be known as data science. Both courses are taught from this perspective, so that while we focus on social science data, the tools and techniques are broadly applicable across disciplines. 

## What is data science?

Given data science's new emergence, its definition remains both contested and often unclear. For me, there are four key aspects to focus on when considering what constitutes data science:

1. Statistics
2. Programming
3. Visualization and Communication
4. Substantive Knowledge

I think of this as a "full stack" approach to computational research. You want to be well versed not only the techniques for generating and analyzing data, but also substantively in the academic literature about your area of interest as well as ways to communicate your findings with other researchers and the wider public.

### Statistics
Statistics covers the mathematical techniques that we use to draw inference from our data. It is the main subject of one my courses, [Quantitative Analysis](https://slu-soc5050.github.io). In [Introduction to GIS](https://slu-soc5650.github.io), we do not explicitly cover much in the way of inferential statistics. However, the course is desinged to prepare you for a next level, Intermediate GIS course that covers spatial statistics. 

### Programming
Computer programming is an essential part of data science broadly and computational social science more specifically. Using a programming language means that our work can be easily reproduced. This emphasis on **reproducibility** is a response to a growing fear in many disciplines that results are replicable from study to study, which raises questions about the validity of much of the research work that we do. Our goal in both courses is to produce research that is as reproducible as possible.

This book introduces two programming languages - [`R`](https://en.wikipedia.org/wiki/R_(programming_language)) and [Python](https://en.wikipedia.org/wiki/Python_(programming_language)). In [Quantitative Analysis](https://slu-soc5050.github.io), we will be focused exclusively on learning `R` and using it to produce statistical analyses. In [Introduction to GIS](https://slu-soc5650.github.io), we will spend a lot of time in `R`, but we will also use some Python to help pass data from `R` to ArcGIS, the mapping application we will use. I will also provide some additional Python lessons to folks who are interested, but these will not be required for the course.

### Visualization & Communication
Visualization is a fundamental aspect of data science work. It is how we make our results easily digestible and accessible to a wider audience, many of whom may not be able to interpret statistical output but can learn from a well-designed scatter plot. In [Quantitative Analysis](https://slu-soc5050.github.io), we will focus on building plots to communicate information about statistical distributions and the relationships between our variables. In [Introduction to GIS](https://slu-soc5650.github.io), we will use the same fundamental skills to build simple maps in `R`. We will extend our emphasis on visualization to ArcGIS, where we will focus on producing cartographically rich depictions of our data.

Separetely, we will discuss the presentation of statistical data in tables using [LaTex](https://en.wikipedia.org/wiki/LaTeX) in [Quantitative Analysis](https://slu-soc5050.github.io) as well as the producing to conference-style presentations to communicate research findings. In [Introduction to GIS](https://slu-soc5650.github.io), we will focus on producing conference-style posters instead. These are different mediums, but they rely on the same design fundamentals that are covered in this text.

### Substantive Knowledge
Substantive knowledge covers two tangentially related topics: the ability to work well in groups and the ability to digest and integrate an academic literature into your own research. Each of these topics receive some focus in both [Quantitative Analysis](https://slu-soc5050.github.io) and [Introduction to GIS](https://slu-soc5650.github.io). Each class has some group work associated with the completion with weekly lab assignments. [Introduction to GIS](https://slu-soc5650.github.io) also has a group work component associated with the final project. In each class, students' final projects are focused on a specific content area that requires at least some background research and knowledge. Synthesizing this knowledge and integrating it into your final projects is a key piece of addressing this facet of data science.

## How is this book organized?

Like many books about data science, this text follows a number of standard conventions related to how it is organized and how examples are given. This section introduces those conventions.

### Typefaces and Fonts
Technical publications that describe scientific computing processes use a `monospaced typewriter style typeface` to refer to commands (inputs) and results (outputs). In some documents, like lecture slides and cheat-sheets, I may highlight a command by using a particular color to increase the visibility of the command name itself.

The `typewriter typeface` is also used to refer to functions (e.g. `library()`), filenames (e.g. `mpg.csv`) or filepaths (e.g. `C:\Users\JSmith\Desktop`). Finally, we will use the `typewriter typeface` to refer to GitHub repositories (e.g. `Core-Documents`, the repository that contains this file).

Technical publications use *italicized text* to refer to text that is meant to be replaced. These references will typically appear in a `typewriter typeface` since they are often part of commands. For example, `str(dataFrame)` (with `dataFrame` *italicized*) indicates that you should replace the text `dataFrame` with the appropriate variable name from your dataset.

These publications also use a sans serif typeface to refer to areas of the user interface, menu items, and buttons. I cannot replicate that here because of the publishing software that I use, but you'll notice this text in course documents. We will therefore use the `typewriter typeface` in the User Guide to identify these same features.

Technical documents also use a sans serif or `typewriter` typeface to refer to keyboard keys (e.g. `Crtl+C`) where the plus sign (`+`) indicates that you should press multiple keys at the same time. A sans serif typeface combined with a right facing triangle-style arrow (`>`) is used to refer to actions that require clicking through a hierarchy of menus or windows (e.g. `File > Save`).

### Data
There are two sets of data that are used in this text, and they are also used as part of [Quantitative Analysis](https://slu-soc5050.github.io) and [Introduction to GIS](https://slu-soc5650.github.io). Both are available as `R` packages. The `testDriveR` package contains some generic data that are particularly well suited for exploring statistical topics. The `stlData` package contains data that can be mapped at various levels. Both of these packages are currently available on [GitHub](https://github.com), and can be installed using the `devtools` package:

```r
install.packages("devtools")
library(devtools)
devtools::install_github("chris-prener/testDriveR")
devtools::install_github("chris-prener/stlData")
```

### Examples
Throughout the semester, I will give you examples both in lecture slides and in an example do-file. Examples in lectures and course documents can be easily identified by their use of the `typewriter typeface`:

```r
> library(stlData)
> str(stlLead)
'data.frame':	106 obs. of  15 variables:
 $ geoID         : num  2.95e+10 2.95e+10 2.95e+10 2.95e+10 2.95e+10 ...
 $ tractCE       : int  118100 117400 126700 119102 126800 126900 108100 127000 127400 103700 ...
 $ nameLSAD      : chr  "Census Tract 1181" "Census Tract 1174" "Census Tract 1267" "Census Tract 1191.02" ...
 $ countTested   : int  345 871 458 182 486 1296 903 585 2116 417 ...
 $ pctElevated   : num  9.57 12.06 18.12 2.2 4.73 ...
 $ totalPop      : int  1161 4307 1089 3237 3490 4590 3144 2052 5486 2408 ...
 $ totalPop_MOE  : int  192 447 199 309 231 826 464 273 516 274 ...
 $ white         : int  414 2604 432 2008 3026 148 108 304 1777 2149 ...
 $ white_MOE     : int  100 303 116 262 270 217 111 82 391 212 ...
 $ black         : int  724 1338 631 646 194 4320 3020 1739 3603 156 ...
 $ black_MOE     : int  179 374 187 210 98 760 442 283 621 190 ...
 $ povertyTot    : int  324 615 506 958 349 1743 652 331 2524 254 ...
 $ povertyTot_MOE: int  140 255 164 234 129 825 305 156 598 88 ...
 $ povertyU18    : int  109 169 98 15 35 627 256 47 1110 15 ...
 $ povertyU18_MOE: int  105 156 60 25 47 595 136 79 318 23 ...
```

Examples will almost always use the dataframe `stlLead`, which comes with the `stlData` package. To open it, simply load the `stlData` package using the `library()` function and then start referencing `stlLead` anytime you need a dataframe. This allows you to easily recreate examples by minimizing dependencies within your code.
