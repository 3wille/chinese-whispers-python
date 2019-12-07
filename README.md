# Chinese Whispers for Python

This is an implementation of the [Chinese Whispers](https://doi.org/10.3115/1654758.1654774) clustering algorithm in Python. Since this library is based on [NetworkX](https://networkx.github.io/), it is simple to use.

[![Build Status][travis_ci_badge]][travis_ci_link] [![PyPI version][pypi_badge]][pypi_link]

[pypi_badge]: https://badge.fury.io/py/chinese-whispers.svg
[pypi_link]: https://pypi.python.org/pypi/chinese-whispers
[travis_ci_badge]: https://travis-ci.org/nlpub/chinese-whispers-python.svg
[travis_ci_link]: https://travis-ci.org/nlpub/chinese-whispers-python

Given a NetworkX graph `G`, this library can [cluster](https://en.wikipedia.org/wiki/Cluster_analysis) it using the following code:

```python
from chinese_whispers import chinese_whispers
chinese_whispers(G, weighting='top', iterations=20)
```

As the result, each node of the input graph is provided with the `label` attribute that stores the cluster label.

More usage examples are available in the [sample notebook](samples.ipynb).

In case you require higher performance, please consider our Java implementation that also includes other graph clustering algorithms: <https://github.com/nlpub/watset-java>.

## Citation

* [Ustalov, D.](https://github.com/dustalov), [Panchenko, A.](https://github.com/alexanderpanchenko), [Biemann, C.](https://www.inf.uni-hamburg.de/en/inst/ab/lt/people/chris-biemann.html), [Ponzetto, S.P.](https://www.uni-mannheim.de/dws/people/professors/prof-dr-simone-paolo-ponzetto/): [Watset: Local-Global Graph Clustering with Applications in Sense and Frame Induction](https://doi.org/10.1162/COLI_a_00354). Computational Linguistics 45(3), 423&ndash;479 (2019)

```bibtex
@article{Ustalov:19:cl,
  author    = {Ustalov, Dmitry and Panchenko, Alexander and Biemann, Chris and Ponzetto, Simone Paolo},
  title     = {{Watset: Local-Global Graph Clustering with Applications in Sense and Frame Induction}},
  journal   = {Computational Linguistics},
  year      = {2019},
  volume    = {45},
  number    = {3},
  pages     = {423--479},
  doi       = {10.1162/COLI_a_00354},
  publisher = {MIT Press},
  issn      = {0891-2017},
  language  = {english},
}
```
