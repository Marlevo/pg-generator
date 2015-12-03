# Template Based Scaffolding for PostgreSQL 

<div style="font-size:1.4em; color:#444466; margin-bottom:15px;"><strong>pg-generator</strong> is a command line utility which generates files for each table and schema of a PostgreSQL database.</div>

 * Reverse engineers PostgreSQL database,
 * Executes [nunjucks](https://mozilla.github.io/nunjucks/) templates for each table, schema and for database,
 * Makes database objects available to templates using [pg-structure](http://www.pg-structure.com).

pg-generator takes your burden of manually creating ORM files or any other files which are based on database structure.

## Installation

    $ npm install -g pg-generator

## Sequelize Example

See [sequelize template](http://www.pg-generator.com/builtin-templates/sequelize/) for usage and details.

    $ pgen template sequelize -t sequelize-template
    $ pgen exec sequelize-template -d our_crm -u user -p tOpSeCrEt -t model

First command copies one of the builtin templates (sequelize) into target directory (sequelize-template). Second command generates files based on given template (sequelize-template) into target directory (model).  

## Basic Usage

1. Use `pgen template` to copy one of the builtin templates or create your own template. (You can use base template for starting up.)
1. Use `pgen exec` to create files based on your template.

## Template

Creating a template from scratch is easy. Execute command below:

    $ pgen template base -t my-template

To see a basic example execute following command from shell and examine files in tutorial-example directory. 

    $ pgen template tutorial -t tutorial-template
    
For a full fledged example which we use at Fortibase, see Sequelize Example above. 
    
## Full Documentation

Documentation is available on [pg-generator.com](http://www.pg-generator.com)

## Special Thanks
**pg-structure** is developed under sponsorship of [Fortibase](http://www.fortibase.com) and released as open source. See [license](http://www.pg-generator.com/license/).

Also documentation is auto generated thanks to:

* [MkDocs](http://www.mkdocs.org/) using a [theme](https://github.com/snide/sphinx_rtd_theme) provided by [Read the Docs](https://readthedocs.org/).
* Markdown is generated by [jsdoc-to-markdown](https://www.npmjs.com/package/jsdoc-to-markdown)

## Contributions

* For contribution please send pull requests with tests on [GitHub](https://github.com/ozum/pg-generator.git).
* Send bugs and feature requests to [GitHub Issues](https://github.com/ozum/pg-generator/issues).