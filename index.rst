Fixie: Cyclus-as-a-Service
============================
Fixie is a xonsh-powered Cyclus cloud. Fixie is thus a collection of services, each
in their own package, which are managed by the top-level ``fixie`` command and package.
Currently available services are:

* ``fixie-creds``: A credentialing service for managing and validating users.
* ``fixie-batch``: A batch execution and queuing service for running Cyclus jobs.
* ``fixie-data``: A service for manganing Cyclus databases and related files.


==================
Installation
==================
You can use ``conda`` or ``pip`` to install any or all of the fixie services, as well
as the top-level fixie package.  For example,


**conda**

.. code-block:: bash

    $ conda install -c conda-forge fixie fixie-batch

**pip**

.. code-block:: bash

    $ pip install fixie fixie-batch

.. note::

    For some services, such as ``fixie-batch``, Cyclus is required. While there
    is a Cyclus package available in conda-forge, there is not one on PyPI, and
    you would need to install Cyclus yourself.


===========
Quick Start
===========
Fixie is a command line application that starts up a Tornado web service. By default,
all services that are installed on a machine are started.  However, you can choose to
run just a subset of services that interest you. For example,

.. code-block:: bash

    $ fixie creds batch
    server:starting fixie http://localhost:8642
    ...

For more information, please see the `Usage page <usage.html>`_.

=========
Contents
=========
**Guides:**

.. toctree::
    :titlesonly:
    :maxdepth: 1

    usage


**Development Spiral:**

.. toctree::
    :titlesonly:
    :maxdepth: 2

    api/index
    devguide/


============
Contributing
============
We highly encourage contributions to rever! If you would like to contribute,
it is as easy as forking the repository on GitHub, making your changes, and
issuing a pull request.
See the `Developer's Guide <devguide.html>`_ for more information about contributing.

=============
Helpful Links
=============

* `Documentation <http://ergs.github.io/fixie-docs>`_
* `GitHub Repository <https://github.com/ergs/fixie>`_
* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

.. raw:: html

    <a href="https://github.com/ergs/fixie" class='github-fork-ribbon' title='Fork me on GitHub'>Fork me on GitHub</a>

    <style>
    /*!
     * Adapted from
     * "Fork me on GitHub" CSS ribbon v0.2.0 | MIT License
     * https://github.com/simonwhitaker/github-fork-ribbon-css
     */

    .github-fork-ribbon, .github-fork-ribbon:hover, .github-fork-ribbon:hover:active {
      background:none;
      left: inherit;
      width: 12.1em;
      height: 12.1em;
      position: absolute;
      overflow: hidden;
      top: 0;
      right: 0;
      z-index: 9999;
      pointer-events: none;
      text-decoration: none;
      text-indent: -999999px;
    }

    .github-fork-ribbon:before, .github-fork-ribbon:after {
      /* The right and left classes determine the side we attach our banner to */
      position: absolute;
      display: block;
      width: 15.38em;
      height: 1.54em;
      top: 3.23em;
      right: -3.23em;
      box-sizing: content-box;
      transform: rotate(45deg);
    }

    .github-fork-ribbon:before {
      content: "";
      padding: .38em 0;
      background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.1));
      box-shadow: 0 0.07em 0.4em 0 rgba(0, 0, 0, 0.3);'
      pointer-events: auto;
    }

    .github-fork-ribbon:after {
      content: attr(title);
      color: #000;
      font: 700 1em "Helvetica Neue", Helvetica, Arial, sans-serif;
      line-height: 1.54em;
      text-decoration: none;
      text-align: center;
      text-indent: 0;
      padding: .15em 0;
      margin: .15em 0;
      border-width: .08em 0;
      border-style: dotted;
      border-color: #777;
    }

    </style>
