---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: "Syllabus"
---

## Session 1 - Introduction to Bibliometric Methodologies & Indicators

- Introduction to the course
- Bibliometrics Definitions, Uses & Limitations
	- Defining bibliometrics
	- Bibliometrics indicators & analysis
	- Limitations of bibliometrics
- Citation Analysis
	- Citation analysis & limitations
	- Non-normalized citation indicators
		- number of publications
		- number of citations
		- citation rate

### Session 1 Slides:
<iframe src="https://widgets.figshare.com/articles/12631400/embed?show_title=1" width="568" height="351" allowfullscreen="true" frameborder="0"></iframe>

### Session 1 Exercises & Videos

1. Go to <https://notebooks.azure.com> and click **Sign In** to create an account. If you have an existing account with Microsoft or Outlook, you may use it.
2. While signed into your account, go to <https://notebooks.azure.com/clarke-iakovakis/projects/intro-to-bibliometrics>
3. Click the **Clone** button in the upper right corner and clone this project. This will create a duplicate of the project in your own Azure Notebooks projects
4. Click on **Getting Started with Jupyter Notebooks and R.ipynb**
5. Watch the video below to use this notebook. This will introduce you to the Azure Notebooks environment and some basics of using R.

<iframe width="917" height="573" src="https://www.youtube.com/embed/hnFio5WCMJI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

		

## Session 2 - Citation Metrics and Bibliometric Data Sources

- Normalized citation indicators
	- Citation normalization
	- Field normalized citation impact
	- Field classification
	- Relative Citation Ratio
	- Percentiles
- Journal-based indicators
	- Journal Impact Factor
	- CiteScore
	- H-index
	- Pushback and limitations
- Data sources
	- Web of Science & Scopus
	- Dimensions
	- Google Scholar
	- Open Citations Corpus
	- Publish or Perish


### Session 2 Slides
<iframe src="https://widgets.figshare.com/articles/12662906/embed?show_title=1" width="568" height="351" allowfullscreen="true" frameborder="0"></iframe>

## Session 2 Exercises and Video
1. Open the **Bibliometrics Lesson 1.ipynb** file in your Azure Notebook
2. Read the entire document and execute all the code chunks. Watch the below video for help.

<iframe width="904" height="550" src="https://www.youtube.com/embed/kU-ZGNpVlw0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Session 3 - Network Analysis

- Bibliographic Network Analysis Concepts
- Bibliographic Network Analysis Tools
- Centrality, Connectedness, & Clustering

### Session 3 Slides

<iframe src="https://widgets.figshare.com/articles/12698705/embed?show_title=1" width="568" height="351" allowfullscreen="true" frameborder="0"></iframe>

### Session 3 Exercises and Video

#### Network Analysis
1. Navigate to <https://notebooks.azure.com/clarke-iakovakis/projects/intro-to-bibliometrics-network> and clone the notebook into your Azure Notebooks environment.
2. homework01.ipynb is a notebook designed to help you build intuition around centrality measures.
3. homework02.ipynb is a notebook designed to introduce you to some network functions using the **bibliometrix** package in R.

#### VOSviewer
1. Complete steps 1-5 Exercise 1 from Session 2, "Getting article data with Dimensions" at <https://notebooks.azure.com/clarke-iakovakis/projects/intro-to-bibliometrics/html/Bibliometrics%20Lesson%201.ipynb>
2. Click **Export for Bibliometric Mapping** and click **Export.** You will get an email when the export is ready for download. At that point, in Dimensions, click your name in the right hand corner and click Export Center. Click Download to download the file to your computer.
3. Download VOSviewer at <https://www.vosviewer.com/download>, or launch it in your browser using the **Web start** option on that page
4. In VOS Viewer, Go to **File > Map > Create**
5. Choose Create a map based on bibliographic data
6. Choose **Read data from bibliographic database files**
7. Click the **Dimensions** tab and upload the file you downloaded in step 2. Note that this file is also available in the Azure Notebooks for this session at <https://notebooks.azure.com/clarke-iakovakis/projects/intro-to-bibliometrics-network>, called **dimensions_network.csv**
8. To create a Journal co-citation network:
* Under Type of Analysis, click **Co-citation**
* Under Unit of Analysis, click **Cited sources**
* Under Counting Method, click **Fractional counting**
* Choose 30 for the Minimum number of citations of a source. This means that a journal will not be included unless it has at least 30 items pointing to it in this set of results. Click Next.
* Choose the maximum number of sources to be selected allowable. Click Next.
* Review the sources, citations, and total link strength. Click Finish.
* It may warn you that some of the items in the network are not connected to each other. Click Yes to show the largest set of connecting items.
* Play around with the various settings on the right side of the page.
9. Experiment with the other types of visualizations and units of analysis.
10. Read Brett Williams, “Dimensions & VOSViewer Bibliometrics in the Reference Interview,” *code4lib 47*, <https://journal.code4lib.org/articles/14964> with screenshots of this process and suggestions for incorporating it into library reference work.






## Session 4 - Eigenfactor Metrics, Altmetrics, Metrics in Evaluation, & Next Steps

- Eigenfactor Metrics
- Altmetrics
- Metrics in Evaluation & Next Steps

### Session 4 Slides

<iframe src="https://widgets.figshare.com/articles/12739988/embed?show_title=1" width="568" height="351" allowfullscreen="true" frameborder="0"></iframe>
