Ways to contribute
==================

* Opening a new ticket to `Issues`_ or by commenting on existing one with new solutions or suggestions
* By improving the project `documentation`_.
* By improving and adding new project `examples`_.
* By contributing code; bug fixes, new features and so on.

.. _Issues: https://github.com/zhinst/zhinst-toolkit/issues
.. _documentation: https://docs.zhinst.com/zhinst-toolkit/en/latest/
.. _examples: https://docs.zhinst.com/zhinst-toolkit/en/latest/examples/index.html

Code contributions
==================

Development environment setup
-----------------------------

- Clone the `zhinst-toolkit` repository

    .. code-block:: sh

        $ git clone https://github.com/zhinst/zhinst-toolkit
        $ cd zhinst-toolkit

- Create a Python virtual environment

- Install the dependencies

    .. code-block:: sh

        $ pip install -r requirements.txt

- Add zhinst-toolkit to `zhinst` package namespace by running the script
  to create a symbolic link between development files and zhinst-package.

    .. note:: 

        Windows: Requires administration privileges.

    .. code-block:: sh
    
        $ python .\scripts\zhinst_toolkit_symlink.py

Running the tests
-----------------

Running all tests
~~~~~~~~~~~~~~~~~

    .. code-block:: sh

        $ pytest

Running lint test
~~~~~~~~~~~~~~~~~

    .. code-block:: sh

        $ tox -e lint

Running typing tests
~~~~~~~~~~~~~~~~~~~~

    .. code-block:: sh

        $ tox -e typing

Running code format check
~~~~~~~~~~~~~~~~~~~~~~~~~

    .. code-block:: sh

        $ tox -e black

Running coverage
~~~~~~~~~~~~~~~~

    .. code-block:: sh

        $ pip install coverage
        $ coverage run -m pytest
        $ coverage html

The report can be seen in your browser by opening `htmlcov/index.html`.

Building the documentation
--------------------------

Zhinst-toolkit uses `Sphinx <https://pypi.org/project/Sphinx/>`_ to build the package documentation.

- Install the package in editable mode

    .. code-block:: sh

        $ pip install -e .

Change to docs directory

    .. code-block:: sh

        $ cd docs

- Install the docs dependencies

    .. code-block:: sh

        $ pip install -r docs/requirements.txt

- Build the HTML documentation along with examples with Sphinx

    .. code-block:: sh

<<<<<<< Updated upstream
        $ make html {remote | local}
=======
        $ make html [local | remote]
>>>>>>> Stashed changes

The generated documentation can be seen in your browser by opening `docs/html/index.html`.

Contributor License Agreement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We appreciate contributions.
