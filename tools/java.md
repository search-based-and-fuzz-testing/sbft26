---
title: SBFT'25 Java Competition Instructions
layout: md
---
# Java Test Case Generation Tool Competition

## Timeline (AoE)
* **13 December 2024**: Tool submission.
* 17 January 2025: Notification of the results for structural metrics (code coverage and mutation score).
* 20 January 2025: Notification of the **readability** results.
* **24 January 2025**: Tool report paper (2 pages, references included) deadline.
* 27 April 2025: Official competition results and tool presentation live at SBFT workshop.


## Benchmarking Platform

The infrastructure concerning the Java tool competition is available on GitHub and can also be tried using Docker: [https://github.com/JUnitContest/JUGE](https://github.com/JUnitContest/JUGE).  Please refer to the GitHub repository for instructions.

**Related publication:**

```
@article{Devroey2022,
  author = {Devroey, Xavier and Gambi, Alessio and Galeotti, Juan Pablo and Just, René and Kifetew, Fitsum and Panichella, Annibale and Panichella, Sebastiano},
  title = {JUGE: An infrastructure for benchmarking Java unit test generators},
  journal = {Software Testing, Verification and Reliability},
  pages = {e1838},
  doi = {https://doi.org/10.1002/stvr.1838},
}
```

## Competition Process
In this edition of the Java Tool Competition, continuing the initiative of the previous year's edition, we will consider the *redability* of the gneerated test cases into consideration, besides code coverage and mutation. However, differently from last year's edition where the assessment of test smelliness was carried out with the help of human evaluators, in this year's edition we will delegate this task to AI.

The readability score for a given tool will be calculated as the average readability socre of a randomly selected set of test cases. The average readability score will account for 10% of the final score.

Please not that the tools should be based on search/fuzz techniques for test generation, however incorporating language models in the tool for specific aspects of the test generation task is allowed. It is essential that the tool submitted for evaluation is self contained (e.g., no access to external APIs or servers) and could be executed on normal computers without special needs (e.g., GPUs) that go beyond the computing resources of the competition. For any doubts, please contact us using the addresses provided at the bottom of this page.
### 1. Tool submission (by 13 December 2024 AoE)

Fill the Google form [https://forms.gle/6MevX18ReAst2XMr6](https://forms.gle/6MevX18ReAst2XMr6) and send a zip file with your tool to the organisers (please find their contacts at the end of this page).

### 2. Notification of the results for structural metrics (code coverage and mutation score) (by 17 January 2025 AoE)

We will run our tool on the benchmark and you will receive by email the results of the code coverage and mutation score. You will need these data to write the report (see point 4).

### 3. Notification of readability results (by 20 January 2025 AoE)

We will conduct an evaluation on the readability of your test cases. We will send you the results which you should also discuss in your report.

### 4. Tool report deadline (by 24 January 2025 AoE)

You will need to submit a short report, which will be included in the workshop proceedings.  The report must follow the [IEEE conference format](https://www.ieee.org/conferences/publishing/templates.html).  The page limit is 2 pages including references.  Please submit the PDF to the organisers by the deadline (please find their contacts at the end of this page).

### 5. Results

Finally, the winners will be announced live during the workshop in April.


## Prizes and awards

Will be announced later. Stay tuned!


## Organizers

The Java tool competition is organized jointly by:
* [Fitsum Kifetew](https://kifetew.github.io) -- kifetew AT fbk DOT eu
* [Lin Yun](http://linyun.info/) -- lin_yun AT sjtu DOT edu DOT cn
* [Davide Prandi](https://se.fbk.eu/team/prandi) -- prandi AT fbk DOT eu
