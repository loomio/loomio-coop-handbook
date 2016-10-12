# Loomio Bug Reporting Guidelines

**The problem:**
Currently we have a tension in the team around the reporting of bugs, and a gap in understanding between the team reporting bugs in the software, and those of us tasked with fixing them. This is an attempt at outlining what makes a great bug report;

So… Oh no! You found a bug! How do you get it fixed? The answer is, get it through the following 4-step process:

The Four Stages of Bugfixing:

1. Needs Confirmation (IE, this is a problem in production)
2. Needs Reproduction (IE, this is a problem in a local dev environment)
3. Needs Prioritization (IE, this is an important thing to be working on right now)
4. Fixed! 🎉

As a bug reporter, we’re relying on you to provide us enough information to get to step 3, at which point someone on the dev team knows why the bug is happening, how many users it affects, and (roughly) how to fix it. To get there, we need to

### How we fix bugs

##### 1) Confirm that the behaviour is indeed happening
The internet is freaking weird. Connectivity issues, third party services, web gremlins, and a whole other myriad of oddities can cause weird things to happen all the time, often in unexpected ways. In order for us to spend time on fixing something, we should be sure that it’s a replicable problem, for a specific chunk of the userbase. Often this means providing a set of steps to demonstrate the problem on Loomio.org.

##### 2) Isolate the behaviour in an environment where it can be fixed
Just because something is happening on Loomio.org doesn’t necessarily mean it appears in a local dev environment. This is the ‘science’ part of computer science; if we can’t imitate the behaviour in the lab, we have no idea what the heck our fixes will do once they make it to the wild. (This is why the trickiest bugs are ones which either happen rather intermittently, or not in the development environment at all.) Do you really want our wild guesses going into your product? This part is a little further out of your grasp as a bug reporter (unless you have a dev environment :D), but is still a necessary step towards getting bugs fixed.

_NB: If we can’t get to this level of information, that’s ok. It’s good for us to know about issues even if we don’t quite know how to fix them yet, so report away. We’ll mark issues which we don’t have enough information to solve yet with a ‘Needs Confirmation’ tag on github._


##### 3) File and classify the issue
Issues, large or small, should be filed in the issues list, with as much information as you’ve deemed appropriate / available. If an issue does not appear in the issues list, you’re welcome to assume we don’t know about it.

If the reporter is unable to provide enough information for the devs to reproduce the bug (either through inability or unresponsiveness), it can be marked ‘Stale’ after a period of inactivity (1 week), and closed after a longer period of inactivity (3 weeks) The issue can be reopened (or another issue can be filed) with further information if it becomes available.

##### 4) The dev team fixes it!
Go dev team, you folks are super great.

---

**Okay great.** So how do you, as a bug reporter, facilitate this process?

**The short answer:**
Provide as much information about the problem that you’re reporting as possible, and be prepared for follow up questions.

**The long answer (with action items!):**

- Check to see if someone else has reported the bug.
All known bugs should be captured in the issues list. If it’s not there, and it’s a bug, it belongs there!

- Gather as much information as you can about the bug. Pieces of information which will come in handy are:
  - A detailed description of the behaviour you’re experiencing, and how it differs from what you’re expecting
  - What browser / operating system you are using
  _(go to http://whatbrowser.org if you’re unsure)_
  - Screenshots or gifs of the behaviour you’re experiencing
_(on Mac, you can use a handy screenshot tool by pressing CMD+SHIFT+4, and we use http://recordit.co/ for a really easy way to make gifs.)_
  - A link to where the issue occurred on production
  - A log of the console while the bug is happening.
_(Not sure how to open the console [or what it is]? Check out [this handy guide](http://webmasters.stackexchange.com/a/77337) for opening the console in all major browsers.)_
Is this related or similar to an already existing bug? If so, what makes this bug different?
Specific steps you can perform to make the behaviour appear on loomio.org
_(^^ this is the most important one. If you can provide this, you usually don’t need anything else.)_

- Report the bug as an issue in the [issues list](http://www.github.com/loomio/loomio/issues), after ensuring it's not a bug which has been reported before.

You’re going to be quizzed on this part, so come prepared with as much information as you can muster! In the case of most simple (and many complex) bugs, it is the responsibility of the reporter to provide enough information for the devs to be able to work on the bug. We only know so much about what your individual experience is!

### How we classify bugs

There are many tags on the loomio repo to classify the type of issue you’re reporting. At a minimum, you should provide a severity level, and whether you think this is a bug or a feature request.

![Table showing different severity levels](https://i.imgur.com/S36ftXX.png)

**Core workflows** are actions that every user will use on a daily basis, or functionality which is at the core of the Loomio value proposition. Examples would be starting a thread, inviting people to a group, or signing in to the app.

**Peripheral workflows** are actions that some subset of users will use (such as group coordinators), or ones which are common, but non-essential functions within the app. Examples would be liking a comment, viewing the list of members, or signing out of the app.

**Minor workflows** are ones which a very small subset of users use, or something which very few users would miss. Examples would be printing a thread, signing up with twitter, ctrl+clicking a link, or performing inline translation.

##### Mitigating factors
The classificaions in the above table should be treated as guidelines; there are many reasons a bug may be more or less severe, so don’t be offended if your bug is reclassified during its lifetime. Some examples may include:

**More severe:**

- It’s affecting a team member’s sprint work
- It’s been reported as annoying by paying or high-leverage customer(s)
- It’s blocking existing feature development

**Less severe:**

- It only affects certain browsers, or occurs very rarely
- The functionality will be removed in a later iteration
- Fixing the bug is likely to introduce significant complexity into the system

This is ok and to be expected. If you think your bug has been misclassified, say so! We’re happy to talk about it.

##### Bug vs Feature Request:
A bug is a regression in behaviour or something that is missing from an existing design
A feature is a request for additional functionality, above and beyond what the app already does.

**What’s the difference?**
The big difference is that bugfixes don’t require design. A feature request, no matter how small, will require some level of consensus beyond the individual dev’s brain to agree that this is functionality we want to see in the app. The other big difference is that fixing bugs should be given priority over building features. Read [point number 5 in this article](http://www.joelonsoftware.com/articles/fog0000000043.html) for why. (Also read that whole article, it’s great.)

(Don’t fret this classification too much, but do pick one.)

Thanks for reading, and keep those bug reports coming!
