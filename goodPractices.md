# "Good Enough" Research Practices

This section introduces some of the core concepts that we will emphasize in this course throughout the semester. The title takes inspiration from a recent article titled ["Good Enough Practices in Scientific Computing"](https://arxiv.org/abs/1609.00037)^[Wilson, G., Bryan, J., Cranston, K., Kitzes, J., Nederbragt, L. and Teal, T.K., 2016. Good Enough Practices in Scientific Computing. *arXiv preprint arXiv:1609.00037.*]. The authors note in their introduction that scientific computing advice can sometimes be both overwhelming and focused on tools that are inaccessible to many analysts. Their goal, and the goal of this course, is to de-mystify the simplist tools that enable researchers to streamline their workflows:

> Our intended audience is researchers who are working alone or with a handful of collaborators on projects lasting a few days to a few months, and who are ready to move beyond emailing themselves a spreadsheet named `results-updated-3-revised.xlsx` at the end of the workday...Many of our recommendations are for the benefit of the collaborator every researcher cares about most: their future self.

I would argue that the skills they describe are useful beyond just a few months. Indeed, most of the skills here can dramatically improve students' dissertation experiences:

> Most importantly, these practices make researchers more productive individually by enabling them to get more done in less time and with less pain. They also accelerate research as a whole by making computational work (which increasingly means all work) more reproducible. But progress will not happen by itself. Universities and funding agencies need to support training for researchers in the use of these tools. Such investment will improve confidence in the results of computational work and allow us to make more rapid progress on important research questions.

While much of what we will talk about in this course is aimed at supporting your work, there are benefits that extend beyond your dissertation or your research projects. These benefits, which include developing sustainable workflows and structuring the way you interact with your own computer, can make everyday computing practices like checking email or organizing files an easier, more structured process.

## Reproducibility

One of the mantras of this course is our emphasis on reproducibility. The unifying feature of all of the "good enough" research practices discussed below is that they contribute to a more reproducible research product.

Reproducibility is very much in vogue right now for number of reasons. [Assessments of studies in psychology](http://science.sciencemag.org/content/349/6251/aac4716)^[Open Science Collaboration, 2015. Estimating the reproducibility of psychological science. *Science*, 349(6251), p.aac4716.], for example, have found weaker on average effect sizes and far fewer statistically significant results than the initial studies reported. There have also been high profile instances of falsified research, including [research by a graduate student at UCLA](http://nymag.com/scienceofus/2015/05/how-a-grad-student-uncovered-a-huge-fraud.html). This particular instance of fraud was identified by graduate students intent on replicating the original study.

At the same time, there is a recognition that the skills necessary for producing reproducible research are not being fostered in academic disciplines and graduate programs. Thus one of the goals of this course, and this **User's Guide** in particular, is to help develop a working knowledge of many of these skills.

One challenge, however, is that reproducibility does not have a consistent definition. Some researchers use the term to narrowly refer to code that can execute without alteration on a person's computer. Others use it to refer to research designs that can be replicated by other researchers. Still others discuss reproducibility as the ability to obtain a similar set of results or draw similar inferences from identical research designs.

When we talk about reproducibility in this class. We'll be primarily concerned with **methods reproducibility**:

> the ability to implement, as exactly as possible, the experimental and computational procedures, with the same data and tools, to obtain the same results.^[Goodman, S.N., Fanelli, D. and Ioannidis, J.P., 2016. What does research reproducibility mean?. *Science translational medicine*, 8(341), pp.341ps12-341ps12.]

Methods reproducibility in statistics means that other analysts have full access to both the original data and the steps used to render those original data into a final research product, such as a set of regression models This is increasingly seen not just a matter of good research methodology, but as a matter of research ethics as well. Being able to be transparent with research decreases the potential for cases like the [fraudulent dissertation research conducted by a UCLA graduate student named Michael LaCour](http://nymag.com/scienceofus/2015/05/how-a-grad-student-uncovered-a-huge-fraud.html). It was the efforts of [two Stanford graduate students who wanted to reproduce LaCour's findings](https://fivethirtyeight.com/features/how-two-grad-students-uncovered-michael-lacour-fraud-and-a-way-to-change-opinions-on-transgender-rights/) that ultimately led to the identification of problematic work.

For statistics, methods reproducibility is derived from a number of sources. The first source is the use of **computer code** for working with data. Rather than making manual changes to tabular data in a spreadsheet application like Microsoft Excel, computer code provides detailed records of each individual alterations. Code can be used execute tasks repeatedly, meaning that errors can be easily fixed if they are discovered an hour, a day, a week, or a month later. During this semester, we'll use `R`'s programming language to execute reproducible data cleaning processes.

The second source of reproducibility in statistics is therefore derived from the **documentation** that we create to accompany our research products. These documents outline where our data originated, what specific variables mean (a codebook), what steps were taken to create specific maps (a research log), and how our data files are organized (a metadictionary).

Our code can also be used as documentation if it is written using [literate programming](https://en.wikipedia.org/wiki/Literate_programming) techniques. In `R`, these techniques produce well annotated output that "weaves" together code, output, and narrative text that describes the function of the code and the results of the output.

The third and final primary source of reproducibility in statistics is derived from our **organizational approach** to our work. Statistics projects can require many megabyes of data spread across dozens of data files, scripts, and output files. A disorganized file system can make replicating your work difficult if not impossible. Much of the research practices discussed in the remainder of this section are aimed at supporting one or more of these three major sources of reproducibility.

## Thinking in Workflows

One way to increase the reproducibility of a project is to approach each and every task with purposeful organization and thoughtfulness. **Workflows** are the processes that we use to approach a given task. Think of checking your email. You (hopefully!) follow a series of steps when you check your email that help you organize your inbox. In our reading for the first week of classes, [Scott Long](http://www.indiana.edu/~jslsoc/)^[Long, J.S., 2009. *The workflow of data analysis using Stata.* College Station, TX: Stata Press.] describes a structured strategy for approaching statistical research. In Long's model, a data analysis project consists of four steps: (a) data cleaning, (b) analysis, (c) presenting results, and (d) protecting files. This is a useful model to build upon, and one that we will discuss over the course of the semester.

Even more useful, not just for statistical work but for any process, are the tasks Long lays out for each step in the data analysis workflow:

  1. Planning
  2. Organization
  3. Documentation
  4. Execution

A good example of the utility of extending this logic to other workflows is with the problem sets. The "typical" approach students take with homework assignments is to sit down, open up their software, and start with question 1. Using Long's four task approach, a workflow-based strategy to the assignment would involve beginning by reading the assignment through in its entirety to develop a **plan** for approaching it - think about what techniques and skills are needed for each step. With a plan in place, you can proceed to **organizing** yourself for the assignment - identifying and obtaining files that you will need, creating dedicated directories for saving assignment data, and getting any necessary software documentation. After pulling together all of these materials, you are ready to move on to **documentation** - setting up your assignment code and output files, and (later in the course) your research log and meta-dictionary. Once you are set-up, you would then begin to address individual assignment questions as part of the **execution** task.

The goal here is to approach everything you do for research or work with an element of mindfulness and structure about your process. This mental model for approaching research supports the creation of **reproducible** research products because we approach our work in a routinized, predictable, organized, and efficient manner. Thinking in terms of workflows also encourages a greater awareness of the complexity of tasks, which also helps you plan more accurately for how long a particular task or project will take.

In reality, there will be multiple workflows that you find yourself navigating. You will want a structured process not just for approaching a large research project like the final project, but also a process for maintaining notes related to a specific assignment, a process for documenting code, a process for approaching assignments, and even a process for backing your data up. As you go through the course, think about how to best integrate these ideas into your work habits.
