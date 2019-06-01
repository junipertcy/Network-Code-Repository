# Network-Code-Repository
This is a centralized repository for network analysis tools, so to speak,
the `awesome list` of network code repositories.

Created during the [OpenNetSci Hackathon](https://opennetsci.github.io/) (May 25-26, 2019), with inputs from
[Nesreen K. Ahmed](http://nesreenahmed.com/),
[Yong-Yeol Ahn](http://yongyeol.com/),
[Tiago P. Peixoto](https://skewed.de/), and
[Jean-Gabriel Young](https://www.jgyoung.ca/),
we host a repository of metadata files for non-standard software.
Our goal is to enhance the exposure of small tools and strengthen the network science community as an ecosystem.

With that, please feel welcomed to send pull requests with the metadata of your code to this repository!

## Motivation
The vast majority of software developed by network scientists takes the form of small standalone code bases,
distributed across researcher's homepages, hosting services, and code sharing site like GitLab, Bitbucket or
GitHub. This practice encourages algorithm duplication, reduces reproducibility and favors a fragmentation of
the research community. A good way of addressing these issues would be to create a large, searchable index of
code bases, perhaps in the spirit of [ICON](https://icon.colorado.edu/) or
[networkrepository](http://networkrepository.com/).

## Infrastructure
We maintain a list of JSON files that encode the metadata to each code repository.
While there is no fancy frontend design yet, it is easy to bootstrap the JSON files contained in this repository
into a beautiful-looking website with JavaScript and HTML, or simply generate an awesome plain list with a parser
script. It is also easy to import the files into a database, such as MongoDB or Postgres.

This repository is structured as follows.

* `library`: contain code that is installable via a package manager, or importable from the language interface.
* `paper`: contain code that is either a script, demo, or prototype directly from a paper.
* `standalone`: contain code that can be compiled to a binary application, runnable on an operating system.
* `web`: contain code to a web application that can be interacted through a browser.

### Metadata

Each JSON file consists of the following fields:

* `name` - _String_: Name of the repository.

* `desc` - _String_: Short description of the repository.

* `category` - _String_: Category of the repository; in the format of `$category.$subcategory`, connected via a dot.

* `links` - _String[]_: Links to the source code, homepage, or Git repository.
* `license` - _Object_
   * `type` - Type of license; typical open source licenses are `MIT`, `Apache-2.0`, or `GNU GPLv3`.
     If you are not sure what to choose, please visit: [choose a license](https://choosealicense.com/)
   * `link` - Link to description. 
     Please paste the link to licenses that have been approved by the Open Source Initiative. 
     For details, please visit: [Licenses by Name](https://opensource.org/licenses/alphabetical) 

* `languages` - _String[]_: Programming languages supported, or based.
* `authors` - _Object[]_:
* `dates` - _Object_:
   * `createdTime` - Created time of the repository; be it a timestamp or just the calendar year.
   * `lastUpdatedTime` - Last updated time of the repository; be it a timestamp or just the calendar year.

* `io` - _Object_:
* `community` - _Object_:
* `tags` - _String[]_:


## Future Work

* Add more recipes to the repository!
* Write a script that generates an awesome list out of these JSON files.
* Build a command-line tool (similar to ``brew`` or ``apt-get``) that can ``search``
  repositories which match user-specified keywords.
