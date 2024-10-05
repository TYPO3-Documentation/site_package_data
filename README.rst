=======================
TYPO3 Site Package data
=======================

You can load this example data to try out the site package extension.

:Repository:      https://github.com/TYPO3-Documentation/site_package_data
:Belongs to:      https://github.com/TYPO3-Documentation/TYPO3CMS-Tutorial-SitePackage-Code
:Published at:    https://docs.typo3.org/typo3cms/SitePackageTutorial/


Usage
=====

Create a brand-new TYPO3 installation, for example with DDEV and composer:

:ref:`Installing TYPO3 with DDEV <t3start:installation-ddev-tutorial>`

Install the :composer:`t3docs/site-package` extension.

Install the :composer:`t3docs/site-package-data` extension.

Import the Example Site data by running the console command
`vendor/bin/typo3 extension:setup`.

After importing the example data you can safely remove this extension again.

With DDEV the following commands would be needed:

..  code-block:: bash

    ddev composer req t3docs/site-package
    ddev composer req t3docs/site-package-data
    ddev typo3 extension:setup
    ddev composer remove t3docs/site-package-data

