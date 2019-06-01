Network-Code-Repository
=======================

This is a centralized repository for network analysis tools, so to speak,
the ``awesome list`` of network code repositories.

Created during the `OpenNetSci Hackathon <https://opennetsci.github.io/>`_ (May 25-26, 2019), with inputs from
`Nesreen K. Ahmed <http://nesreenahmed.com/>`_,
`Yong-Yeol Ahn <http://yongyeol.com/>`_,
`Tiago P. Peixoto <https://skewed.de/>`_, and
`Jean-Gabriel Young <https://www.jgyoung.ca/>`_,
we host a repository of metadata files for non-standard software.
Our goal is to enhance the exposure of small tools and strengthen the network science community as an ecosystem.

With that, please feel welcomed to send pull requests with the metadata of your code to this repository!

Motivation
----------
The vast majority of software developed by network scientists takes the form of small standalone code bases,
distributed across researcher's homepages, hosting services, and code sharing site like GitLab, Bitbucket or
GitHub. This practice encourages algorithm duplication, reduces reproducibility and favors a fragmentation of
the research community. A good way of addressing these issues would be to create a large, searchable index of
code bases, perhaps in the spirit of `ICON <https://icon.colorado.edu/>`_ or
`networkrepository <http://networkrepository.com/>`_.

Infrastructure
--------------
We maintain a list of JSON files that encode the metadata to each code repository.
While there is no fancy frontend design yet, it is easy to bootstrap the JSON files contained in this repository
into a beautiful-looking website with JavaScript and HTML, or simply generate an awesome plain list with a parser
script. It is also easy to import the files into a database, such as MongoDB or Postgres.

This repository is structured as follows.

* ``library``: contain code that is installable via a package manager, or importable from the language interface.
* ``paper``: contain code that is either a script, demo, or prototype directly from a paper.
* ``standalone``: contain code that can be compiled to a binary application, runnable on an operating system.
* ``web``: contain code to a web application that can be interacted through a browser.

Metadata
~~~~~~~~
Each JSON file consists of the following fields:

* ``name`` - `String`: Name of the repository.

* ``desc`` - `String`: Short description of the repository.

* ``category`` - `String`: Category of the repository; in format of ``$category.$subcategory``, connected by a dot.

* ```links``` - `String[]`: Links to the source code, homepage, or Git repository.

* ``license`` - `Object`
   * ``name`` - Type of license.
   * ``link`` - Link to description.

* ``languages`` - `String[]`: Programming languages supported, or based.
* ``authors`` - `Object[]`
* ``dates`` - `Object`
* ``io`` - `Object`
* ``community`` - `Object`
* ``tags`` - `String[]`


Future Work
-----------
* Add more recipes to the repository!
* Write a script that generates an awesome list out of these JSON files.
