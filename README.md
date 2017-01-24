# Elvis EasyCatalog integration

This package contains everything to setup a complete Elvis <-> EasyCatalog integration. This README describes how to set it up.

## Prerequisites

The integration requires:

* Fully installed and licensed Elvis server. You can obtain Elvis via: https://www.woodwing.com/en/digital-asset-management-system
* InDesign with EasyCatalog. EasyCatalog be downloaded at: https://www.65bit.com

## Elvis setup

These setup instructions assume a single node Elvis environment, for a multi-node environment, apply the settings to each node in the cluster.

* Install Elvis, I used 5.18 but older versions should also work. If Elvis is already started, stop it.
* Place all configuration files supplied in `elvis-config` in your Elvis config folder. Note: If you already have Elvis installed, you might need to merge them with your existing config files.
* Install the excel_import plugin as plugin in the Elvis Server.
* Start the Elvis server.

## Elvis configuration

* Create a folder in Elvis for the test files, I used `/Demo Zone/EasyCatalog`
* Add "Brand", "Body" and "Transmission" to the filters panel.
* Add all "Car" fields to the metadata panel on the right side.
* Add "Full name" to the thumb view.
* Create a new user with restricted permissions to limit the amount of metadata fields in EasyCatalog, setup:
  * Pro or standard user.
  * Assign all capabilities.
  * Assign a rule that points to the previously created folder and give all permissions to that rule.
  * Assign view and edit permission on just the "Car" metadata fields.


## Install InDesign & EasyCatalog

* Install InDesign CC 2017 or later (earlier versions of EasyCatalog might not support Elvis).
* Install EasyCatalog.
* Open InDesign.
* Choose File -> New EasyCatalog Panel... -> New Elvis Data Source.
* Give it a name, e.g. 'Elvis' and supply the required authentication values.
* Hit authenticate, you should see Elvis records including the 'Car' fields.
* Activate the fonts in the `template/fonts` folder.
* Open the template documents in `template` and validate that they open without errors.

## Go demo!

Everything is now setup, you're ready to demo!
