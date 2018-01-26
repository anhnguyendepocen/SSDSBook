# Slack

One of the three core areas for analysis development identified by Parker (2017) is collaboration. Data science work often occurs in teams, sometimes remotely, and building a skill set in working collaboratively from the outset is important. This chapter will not focus on the soft skills required for working as part of a team. Rather, we'll focus on some of the technical tools that are useful for facilitating this work. One of the more common tools used today in data science, research, software development, and other technical settings is the service [Slack](https://slack.com). At its core, Slack is a messaging tool designed to keep people in touch with one another. The following sections introduce some basic Slack functions. You can also use [Slack's knowledge base for users](https://get.slack.help/hc/en-us/categories/200111606), which has a wealth of information for using Slack and adjusting the various settings described here.

## Slack Basics
Slack is organized into **workspaces**, which are dedicated organizations that are independent from each other. This means that you have individual login credentials (username and password) for each Slack workspace. The image below is of a Slack workspace for [Introduction to Geographic Information Science (SOC 4650/5650)](https://slu-soc5650.github.io). We will discuss some of the individual elements of this image below.

<img src="images/slackOverview.png" width="95%" style="display: block; margin: auto;" />

### Channels
**Channels** are found on the left-hand sidebar of a Slack **workspace**. Channels with a `#` sign are public, and those with a lock symbol are private. Slack workspaces are typically organized around channels that are dedicated to a specific topic or project. For the courses that I teach, there are dedicated helpdesk channels for some of the various tools that the course introduces as well as for coursework and assignments. For example, the `#helpdesk-slack` channel is open in the image above. Messages from individual users or updates appear in the main window. You can see messages from myself and another user in the image above.

### New Messages
To post a new message, use the field at the bottom of the main window that contains the placeholder text (visible in the image) "Message #helpdesk-slack". Click on the field and begin typing your message. You can click on the `@` icon to tag individuals using their user names, or use the channel's name - `#helpdesk-slack` - to notify all users. Using the channel name hashtag in your initial message to a channel can help speed up people's response, particularly if they have reduced the frequency of notifications.

The smiley face icon allows you to use emojis in your message. Messages can be composed using a flavor of Markdown (see the next section [Markdown in Slack]). Emojis will appear as text in a new message like `:smiley:` after they are selected. A newly composed message looks like this:

<img src="images/slackMessage.png" width="95%" style="display: block; margin: auto;" />

To send a message, use the `Enter` or `Return` key. Once sent, that message will render so that it looks like this:

<img src="images/slackMessageSent.png" width="95%" style="display: block; margin: auto;" />

### Editing Messages

To edit a message after it has been sent, hover your mouse over the message (or push your thumb down on the message and hold if you are on mobile). Doing so will bring up a menu of options. These are what the desktop options look like:

<img src="images/slackMessageOpts.png" width="95%" style="display: block; margin: auto;" />

Four buttons will appear on the desktop when you hover over the message. The furthest right, with three small dots, can be selected to reveal a menu with a number of options, including editing the message. Use this if you want to correct a typo or clarify a point.

### Responding to Messages

The image above also shows options for responding to messages. All four of the icons that appear when you hover over the messages with your mouse on desktop contain response options. The first icon from the left allows you to add an emoji reaction to a message. The second icon from the left allows you to to create a threaded response to the message. In the image below, you can see both the "thumbs up" reaction to the message as well as the visual indicator that a reply to the message has been posted:

<img src="images/slackMessageReact.png" width="95%" style="display: block; margin: auto;" />

When you click on the reply, it will open a right-hand sidebar that will contain the original message and any responses:

<img src="images/slackMessageThread.png" width="60%" style="display: block; margin: auto;" />

Use threaded replies if the answer is longer than a few words and requires intricate detail. If you want to add a reply on mobile, tap a message with your thumb and select Start a thread.

### Sharing Messages

If you want to refer to a previous message, there are two options. In the image under [Editing Messages], the third icon from the left (found by hovering the mouse over the message on desktop) allows you to share the original message's content. When you click on the share button, a dialogue box will open that will optionally allow you to add your own message as well. This is not a requirement, however.

<img src="images/slackMessageShare.png" width="75%" style="display: block; margin: auto;" />

Once you hit the Share button, the shared message will be re-posted in the thread. Shared messages appear similarly to quotes in [Markdown], with a vertical grey colored line on the left side of the message:

<img src="images/slackMessageShared.png" width="95%" style="display: block; margin: auto;" />

You can also click on the same icon with three dots (see the image under [Editing Messages]) and select Copy Link, which will add a hyperlink to your clipboard that you can add to a post. 

### Direct Messages
Direct messages are messages can be accessed only by the participants. Direct message channels are useful for reaching out directly to other individuals to have private conversations. You can start a new direct message by clicking on the plus icon to the right of the Direct Messages heading (see the first image in this chapter). Messages are authored using the same means as in public and private channels (see [Channels] above as well as [Markdown in Slack]). 

I ask that questions about Problem Sets that are specific be addressed as direct messages first. For all other questions, I encourage students to use the public channels so that we can learn collectively from each other's experiences. If you are not sure whether or not a question is appropriate for a public channel or would prefer to not ask the question publicly, feel free to use a direct message!

## Settings
Slack has a number of ways to adjust its settings and its preferences. In many cases, there are multiple ways to adjust the same setting. What follows is a guide for quick ways to address some of the most common settings.

### Main Toolbar
Across the top of the screen, there will be a toolbar with access to settings about the workgroup, your profile, and specific channels. The toolbar looks like this:

<img src="images/slackToolbar.png" width="95%" style="display: block; margin: auto;" />

You can search a channel (helpful if you are looking for information about a specific topic or issue) using the search field in the menu bar along the top of the main window. 

### Notifications
Notifications can be adjusted either on a channel by channel basis or for all channels in a workspace. To adjust settings for a specific channel, you can click on the 

### Channel Preferences
Information and preferences for individual channels can be accessed by clicking on the info icon along the top of the main window. For instance, I will sometimes "pin" posts so that they can be accessed later. You can see a list of pinned items by pulling down the Pinned Items menu.

These preferences include the ability to adjust the notifications for both desktop and mobile on a channel by channel basis. To adjust notifications for a channel:

1. Open the Channel Preferences
2. Pull down the Notification Preferences menu, where you will see an overview of your current desktop and mobile notification preferences
3. Click on `Edit preferences`
4. Make changes as desired in the Notification Preferences window

The Notification Preferences window for the `#helpdesk-slack` channel looks like this:

<img src="images/slackNotifications.png" width="75%" style="display: block; margin: auto;" />

If you do not want to set notifications on a channel by channel basis, you can set workspace-wide notification preferences by following the `Account Preferences` link in this window (see [Preferences] below). I do warn students, however, that Slack is our primary means of communication and muting or reducing notifications puts more of an onus on students to mindfully check-in on channel activity on a regular basis. I would not reduce notifications, for instance, on the `#_news` channel. 

### General Preferences
The Preferences window can be used to adjust settings that control your Slack workspace. These include how your sidebar is organized, how "mark as read" functions, and how notifications for all channels work by default. You can access the Preferences from the main menu, which is available by clicking on the workspace name:

<img src="images/slackMenu.png" width="95%" style="display: block; margin: auto;" />

The Notifications tab can be used to set global defaults for notifications:

<img src="images/slackPreferences.png" width="95%" style="display: block; margin: auto;" />

You can use this window to create additional notifications for when specific keywords appear. For example, if you wanted to be notified if any mentions of the `ggplot2` package appear in a Slack channel, you could add "ggplot2" as a keyword. This window also allows you to adjust your do not disturb settings and the sounds that are played when new messages are posted while you are online.

### Profile Settings
Profile settings, like your name, display name, timezone, and other items can be edited as well. You can access them by selecting Profile & Account from the main menu, which is available by clicking on the workspace name:

<img src="images/slackProfileMenu.png" width="95%" style="display: block; margin: auto;" />

This will open a sidebar on the right side of your screen that looks something like this:

<img src="images/slackProfile.png" width="40%" style="display: block; margin: auto;" />

If you select Edit Profile, you can change your full name and display name, adjust your timezone, and optionally add other details as well. There is no need to add phone numbers or Skype handles for course workspaces. You can also change your profile picture here. The window will look like this:

<img src="images/slackProfileEdit.png" width="95%" style="display: block; margin: auto;" />

Make sure you hit Save Changes when you are done!

To make more fine-grained changes to your account for this Slack workspace, click on the wheel icon in the sidebar that opens after selecting Profile & Account from the main menu. The wheel icon is next to the Edit Profile button. Clicking the wheel icon will open a new tab in your browser:

<img src="images/slackAccount.png" width="95%" style="display: block; margin: auto;" />

Many of the changes that can be made in other places can also be made here. Additionally, you can adjust Two-Factor Authentication security settings here as well.

## Markdown in Slack
Slack uses a simplified ["flavor"](https://github.com/commonmark/CommonMark/wiki/Markdown-Flavors) of Markdown. All of the available Markdown syntax characters are included below. 

### Styling Text
Text can be styled using bold and italics To create bold text, wrap your text with a single pair of asterisks `*text*`. To create bold text, wrap your text with a single pair of underscores `_text_`. Strike through text can be created by wrapping your text with a single pair of tildes `~text~`.

**Input:**
<img src="images/slackMdStyleIn.png" width="95%" style="display: block; margin: auto;" />

**Output:**
<img src="images/slackMdStyle.png" width="95%" style="display: block; margin: auto;" />

Note that the use of single asterisks is frustratingly non-standard for Markdown. In the original Markdown spec (see [Markdown]), `*text*` was reserved for italicized text. Here it is used for bold, and an underscore is used for italicized. This inconsistency [has not gone unnoticed](https://daringfireball.net/linked/2015/11/05/markdown-strikethrough-slack) by Markdown's creator, John Gruber, who tweeted this in 2015:

<div align="center"><blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/vhgalvao?ref_src=twsrc%5Etfw">@vhgalvao</a> Like I said, Slack has its collective head up its ass regarding text formatting.</p>&mdash; John Gruber (@gruber) <a href="https://twitter.com/gruber/status/662451994720911360?ref_src=twsrc%5Etfw">November 6, 2015</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></div>

### Quoting Text
Quoting text is done with a greater then symbol (`>`).

**Input:**
<img src="images/slackMdQuoteIn.png" width="95%" style="display: block; margin: auto;" />

**Output:**
<img src="images/slackMdQuote.png" width="95%" style="display: block; margin: auto;" />

### Quoting Code
There are two types of code quotes in Slack's flavor of Markdown. When you create reproducible examples (see [Getting Help]) and ask questions, please try to use the in-line and code block syntax as much as possible - it makes questions much easier to read!

#### In-Line Code
In-line quotes, which are included in a sentence, are wrapped in single backticks:

**Input:**
<img src="images/slackMdInlineIn.png" width="95%" style="display: block; margin: auto;" />

**Output:**
<img src="images/slackMdInline.png" width="95%" style="display: block; margin: auto;" />

#### Code Blocks
To include code blocks, which are better for including the full syntax of particular commands and their output, use triple backticks:

**Input:**
<img src="images/slackMdBlockIn.png" width="95%" style="display: block; margin: auto;" />

**Output:**
<img src="images/slackMdBlock.png" width="95%" style="display: block; margin: auto;" />

Note that we do not include the name of the language that the code is written in, as we do in standard Markdown. Slack does not include syntax highlighting and it will instead include any text written on the same line of the top row of backticks as output. If the code block is more than a few lines long, however, I suggest looking at other options for posting code (see next section on [Posting Text and Code]).

## Posting Text and Code
To post longer code snippets or text files, you can click on the plus icon on the left side of box where messages are composed:

<img src="images/slackUpload.png" width="95%" style="display: block; margin: auto;" />

If you want to upload a file, like an image, text document, or really any other file type, chose the "Your computer" option. You will be taken to a window to find the document on your computer, and then given the option to add a comment while posting it. I usually use this space to describe the contents of the document I am uploading. 

If you want to add a longer block of code, select "Code or text snippet". Selecting this will bring up a window that allows you to:

1. Give the snippet a title,
2. select the language the snippet is written in (including an option for `R`),
3. add the code,
4. and optionally add a comment.

A completed version of this window looks like this:

<img src="images/slackSnippetCreate.png" width="75%" style="display: block; margin: auto;" />

When you are ready to post the snippet, click the "Create Snippet" button. A completed snippet will then be posted on Slack:

<img src="images/slackSnippet.png" width="95%" style="display: block; margin: auto;" />

Hovering your mouse over the message will bring up options to expand the snippet, download it, and edit it (if you are the creator):

<img src="images/slackSnippetEdit.png" width="95%" style="display: block; margin: auto;" />

You will also have the option to respond, add emojis, and share these posts - just like any other message on Slack!
