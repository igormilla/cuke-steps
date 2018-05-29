[![Build Status](https://travis-ci.org/raels/cuke-steps.svg?branch=master)](https://travis-ci.org/raels/cuke-steps)

cuke-steps
==========

Cucumber step documentation.

This is a small script that reads Cucumber/Gherkin step definition files and outputs pretty-printed documentation of those steps.  It is meant as a tool for developers to easily see what step definitions already exist.

Currently supported output formats include HTML and Confluence wiki markup.  The documentation can be pushed into a wiki using the [Confluence Publisher Plugin] [cpp] for Jenkins.  Adding outputters for other formats is straightforward.

  [cpp]: https://wiki.jenkins-ci.org/display/JENKINS/Confluence+Publisher+Plugin


Usage
-----

You might install with either the gem command or using bundler.

Assuming you installed with Bundler:

> bundle exec cuke-steps \[options\] &lt;directories...&gt;

In its simplest form:

> bundle exec cuke-steps features/

Supported options:

*  -f FORMAT, --format FORMAT  
   Select output format, either "html" or "cf"

*  -o FILE, --output FILE  
   Output to FILE, default "steps.html" or "steps.cf"

*  -h, --help  
   Usage instructions

This will scan the provided directories for step definition files (*.rb) and output the documentation in the specified file.

The tool supports having step definitions in multiple directories.  It will generate a separate section for each directory specified on the command line, and (if multiple directories are provided) a section containing all step definitions.


License
-----------
BSD
