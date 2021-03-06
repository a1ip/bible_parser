# BibleParser

[![Build Status](https://travis-ci.org/churchio/bible_parser.svg?branch=master)](https://travis-ci.org/churchio/bible_parser)

This is a Ruby library for parsing different bible XML formats.

For now, it only supports USFX and OSIS, but I hope to add support for other formats also.

## Install

```
gem install bible_parser
```

## Use

You can get the a bible in XML format [here](https://github.com/churchio/open-bibles).

```ruby
require 'bible_parser'

bible = BibleParser.new(File.open('web.usfx.xml'))
verse = bible.books.first.chapters.first.verses.first
# => <Genesis 1:1>
verse.text
# => "In the beginning, God created the heavens and the earth.\n"
```

## License

Copyright (c) Tim Morgan. Licensed MIT. See LICENSE file.
