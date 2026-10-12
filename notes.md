# Assignment 3: Working Notes

## Project setup
**10/10/2026**

- **What I worked on:** Couldn't get into the Classroom50 org at first (kept getting a 404), so I emailed Michael to add me. Once I had access I read the full brief properly.
- **Files changed:** Nothing yet, just created the repo.
- **What I learned:** There's a lot more to this than a blog post. I'll need to go back through the Week 3, 5, 6 and 7 material to understand how to build and style the site.

## YAML changes
**11/10/2026**

- **What I changed:** Added my name as the site title, edited the navbar and set the format options.
- **Why I changed it:** Had to start somewhere, and the title is the first thing anyone sees.
- **Result after previewing:** Not too bad for a first change.

**12/10/2026**

- **What I changed:** Changed the homepage title from "ETC5523 Blog Assessment" to "Posts" and added a subtitle.
- **Why I changed it:** The old title read like a placeholder, not a personal site.

## CSS and website design
**11/10/2026**

- **What I changed:** Picked the most boring colour palette on purpose to see what happens, and set the page background and body text.
- **Why I chose this design:** Just wanted to see how the CSS actually changes the page before deciding on anything.
- **What I noticed in the preview:** Very flat. Everything feels like it's everywhere, nothing stands out.
- **Anything I still need to fix:** Headings need to be bigger, and the colours need to change.

## Blog post and visualisations
**12/10/2026**

- **What I worked on:** Removed the template's welcome post and started my Black Summer post. So far I've added the YAML and the first two sections: the problem ("Is this the new normal?") and what the Fire Weather Index is. I used AI to help draft these, so I still need to rewrite them in my own voice.
- **Design or analysis decisions:** Audience is people living near bushland in southeastern Australia, not the insurance analytics team from Assignment 2. Opening with the question people actually asked after the fires instead of jumping into results.
- **Why I made these decisions:** My Assignment 2 feedback said to give the reader the problem first and to mention FWI early so the results make sense. So those are the first two things in the post.
- **Questions to revisit:** Does the FWI explanation make sense to someone with no science background? Does it sound like me?

**12/10/2026 (later)**

- **What I worked on:** Added references.bib with the van Oldenborgh et al. (2021) BibTeX, copied straight from the journal page. Added [which sections, e.g. "Where the evidence comes from" and "So, has it become more likely?"] and the first version of the likelihood plot.
- **Design or analysis decisions:** Rebuilt Figure 6a from Assignment 2 as a simple bar chart instead of reusing the original image. Each bar is the lowest increase the evidence supports, the dot is the best estimate, and the dashed line at 1 means "same as 1900".
- **Why I made these decisions:** The original figure had model names, a log scale and probability ratios, which my audience wouldn't understand. "How many times more likely" is something anyone can read.
- **Questions to revisit:** Does the chart still make sense without reading the caption? Are the colours readable once I finish the CSS?

## Problems and solutions

- **Problem:** Got a 404 when accepting the assignment.
- **What caused it:** I hadn't been added to the ETC5523-2026 org yet.
- **How I fixed it:** Emailed Michael with my GitHub username and the error details.

- **Problem:** Named my post folder "black summer" with a space.
- **What caused it:** Didn't think about it. Spaces turn into %20 in the URL and can break things.
- **How I fixed it:** Renamed it to black-summer before committing.
- **What I learned:** Use hyphens in folder and file names.

- **Problem:** `_site/` kept showing up as untracked in git.
- **What caused it:** Quarto rebuilds the site into `_site/` every time I render.
- **How I fixed it:** Added it to `.gitignore`, since `quarto publish gh-pages` handles the published HTML separately.

- **Problem:** RStudio said my index.qmd had been deleted.
- **What caused it:** Both the welcome post and my new post had a file called index.qmd. I had the welcome one open in a tab when I deleted the welcome folder, so I thought I'd lost my own post too.
- **How I fixed it:** Checked with `ls posts/black-summer` and my file was still there. Closed the old tab and reopened the right one.
- **What I learned:** Check the file path at the top of the tab before editing, since every post's file is called index.qmd.

- **Problem:** The post needed a bibliography file before it could render.
- **What caused it:** The YAML says `bibliography: references.bib` but the file didn't exist yet.
- **How I fixed it:** Created references.bib in the post folder and pasted the BibTeX from the journal's download link.

## Final checks

- [ ] Website previews correctly
- [ ] Website published through GitHub Pages
- [ ] README includes audience statement
- [ ] README includes AI-use declaration
- [ ] Walkthrough recorded
