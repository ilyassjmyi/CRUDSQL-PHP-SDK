# # QueryFilterResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | **object** | @Description Array of entities matching the filter conditions @Description For relationship queries, includes related entities based on the filter | [optional]
**page** | **int** | @Description Current page number (1-based indexing) @Description Example: page&#x3D;2 returns the second page of results | [optional]
**page_size** | **int** | @Description Number of items per page (default may vary) @Description Example: page_size&#x3D;20 returns 20 items per page | [optional]
**total** | **int** | @Description Total number of records matching the filter conditions @Description Used for calculating pagination metadata | [optional]
**total_pages** | **int** | @Description Total number of pages based on total records and page size @Description Calculated as ceil(total/page_size) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
