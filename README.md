# Python project template

A somewhat complete Python project template with packaging and testing support.


## Usage

Fork this project and create your Python code under the `src` directory.
Run `grep package_name` to know where to update the name of your package.
Projects with a single package should probably be named the same as the package.

Go through `setup.cfg` and see if you'd wish to update something there.

Freeze the dependencies on `dev_dependencies.txt`.


Versioning
----------

This template always generates version 0.1.0 for the Python project. Make sure
to change `tox.ini` to output the correct version during tests.


Packaging with `setuptools`
---------------------------

Packaging is done with `setuptools` using `pyproject.toml` in and `setup.cfg`.
Transitioning to a project fully on `pyproject.toml` would require eitheri
switching to Poetry or wait for `setuptools` to addapt.


Testing
-------

With Pytest, MyPy, Tox, coverage and generation of HTML reports.
Coverage is currently buggy but I have spent too much time in this for
the moment. To run the tests simply run:

    tox


Configuration
-------------

It is hard to keep all configuration in one file when the Python packaging
standards are changing so quickly. To keep compatible back to at least Python
3.6, some compromises need to be made. Most of the configuration is done in
`setup.cfg` and only what is absolutely necessary is done in other files.


Installation
------------

Running `pip install .` will install the project from source, and `pip install
-e .` does not work for the moment. This installs `project-name` and a package
called `package_name`.


CI
--

Still deciding whether to split the CI into separate repositories. Currently the
