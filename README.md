# MIDAS
_Minimising Inferred Distance to Average Sentences_

### About this repository
This repo contains both code and documentation for my [UTS MDSI iLab 1](http://handbook.uts.edu.au/subjects/36102.html) project. Every component of this project other than the powerpoint presentation is contained within this repository to make it as easy as possible for students undertaking iLab projects in future semesters to fork the repository and continue working on the project. Visitors to this repo who are not MDSI students are welcome to take a look around and fork the repo as well!

## The Project
### Original Specification
In the UK academics submit 'impact case studies' as part of the Research Excellence Framework (REF) assessment of research quality across universities. These case studies were made available openly. Some analysis has been conducted on these, but further opportunities should be available. It may be possible to work with the Research and Innovation Office at UTS to explore the datasets we hold, including text data (from impact statements, funding applications and reports, publications, etc.) and other data such as collaboration networks. Outcomes might help researchers understand their reach, or flag ways that researchers could increase their impact, or foster new successful collaborations. 

Additionally, the Connected Intelligence Centre (CIC) has an existing body of work aiming to use Natural Language Processing tools to parse written works and make suggestions about how to improve those works. One potential outcome for this project could be a similar system to assist researchers writing research grants, impact case studies, etc.

The course outline for this subject can be accessed [here](https://ca.uts.edu.au/wp-content/uploads/2016/02/2016_Spring_36102_update.pdf).

### Project Scope

This iLab project will establish capability for the linguistic analysis of large text datasets. The key tasks which make up this phase of the project are:

- [x] Identify and implement project structure and data science best practice to ensure project can be efficiently paused and handed over between iLab semesters
- [x] Research and document the scope of modern text mining practices, and identify suitable algorithms and approaches to meet client objectives
- [x] Implement and document proof-of-concept analysis to demonstrate the viability of specific approaches
- [x] Build an interactive tool for demonstration 
- [ ] Prepare and deliver presentation for client and stakeholders

The project plan can be viewed [here](./ProjectPlan.md).

## Code

[refimpact](https://github.com/perrystephenson/refimpact) - I wrote some R functions to interface with the REF 2014 Impact Case Studies Database API and turned them into a package. Version 0.1.0 [now available on CRAN](https://cran.r-project.org/package=refimpact).

[Exploration](./Experimentation/exploration.md) - Exploring the dataset and basic text analytics

[Proof of Concept - GloVe distributions as a method of detecting outlier sentences](./Experimentation/GloVeDistributions.md) - Explored the use of the GloVe word embedding model to identify sentences which are potential outliers.

[Proof of Concept - Replacement Sentences](./Experimentation/Replacement.md) - Explored the use of the Word Mover's Distance as a way of identifying potential replacement sentences.

[Tuning GloVe](./Experimentation/Tuning.md) - Trained a series of GloVe models using different dimensions and skip-window lengths and evaluated the resulting model using a standard test set.

[Implementation](./Implementation.md) - A first pass at connecting all of the elements together.

[Web App](./webapp/app.R) - A live demonstration system built using the `shiny` and `shinydashboard` packages. Several computationally expensive steps are completed using the [PrepareWebApp.R](./PrepareWebApp.R) script. A copy of this live demonstration is hosted on [shinyapps.io](http://midas.perrys.cloud/)

## Documentation

[Data Science Hygiene](./Documentation/DataScienceHygiene.md) - an attempt to distil the concept of "good practice" for a rapidly developing field into a single list. Posted to [CIC Around blog](https://15-9203.ca.uts.edu.au/data-science-hygiene/) Friday 16th September (requires UTS login).

[Developing Data Science Hygiene](./Documentation/DevelopingDSH.md) - the process I went through when developing the above document.

[Understanding Text Mining](./Documentation/UnderstandingTextMining.md) - a thorough and detailed set of notes about my understanding of current best practices in text mining.

[Text Mining in R](./Documentation/TextMiningInR.md) - a review of the set of text mining techniques which are currently available in R.

## Presentation

[MIDAS - turning bad sentences into GOLD](https://docs.google.com/presentation/d/145d4z3AJHKXS0dUcVHATFCTsw6XanWpE5hKwrZmhH0g/edit?usp=sharing) - Presentation for iLab assessment on 26 October 2016.

## Additional Information

### Key R packages used in this project

Aside from several packages from Hadley Wickham's tidyverse, I have used the following key packages:

[text2vec](https://cran.r-project.org/web/packages/text2vec/)

[tidytext](https://github.com/juliasilge/tidytext)

### Reference and Inspiration
[API for accessing the Impact Case Studies dataset](http://impact.ref.ac.uk/CaseStudies/APIhelp.aspx)

[Prior analysis of this dataset (Kings College)](http://www.kcl.ac.uk/sspp/policy-institute/publications/Analysis-of-REF-impact.pdf)

[Parsey McParseface (Google's English Language Parser)](https://research.googleblog.com/2016/05/announcing-syntaxnet-worlds-most.html)

[Coursera - Text Mining MOOC](https://www.coursera.org/learn/text-mining)

[Academic Writing Analysis - UTS CIC](https://utscic.edu.au/tools/awa/)

[Global Vectors for Word Presentation - GloVe](http://nlp.stanford.edu/projects/glove/)

[How is GloVe different to word2vec](https://www.quora.com/How-is-GloVe-different-from-word2vec)

[Song Lyrics Across the United States](http://juliasilge.com/blog/Song-Lyrics-Across/)


