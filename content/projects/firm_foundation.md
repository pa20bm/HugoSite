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

### Overall Project Link <img src="https://raw.githubusercontent.com/pa20bm/HugoSite/main/content/images/FF_1960.png" style="float:right;width:350px;">

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

Further **experimenting with word counts and visualization** didn't result in much beyond [Voyant word clouds](https://github.com/pa20bm/firm-foundation/tree/main/anthony-firm-foundation-main/word-counts/word-clouds), although some of the following tables proved to be interesting:
- The top words from each of my randomly selected issues of the *Firm Foundation* (after deleting date- and location-specific words like "July" and "Texas"):

| Date   | 5/22/45 | count | 7/29/52 | count | 11/8/60 | count | 8/10/76 | count |
|--------|---------|-------|---------|-------|---------|-------|---------|-------|
| Word 1 | church  | 108   | church  | 158   | church  | 90    | church  | 160   |
| Word 2 | work    | 84    | meeting | 89    | god     | 50    | restoration | 99 |
| Word 3 | christ  | 70    | work    | 82    | bible   | 43    | christ  | 98    |
| Word 4 | meeting | 60    | brother | 68    | worship | 35    | new     | 84    |
| Word 5 | brother | 49    | good    | 55    | christ  | 33    | bible   | 59    |
| Word 6 | new     | 47    | bible   | 49    | man     | 26    | movement | 59   |
| Word 7 | time    | 42    | congregation | 43 | work  | 26    | god     | 57    |
| Word 8 | god     | 36    | god     | 37    | people  | 25	   | testament | 55  |
| Word 9 | bible   | 35    | time    | 37    | religious | 25  | men     | 48    |
| Word 10| good    | 35    | new     | 36    | christian | 24  | churches | 42   |

<img src="https://raw.githubusercontent.com/pa20bm/firm-foundation/main/anthony-firm-foundation-main/word-counts/word-clouds/1960-11-08.png" style="float:right;width:350px;">

Things to note: 
- "Church" is obviously the No. 1 word, and "Christ" ranks in the Top 5 for three of the four issues (and No. 11 in the fourth), which indicates the phrase "Church of Christ" likely accounts for a lot of this overlap. Not all of it, though: "Jesus" ranks fairly low on these lists, indicating the preferred name for him is more formal Greek title rather than the Hebrew name.

- Key words associated with the groups's doctrinal commitments rank high throughout the sample: "meeting," "restoration," "Bible," congregation," and "new," which appears close to "testament" in the 1976 issue.

- Unique appearances tend to be concentrated in the later issues. The 1960 issue coincides with the presidential election mentioned above, providing an unusually high prevalence of the word, "religious," which is concentrated in article arguing that opposition to a Catholic candidate is not an example of "religious prejudice," as Kennedy himself termed it. 

- Meanwhile, the 1976 issue features a number of articles reflecting on the legacy and future of the Restoration Movement, which broadly applies to Churches of Christ and other groups arising out of the Stone-Campbell merger in the 19th century. Thus the unusually high prevalence of those words, as well as "churches" and, just below that, "unity." 

- The patriarchal nature of the movement is clear. "Brother" and "man" or "men" appear often, likely as stand-ins for "people" but also likely including references to the roles of men in worship – a position that came under increasing pressure as the century moved along.

- Likewise, the movement's silence on civil rights and other questions revolving around the oppression of Black people is clear: no words among the Top 100, not even in 1976, are obviously connected to equality, rights, justice, or race.