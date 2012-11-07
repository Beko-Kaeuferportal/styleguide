Dan Kubb's Ruby Style Guide
======

You may not like all rules presented here, but they work very well for
me and have helped producing high quality code. Everyone is free to
code however they want, write and follow their own style guides, but
when you contribute to my code, please follow these rules:


Formatting:
=====

* Use ASCII (or UTF-8, if you have to).

* Use 2 space indent, no tabs.

* Use Unix-style line endings.

* Use spaces around operators, after commas, colons and semicolons,
  after { and before }.

* No spaces after (, [ and before ], ).

* Align `when` and `else` with `case`.

* Use an empty line before the return value of a method (unless it
  only has one line), and an empty line between defs.

* Use YARD and its conventions for API documentation. Don't put an
  empty line between the comment block and the def.

* Use empty lines to break up a long method into logical paragraphs.

* Keep lines fewer than 80 characters.

* Strip trailing whitespace.


Syntax:
=====

* Use def with parentheses when there are arguments.

* Never use for, unless you exactly know why.

* Never use then, except in case statements.

* Use when x then ... for one-line cases.

* Use &&/|| for boolean expressions, and/or for control flow. (Rule
  of thumb: If you have to use outer parentheses, you are using the
  wrong operators.)

* Avoid multiline ?:, use if.

* Use parentheses when calling methods with arguments.

* Use {...} when defining blocks on one line. Use do...end for multiline
  blocks.

* Avoid return where not required.

* Use return when returning a variable

* Avoid line continuation (\) where not required.

* Use ||= freely.

* Use OO regexps, and avoid =~ $0-9, $~, $` and $' when possible.


Naming:
====

* Use snake_case for methods.

* Use CamelCase for classes and modules. (Keep acronyms like HTTP,
  RFC, XML uppercase.)

* Use SCREAMING_SNAKE_CASE for other constants.

* Do not use single letter variable names. Avoid uncommunicative names.

* Use consistent variable names. Try to keep the variable names close
  to the object class name.

* Use names prefixed with _ for unused variables.

* Do not use inject in library code. In app code it is ok.

* When defining binary operators, name the argument "other".

* Prefer detect over find, select over find_all.


Comments:
====

* Comments longer than a word are capitalized and use punctuation.
  Use one space after periods.

* Avoid superfluous comments.


The rest:
=====

* Avoid hashes-as-optional-parameters. Does the method do too much?

* Avoid long methods.

* Avoid long parameter lists.

* Use def self.method to define singleton methods.

* Avoid alias when alias_method will do.

* Always freeze objects assigned to constants.

* Use OptionParser for parsing complex command line options and
  ruby -s for trivial command line options.

* Write for 1.9, but avoid doing things you know that will break in 1.8.

* Avoid needless metaprogramming.

* Only give a method one purpose for existing. If you pass in a boolean
  to a method, what you're saying is that this method has two different
  behaviours. Just split it into two single purpose methods. If you have
  to use the words "AND" or "OR" to describe what the method does it
  probably does too much.

* If sections of a method are logically separate by blank lines, then
  that's probably a sign that those sections should be split into separate
  methods.

* Try to keep methods at no more than 10 lines long, and preferably
  5 or less.

General:
====

* Try to have methods either return the state of the object and have
  no side effects, or return self and have side effects. This is
  otherwise known as Command-query separation (CQS):

    http://en.wikipedia.org/wiki/Command-query_separation

* Do not mutate arguments unless that is the purpose of the method.

* Do not mess around in core classes when writing libraries.

* Do not program defensively.
  (See http://www.erlang.se/doc/programming_rules.shtml#HDR11.)

* Keep the code simple.

* Don't overdesign.

* Don't underdesign.

* Avoid bugs.

* Read other style guides and apply the parts that don't dissent with
  this list.

* Be consistent.

* Use common sense.
