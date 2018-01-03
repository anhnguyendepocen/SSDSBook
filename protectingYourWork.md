# Protecting Your Work
One of the biggest challenges to with doing computational work is that it requires a high degree of organization. Our approaches to file management on computers are often haphazard, with `Documents` and `Downloads` folders filled with disorganized files or a `Desktop` covered in dozens of files. Perhaps this has worked in the past, but that approach (or lack thereof) **will** fail students in [Introduction to Geographic Information Science (SOC 4650/5650)](https://slu-soc5650.github.io) and [Quantitative Analysis: Applied Inferential Statistics (SOC 4930/5050)](https://slu-soc5050.github.io). Moreover, if left un-checked, it will fail students down the road when a hard drive failure or natural disaster renders their data irrevocably inaccessible. This chapter covers what some of those threats are and ways to manage those risks when conducting computational research. 

## Threats To Our Data
Each semester that I teach [Introduction to GIS](https://slu-soc5650.github.io) and [Quantitative Analysis](https://slu-soc5050.github.io), several things happen. The first thing that happens is that students regularly lose files. The effects of losing files can range from being a minor frustration to a major headache depending on the file in question. Losing files often results in downloading multiple copies of the same data and recreating work. Both of these are wastes of your time. Moreover, files are rarely gone. They are typically just misplaced. This is bad for reproducibility, particularly when you happen across multiple versions of the same file and have to sort out which version is the version you last worked on.

The second thing that happens is that students who use thumb drives for data storage lose them. Depending on the timing of this loss, this can again range from being a minor frustration (very early in the semester) to being downright anxiety attack producing (last few weeks of the semester). Recreating an entire semester’s worth of work on the final project is both a tremendous waste of your time and a particularly unpleasant experience.

Fortunately, I have never had a student’s computer hard drive die during the course of the semester. However, I assume that if I teach this course long enough a hard drive failure will indeed occur. The backup provider [Backblaze](https://www.backblaze.com/) has [analyzed](https://www.backblaze.com/blog/how-long-do-disk-drives-last/) their own hard drives and found that about 5% of drives fail within the first year. After four years, a quarter (25%) of drives in their data center fail. Similarly, it is only a matter of time before a student’s computer is stolen along with all of their hard work. A less likely though still very plausible scenario involves the destruction of a student’s belongings (computer and thumb drive included) in a fire, car accident, or natural disaster.

Despite the likelihood that you will at some-point lose a thumb drive (if not during this semester than sometime down the road) and the near certainty that your computer’s hard drive will eventually fail if a rogue wave does not get it first, few students and faculty take these risks seriously. While you cannot prevent many of these things from happening, I want to suggest to you that you can take some simple steps to sure that *when* (not if) they happen, you are well prepared to get back to work with minimal disruption.

## Creating a Sustainable File System
The first thing that students can do to stave off problems with lost files is to actively and mindfully manage their files. In his excellent document [*The Plain Person’s Guide to Plain Text Social Science*](http://plain-text.co), Kieran Healy describes two important revolutions in computing that are currently taking place. One of them is the advent of mobile touch-screen devices, which he notes

> hide from the user both the workings of the operating system and (especially) the structure of the file system where items are stored and moved around.

For most users, I would argue that this extends to their laptop or desktop computers as well. I would venture to guess that the majority of my students are used to keeping large numbers of files on their desktops or in an (distressingly) disorganized `Documents` folder. For research, particularly quantitative research, such an approach to file management is unsustainable. It is difficult to produce *any* research, let alone work that is reproducible, without an active and mindful approach to file management.

### Create a *Single* Course Directory
The most successful approach to organizing files is to identify *one and only one* area that you will store course files in. Having files scattered around you hard drive between you `Desktop` directory, `Downloads`, `Documents`, and a half dozen other places is a recipe for lost files. It can also add complexity to the task of backing these files up. I recommend naming this directory simply based on the course you are enrolled in:

* `SOC4650`
* `SOC4930`
* `SOC5050`
* `SOC5650`

These names are short, have no punctuation or spaces (which can create conflicts with software), and explicitly connects the directory to this course as opposed to other courses you may take that are also statistics or GIS courses (a good reason to avoid naming the directory `Stats` or `GIS`!).

This single course directory should reside in *one and only one* place. Once you have these folders set-up, I want you to an agreement with yourself: files for the course will *only* be saved within this structure. Do not temporarily save files to the `Desktop`, for example, intending to move them later. They will be forgotten. Like New Years resolutions, it is easy to say that you will use a file system but difficult to maintain that promise when stress sets in or you are rushed. Do *everything* you can to maintain your file system.

### Storing the Course Directory
Storing this directory inside a sync'd directory (like Dropbox or Google Drive) may cause conflicts with your Git repositories. Instead, students for both of my courses should utilize a large sized thumb drive or an external hard drive for data storage (see the "Course Onboarding" section of the respective course's website for additional details). Having data stored on an external device raises the risk of physical loss, but also makes it easier to move work between different computers. This is particularly challenging for GI Science work, where spatial data sources can be may megabytes in size.

macOS users should make sure that the external drive is formatted using the ExFat file system specification so that it is readable both by their operating system and the Windows operating system in the computer lab. If you buy a new drive, you will likely have to re-format it. Directions for doing so are [available from Apple](https://support.apple.com/kb/PH22241?locale=en_US).


### Approach Organizing Systematically
Within your single course directory, I recommend following a mindful, purposeful approach to organization. This approach begins with having a number of dedicated subfolders within your course directory:

```
/SOC5650
  /Core-Documents
  /DataLibrary
  /DoeAssignments
  /Lectures
  /Notes
  /Readings
```

Note again how these directories are named - there are no spaces, special characters, and the names are deliberately short but specific. For a directory with two words (e.g. `DataLibrary`), I use what is known as camelCase to name the file where the second (any any subsequent) words have their first character capitalized. You could also use dash-case (e.g. `Core-Documents`) or snake_case (e.g. `Core_Documents`) as a naming strategy. Regardless of which of these approaches you take, try to use it consistently.

For both of the courses that I teach, a basic file system will be made available for download onto your external device. See the respective course websites for more information about course data releases. Only the data release for [Introduction to Geographic Information Science (SOC 4650/5650)](https://slu-soc5650.github.io) will contain a `DataLibrary` directory.

### The `Core-Documents` Directory
The `Core-Documents` directory is used for storing the course syllabus, reading list, and a sample schedule for 3600 Morrissey Hall for the semester. You can view it online for both [Introduction to GIS](https://github.com/slu-soc5050/Core-Documents) and [Quanitative Analysis](https://github.com/slu-soc5650/Core-Documents). Once we cover using Git and GitHub in class, you should **clone** the appropriate `Core-Documents` repository into your file system. If there are updates, you will want to make sure you **pull** them down onto your local copy of the repository. You can read ahead in the [Basic Git] chapter for more information on how this works.

You will not be able to **push** changes that you make in this directory to GitHub, and making other changes could cause conflicts. I suggest not making changes inside this repository beyond opening files for reference purposes.

### The `DataLibrary` Directory
This directory is only applicable to students in [Introduction to GIS](https://slu-soc5650.github.io), whose data release will contain it. It will have copies of most data not disseminated to you as `R` packages. The data in this directory should be used as needed but not altered (one of the of the ["Good Enough" Research Practices] from the next chapter).

### The `DoeAssignments` Directory
Like the `Core-Documents` repository, this will not be included in the course data release. Once we cover using Git and GitHub in class, you should **clone** the appropriate `Core-Documents` repository into your file system. It will also have a different name - your last name instead of 'Doe'. Once you add it, it will contain a number of subdirectories:

```
  /SOC5650
    /DoeAssignments
      /FinalProject

      /Labs
        /Lab-01
        ...
        /Lab-15

      /LecturePreps
        /LP-01
        ...
        /LP-15
        
      /ProblemSets
        /PS-01
        ...
        /PS-08
```

The `FinalProject` directory will not have any subfolders in it. You will be asked to populate it with the appropriate subdirectories (see [Organizing Projects] below). These will be detailed in the final project instructions. The `Labs`, `LecturePreps`, and `ProblemSets` subdirectories have folders dedicated to the individual assignments you'll have to submit over the course of the semester. Like the `FinalProject` directory, you will need to populate them with the appropriate deliverables. These will be detailed in each assignment's instructions.

### The `Lectures` Directory
This directory should contain subfolders for each of the sixteen weeks of the course.

```
  /SOC5650
    /Lectures
      /Lecture-01
      ...
      /Lecture-16
```

You will need to add these subfolders each week by **cloning** them from GitHub.com. You will not be able to push changes that you make in these directories to GitHub, and making other changes could cause conflicts. I suggest not making changes inside this repository beyond opening files for reference purposes. If there is something you need to edit, copy it to the appropriate subdirectory of `DoeAssignments` and make your changes there.

### The `Notes` Directory
Use this as a home for course notes if you decide to take notes digitally and do not already use notebook software of some kind that organizes notes for you.

### The `Readings` Directory
Use this as a home for `.pdf` copies of course readings. I suggest creating subdirectories *only* for weeks that have readings assigned from outside of the main texts, such as Lecture 01:

```
  /SOC5650
    /Readings
      /Lecture-01
```

## Organizing Projects

```
  /projectName
    /data
    /doc
      notebook.md
    /results
      map1.png
    /src
    .gitignore
    LICENSE.md
    README.md
```

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

<div class="rmdtip">
<p>I gave a presentation on workflows for backing data up as part of the <a href="https://slu-dss.github.io">Data Science Seminar</a> series at <a href="https://slu.edu">Saint Louis University</a>. You can easily view the slides from that presentation on <a href="https://speakerdeck.com/chrisprener/protecting-your-data">Speaker Deck</a>, and you can download the session's materials from <a href="https://github.com/slu-dss/protectData">GitHub</a>.</p>
</div>

For this course in particular, it is *imperative* that you backup the data on your flash drive. A number of possibilities exist for accomplishing this:

  - Keep a local copy of your flash drive's files on your computer.
  - Keep a `.zip` archive of your files in a service like Dropbox or Google Drive. (Using a `.zip` archive will prevent issues with your `.git` repositories.)
  - Maintain a second flash drive copies of all of your files.

Whatever solution you select, make sure you regularly update your backup. The more often you keep your backup archive updated, the less stressful and disruptive losing your drive will be. This will likely be a manual task, so follow the guidance above about creating a repeating calendar event or to-do list task reminder.

