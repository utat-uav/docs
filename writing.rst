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

#. After selecting this virtualenv directory, you'll need to install `sphinx`. You'll need to get `MarkupSafe`, which is a dependency. However, I've experienced issues with installing this package using `pip`. `You'll need to download the binary`_. 
   
   ``MarkupSafe-0.23-cp27-none-win32.whl`` worked for me. Move it into the virtualenv folder and run ``pip install <your-whl-file-name>``. Usually if you type the first couple letters, you can press tab for autocomplete. Afterwards, run ``pip install sphinx recommonmark``.

#. Then, log into (or create) your Github account and go to the UAV docs repository at https://github.com/utat-uav/docs. Click ``fork``. You now have a personal copy of the UAV docs. You can change it at will and it won't affect the production docs. Afterwards, `clone it to your local machine`_. Make sure to clone it inside your virtualenv directory.

#. Use the source for this document (also take a look at other read-the-docs websites such as `Canberra's website`_) as a template for the features that Sphinx offers.

#. Once you're ready, type in ``make html`` to build the docs. You can find the built html pages under ``_build\html``.

#. If it builds correctly, you can `commit and push`_ your changes. Now, the new docs are sitting in your personal repository, but the UAV repository still contains the old docs. To update the UAV repository, go into your personal repo and press the ``New pull request`` button. Fill out the required fields and submit. This will send a request to the UAV repository admins telling them that you want to merge your changes into the main website.

#. The UAV admins will get back to you (soon hopefully, otherwise bug them on Slack) and you may need to make changes and make new commits (no need to make new pull requests, it updates automatically). Once they're satisfied, they'll accept your changes into the main code base and Bob's your uncle.

.. _batch commands: http://www.makeuseof.com/tag/a-beginners-guide-to-the-windows-command-line/
.. _github account: https://github.com/join
.. _Git: https://www.atlassian.com/git/tutorials/what-is-git/
.. _this Trello card: https://trello.com/c/YtKzXflF
.. _Python 2.7: https://www.python.org/downloads/
.. _Virtualenv: https://www.dabapps.com/blog/introduction-to-pip-and-virtualenv-python/
.. _introduction to command line: http://www.makeuseof.com/tag/a-beginners-guide-to-the-windows-command-line/
.. _You'll need to download the binary: http://www.lfd.uci.edu/~gohlke/pythonlibs/#markupsafe
.. _clone it to your local machine: https://help.github.com/articles/cloning-a-repository/
.. _Canberra's website: https://canberrauav.readthedocs.io/en/latest/index.html
.. _commit and push: https://www.atlassian.com/git/tutorials/saving-changes/
