
# Master's Thesis: Adapting and Evaluating Buddy Allocators for use Within ZGC

## Overview

This repository hosts the master's thesis "Adapting and Evaluating Buddy Allocators for use Within ZGC" by Casper Norrbin, submitted to Uppsala University in June 2024. The thesis explores the adaptation and evaluation of buddy allocators for potential integration within the Z Garbage Collector (ZGC) in the Java Virtual Machine (JVM), aiming to enhance memory allocation efficiency and minimize fragmentation.

## Thesis Abstract

In the current software development environment, Java remains one of the major languages, powering numerous applications. Central to Java’s effectiveness is the Java Virtual Machine (JVM), with HotSpot being a key implementation. Within HotSpot, garbage collection (GC) is critical for efficient memory management, where one collector is Z (ZGC), designed for minimal latency and high throughput.

ZGC primarily uses bump-pointer allocation, which, while fast, can lead to fragmentation issues. An alternative allocation strategy involves using free-lists to dynamically manage memory blocks of various sizes, such as the buddy allocator. This thesis explores the adaptation and evaluation of buddy allocators for potential integration within ZGC, aiming to enhance memory allocation efficiency and minimize fragmentation.

The thesis investigates the binary buddy allocator, the binary tree buddy allocator, and the inverse buddy allocator, assessing their performance and suitability for ZGC. Although not integrated into ZGC, these exploratory modifications and evaluations provide insight into their behavior and performance in a GC context. The study reveals that while buddy allocators offer promising solutions to fragmentation, they require careful adaptation to handle the unique demands of ZGC.

## Full Thesis

The full thesis can be accessed and downloaded from Diva, the academic archive online. Click the link below to view the thesis:

[Adapting and Evaluating Buddy Allocators for use Within ZGC - Diva Portal](https://www.diva-portal.org/)

## Code

The code developed for this project is located in a separate repository. It can be accessed from the link below:

[Buddy Allocators at Oracle](https://github.com/caspernorrbin/buddy-allocators-zgc)

## Building 

### Prerequisites

Ensure you have the following tools installed:

- LaTeX distribution (e.g., TeX Live, MikTeX)

### Build Instructions

1. Clone the repository
```bash
git clone https://github.com/caspernorrbin/master-thesis-oracle.git
cd master-thesis-oracle
```
2. Build the thesis using the provided Makefile:
```bash
make all
```
3. To clean up auxiliary files generated during the build process:
```bash
make clean
```
4. To open the resulting PDF:
```bash
make open
```
### Additional Makefile Targets
-   `make cycle`: Run the full build cycle (LaTeX, BibTeX, LaTeX twice).
-   `make bib`: Run BibTeX.
-   `make main`: Run a single LaTeX pass.
-   `make diff`: Create a diff between `prev.tex` and the current version using `latexdiff`.