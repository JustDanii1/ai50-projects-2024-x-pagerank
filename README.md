# PageRank

A solution to **Project 2 — PageRank** from Harvard's **CS50's Introduction to Artificial Intelligence with Python**.

## About

This project implements the **PageRank algorithm**, which is used to estimate the importance of web pages based on the links between them.

The project uses two approaches to calculate PageRank:

* Random sampling using a Markov Chain
* Iterative calculation using the PageRank formula

The algorithm is based on the idea that a page is more important when it is linked to by other important pages.

## How It Works

The program first builds a corpus representing the links between web pages.

For example:

```text
1.html → 2.html, 3.html
2.html → 3.html
3.html → 2.html
```

The program then calculates the probability of a random surfer visiting each page.

The implementation includes:

```text
transition_model()
sample_pagerank()
iterate_pagerank()
```

### Transition Model

`transition_model()` calculates the probability of moving from the current page to every other page.

The model uses a **damping factor of 0.85** and gives the remaining probability to randomly selecting any page in the corpus.

### Sampling

`sample_pagerank()` estimates PageRank by simulating a random surfer.

The program generates a large number of samples and uses the proportion of visits to each page as its estimated PageRank.

### Iteration

`iterate_pagerank()` calculates PageRank repeatedly using the PageRank formula.

The process starts with every page having the same rank and continues until the values converge within the required threshold.

## Technologies

* Python
* PageRank
* Markov Chains
* Probability
* Graph Algorithms
* Random Sampling
* Iterative Algorithms

## Running the Project

Run the program with one of the provided corpora:

```bash
python pagerank.py corpus0
```

You can also use the other corpus directories included with the project.

The program outputs PageRank values calculated using both sampling and iteration.

Example:

```text
PageRank Results from Sampling
1.html: 0.2223
2.html: 0.4303
3.html: 0.2145
4.html: 0.1329

PageRank Results from Iteration
1.html: 0.2202
2.html: 0.4289
3.html: 0.2202
4.html: 0.1307
```

The two methods should produce similar results when run on the same corpus.

## Project Structure

```text
ai50-projects-2024-x-pagerank/
├── pagerank.py
└── README.md
```

## Course

**CS50's Introduction to Artificial Intelligence with Python**

**Project 2 — PageRank**

Course: [CS50's Introduction to Artificial Intelligence with Python](https://cs50.harvard.edu/ai/?utm_source=chatgpt.com)

Project: [PageRank Project Specification](https://cs50.harvard.edu/ai/projects/2/pagerank/?utm_source=chatgpt.com)
