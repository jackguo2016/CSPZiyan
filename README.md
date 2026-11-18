# Graph Coloring in Java · Early Prototype

This coursework prototype explores graph coloring as a constraint satisfaction problem. Given a graph and a fixed number of available colors, the goal is to assign a color to each vertex so that adjacent vertices have different colors.

## What is implemented

- [`src/Main.java`](src/Main.java) reads the color count and comma-separated edges from `src/test.txt`. It prints the values as it reads them and attempts to construct a graph in memory.
- [`src/Node.java`](src/Node.java) stores a vertex ID, its neighbors, and the list of available colors.
- [`src/test.txt`](src/test.txt) is a sample graph. The first line, `colors = 4`, sets the color budget. Each later line, such as `1,2`, defines an undirected edge.

## Inspect the prototype

Run this command from the repository root with a JDK installed to compile the two source files into a separate directory.

```bash
mkdir -p build
javac -encoding UTF-8 -d build src/Main.java src/Node.java
```

The entry point expects `src/test.txt` relative to your working directory. Graph construction is unfinished and can create duplicate nodes. `AC3`, `MRV`, and `LCV` are placeholders for removing inconsistent colors and choosing which vertex and color to try next. The prototype has no coloring output.

[`CSPZiyan1`](https://github.com/jackguo2016/CSPZiyan1) documents the same prototype. For the version that attempts to solve the graph and includes test files, see [`java-graph-coloring-csp`](https://github.com/jackguo2016/java-graph-coloring-csp).
