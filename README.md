# datasette-edit-tables

[![PyPI](https://img.shields.io/pypi/v/datasette-edit-tables.svg)](https://pypi.org/project/datasette-edit-tables/)
[![Changelog](https://img.shields.io/github/v/release/simonw/datasette-edit-tables?include_prereleases&label=changelog)](https://github.com/simonw/datasette-edit-tables/releases)
[![Tests](https://github.com/simonw/datasette-edit-tables/workflows/Test/badge.svg)](https://github.com/simonw/datasette-edit-tables/actions?query=workflow%3ATest)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/simonw/datasette-edit-tables/blob/master/LICENSE)

Datasette plugin for renaming, deleting and modifying tables.

## Features (planned)

* Rename a table
* Delete a table
* Modify the type of columns in a table
* Add new columns to a table
* Create a new empty table from scratch

## Installation

Install this plugin in the same environment as Datasette.

    $ pip install datasette-edit-tables

## Usage

Navigate to `/-/edit-tables/dbname/tablename` on your Datasette instance to edit a specific table.

Use `/-/edit-tables/dbname` to create a new table in a specific database.


By default only [the root actor](https://datasette.readthedocs.io/en/stable/authentication.html#using-the-root-actor) can access the page - so you'll need to run Datasette with the `--root` option and click on the link shown in the terminal to sign in and access the page.

The `edit-tables` permission governs access. You can use permission plugins such as [datasette-permissions-sql](https://github.com/simonw/datasette-permissions-sql) to grant additional access to the write interface.
