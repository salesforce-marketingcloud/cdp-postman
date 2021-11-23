
> ℹ️   **April 2021 update:** This collection is maintained as a [Postman Public Workspace](https://www.postman.com/salesforce-developers). This makes it easier to install, update and contribute to the collection.<br/>
This repository is dedicated to hosting the setup/contribution documentation and tracking issues.

# CDP APIs for Postman

The current [Postman](https://www.postman.com) collection of consists of 35+ requests for the following Salesforce CDP APIs:

<table>
   <tr>
      <td>
         <ul>
            <li>Profile API</li>
            <li>Query API</li>
            <li>Calculated Insights API</li>
            <li>Metadata</li>
            <li>Ingestion</li>
         </ul>
      </td>
   </tr>
</table>

The collection is divided into 2 API types. 

- **Direct APIs** - allows you to perform some of the Salesforce CDP application tasks programmatically via a Direct API to the underlying data store. This is the preferred approach to API connections.
- **Connect APIs** - The Connect APIs allow users to make the same API calls directly from Salesforce’s connect interface. This allows for these APIs to be called in flows as well.

Calling APIs directly using the non connect method typically offers the best performance. However, there are use cases where that doesn't make sense. Therefore, please be advised that calling CONNECT APIs directly does not conform to the same SLAs that calling the API directly offers.

As new APIs are made available to the CDP, the collection will be expanded to include those.

![Collection Overview](images/collection-overview.png)

**⚠️  Disclaimers:**
- This collection is provided as-is. It's not officially supported by Salesforce or covered by SLAs.
- API documentation is not provided with the collection. Please refer to the [official documentation](https://developer.salesforce.com/docs/atlas.en-us.c360a_api.meta/c360a_api/c360a_api_quick_start.htm).
- To help us better understand usage of the collection, we leverage Google Analytics. If you would like to opt out of the tracking, you can remove the Pre-request Script set at the collection level.

![Tracking Request](images/tracking-request.png)

## Issues and Questions

Report issues and ask questions [here](https://github.com/salesforce-marketingcloud/c360-postman/issues).


## Installation

This collection currently only supports the **Postman desktop app** to connect to CDP with the Salesforce CDP APIs collection. 

- [Install the Collection](install-the-collection.md)

We are evaluating the changes required to support the **Postman web app** as an alternative approch. 


## Additional Documentation

- [Keeping the collection up to date](updating.md)
- [Working With Environments To Connect To Multiple CDP Instances](working-with-environments.md)
- [Contributing](contributing.md)