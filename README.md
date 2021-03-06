ReproZip Examples
=================

This repository holds some examples and use cases from different domains that showcase [the ReproZip software packing tool](https://www.reprozip.org/).

You'll find more information about each particular example in its associated README.

Examples
--------

*Creating a provenance graph*

* [bash-count](bash-count): A simple bash script that counts the number of pages of an input file.

*Reproducing published results*

* [bechdel-test](bechdel-test): A data analysis experiment that tries to reproduce the claims of an [article](http://fivethirtyeight.com/features/the-dollar-and-cents-case-against-hollywoods-exclusion-of-women/) from FiveThirtyEight.
* [data-polygamy](data-polygamy): A paper published at SIGMOD 2016 whose plots were made reproducible using ReproZip.
* [ising-model](ising-model): A typical simulation in statistical physics, consisting of large scale Monte Carlo simulations followed by an involved statistical analysis of the results.
* [irish-schools](irish-schools): An example from digital humanities, where publication ready graphs and materials are generated from tabular data using R.
* [mongodb-vls](mongodb-vls): A paper published at ICDE 2016 whose plots were made reproducible using ReproZip.

*Extending the original experiment in VisTrails*

* [digits-sklearn](digits-sklearn): A supervised learning and classification experiment written in Python, using [scikit-learn](http://scikit-learn.org/).

*Packing interactive and GUI applications*

* [bus-vis](bus-vis): A Java application for visualizing the Konstanz bus transportation system.

*Reproducing the experiment with a different input*

* [digits-sklearn-opencv](digits-sklearn-opencv): A similar experiment to [digits-sklearn](digits-sklearn), but using [the OpenCV library](http://opencv.org/) to extract the digits from a photograph before predicting their values.

*Archiving and porting web applications*

* [django-blog](django-blog): A simple website built with Django that displays a list of blog posts and allows the admin to edit or post. Despite its simplicity, it represents a realistic small web application using a database (SQLite3).
* [stacked-up](stacked-up): A website called [Stacked Up](http://stackedup.org/), also built with Django, to explore the textbook inventory of Philadelphia public schools. All the data is stored in a PostgreSQL database.

Instructions for reproducing the examples use the [vagrant](http://reprozip.readthedocs.io/en/stable/unpacking.html#the-vagrant-unpacker-building-a-virtual-machine) and the [docker](http://reprozip.readthedocs.io/en/stable/unpacking.html#the-docker-unpacker-building-a-docker-container) unpackers. However, any of the [available unpackers](http://reprozip.readthedocs.io/en/stable/unpacking.html#unpackers) can be used.

Vagrant Machine
---------------

This repository contains a [Vagrantfile](Vagrantfile) that automatically configures a machine with the following examples:

* [bechdel-test](bechdel-test)
* [bus-vis](bus-vis)
* [digits-sklearn](digits-sklearn)
* [digits-sklearn-opencv](digits-sklearn-opencv)
* [irish-schools](irish-schools)
* [stacked-up](stacked-up)

To startup the machine, make sure you have [Vagrant](https://www.vagrantup.com/) and [VirtualBox](https://www.virtualbox.org/) installed, and then run the following:

    $ vagrant up

Note that this will take some time for the first time, since all the dependencies will need to be properly installed. By default, the machine starts in headless mode (no UI visible on the host machine). To boot it with a GUI, uncomment the ``vb.gui = true`` line in the [Vagrantfile](Vagrantfile).

Instructions on how to run each of the examples in this machine are available in their respective pages.

Other Useful Links
------------------

* [Main Website](https://www.reprozip.org/)
* [Documentation](http://reprozip.readthedocs.io/)
* [GitHub Repository](https://github.com/ViDA-NYU/reprozip)
* [Packing and Unpacking with ReproZip](https://www.youtube.com/watch?v=-zLPuwCHXo0): A YouTube video showing how to pack and unpack an experiment using ReproZip.

Team
----

ReproZip is currently being developed at [NYU](http://engineering.nyu.edu/). The team includes:

* [Fernando Chirigati](http://vgc.poly.edu/~fchirigati/)
* [Juliana Freire](http://vgc.poly.edu/~juliana/)
* [Rémi Rampin](https://remram.fr/)
* [Dennis Shasha](http://cs.nyu.edu/shasha/)
* [Vicky Steeves](http://vickysteeves.com/)
