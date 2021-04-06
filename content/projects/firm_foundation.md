---
title: Firm Foundation
description: Digitizing and Analyzing the Firm Foundation
toc: false
authors: []
tags: []
categories: []
series: []
date: 2021-03-26T10:55:37-04:00
lastmod: 2021-03-26T10:55:37-04:00
featuredVideo:
featuredImage: images/Tableau.png
draft: false
---


### Digitizing and Analyzing the Firm Foundation

Founded in 1884 in Austin, Texas, the *Firm Foundation* grew to become one of the most influential publications affiliated with Churches of Christ, the most conservative of the three main branches of the restorationist Stone-Campbell Movement. As an ostensibly nondenominational group, Churches of Christ relied on informal structures of authority, including ministers at large churches, affiliated college administrators and faculty, and journal editors and writers. By the 1960s, the *Firm Foundation* and the Nashville-based *Gospel Advocate* were the organs through which leaders within the White portion of the movememnt adjudicated doctrinal and ecclesial disputes.

As such, with no denominational arvhives available, these weekly journals are invaluable sources for historians seeking to contextualize mainstream views among Churches of Christ – and, more generally, among Southern White Protestants, of which Churches of Christ comprised a significant, if more fundamentalist, portion – during the turbulent years of the middle 20th century. Although these journals have been digitized (available for purchase from [TLC Publishing](https://www.tomchilders.net/Journals_c_17.html)), this project seeks to begin the painstaking process of converting these PDFs into a format better able to accommodate large-scale computational analysis.

Begun to fulfill assignments for a class on computational methods in the humanities, this project has a number of facets that may be of limited relevance or worth outside of simply practicing various methods for classwork; nevertheless, here are links to my work:

### Overall Project Link <img src="https://www.therestorationmovement.com/images4/chism14.jpg" style="float:right;width:250px;">

- [On GitHub](https://github.com/pa20bm/firm-foundation/tree/main/anthony-firm-foundation-main)

### Indexes

- [*Firm Foundation* volumes](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/FFVolumesIndex.csv) I have in PDF form
- [*Firm Foundation* issues](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/FFIssuesIndex.csv) from the above volumes (with notes for which ones I've begun working with)

### Plain-text files

Individual issues, randomly selected, text extracted through OCR, cleaning in progress:
- [1945-05-22](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/Issues/FF-1945-05-22)
- [1952-07-29](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/Issues/FF-1952-07-29)
- [1960-11-08](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/Issues/FF-1960-11-08)
- [1976-08-10](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/Issues/FF-1976-08-10)


### Data and analysis

In 1976, the *Firm Foundation* published a **state-by-state table of congregations**, measuring the number of cities with at least one Church of Christ congregation and the number of cities without one. I played with cleaning this data, comparing it to 2020 state-by-state presidential election results, then visualizing that comparison through RStudio/GGPlot and Tableau:
- [Plain text table](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/Table_cleanup/1976StateCongregationsTable) (includes state abbreviations as appearing in original)
- [CSV table](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/Table_cleanup/1976StateCongregationsTable.csv) (keeps abbreviations from original)
- [CSV table](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/Table_cleanup/CongsxDems.csv) comparing 1976 state congregation density vs. Democratic support in the 2020 presidential election
- [GGplot scatterplot](https://github.com/pa20bm/firm-foundation/blob/main/anthony-firm-foundation-main/Plotting/congregations_democrats_plot.png) comparing two percentages shows a slight negative correlation between Church of Christ congregation density in 1976 and Democratic presidential support in 2020.
- [Tableau scatterplot](https://public.tableau.com/profile/paul.anthony3275#!/vizhome/ChurchesofChristxPresidentialResults/Sheet1) showing the same thing
- [Tableau map](https://public.tableau.com/profile/paul.anthony3275#!/vizhome/CoCData/Sheet1) showing Church of Christ congregation density by state in 1976 (blank states caused by unusual abbreviation scheme in the original table)
- [Tableau map](https://public.tableau.com/profile/paul.anthony3275#!/vizhome/1976ChurchesofChristbyState/Sheet1) comparing 1976 Church of Christ congregation density with 2020 Democratic presidential support (fixed abbreviations, colored states red with a per-city congregation density over 35%)
- [Automatically generated Tableau map](https://public.tableau.com/profile/paul.anthony3275#!/vizhome/ChurchesofChristxPresidentialResultsClusters/Sheet1) showing three clusters of states based on congregational density and presidential election data: high-density, low-Democratic-support states (red), low-density, high-Democratic-support states (blue), and states that don't fit in either category (yellow)

The 1960 **presidential candidacy of John F. Kennedy** sparked alarm among writers in both the *Firm Foundation* and the *Gospel Advocate*. Playing with topic modeling showed that commentary on Catholicism and its role in American government was a prominent topic of discussion among editorials published in both magazines during the summer and fall of 1960, although I'm not sure how useful this process ended up being since it was obvious just by looking at headlines:
- [*Firm Foundation* editorials](https://github.com/pa20bm/firm-foundation/tree/main/anthony-firm-foundation-main/1960-editorials/ff), August 9-November 1, 1960 (lightly cleaned plain text files and CSV index)
- [*Gospel Advocate* editorials](https://github.com/pa20bm/firm-foundation/tree/main/anthony-firm-foundation-main/1960-editorials/ga), October 6-December 22, 1960 (lightly cleaned plain text files and CSV index, different date range because *GA* redesigned in October, and its issues pre-10/6/60 are much messier)
- [Various topic modeling spreadsheets](https://github.com/pa20bm/firm-foundation/tree/main/anthony-firm-foundation-main/1960-editorials), to the extent they are helpful