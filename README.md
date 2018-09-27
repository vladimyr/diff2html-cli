# diff2html-cli

[![Codacy Quality Badge](https://api.codacy.com/project/badge/Grade/e6139937d72f40ed8b3920d53c74298a)](https://www.codacy.com/app/rtfpessoa/diff2html-cli?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=rtfpessoa/diff2html-cli&amp;utm_campaign=Badge_Grade)
[![Codacy Coverage Badge](https://api.codacy.com/project/badge/Coverage/e6139937d72f40ed8b3920d53c74298a)](https://www.codacy.com/app/rtfpessoa/diff2html-cli?utm_source=github.com&utm_medium=referral&utm_content=rtfpessoa/diff2html-cli&utm_campaign=Badge_Coverage)
[![Circle CI](https://circleci.com/gh/rtfpessoa/diff2html-cli.svg?style=svg)](https://circleci.com/gh/rtfpessoa/diff2html-cli)
[![Dependency Status](https://dependencyci.com/github/rtfpessoa/diff2html/badge)](https://dependencyci.com/github/rtfpessoa/diff2html)

[![npm](https://img.shields.io/npm/v/diff2html-cli.svg)](https://www.npmjs.com/package/diff2html-cli)
[![David](https://img.shields.io/david/rtfpessoa/diff2html-cli.svg)](https://david-dm.org/rtfpessoa/diff2html-cli)
[![David](https://img.shields.io/david/dev/rtfpessoa/diff2html-cli.svg)](https://david-dm.org/rtfpessoa/diff2html-cli)

[![node](https://img.shields.io/node/v/diff2html-cli.svg)]()
[![npm](https://img.shields.io/npm/l/diff2html-cli.svg)]()
[![npm](https://img.shields.io/npm/dm/diff2html-cli.svg)](https://www.npmjs.com/package/diff2html-cli)
[![Gitter](https://badges.gitter.im/rtfpessoa/diff2html.svg)](https://gitter.im/rtfpessoa/diff2html?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

Diff to Html generates pretty HTML diffs from unified and git diff output in your terminal

## Features

* Unified diff and Git diff input

* `line-by-line` and `side-by-side` diff

* new and old line numbers

* inserted and removed lines

* GitHub like style

* Code syntax highlight

* Line similarity matching

## Online Example

> Go to [Diff2HTML](https://diff2html.xyz/)

## Distributions

* [WebJar](http://www.webjars.org/)

* [Node Module](https://www.npmjs.org/package/diff2html)

* [Bower Package](http://bower.io/search/?q=diff2html)

* [Node CLI](https://www.npmjs.org/package/diff2html-cli)

* Manually download and import `rtfpessoa/diff2html/dist/diff2html.min.js` into your page

## Setup

    npm install -g diff2html-cli

## Usage

    Usage: diff2html [options] -- [diff args]

    Options:
      -s, --style                       Output style   [choices: "line", "side"] [default: "line"]
      --sc, --synchronisedScroll        Synchronised horizontal scroll   [choices: "enabled", "disabled"] [default: "enabled"]
      --su, --summary                   Show files summary   [choices: "closed", "open", "hidden"] [default: "closed"]
      --lm, --matching                  Diff line matching type   [choices: "lines", "words", "none"] [default: "none"]
      --lmt, --matchWordsThreshold      Diff line matching word threshold   [default: "0.25"]
      --lmm, --matchingMaxComparisons   Diff line matching maximum line comparisons of a block of changes [default: 2500]
      --hwt, --htmlWrapperTemplate      Path to custom template to be rendered when using the "html" output format [string]
      -f, --format                      Output format   [choices: "html", "json"] [default: "html"]
      -d, --diff                        Diff style   [choices: "word", "char"] [default: "word"]
      -i, --input                       Diff input source   [choices: "file", "command"] [default: "command"]
      -o, --output                      Output destination   [choices: "preview", "stdout"] [default: "preview"]
      -u, --diffy                       Upload to diffy.org   [choices: "browser", "pbcopy", "print"]
      -F, --file                        Send output to file (overrides output option)   [string]
      --version                         Show version number
      -h, --help                        Show help

    Examples:
      diff2html -s line -f html -d word -i command -o preview -- -M HEAD~1
          -> diff last commit, line by line, word comparison between lines,previewed
             in the browser and input from git diff command
      diff2html -i file -- my-file-diff.diff
          -> reading the input from a file
      diff -u file1.txt file2.txt | diff2html
          -> reading diff from stdin
      diff2html -f json -o stdout -- -M HEAD~1
          -> print json format to stdout
      diff2html -F my-pretty-diff.html -- -M HEAD~1
          ->  print to file
      diff2html -F my-pretty-diff.html --hwt my-custom-template.html -- -M HEAD~1
          ->  print to file using custom markup
              templates can include the following variables:
                `<!--diff2html-css-->` - writes default CSS to page
                `<!--diff2html-js-ui-->` - writes default JavaScript UI scripts to page
                `//diff2html-fileListCloseable` - writes code to support selected list interaction, must be within a <script> block
                `//diff2html-synchronisedScroll` - writes code to support selected scroll interaction, must be within a <script> block
                `<!--diff2html-diff-->` - writes diff content to page

    © 2014-2016 rtfpessoa
    For support, check out https://github.com/rtfpessoa/diff2html-cli

> NOTE: notice the `--` in the examples

## Contributions

This is a developer friendly project, all the contributions are welcome.
To contribute just send a pull request with your changes following the guidelines described in `CONTRIBUTING.md`.
I will try to review them as soon as possible.

## License

Copyright 2014-2016 Rodrigo Fernandes. Released under the terms of the MIT license.

## Thanks

This project is inspired in [pretty-diff](https://github.com/scottgonzalez/pretty-diff) by [Scott González](https://github.com/scottgonzalez).

---
