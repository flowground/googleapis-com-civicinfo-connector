# ![LOGO](logo.png) Google Civic Information **flow**ground Connector

## Description

A generated **flow**ground connector for the Google Civic Information API (version v2).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/civicinfo/v2/swagger.json<br/>
Generated at: 2019-05-23T12:13:03+03:00

## API Description

Provides polling places, early vote locations, contest data, election officials, and government representatives for U.S. residential addresses.

## Authorization

This API does not require authorization.

## Actions

### Searches for political divisions by their natural name or OCD ID.

*Tags:* `divisions`

#### Input Parameters
* `query` - _optional_ - The search query. Queries can cover any parts of a OCD ID or a human readable division name. All words given in the query are treated as required patterns. In addition to that, most query operators of the Apache Lucene library are supported. See http://lucene.apache.org/core/2_9_4/queryparsersyntax.html
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### List of available elections to query.

*Tags:* `elections`

#### Input Parameters
* `alt` - _optional_ - Data format for the response.
    Possible values: json.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Looks up political geography and representative information for a single address.

*Tags:* `representatives`

#### Input Parameters
* `address` - _optional_ - The address to look up. May only be specified if the field ocdId is not given in the URL.
* `includeOffices` - _optional_ - Whether to return information about offices and officials. If false, only the top-level district information will be returned.
* `levels` - _optional_ - A list of office levels to filter by. Only offices that serve at least one of these levels will be returned. Divisions that don't contain a matching office will not be returned.
* `roles` - _optional_ - A list of office roles to filter by. Only offices fulfilling one of these roles will be returned. Divisions that don't contain a matching office will not be returned.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Looks up representative information for a single geographic division.

*Tags:* `representatives`

#### Input Parameters
* `levels` - _optional_ - A list of office levels to filter by. Only offices that serve at least one of these levels will be returned. Divisions that don't contain a matching office will not be returned.
* `ocdId` - _required_ - The Open Civic Data division identifier of the division to look up.
* `recursive` - _optional_ - If true, information about all divisions contained in the division requested will be included as well. For example, if querying ocd-division/country:us/district:dc, this would also return all DC's wards and ANCs.
* `roles` - _optional_ - A list of office roles to filter by. Only offices fulfilling one of these roles will be returned. Divisions that don't contain a matching office will not be returned.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Looks up information relevant to a voter based on the voter's registered address.

*Tags:* `elections`

#### Input Parameters
* `address` - _required_ - The registered address of the voter to look up.
* `electionId` - _optional_ - The unique ID of the election to look up. A list of election IDs can be obtained at https://www.googleapis.com/civicinfo/{version}/electionsIf no election ID is specified in the query and there is more than one election with data for the given voter, the additional elections are provided in the otherElections response field.
* `officialOnly` - _optional_ - If set to true, only data from official state sources will be returned.
* `returnAllAvailableData` - _optional_ - If set to true, the query will return the success codeand include any partial information when it is unable to determine a matching address or unable to determine the election for electionId=0 queries.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

## License

**flow**ground :- Telekom iPaaS / googleapis-com-civicinfo-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
