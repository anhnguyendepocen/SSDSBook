# Protecting Your Work
I believe that one of the biggest challenges to with doing computational work is that it requires a high degree of organization. Prior to one of my courses, students' approaches to file management on their computers are often haphazard. I am very used to seeing students' desktops or documents directories in various states of disarray. Perhaps that has worked for them in the past, but that approach (or lack thereof) **will** fail students in [Introduction to Geographic Information Science (SOC 4650/5650)](https://slu-soc5650.github.io) and [Quantitative Analysis: Applied Inferential Statistics (SOC 4930/5050)](https://slu-soc5050.github.io). Moreover, if left un-checked, it will fail students down the road when a hard drive failure or natural disaster renders their data irrevocably inaccessible. This chapter covers what some of those threats are and ways to manage those risks when conducting computational research. 

## Threats To Our Data

Each semester that I teach [Introduction to GIS](https://slu-soc5650.github.io) and [Quantitative Analysis](https://slu-soc5050.github.io), several things happen. The first thing that happens is that students regularly lose files. The effects of losing files can range from being a minor frustration to a major headache depending on the file in question. Losing files often results in downloading multiple copies of the same data and recreating work. Both of these are wastes of your time. Moreover, files are rarely gone. They are typically just misplaced. This is bad for reproducibility, particularly when you happen across multiple versions of the same file and have to sort out which version is the version you last worked on.

The second thing that happens is that students who use thumb drives for data storage lose them. Depending on the timing of this loss, this can again range from being a minor frustration (very early in the semester) to being downright anxiety attack producing (last few weeks of the semester). Recreating an entire semester’s worth of work on the final project is both a tremendous waste of your time and a particularly unpleasant experience.

Fortunately, I have never had a student’s computer hard drive die during the course of the semester. However, I assume that if I teach this course long enough a hard drive failure will indeed occur. The backup provider [Backblaze](https://www.backblaze.com/) has [analyzed](https://www.backblaze.com/blog/how-long-do-disk-drives-last/) their own hard drives and found that about 5% of drives fail within the first year. After four years, a quarter (25%) of drives in their data center fail.

Similarly, it is only a matter of time before a student’s computer is stolen along with all of their hard work. A less likely though still very plausible scenario involves the destruction of a student’s belongings (computer and thumb drive included) in a fire, car accident, or natural disaster.

Despite the likelihood that you will at some-point lose a thumb drive (if not during this semester than sometime down the road) and the near certainty that your computer’s hard drive will eventually fail if a rogue wave does not get it first, few students and faculty take these risks seriously. While you cannot prevent many of these things from happening, I want to suggest to you that you can take some simple steps to sure that *when* (not if) they happen, you are well prepared to get back to work with minimal disruption.

## Data Management
One of the themes in ["Good Enough Practices in Scientific Computing"](https://arxiv.org/abs/1609.00037), referenced in the previous chapter, is an emphasis on data management. One of their core messages is to ``save the raw data''. Particularly in GISc work, the raw data can be expansive - dozens of shapefiles, tabular files, and associated metadata. These files often come from disparate sources - city open data sites, the U.S. Census Bureau, state data repositories, and other federal agencies. Moreover, GIS data are often updated over time to reflect on-the-ground changes. Saving the raw data in GISc work therefore means not only creating a well-organized directory containing *all* of your original data. It also means logging the source of each file, when it was downloaded, and (if applicable) a permanent web link to your data source. For that reason, we'll give you not just the course data but a read me file and a metadictionary that lists all of the files we've disseminated to you.

A second message in the paper is to "create the data you wish to see in the world". The authors encourage readers to "create the dataset you wish you had received." First and foremost, this means using open and not proprietary data formats. For spatial data, [ESRI shapefiles](https://en.wikipedia.org/wiki/Shapefile) are technically proprietary, though their standard is open. This means that other software applications, like `R` and QGIS can read and in some cases write shapefiles. For sharing spatial data, a better option is the [GeoJSON](https://en.wikipedia.org/wiki/GeoJSON), which is a plain text file format.

Tabular data are best stored as `CSV` files, which is also a plain text file format that can be opened by a wide variety of applications. In contrast, common file formats like Microsoft Excels's `XLS` and `XLSX` are proprietary file packages that cannot be read as plain text and are therefore less desirable for storing data.

## Creating a Sustainable File System
In his excellent document [*The Plain Person’s Guide to Plain Text Social Science*](http://plain-text.co), Kieran Healy describes two important revolutions in computing that are currently taking place. One of them is the advent of mobile touch-screen devices, which he notes

> hide from the user both the workings of the operating system and (especially) the structure of the file system where items are stored and moved around.

For most users, I would argue that this extends to their laptop or desktop computers as well. I would venture to guess that the majority of my students are used to keeping large numbers of files on their desktops or in an (distressingly) disorganized `Documents` folder. For research, particularly quantitative research, such an approach to file management is unsustainable. It is difficult to produce *any* research, let alone work that is reproducible, without an active and mindful approach to file management.

### Create a *Single* Course Directory
The most successful approach to organizing files is to identify *one and only one* area that you will store course files in. Having files scattered around you hard drive between you `Desktop` directory, `Downloads`, `Documents`, and a half dozen other places is a recipe for lost files. It can also add complexity to the task of backing these files up. I recommend naming this directory simply based on the course you are enrolled in:

* `SOC4650`
* `SOC4930`
* `SOC5050`
* `SOC5650`

These names are short, have no punctuation or spaces (which can create conflicts with software), and explicitly connects the directory to this course as opposed to other courses you may take that are also statistics or GIS courses (a good reason to avoid naming the directory `Stats` or `GIS`!).

This single course directory should reside in *one and only one* place. Storing it inside a sync'd directory (like Dropbox or Google Drive) may cause conflicts with your Git repositories. I strongly recommend storing your course directory on the computer that you will regularly do work on for the course. For some students, that will be the desktop computer in our lab. For others, it will their laptop computer. If you find yourself having to regularly switch between computers, I'll provide some suggestions later in this chapter.

### Approach Organizing Systematically
Within your single course directory, I recommend following a mindful, purposeful approach to organization. This approach begins with having a number of dedicated subfolders within your course directory:

```
/SOC5650
  /Core-Documents
  /Data
  /DoeAssignments
  /FinalProject
  /Labs
  /Lectures
  /Notes
  /ProblemSets
  /Readings
  /WeeklyPreps
  /WeeklyRepos
```

Note again how these directories are named - there are no spaces, special characters, and the names are deliberately short but specific. For a directory with two words (`FinalProject` or `ProblemSets`), I use what is known as camelCase to name the file where the second (any any subsequent) words have their first character capitalized. You could also use dash-case (`Core-Documents`) or snake_case (`Core_Documents`) as a naming strategy. Regardless of which of these approaches you take, try to use it consistently.

Once you have these folders set-up, I want you to an agreement with yourself: files for the course will *only* be saved within this structure. Do not temporarily save files to the `Desktop`, for example, intending to move them later. They will be forgotten.

### The `Core-Documents` Directory
This directory has already been created and will be added to your file system during **Week 03**, when it is **cloned** from GitHub. 

\begin{rmdnote}
A cloned directory is one that retains a digital link to the data stored
on GitHub, meaning that it can be easily updated if changes are made.
This will be explained in greater depth in Introduction to GitHub
chapter in this text.
\end{rmdnote}

\begin{rmdwarning}
You will not be able to push changes that you make in this directory to
GitHub, and making other changes could cause conflicts. I suggest not
making changes inside this repository beyond opening files for reference
purposes.
\end{rmdwarning}

The `Core-Documents` directory is used for storing the course syllabus, reading list, and a sample schedule for 3600 Morrissey Hall for the semester.

### The `Data` Directory

\begin{rmdwarning}
This directory is only applicable to students in
\href{https://slu-soc5650.github.io}{Introduction to GIS}, who will
receive a data release at the beginning of the semester that should be
saved here. Students in
\href{https://slu-soc5050.github.io}{Quantitative Analysis} will receive
most data through \texttt{R} packages and may reiceve a small amount of
data through weekly repositories.
\end{rmdwarning}

The data directory should have copies of any original data and their documentation that are not disseminated to you as `R` packages. Most of these data are included in the initial data release, but you will have to add some additional data to this directory over the course of the semester. The data in this directory should be used as needed but not altered (one of the of the "good enough" research practices from the previous chapter).

### The `DoeAssignments` Directory
Like the `Core-Documents` repository, this will not be included in the course data release. You will add it to your file system during **Lab-03**. It will also have a different name - your last name instead of 'Doe'. Once you add it, it will contain a number of subdirectories:

```
  /SOC5650
    /DoeAssignments
      /FinalProject
        /Documentation
        /Memo
        /PaperDraft
        /PaperFinal
        /PosterDraft
        /PosterFinal

      /Labs
        /Lab-01
        ...
        /Lab-16

      /ProblemSets
        /PS-01
        ...
        /PS-10
      
      /WeeklyPrep
        /WP-02
        ...
        /WP-16
```

The `FinalProject` directory contains submission folders for each component of the final project. If you a registered for SOC 4650, your directory will look like what appears above. Students registered for SOC 5650 will have three additional subfolders for deliverables related to the final paper element of the course.

The `Labs`, `ProblemSets`, `WeeklyPrep` directories have subfolders dedicated to the individual assignments you'll have to submit over the course of the semester. **These directories are intended to store only the deliverables that are requested in each assignment's directions.** All other files related to each assignment should be stored elsewhere in your folder structure.

\begin{rmdwarning}
Unlike \texttt{Core-Documents}, you have the ability to push changes
made here to GitHub.com. Please make sure you understand that changes
made will be reflected, for better or worse, on the website the next
time you complete that push.
\end{rmdwarning}

### The `FinalProject` Directory
The final project directory should be a microcosm of the larger directory structure, with most major directories replicated so that your final project files have a dedicated, organized home:

```
  /SOC5650
    /FinalProject
      /AnnotatedBib
      /Data
      /DataAnalysis
      /Documentation
      /Memo
      /Notes
      /Paper
      /Poster
      /Readings
```
You'll notice that there are a number of new directories dedicated to specific aspects of the project.

\begin{rmdnote}
You will want to tailor this subdirectory's contents to match the
specific requirements of the section you are enrolled in. This may
entail removing certain folders - the \texttt{AnnotatedBib/} for example
- that do not correspond to deliverables you have to complete.
\end{rmdnote}

### The `Labs`, `ProblemSets`, and `WeeklyPreps` Directories
This directory contains subfolders for each of the sixteen lab assignments for this course. Save *all* of the associated materials for each lab assignment here. 

```
  /SOC5650
    /Labs
      /Lab-01
      ...
      /Lab-16
      
    /ProblemSets
      /PS-01
      ...
      /PS-10
      
    /WeeklyPreps
      /Week-01
      ...
      /Week-16
```

These directories differ from what you save in your `DoeAssignments` repository. Unlike `DoeAssignments`, which is **only** for submission files, these directories can contain any number of files you wish. Use each of these assignment folders as a place to work and experiment, and the folders under `DoeAssignments` as the place to submit your final versions.

Each of these assignments that utilizes `R` and RStudio should have an R Project associated with it:

```
  /SOC5650
    /Labs
      /Lab-01
        Lab-01.Rproj
        
      /Lab-02
        Lab-02.Rproj
        
      /Lab-03
        Lab-03.Rproj
```

Using R Projects will help you keep your work organized by ensuring that the working directory for RStudio is correctly set every time and that output is always saved to the appropriate assignment directory.

### The `Lectures` Directory
This directory should contain subfolders for each of the sixteen weeks of the course. When we create new files during lectures, save these documents in the appropriate week's folder.

```
  /SOC5650
    /Lectures
      /Week-01
      ...
      /Week-16
```

### The `Notes` Directory
Use this as a home for course notes if you decide to take notes digitally and do not already use notebook software of some kind that organizes notes for you.

### The `Readings` Directory
Use this as a home for `.pdf` copies of course readings. I suggest creating subdirectories *only* for weeks that have readings assigned from outside of the main texts, such as Week 01:

```
  /SOC5650
    /Readings
      /Week-01
```

### The `WeeklyRepos` Directory
Clone each of the weekly repos to this directory, and sync them when updates are made to ensure you have the latest versions of files. By the end of the course, this directory should have sixteen subfolders like this:

```
  /SOC5650
    /WeeklyRepos
      /Week-01
      ...
      /Week-16
```

\begin{rmdwarning}
You will not be able to push changes that you make in these directories
to GitHub, and making other changes could cause conflicts. I suggest not
making changes inside this repository beyond opening files for reference
purposes. If there is something you need to edit, copy it to the
appropriate subdirectory (\texttt{Labs}, \texttt{WeeklyPreps}, etc.) and
make local changes there.
\end{rmdwarning}

## Backing Up Your Data
There are a number of different ways to think about backing up your data. The most successful backup strategies will incorporate all of these elements.

### Bootable Backups
“Bootable” backups are mirrored images of your *entire* hard drive, down to temporary files, icons, and system files. With a bootable backup, you can restore your entire computer in the event of a hard drive failure or a corruption of the operating system files. They are named as such because you can plug in the external drive that you are using for this backup and literally boot your computer up from that drive (typically a *very* slow process).

These backups are often made less frequently because they can be resource intensive and it is best not to use your operating system while creating a clone. They are typically made to an external hard drive, which is subject to similar failure rates as the hard drives inside your computer. So bootable drives need to be replaced every few years to maintain their reliability.

Both major operating systems come with applications for creating clones of your main hard drive that are bootable, and there are a number of third party applications that provide this service as well.

### Incremental Backups
Incremental backups are designed to keep multiple copies of a single file (how often depends on the type of software you use and the settings you select). These can be used to restore an older copy of a file if work is lost or a newer file is corrupted.

Apple’s TimeMachine is a great example of an incremental backup - when kept on, it creates hourly backups of files that have been changed, daily backups for the previous month, and weekly backups for previous months. Once the disk is full, the oldest backups are deleted. Dropbox also provides a similar service, retaining all previous versions of files (and deleted files) for thirty days.

Incremental backups are typically good options for recovering files that have been recently changed (again, depending on the software you use and the settings you select). Since they run frequently (every time a file is changed or every hour, for example), recent changes tend to get captured. They can be limited in terms of their long-term storage - it may not be possible to recover older versions of a file past a few weeks.

They are also not always good solutions for recreating your entire computer since they do not save all necessary program and operating system files, and may be cumbersome to work with if you need to recover a large quantity of files. Like bootable backups, these are typically stored on external hard drives that need to be replaced on a regular basis.

In addition to the aforementioned Apple TimeMachine, the Windows OS also comes with a built-in service for creating incremental backups. Dropbox is a good option if you have a small number of files, but you may find the need to upgrade to a paid account if you have a large amount of data.

### Cloud Backups
Cloud backup services like [Backblaze](https://www.backblaze.com) or [Crashplan](https://www.code42.com/crashplan/) offer comprehensive backup solutions for customers. These plans typically require a monthly subscription fee to maintain access to your backups. While bootable backups protect against hard drive failure and incremental backups protect against data corruption, cloud backups protect against catastrophic events like robberies, fires, and other natural disasters. A fire or a tornado that affect your house may destroy your laptop and any external hard drives you use for backup, but your cloud backup will be unaffected.

### A Workflow for Backups
Just as we need a workflow for approaching file management, it is also important to establish a routine for backups. With backups, the most successful workflows are those that require next to no effort on your part. If you primarily use a desktop, this can be as simple as leaving two external hard drives plugged into your computer since most backup software can be set to run automatically. If you have tasks that require you to manually do something (plug an external hard drive into your computer, for instance), create a reminder for yourself on a paper calendar or a digital calendar or to-do list application.

\begin{rmdtip}
I gave a presentation on workflows for backing data up as part of the
\href{https://slu-dss.github.io}{Data Science Seminar} series at
\href{https://slu.edu}{Saint Louis University}. You can easily view the
slides from that presentation on
\href{https://speakerdeck.com/chrisprener/protecting-your-data}{Speaker
Deck}, and you can download the session's materials from
\href{https://github.com/slu-dss/protectData}{GitHub}.
\end{rmdtip}

For this course in particular, it is *imperative* that you backup the data on your flash drive. A number of possibilities exist for accomplishing this:

  - Keep a local copy of your flash drive's files on your computer.
  - Keep a `.zip` archive of your files in a service like Dropbox or Google Drive. (Using a `.zip` archive will prevent issues with your `.git` repositories.)
  - Maintain a second flash drive copies of all of your files.

Whatever solution you select, make sure you regularly update your backup. The more often you keep your backup archive updated, the less stressful and disruptive losing your drive will be. This will likely be a manual task, so follow the guidance above about creating a repeating calendar event or to-do list task reminder.

## Managing Multiple Devices
If you are trying to manage your work across multiple computers, the task of staying organized becomes more difficult. One option is to use a thumb drive or external hard drive as the primary site where your course directory lives. That way you can save everything there and it is accessible by as many computers as necessary. If you decide go this route, it is **imperative** that you back-up your work to a computer or to another external drive.

\begin{rmdtip}
macOS users should make sure that the external drive is formatted using
the ExFat file system specification so that it is readable both by their
operating system and the Windows operating system in the computer lab.
If you buy a new drive, you will likely have to re-format it.
\end{rmdtip}

Another option is to utilize GitHub extensively. You can create repos for the some of the key subdirectories referenced above, like `ProblemSets`, `WeeklyPreps`, and others, and keep you work synced between computers using the same process we use for submitting work. If you want to do this, make sure you get the [student GitHub discount](https://education.github.com/discount_requests/new), which will give you unlimited private repositories. That way, your course work will not be public facing. If you pursue this strategy, make sure you still have only one place for a specific file typoe - you do not want some problem set materials saved outside of your GitHub repo and some saved in it. 
