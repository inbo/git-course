# Git & GitHub con R 

[![Netlify Status](https://api.netlify.com/api/v1/badges/438c89f1-5c35-49a7-a2b6-2db57ad28824/deploy-status)](https://app.netlify.com/sites/corso-git/deploys)

<!---
<p align="center">
<img src="https://cdn.icon-icons.com/icons2/2351/PNG/512/logo_github_icon_143196.png" width="512" height="512"/>
</p>
-->

## Let's Git started...


Generalmente chi sviluppa software e lo fa di lavoro ha bisogno di uno strumento di controllo delle versioni (i.e. version control system **VCS**), che gli permetta di:

  * Mantenere il codice accessibile
  * controllare il codice
  * ritornare a versioni precedenti del codice se il software si rompe
  * far usare una versione del codice a degli utenti e sbilupparne un'altra contestualmente
  * avere un ambiente collaborativo dove condividere, rivedere e richidere aiuto a utenti o colleghi (questo fa in modo di non lavorare più persone sullo stesso documento)
  * etc.

`git` è la soluzione a ciascuno di questi (emoji sopra) problemi per collaborare con programmatori esperti e, con tutta la buona volontà dopo aver letto questa dispensa, utenti non-IT o mai stati esposti a questi strumenti. In questo documento si predilige un approccio pratico introducendo un _modus operandi_ per essere subito pronti a partire e garantire un impatto immediato, tuttavia si lascia anche spazio ad approfondimenti e "linee parallele" tramite strumenti alternativi e approcci con più respiro rispetto allo stretto scopo della dispensa.


<!---

## Workshop content

### Morning session

We explain the main terminology of Git based on 5 important tasks:

1. Tell the story of your project
1. Travel back in time
1. Experiment with changes
1. Backup your work
1. Collaborate on projects

The morning session is provided using slideshows, split in two main sections:

* [Git](https://inbo.github.io/git-course/static/presentations/git.pdf)
* [GitHub](https://inbo.github.io/git-course/static/presentations/github.pdf)

We like to thank Alice Bartlett, as her [git-for-humans](https://speakerdeck.com/alicebartlett/git-for-humans) talk,  was a major source of inspiration to the course material.

### Afternoon session

The content of the hands-on session in the afternoon depends on the audience of the workshop. Most of the people mainly work in Rstudio and it makes sense to use the integrated git-tools of Rstudio. Others are used to work in the command line or prefer Github Desktop to handle version control. As such, we have three similar sessions, targeted at the different audiences:

* Using Git with [RStudio](https://inbo.github.io/git-course/course_rstudio.html)
* Using Git with GitHub Desktop (old presentation not yet converted)
* Using Git with the command line (old presentation not yet converted)

## Setup

In order to follow the git-course, the main installation requirement is [git](https://git-scm.com/) itself. Further configuration is explained during the tutorial. 

For the git through RStudio, an installation of R and Rstudio is expected as well. For the Github Desktop version, an installed version of [Github Desktop](https://desktop.github.com/).
-->

## Messa in produzione del corso

Il corso è scritto grazie ad una combinazione di documenti  `.md` e `.Rmd` (contenuti in `src`) compilati con `rmarkdown` trasformandoli in documenti `.html`.

```r
rmarkdown::render_site("src")
```

Il render dei files `.html` viene raccolto nella cartella  `/docs`. La cartella è quindi l'oggetto del deployment. [Netlify](https://www.netlify.com/) è un'intuitiva piattforma serverless e basata su git per fare build, deployment e collaborare su web apps. Inoltre rende possibile avere un ambiente di CI/CD con hosting scalabile.


## Contribuisci

Questa dispensa ti darà una mano a familiarizzare con Git + GitHub e RStudio, perchè non provi direttamente a contribuire alla repo cosicchè tu possa sperimentare quello che hai imparato? Inoltre se trovi errori, inesattezze per favore clicca in alto a destra nel sito per essere rediretto all'issue pane e segnalarmelo, se te la senti prova a fare direttamente la correzione tu tramite PR.


## Ringraziamenti 👏

Il set up del progetto viene da [questo corso di git](https://inbo.github.io/git-course/index.html) promosso da [INBO](https://www.vlaanderen.be/inbo/home/), la [cui repo](https://github.com/inbo/git-course). Gli autori a cui vanno i miei ringraziamenti per la contribuzione open source sono [\@stijnvanhoey](https://github.com/stijnvanhoey), [\@peterdesmet](https://github.com/peterdesmet), [\@ThierryO](https://github.com/ThierryO). Si ringraziano anche gli ulteriori contributori ([\@ElsLommelen](https://github.com/ElsLommelen), [\@IPauwels](https://github.com/IPauwels), [\@damianooldoni](https://github.com/damianooldoni)) e le referenze della contribuzione e quelle della mia contribuzione:

webinars:

* [Github and Rstudio management](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN)
* [Collaboration and time travel: version control with git, github and RStudio](https://www.rstudio.com/resources/webinars/collaboration-and-time-travel-version-control-with-git-github-and-rstudio/) (un po' datata, 2016, ma sempre di grande interesse dato l'autore i.e. Wickham)

books (e-books): 

* [happy GIT with R](https://happygitwithr.com/), di gran lunga la risorsa più completa, il miglior punto per iniziare e per rifinire.
* [R Packages](https://r-pkgs.org/git.html), nella sezione del libro di git legata al ciclo di vita dei pacchetti e la condivisione. ottima risorsa in ogni caso, specialmente per git e github come strumento di mantenimento e diffusione dei pacchetti R.

posts:

* [An introduction to Git and how to use it with RStudio](https://r-bio.github.io/intro-git-rstudio/) un'altra grande risorsa che mira all'essenziale. La parte delle PR (Pull Requests) ricalca quella del post.
* [How to Use Git/GitHub with R](https://rfortherestofus.com/2021/02/how-to-use-git-github-with-r/) una risorsa valida con annessiu tutorial. La miglior parte è quella iniziale.
* [Glossario GitHub](https://git-scm.com/docs/gitglossary): dalla documentazione originale estraggo le parole meno comuni e le rinterpeto.

style:

* [rstudio4edu](https://rstudio4edu.github.io/rstudio4edu-book/) aggiungi stile ai documenti R Markdown.
* [STA210-Sp19](https://github.com/STA210-Sp19/website) by Maria Tackett [@matackett](https://github.com/matackett) (Duke University) Per alcuni elementi del file CSS (la parte delle domande) e per aver costruito il miglior corso di statistica su GitHub.


<!--- metti script che richiama i contributori e gli autori tramite API -->

<!---

The source for the Git and GitHub presentations are Google Presentations by @stijnvanhoey and @peterdesmet. In the directory `slideshow`, there are a number of presentations not yet converted to course pages.

-->