.. _how_to_docs:

How to Write Documentation
==========================

Prerequisites
-------------

* You should be passably familiar with windows `batch commands`_. Stuff like navigating directories and such.

* You should have some knowledge of git. See `this Trello card`_ for Git installation and tutorials.

.. _how_to_docs_windows:

Windows
-------

Simple steps to set up an environment for writing the documentation on Windows:

#. You'll need a `github account`_.

   If you don't have Git_ installed on your computer, see `this Trello card`_ for instructions.

#. Install `Python 2.7`_. Make sure to get 2.7.12, this is the version we will be using for docs. Don't worry about previous versions of python that you may have installed, we'll be using virtualenv.

#.  Open up a command line terminal and type ``pip``, this should give you something like:

        ``Usage: pip <command> [options]  ...``

    If it doesn't, make sure you have the correct version of Python installed (look in ``C:\Python27``, this is the default install directory).

#. Next, type in ``pip install virtualenv``. Virtualenv_ is a tool for managing different versions of python packages.

#. Navigate to the directory in which you want to put your python virtual environment either in command line, or with File Explorer. If you're using the latter, type ``cmd`` into the folder path bar at the top to open up a terminal at your current location.

#. Type in ``virtualenv -p C:\Python27\python.exe python_env``. You can substitute `python_env` for whatever directory name you prefer. The part after the ``-p`` is the path to the python executable that you want your virtual environment to run.

#. To set this `virtualenv` as your current working environment, navigate into your virtualenv directory and run ``Scripts\activate.bat``. To deselect, run ``Scripts\deactivate.bat``.

#. After selecting this virtualenv directory, run ``pip install sphinx sphinx-autobuild``.

#. Then, clone the documentation repo from github. The current one is 

.. _batch commands: http://www.makeuseof.com/tag/a-beginners-guide-to-the-windows-command-line/
.. _github account: https://github.com/join
.. _Git: https://www.atlassian.com/git/tutorials/what-is-git/
.. _this Trello card: https://trello.com/c/YtKzXflF
.. _Python 2.7: https://www.python.org/downloads/
.. _Virtualenv: https://www.dabapps.com/blog/introduction-to-pip-and-virtualenv-python/
.. _introduction to command line: http://www.makeuseof.com/tag/a-beginners-guide-to-the-windows-command-line/

