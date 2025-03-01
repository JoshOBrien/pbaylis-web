---
layout: post
title:  "Work process and Dropbox organization"
date:   2015-09-08
categories:
  - productivity
---

_Update (April 2018): I still do this to a certain extent, but I'm transitioning to using all github projects. See Gentzkow and Shapiro's [lab notes](https://web.stanford.edu/%7Egentzkow/research/CodeAndData.pdf) for related thoughts._

# Work process notes

- Beginning of arrival in new space: 30 minutes of uninterrupted work
- No e-mail, no paying CC bills, definitely no dicking around on the internet. Momentum is important!
- After the frenzy, 25min on, 5 min off (pomodoro)
- Long-term schedule sketches out broad goals. In general maybe for a semester or something, right now focus on JMP.
- Short-term schedule made at the beginning of every week. Sketch out morning and afternoon activities.
- At end of workday, write down what I accomplished in a work journal. It'd be really nice to do this in the same place where the schedule is, somehow

# Dropbox organization
Winter break is a good time to sit back, reflect on the year, and... reorganize your Dropbox folder. If you're the kind of semi-compulsive organizer that I am, that is. After stumbling upon Michael Descy's [Plaintext Productivity](http://plaintext-productivity.net/), the notion to reorganize my work documents and habits has been stealthily invading my brain. I don't need a system as complex as Descy, but I do need a system. I've made two major changes:

1. Converted my note-taking process and most informal writing into markdown. Markdown is, in some ways, an incomplete replacement for org-mode (my previous note-taking methodology) in emacs, but with [SmartMarkdown](https://github.com/demon386/SmartMarkdown) in [Sublime Text 3](http://www.sublimetext.com/), I can at least fold up the sections. Which is 90% of what I was missing from org-mode. Markdown is nice because it can be easily edited with any editor in any operating system, looks almost exactly like plaintext to most people, and can be used to VERY easily generate HTML. Also, a good deal of my work is already in Sublime Text and while knowing emacs did hold a certain cachet, I don't have a strong desire to keep two distinct sets of keyboard shortcuts in mind. Also emacs loads more slowly. Also lisp (and elisp) drive me crazy.

2. Restructured my Dropbox folder.

I had the following requirements:
1. Quick, logical access to data/work
2. Pain-free archiving
3. Incorporate school and work into Dropbox
4. Deal elegantly with non-Dropbox files (too big for Dropbox)

To do this, I've restructured my Dropbox folder as follows:

1. 01_Work
	1. 01_Current: Current projects
		- Projects on which I am an author in base directory
		- Work for others in subdirectories
			- e.g. 01_Current/Joe/Project A
	2. 02_Archive: Archived projects by year most recently updated
		- Same structure as Current projects
		- e.g. 02_Archive/2013/Joe/...
	3. 03_Ideas: Project ideas
		- Nascent ideas that have some associated documents in them in base directory
			- Once they're more developed, move to 01_Current
		- Once ideas are stale, move to subdirectory Archive/... (no year necessary)
	4. 04_Notes
		- Includes notes like, work.md, and so on
		- Toolbox: math, econometrics, etc. handouts that I've downloaded and want to save
2. 02_Personal
	- Everything from my non-work life

If I don't break Dropbox, this will be great. The only requirement this doesn't capture is #4. I've decided the best thing (for now) is to just include shortcuts to the data folders. Since almost all of these are my bigger machine MONDO, it's an issue I only need to deal with there.
