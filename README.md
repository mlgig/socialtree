This repository contains the postprint, the dataset, the code and interactive news story summaries used in the <i>"SocialTree: Socially Augmented Structured Summaries of News Stories"</i> paper by <i>Gevorg Poghosyan</i> and <i>Georgiana Ifrim</i> presented at the [30th ACM Conference on Hypertext & Social Media (HT '19)](https://human.iisys.de/ht2019/).

The authors' version of the work is available [locally in this repository](./socialtree.pdf). 
It is posted here for your personal use. Not for redistribution. 
The definitive Version of Record was published in Proceedings of 30th ACM Conference on Hypertext & Social Media (HT '19), [https://doi.org/10.1145/3342220.3343668](https://doi.org/10.1145/3342220.3343668).


# Interactive examples
The rendered examples are available also online at [https://gevra.github.io/socialtree/](https://gevra.github.io/socialtree/).
<br>
<br>
The <tt>interactive_summaries</tt> directory contains 6 example story summaries extracted from a multi-source dataset of news. These examples were used for the user study described in the paper.
<br>
The <tt>interactive_summaries_WaPo</tt> directory contains 6 example story summaries from [The Washington Post news article collection](https://trec.nist.gov/data/wapost/).
<br>
Each <tt>.html</tt> file in <tt>interactive_summaries</tt> directory (along with the identically named directory holding the supporting files) presents summaries produced for the same story using different methods.
<br>
<br>
<b>Please make sure your browser doesn't block any javascript running. Some adblockers may block it.</b>



# Dataset(s)
The <tt>data</tt> folder contains the dataset used in the paper.
The a coma-separated file contains <tt>290657</tt> articles in the period from <i>15.07.2015</i> to <i>24.05.2017</i>.
<br>
In addition to the full dataset, <tt>data</tt> directory contains the retrieved articles for each of the queries used in the user study.
<br>
Similarly, <tt>data_WaPo</tt> folder contains <tt>184759</tt> tagged articles of [The Washington Post dataset](https://trec.nist.gov/data/wapost/).

These datasets were produced with <i>Hashtagger+</i> tool described in [this paper](https://doi.org/10.1109/TKDE.2017.2754253) and available at [https://github.com/gevra/hashtagger_plus_offline](https://github.com/gevra/hashtagger_plus_offline).
<br>
A collection of <b><tt>198</tt> million</b> high quality news-related hashtagged tweets used for creating the tagged article datasets is available at [https://doi.org/10.6084/m9.figshare.7932422](https://doi.org/10.6084/m9.figshare.7932422) for <i>15.07.2015</i>-<i>24.05.2017</i> period.

<b>To avoid copyright infingement, we share only the article URL, the tag profile and the query relevance score.</b>
<br>
The code for article crawling and processing is included in the main package.



# Code
The current implementation of SocialTree extraction requires Python 3.6 or later. 
You can install required packages (we recommend using a virtual environment) running 
```pip install -r requirements.txt```.
<br>
Open <tt>socialtree.ipynb</tt> Jupyter notebook and generate summaries from scratch.


This code is using an [implementation](http://www.borgelt.net/eclat.html) of the Eclat algorithm by Christian Borgelt.
<br>
Please, download it [here](http://www.borgelt.net/bin64/eclat) and save it in the <tt>code</tt> directory where <tt>socialtree.ipynb</tt> is located.
<br>
Make sure to change the permissions to make <tt>eclat</tt> executable!


The code comparing to the state-of-the-art methods requires full article text.
<br>
In the next release of the code we'll provide the code for this comparison and also a code for crawling articles using the provided URLs.

