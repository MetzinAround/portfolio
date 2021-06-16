---
title: Adding slides
nav_order: 5
parent: How to use
---

# Adding slides

`markdown` has more uses than creating pages for your course.
You can build slides with it as well!
To do this create a new `markdown` file (remember that it **needs** to have a `.md` or `.markdown`) extension in the `attached_files/slides_markdown` directory.

Just like we did with the pages, we'll have to write a header right at the top of all the slides files:

```yaml
---
title: 
- Slides Title
author:
- Your Name
---
```

Now each `markdown` title in that file (remember that `markdown` titles begin with a `#`) will become a slide in your slide deck!
We can also make use of all the `markdown` we learned before: we can add pictures, hyperlinks and format our text.

```yaml
---
title: 
- Git Workflow
author:
- Évariste Galois
---

# Introduction

*Git* is a **distributed version-control** system for tracking changes in files and coordinating work on those files among multiple people.
Distributed means that all users have a copy of the repository instead of a centralized version on a server.

![what-is-git](https://i.imgur.com/rxpXW0j.png)

# Git Workflow

- Create an issue
- Create a branch to tackle that issue
- Push commits
- Open a Merge Request
- Ask from feedback from your colleagues
- Deploy and merge once it's approved!
```

Now we can attach our slides like we learned:

`{% attach_file {"file_name": "slides_markdown/git_slides.pdf", "title":"Git slide deck"} %}`

## Customizing your slides

The header supports lots of configurations. They are listed [here](https://pandoc.org/MANUAL.html#variables-for-beamer-slides).

For example, we could add a *theme*, the insitute where we're presenting our slide presentation and school logo.

```yaml
---
title: 
- Git Workflow
author:
- Évariste Galois
insitute:
- École normale supérieure
theme:
- Copenhagen
---
```

You can check the resulting slides [here](https://alejandro-rusi.gitlab.io/courseware-git-example/attached_files/slides_pdf/git_slides.pdf)!