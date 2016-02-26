# Python implementation for the MRPT algorithm

Get started
-----------

To creata a MRPT index instance, simply call 

	index = MRPTIndex(data_to_be_indexed)

A k-nn query can then be made by

	neighbors = index.ann(query_object, k)

The query returns the indices of the approximate nearest neighbors in the original data set.

Advanced
--------

The algorithm can also take optional inputs, the number of random projection trees used in the index ´n_trees´ and the maximum leaf size 
of the trees ´n0´. Simply put, increasing either value improves the accuracy of the approximation, but makes the algorithm (both index 
building and queries) run slower.

	index = MRPTIndex(data, n0=32, n_trees=64)

Extras
------
The file ´mnist_utils.py´ contains python functions to read and visualize the popular mnist data set.