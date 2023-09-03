# AI Website
NASA International Space Apps Challenge Global Nominees (top 10%) - Oct 2022

# HIGH-LEVEL PROJECT SUMMARY
Our project, 0TO∞, is a website that uses AI to extract keywords from items containing scientific or technical information (STI). Increasing accessibility by summarizing lengthy articles, users can quickly locate their desired items based on keywords’ weight (degree * centrality) greater than or equal to 100 in the article. This solves the challenge “Can AI Preserve our Scientific Legacy?” because it reduces the search time of users and improves the efficiency of scientific searches. It’s important because the NASA Technical Report Server (NTRS) contains so much information that most of it is irrelevant to what a user might be looking for!

# LINK TO PROJECT "DEMO"
https://docs.google.com/presentation/d/1As9mIIRdsxgNEFOHAH-aYKAv5u7i92wFFiEd5qj4dOI/edit?usp=sharing

# DETAILED PROJECT DESCRIPTION
Our main programming language for this project was Python, and the framework we used was tensor2tensor. 

When a user selects an item from the NASA Technical Report Server out of the hundreds and thousands of options, our code runs through the article and scans for every word. Here are 2 structures contained in our project:



## Complex Network
Assuming that in a sentence, word A and word B appear at the same time, then a new edge with a weight of 1 will be created in the network (if this edge already exists, the weight will be +1), thus constructing a complex network. Then some topological features of the network are used to measure the importance of words in the network to achieve the purpose of keyword extraction. A measure of close centrality, such as degree, can reflect the importance of nodes in the network. If such words are found, they are extracted and labeled “keywords.” This allows users to get the gist of an article instead of having to skim through it themselves. It saves time and allows for the potential of keywords to be grouped together for an even more efficient search in the future.



## Tensor2Tensor
We use Tensor2tensor package to process passages. It’s a supervised learning frame that requires abundant datasets. 

In terms of future developments, we hope to implement the reverse function of our project by allowing users to search up keywords and find articles related to it, similar to any search engine. We hope to help increase the efficiency and productivity of researchers who may be using NASA’s Technical Report Server and use AI to preserve our scientific legacy!

## SPACE AGENCY DATA
We used lots of open data from NASA: the NASA Technical Report Server, NASA NTRS OpenAPI, and NASA Thesaurus. We wrote a Python web-scraper to download data from the NTRS. The program used the NTRS Open API (https://ntrs.nasa.gov/api/openapi/). It sends a JSON formatted search request and processes the response. It then looks for PDF files available for download with sizes of less than 5MB (to exclude scanned or image-only files) among the results and downloads them. These PDFs are converted into text files and used to train the AI.

## HACKATHON JOURNEY
Being Computer Science and Software Engineering students, we’re naturally interested in AI. AI is only going to become more important as technology advances which is why we want to explore this field. We were inspired by the challenge itself because it intersected science and technology, and we’re incredibly grateful for our Space Apps experience as we learned so much in such a short time span. 

Space Apps was also the first hackathon for most of our members. It was the first time that we had so little time to complete a project which really stressed the importance of teamwork and communication especially as we worked remotely. With each of our strengths being different such as some in frontend and some in backend, we were able to strategically complete our project within the given timeframe using maximum efficiency.

## REFERENCES
We used Python, tensor2tensor, and open data such as the NASA Technical Report Server, NASA NTRS OpenAPI, and NASA Thesaurus (https://ntrs.nasa.gov/api/openapi/).

## TAGS
#API #AI #datascience #artificialintelligence #Python #complexnetwork #keywords #tensorflow #tensor2tensor
