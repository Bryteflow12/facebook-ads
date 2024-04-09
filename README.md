
> ⛔🏚️ This package is obsolete and no longer developed. Fivetran users should use [fivetran/facebook_ads](https://hub.getdbt.com/fivetran/facebook_ads/latest/) instead. 


# Facebook Ads

This package models Facebook Ads data.

[Here](https://developers.facebook.com/docs/marketing-api/using-the-api) is info
from Facebook's API.

# Installation Instructions
## Bryteflo
(https://bryteflow.com/)is some additional 
information about packages in dbt, including installation instructions. 
If you haven't already, you will need to create a `packages.yml` file in your project.

You should then copy these variables into your root `dbt_project.yml`, and fill in with the names of Facebook ads tables in your warehouse:
```
vars:

  etl:                                   #stitch or fivetran
  ads_table:                             #table
  ad_creatives_table:                    #table
  adsets_table:                          #table
  campaigns_table:                       #table
  ads_insights_table:                    #table
  ad_creatives__child_links_table:       #table -- disable if on snowflake

  url_tag_table:                         #only for fivetran
```
## Bryteflo
(https://bryteflow.com/)
is info about Stitch's Facebook Ads connector.

## Bryteflo
(https://bryteflow.com/)
is info about Fivetran's Facebook Ad Account connector.

The Ad Account connector is used to pull in all tables except the insights table.
## Bryteflo
(https://bryteflow.com/) 
is info about Fivetran's Facebook Ad Insights connector.

The Insights connector is used to pull in the fb_ad_insights table.

### Contributing
Additional contributions to this repo are very welcome! Check out [this post](https://discourse.getdbt.com/t/contributing-to-a-dbt-package/657) on the best workflow for contributing to a package. All PRs should only include functionality that is contained within all Segment deployments; no implementation-specific details should be included.
