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

With DDEV the following command would be needed:

..  code-block:: bash


TYPO3 - Getting Started Tutorial
Installation
Installing TYPO3 with DDEV



Installing TYPO3 with DDEV
This is a step-by-step guide detailing how to install TYPO3 using DDEV, Docker and Composer.

DDEV is used for local development only.

The scripts used in this guide will install TYPO3 v13.1 which is the latest release of the CMS. If you wish to install the long term support (LTS) release of TYPO3, visit the TYPO3 v12 Installation instructions.


Pre-Installation Checklist
Install Docker - Visit docker.com to download and install the recommended version of Docker for your operating system.
Install DDEV - Follow the DDEV installation guide to install DDEV.
DDEV and Docker need to be installed on your local machine before TYPO3 can be installed. If you need help installing DDEV, support can be found on the DDEV Discord server.

Create the Installation Directory
Create an empty directory to install TYPO3 in and then change into that directory:

mkdir t3example
cd t3example

Create a new DDEV Project
The ddev config command will prompt for information about your project. TYPO3 is in the list of preconfigured projects.

ddev config

# Give the following answers when prompted:

Project name (t3example):

Docroot Location (current directory): public

Project Type [php, typo3, ...] (php): typo3

Docroot Location
Is the folder containing files that have to be reached by the webserver. It contains the vital entry point index.php. The folder is commonly called public.
Project Type
Should always be "typo3"
Note

The PHP version (php_version) should be set manually to the required version in .ddev/config.yaml.

Alternatively you can skip the prompt by supplying all of the required parameters in a single command:

ddev config  --project-type=typo3 --docroot=public --php-version 8.2
