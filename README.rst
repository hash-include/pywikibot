.. image:: https://secure.travis-ci.org/wikimedia/pywikibot.png?branch=master
   :alt: Travis Build Status
   :target: https://travis-ci.org/wikimedia/pywikibot
.. image:: https://img.shields.io/appveyor/ci/ladsgroup/pywikibot-g4xqx/master.svg?style=flat-square&label=AppVeyor%20CI
   :alt: AppVeyor Build Status
   :target: https://ci.appveyor.com/project/ladsgroup/pywikibot-g4xqx
.. image:: https://codecov.io/gh/wikimedia/pywikibot/branch/master/graphs/badge.svg?branch=master
   :alt: Code coverage
   :target: http://codecov.io/github/wikimedia/pywikibot?branch=master
.. image:: https://codeclimate.com/github/wikimedia/pywikibot-core/badges/gpa.svg
   :alt: Maintainability
   :target: https://codeclimate.com/github/wikimedia/pywikibot-core
.. image:: https://img.shields.io/pypi/v/pywikibot.svg
   :alt: Pywikibot release
   :target: https://pypi.python.org/pypi/pywikibot

Pywikibot
=========

The Pywikibot framework is a Python library that interfaces with the
`MediaWiki API <https://www.mediawiki.org/wiki/Special:MyLanguage/API:Main_page>`_
version 1.14 or higher.

Also included are various general function scripts that can be adapted for
different tasks.

For further information about the library excluding scripts see
the full `code documentation <https://doc.wikimedia.org/pywikibot/>`_.

Quick start
-----------

::

    git clone https://gerrit.wikimedia.org/r/pywikibot/core.git
    cd core
    git submodule update --init
    python pwb.py script_name

Or to install using PyPI (excluding scripts)
::

    pip install -U setuptools
    pip install pywikibot

Our `installation
guide <https://www.mediawiki.org/wiki/Special:MyLanguage/Manual:Pywikibot/Installation>`_
has more details for advanced usage.

Basic Usage
-----------

If you wish to write your own script it's very easy to get started:

::

    import pywikibot
    site = pywikibot.Site('en', 'wikipedia')  # The site we want to run our bot on
    page = pywikibot.Page(site, 'Wikipedia:Sandbox')
    page.text = page.text.replace('foo', 'bar')
    page.save('Replacing "foo" with "bar"')  # Saves the page

-------------------------------------------------------------------------------------------

For more documentation on pywikibot see our `docs <https://doc.wikimedia.org/pywikibot/>`_.

.. include:: pywikibot/DIRECTORIES.rst

Required external programs
---------------------------

It may require the following programs to function properly:

* `7za`: To extract 7z files

.. include:: HISTORY.rst

Contributing
------------

Our code is maintained on Wikimedia's `Gerrit installation <https://gerrit.wikimedia.org/>`_,
`learn <https://www.mediawiki.org/wiki/Special:MyLanguage/Developer_access>`_ how to get
started.

.. include:: CODE_OF_CONDUCT.rst
