# News #
**12 Jun 2010** - iniparse-0.4 released
  * Fixed pickling and multiprocessing bugs
  * Enabled auto-addition of config attributes via square bracket syntax

**17 Apr 2010** - iniparse-0.3.2 released
  * Utility function to tidy INI files
  * Ability to change comment syntax for parsing Mercurial config files
  * Added ConfigParser exceptions and constants to the top-level iniparse module

**2 Mar 2009** - iniparse-0.3.1 released
  * Fix empty-line handling bugs introduced in 0.3.0

**27 Feb 2009** - iniparse-0.3.0 released
  * Fix handling of continuation lines
  * Fix DEFAULT handling
  * Fix picking/unpickling

**6 Dec 2008** - iniparse-0.2.4 released
  * Updated to work with Python-2.6 (Python-2.4 and 2.5 are still supported)
  * Support for files opened in unicode mode
  * Fixed Python-3.0 compatibility warnings
  * Minor API cleanup

[Full Changelog](http://code.google.com/p/iniparse/source/browse/trunk/Changelog)

# Introduction to iniparse #

`iniparse` is a INI parser for [Python](http://www.python.org) which is:

  * **Compatiable with [ConfigParser](http://docs.python.org/lib/module-ConfigParser.html)**: Backward compatible implementations of `ConfigParser`, `RawConfigParser`, and `SafeConfigParser` are included that are API-compatible with the Python standard library. They pass all the unit tests included with Python.

  * **Preserves structure of INI files**: Order of sections & options, indentation, comments, and blank lines are preserved as far as possible when data is updated.

  * **More convenient**: Values can be accessed using dotted notation (`cfg.user.name`), or using container syntax (`cfg['user']['name']`).

It is very useful for config files that are updated both by users and by programs, since
it is very disorienting for a user to have her config file completely rearranged whenever
a program changes it.  `iniparse` also allows making the order of entries in a config file significant,
which is desirable in applications like image galleries.

# More Information #

  * UsageExamples
  * [PyPI / Cheese Shop](http://www.python.org/pypi/iniparse/)
  * UpgradeNotes for people using `cfgparse-0.1`