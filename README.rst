.. figure:: https://img.shields.io/badge/version-1.0-blue.svg 

.. figure:: https://img.shields.io/github/license/cicerolp/pmq.svg

====================
Related Repositores 
====================

- `Main Source Code <https://github.com/cicerolp/pmq>`_
- `Supplementary Material <https://github.com/cicerolp/pmq-extras>`_

====================
Authors
====================

- Júlio Toss, Cícero L. Pahins, Bruno Raffin, and João L. Comba

====================
Packed-Memory Quadtree Supplementary Material
====================

Packed-Memory Quadtree: a Cache-Oblivious Data Structure for Visual Exploration Of Streaming Spatiotemporal Big Data
---------------------------

ABSTRACT
---------------------------
The visual analysis of large multidimensional spatiotemporal datasets poses challenging questions regarding storage requirements and query performance. Several data structures have recently been proposed to address these problems that rely on indexes that
pre-compute different aggregations from a known-a-priori dataset. Consider now the problem of handling streaming datasets, in which data arrive as one or more continuous data streams. Such datasets introduce challenges to the data structure, which now has to support dynamic updates (insertions/deletions) and rebalancing operations to perform self-reorganizations. In this work, we present the Packed-Memory Quadtree (PMQ), a novel data structure designed to support visual exploration of streaming spatiotemporal datasets. The PMQ is cache-oblivious to perform well under different cache configurations. We store streaming data in an internal index that keeps a spatiotemporal ordering over the data following a quadtree representation, with support for real-time insertions and deletions. We validate our data structure under different dynamic scenarios and compare to competing strategies. We demonstrate how PMQ can be used to answer different types of visual spatiotemporal range queries of streaming datasets.

====================
Experiments with PMQ
====================


.. contents::

1 Benchmark Insert and Scan
---------------------------

.. _exp20170822165129:

1.1 **DONE** [2017-08-22 Ter]  Experiment *bench_insert_and_scan* ``exp20170822165129``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`./data/cicero/exp20170822165129/exp.rst <./data/cicero/exp20170822165129/exp.rst>`_

1.2 **ANALYSIS** [2017-08-25 Sex]  Twitter dataset *bench_insert_and_scan* ``exp20170825181747``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Testing with twitter distribution of data

`./data/cicero/exp20170825181747/exp.rst <./data/cicero/exp20170825181747/exp.rst>`_

1.3 **DONE** [2017-08-22 Ter]  *bench_insert_and_scan* V.2 ``exp20170907112116``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Old experiment used Rtree\* algorithm, use the quadratic one now.

- Count was not correct in the plots from `exp20170822165129`_

`./data/cicero/exp20170907112116/exp.rst <./data/cicero/exp20170907112116/exp.rst>`_

1.4 **DONE** [2017-09-15 Sex]  Uniform Dataset *bench_insert_and_scan* ``paper``  ``exp20170919161448``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Test insertions with larger inputs

- Rtree (quadratic)

- Btree

- PMQ

- DenseVector

`./data/cicero/exp20170919161448/exp.rst <./data/cicero/exp20170919161448/exp.rst>`_

1.5 **DONE** [2017-09-15 Sex]  Twitter Dataset *bench_insert_and_scan* ``paper``  ``exp20170923193058``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Test insertions with larger inputs

- Rtree (quadratic)

- Btree

- PMQ

- DenseVector

`./data/cicero/exp20170923193058/exp.rst <./data/cicero/exp20170923193058/exp.rst>`_

2 Benchmark Queries region
--------------------------

2.1 **DONE** [2017-08-30 Qua]  *bench_queries_region* ``exp20170830124159``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`./data/cicero/exp20170830124159/exp.rst <./data/cicero/exp20170830124159/exp.rst>`_

- PMQ best on queries with large amount of elements

2.2 **DONE** [2017-09-04 Seg]  Test the refinments levels ``exp20170904153555``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Test the best refinement level to use in Geohash programs. 

`./data/cicero/exp20170904153555/exp.rst <./data/cicero/exp20170904153555/exp.rst>`_

2.3 **DONE** [2017-09-07 Qui]  *bench_queries_region* V.2 ``exp20170907145711``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Test with a larger ammount of data -> 10\*8

- added bulk RTREE loading to the experiments

**NOTE**: Rtree used ineficient boost geogarphic coordinates.

`./data/cicero/exp20170907145711/exp.rst <./data/cicero/exp20170907145711/exp.rst>`_

2.4 **DONE** [2017-09-15 Sex]  *bench_queries_region* V.3 ``paper``  ``exp20170915143003``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Fixed code of Rtree (efficient Cartesian coordinates) .

- More elements in the time window: 6h \* batches of size 1000 ( total of 26.000.000 elements )

`./data/cicero/exp20170915143003/exp.rst <./data/cicero/exp20170915143003/exp.rst>`_

2.5 **DONE** [2017-09-23 Sáb]  *bench_queries_region* Twitter Dataset ``paper``  ``exp20170923144931``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Test queries on real datasets

- Use a time window of 6h \* batches of size 1000  = 26.000.000 elements

`./data/cicero/exp20170923144931/exp.rst <./data/cicero/exp20170923144931/exp.rst>`_

3 Benchmark Insert and Remove
-----------------------------

3.1 **DONE** [2017-09-14 Qui]  *bench_insert_remove_count* ``paper``  ``exp20170914091842``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Test performance of removals in the PMQ. 

`./data/cicero/exp20170914091842/exp.rst <./data/cicero/exp20170914091842/exp.rst>`_

3.2 **DONE** [2017-09-25 Seg]  *bench_insert_remove_count* ``paper``  ``exp20170925155952``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Test performance of removals in the PMQ. 

Use the same window size for every algorithm and set a best remove frequency for BTree and Trees

`./data/cicero/exp20170925155952/exp.rst <./data/cicero/exp20170925155952/exp.rst>`_
