---
layout: post
title:  "Debugging in R, RStudio"
date:   2018-09-11
categories: 
  - programming
tags:
  - R
  - RStudio
  - debugging
---

Debugging can be a challenge in RStudio. One of my main frustrations is that once you execute the Run command on a selection of code (i.e., running it in interactive mode), it will send all the commands you selected, _even if one or more of them raises an error_. This often results in me running a full script, even after an error occurs on one of the first few lines of code. In most cases, nothing remaining in the script can run successfully without whatever errored out earlier. For example, suppose I'm executing the following code:

```r
x <- 4
z <- x + y
print(z)
x <- x^2
Sys.sleep(5000) # Placeholder for a time-consuming command
```

Because I forgot to define `y` before calling it, the second command fails with an error. But because I'm running this interactively, the third command runs (and fails) as well. The fourth command then runs successfully, modifying `x`. This introduces a new problem: I can no longer easily fix the problem by fixing the second command and rerunning the subsequent commands -- I have to either start from the beginning or manually fix the modified variables. Finally, the fifth command runs and hangs the R console until I hit stop. If this was a command that was loading a large dataset (as it often is), the only way I can stop it is by killing R and restarting.

Unfortunately, there's no way to solve this in interactive mode -- RStudio seems to be committed to [running everything you send](https://stackoverflow.com/questions/42256291/make-execution-stop-on-error-in-rstudio-interactive-r-session), no matter what. The best solution is to instead source the document (CTRL-S in RStudio), which runs the entire script from the beginning. This is fine if you don't have a bunch of data you need to load initially. But since I often do, I have to comment out everything I don't want re-run.

One alternative to this is encasing everything in a function, since functions do halt on errors. This makes debugging and development challenging (despite the `browser()` command), so I view this as a less-useful solution.

I'm still thinking this over, but here are a general set of principles for efficient debugging in a research context:
1. Minimize overall execution time whenever possible -- sample from datasets and save intermediary datasets that are time-consuming to compile.
2. If the above is not possible, run from source (commenting higher up portions as needed - this can be made easier with intermediary datasets) instead of interactively.
3. Functionalize as much as possible.
