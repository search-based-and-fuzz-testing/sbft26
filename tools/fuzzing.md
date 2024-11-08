---
title: SBFT'25 Fuzzing Competition Instructions
layout: md
---

# Fuzzing Competition

We invite you, researchers, practitioners, and hobbyists, to submit your fuzzer to the *annual SBFT Fuzzing Competition!*

This year, we plan to score submissions based on a new scoring system: "novelty coverage", a coverage metric we introduce to score for fuzzers which explore *atypical code regions*.

Concretely, a fuzzer's novelty coverage score is the sum of its edge scores, where each edge score is: 

```math
(number of fuzzers which did not discover this edge) × 
 (fraction of trials of this fuzzer which discovered this edge) 
```

If all fuzzers discover an edge, the edge has zero points; if only one fuzzer discovers an edge, it has maximum points; if only a few of the fuzzer's trials discover that edge, then it will get a very small fraction of those points. In local experiments, we already find interesting results, e.g. regressions in AFL++'s discovery of some edges vs. AFL, using this metric.

## Competition Process

Contestants this year, guided by this scoring system, should **submit open-source fuzzers** which *consistently discover edges which have so far evaded discovery by COTS fuzzers*. In other words, modifications to existing fuzzers may not be enough -- we are biased to *novelty*! As baselines, we select *AFL++, Centipede, LibAFL, and libFuzzer*.

In addition to submitting a fuzzer, contestants must also submit an **OSS-Fuzz target** which is *not yet in Fuzzbench*. We encourage contestants to submit targets for which their fuzzers are capable of finding edges that are otherwise difficult to find.

To take part, [register your submission](https://forms.gle/X559Fs36nv1w6M2x9){:target="_blank"} by December 6th, then **provide your submission as a pull request** to the [Fuzzbench repository](https://github.com/google/fuzzbench/pulls){:target="_blank"} by January 6th. Then, provide your tool report by February 4th.

We wish all competitors the best of luck and look forward to their submissions!

<!-- ## tl;dr

* Express your interest [here](https://forms.gle/pwxtqgEaN724NESC9) (Deadline: **AoE Friday 01 Dec 2023**).
* Write a fuzzer for C/C++ programs (or choose an existing fuzzer and _make your own novel modifications_).
* Maximize the mutation score and coverage achieved in 23 hours.
* Integrate fuzzer into [FuzzBench](https://google.github.io/fuzzbench/getting-started/adding-a-new-fuzzer/) (Deadline: **AoE Friday 28 Dec 2023**).
* Competition results will be reported live at SBST’24. -->

## Timeline
* **December 6th: Registration deadline.**
* December 9th: Acceptance notification
* **January 6th: First PR deadline**
* January 13th: Preliminary results revealed
* **January 20th: Second PR deadline (e.g., for bugfixes/improvements)**
* January 28th: Final results revealed
* **February 4th: Camera-ready tool report deadline**
* April 27th: Official results and **tool presentations** live at SBFT'25


## Benchmarking Platform
Regarding fuzzer submissions: Rather than giving concrete instructions on how your fuzzer must be developed, we instead simply say that fuzzers must be Fuzzbench-compatible and general-purpose (that is, you may not insert code which unfairly accesses information about benchmarks). Refer to [the documentation](https://google.github.io/fuzzbench/getting-started/adding-a-new-fuzzer/){:target="_blank"} for details. *You may submit previously published fuzzers, provided that you are the authors of the corresponding fuzzer*.

Regarding benchmark submissions: the benchmarks must be compatible with the baseline fuzzers listed, that is: *AFL++, Centipede, LibAFL, and libFuzzer*. These benchmarks **must be existing OSS-Fuzz targets, without unnecessary modification**.

## Prizes and awards
TBA

## Organizers
The fuzzing competition is organized jointly by the [Addison Crump](https://addisoncrump.info){:target="_blank"}, [Matteo Leonelli](https://leonelli.github.io){:target="_blank"}, and [Sahil Sihag](https://cispa.de/en/people/c01sasi){:target="_blank"}, of [CISPA Helmholtz Center for Information Security](https://cispa.de/en){:target="_blank"}, Germany.
