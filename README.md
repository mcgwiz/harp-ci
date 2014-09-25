harp-ci
=======

Harp is useful for templated static sites if you find the Node ecosystem saner than the Ruby ecosystem on which Jekyll relies (given you have no desire to become fluent in Ruby). Here I mess around with Harp, Travis CI, and GitHub Pages to:
* evaluate Harp's development exeprience and EJS componentization power, and
* prove that Travis CI can continuously publish a Harp website to GitHub Pages.

The Harp team also provides a guide to [publishing to GitHub Pages](http://harpjs.com/docs/deployment/github-pages). Their approach combines source files and generated files into a single repo.  (GitHub Pages actually treats the gh-pages branch as a Jekyll website, wherein files beginning with underscore are not copied to the actual webroot.  The Harp guide cleverly takes advantage of this by prefixing the source directory's name with an underscore in order to keep it out of the webroot.) The drawbacks to this are that publishing isn't continuous/automated (unless developer runs something like [Grunt](https://www.npmjs.org/package/grunt-harp)) and it is less obvious when source changes were published (developer must still remember to start Grunt). The two-branch approach demonstrated here is free of these issues, while also idiomatically supporting feature branches for bigger content changes.

[![Build Status](https://travis-ci.org/mcgwiz/harp-ci.svg?branch=master)](https://travis-ci.org/mcgwiz/harp-ci)
