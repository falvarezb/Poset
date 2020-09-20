# Poset

[Partially ordered sets](https://en.wikipedia.org/wiki/Partially_ordered_set) and [Directed graphs](https://en.wikipedia.org/wiki/Directed_graph)
are two sides of the same coin.

This repo shows how to implement a Poset in Java.

## Tech stack

- Java 11
- Junit 5 (unit test library)
- jqwik (property based tests library)
- assertj (test assertions library)
- graphviz (graph visualization library)


## Techniques

Here's a list of some of the techniques used in this repo:

- Use of the Observer pattern to calculate the transitive expansion of the incidence matrix
- Definition of property based tests (PBT) to verify the correctness of the Poset implementation 
- Implementation of a jqwik *Arbitrary* to produce random permutations with replacement in order to
generate Posets for the PBT
- Implementation of a Java *Set*


### How to run the application

The entry point is a Main class that creates a Poset and iterates over the elements in 
topological order.

- `mvn clean test`
- `mvn exec:java -Dexec.mainClass="fjab.poset.Main"`


## Graphviz

Graphviz is used to generate graphs based on **.dot** files.

Here's an example of how to use it:

```
dot -Tpng poset_graph.dot -o outfile.png
```

The file `poset_graph.dot` can be found on `src/main/resources`
