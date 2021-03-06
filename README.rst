Welcome to the dtw-python package
=================================

Comprehensive implementation of `Dynamic Time Warping algorithms
<https://dynamictimewarping.github.io>`__.

DTW is a family of algorithms which compute the local stretch or
compression to apply to the time axes of two timeseries in order to
optimally map one (query) onto the other (reference). DTW outputs the
remaining cumulative distance between the two and, if desired, the
mapping itself (warping function). DTW is widely used e.g. for
classification and clustering tasks in econometrics, chemometrics and
general timeseries mining.

This package provides the most complete, freely-available (GPL)
implementation of Dynamic Time Warping-type (DTW) algorithms up to
date. It is a faithful Python equivalent of `R's DTW package on CRAN
<https://cran.r-project.org/package=dtw>`__.  Supports arbitrary local (e.g.
symmetric, asymmetric, slope-limited) and global (windowing)
constraints, fast native code, several plot styles, and more.



Documentation
~~~~~~~~~~~~~

Please refer to the main `DTW project homepage
<https://dynamictimewarping.github.io>`__ for the full documentation
and background.

The best place to learn how to use the package (and a hopefully a
decent deal of background on DTW) is the companion paper `Computing
and Visualizing Dynamic Time Warping Alignments in R: The dtw Package
<http://www.jstatsoft.org/v31/i07/>`__, which the Journal of
Statistical Software makes available for free.  It includes detailed
instructions and extensive background on things like multivariate
matching, open-end variants for real-time use, interplay between
recursion types and length normalization, history, etc.

To have a look at how the *dtw* package is used in domains ranging from
bioinformatics to chemistry to data mining, have a look at the list of
`citing
papers <http://scholar.google.it/scholar?oi=bibs&hl=it&cites=5151555337428350289>`__.

Links to prebuilt documentation are available
`for R <http://www.rdocumentation.org/packages/dtw>`__
and
`Python <https://dynamictimewarping.github.io/py-api/html/>`__.

**Note**: **R** is the preferred environment for the DTW
project. Python's docstrings and the API below are generated
automatically for the sake of consistency and maintainability, and may
not be as pretty.


Features
~~~~~~~~

The implementation provides:

-  arbitrary windowing functions (global constraints), eg. the
   `Sakoe-Chiba
   band <http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=01163055>`__
   and the `Itakura
   parallelogram <http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=1162641>`__;
-  arbitrary transition types (also known as step patterns, slope
   constraints, local constraints, or DP-recursion rules). This includes
   dozens of well-known types:

   -  all step patterns classified by
      `Rabiner-Juang <http://www.worldcat.org/oclc/26674087>`__,
      `Sakoe-Chiba <http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=1163055>`__,
      and `Rabiner-Myers <http://hdl.handle.net/1721.1/27909>`__;
   -  symmetric and asymmetric;
   -  Rabiner's smoothed variants;
   -  arbitrary, user-defined slope constraints

-  partial matches: open-begin, open-end, substring matches
-  proper, pattern-dependent, normalization (exact average distance per
   step)
-  the Minimum Variance Matching (MVM) algorithm `(Latecki et
   al.) <http://dx.doi.org/10.1016/j.patcog.2007.03.004>`__

Multivariate timeseries can be aligned with arbitrary local distance
definitions, leveraging the *{proxy}dist* function. DTW itself becomes a
distance function with the *dist* semantics.

In addition to computing alignments, the package provides:

-  methods for plotting alignments and warping functions in several
   classic styles (see plot gallery);
-  graphical representation of step patterns;
-  functions for applying a warping function, either direct or inverse;
-  a fast native (C) core.



Citation
~~~~~~~~

When using in academic works please cite:

* T. Giorgino. Computing and Visualizing Dynamic Time Warping Alignments in R: The dtw Package. J. Stat. Soft., 31 (2009) `doi:10.18637/jss.v031.i07 <https://www.jstatsoft.org/article/view/v031i07>`__.

When using partial matching (unconstrained endpoints via the open.begin/open.end options) and/or normalization strategies, please also cite:

* P. Tormene, T. Giorgino, S. Quaglini, M. Stefanelli (2008). Matching Incomplete Time Series with Dynamic Time Warping: An Algorithm and an Application to Post-Stroke Rehabilitation. Artificial Intelligence in Medicine, 45(1), 11-34. `doi:10.1016/j.artmed.2008.11.007 <http://dx.doi.org/10.1016/j.artmed.2008.11.007>`__


Source code
~~~~~~~~~~~

Releases (stable versions) are available in the `dtw-python project on 
PyPi <https://pypi.org/project/dtw-python/>`__. Development
occurs on GitHub at <https://github.com/DynamicTimeWarping/dtw-python>.


License
~~~~~~~

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.




Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
