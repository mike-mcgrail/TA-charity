# TA-charity

Splunk add-on to ingest data from third-party charity evaluator APIs. Initial integration is with Charity Navigator from the USA; looking to add more integrations soon.

## Thanks

* Data retrieved from the <a href="https://www.CharityNavigator.org">Charity Navigator</a> API. CHARITY NAVIGATOR and the CHARITY NAVIGATOR logo are registered trademarks of Charity Navigator. All rights reserved. Used with permission.
* Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon"> www.flaticon.com</a>


## Pre-Reqs

1. Register for Charity Navigator API access at https://charity.3scale.net/choose_application_plan
2. If necessary, <a href="https://docs.splunk.com/Documentation/Splunk/8.1.1/Indexer/Setupmultipleindexes">create Splunk events index</a>
3. Install add-on to Splunk HF to ingest data & Search Head(s) for search-time field extractions

## Configure Inputs

1. Navigate to add-on > Inputs
2. Select Create New Input
    * Name = (enter a unique name)
    * Interval = 86400 (default is 1x/day; adjust as desired)
    * Index = (enter an index name)
    * App ID = (ID from pre-req #1)
    * App Key = (key from pre-req #1)

## Configure Macro
1. Navigate to Splunk Settings > Advanced search > macros
2. Update charityindex to match index from pre-req #2 (default is index=charity)