Change Log
----------
## Version 1.7.0
### Added
- \#48 Add templates node to cluster tree
- \#49 Support exporting all documents using Scroll API
- \#50 Support quick jump to table column from Index Structure view
### Fixed
- \#51 Table-view doesn't work for some indices
- \#52 Error when export result of wildcard search
- Query parameters are ignored in search requests
- Some other bugs

## Version 1.6.0
### Added
- Support physical and scratch files, you can keep your requests in project
- Support multiple requests in one console
- Added Elasticsearch Consoles similar to Database Consoles
- Added Update Mapping action in index context menu
- \#48 Added Index Templates action in cluster context menu
### Changed
- Merged Rest API and Search consoles
### Fixed
- \#47 Elasticsearch plugin window does not follow Intellij editor theme
- \#46 HTTP method dropdown in REST query console is truncated
- Fixed some bugs

## Version 1.5.1
### Added
- \#40 Global settings can be shared through settings repository
- \#39 Copy absolute URL when whole URL is selected
- On the editor panel added buttons for changing view mode:
  Only editor / Only response view / Vertical editor and response / Horizontal editor and response
- On the search actions panel added button to enable/disable updating request in editor when executing actions like pagination, KQL filter, sorting, hiding fields
- KQL filter is applied as additional filter to query instead of replacing it
- Added connection timeout setting
### Fixed
- \#41 Invalid update format for Bulk API export
- \#42 Unnecessary data in Bulk API export
- \#43 Multi node connection doesn't work as expected due to missing connection timeout
- Refreshing nodes in cluster tree collapse tree

## Version 1.5.0
- Support connection to multiple nodes
- \#37 Support export to CSV, JSON, Bulk API
- Ability to select rows and copy to clipboard row converted to CSV, JSON or Bulk API
- Support deleting multiple documents
- Fix copying table cell value

## Version 1.4.2
- \#38 Fix: Data browser not working for indices with name containing `_cat`

## Version 1.4.1

- \#35 Fix regression that indices cannot be loaded in some cases
- \#34 Fix SSH connection with password

## Version 1.4.0

- REST API autocomplete
- Elasticsearch Documentation for Query DSL and REST API
- Aliases and nodes in cluster tree
- Fix some bugs

## Version 1.3.0

- Query DSL autocomplete
- Added full json response view mode
- View mode settings moved to toolbar
- View orientation settings moved to Preferences->Tools->Elasticsearch
- Configuring history size
- Fixed some bugs

## Version 1.2.0

- Ability to save requests in Favorites

## Version 1.1.0

- Support SSH
- \#29 Fix regressions:
    1) aggregations are not shown in Data Browser JSON View
    2) request history is missing in Data Browser

## Version 1.0.0

- Search with Kibana Query Language
- Field names autocomplete in KQL query
- Highlighting matches in search results
- Split into Data Browser for searching and REST Console for any requests
- Ability to Hide/Show request in Data Browser
- Show notifications as Balloon Notification instead of Message box
- \#27 Allow newline delimited JSON for Multi search
- \#28 Remove ability to sort by _id

## Version 0.7.2

- \#26 Fix: IDE hangs
- \#25 Fix: host cannot have path
- Fix: in table view Update document dialog opens incorrect document if selection was changed

## Version 0.7.1

- \#24 Fix: fields are not visible for explicit _doc type

## Version 0.7.0

- Ability to Create, Update, Delete documents
- Ability to hide fields
- Index mapping in structure view with ability to sort and hide fields.
- UI enhancements
- Ability to specify mapping in create index dialog

## Version 0.6.0

- Add tree view mode
- \#23 Fix: Wrong line separators \r\n
- Fix adjusting number column width when number >= 100

## Version 0.5.1

- Add search by request history
- \#23 Fix: Unable to parse unicode value: cm_c

## Version 0.5.0

- \#13 Support global (for all projects) cluster configurations
- Add request history
- \#22 Support SSL via IDE build-in "Server Certificates"
- Add shortcuts for Next / Previous page

## Version 0.4.4

- Fix dynamic plugin reloading
- Small UI fixes

## Version 0.4.3

- Fix: Incorrect colors when schemeForCurrentUITheme is used in 2020.3
- Fix: Index and cluster icons are not shown in 2020.3
- \#21 Fix error when mapping without `properties`

## Version 0.4.2

- \#19 Add ability to delete multiple indices at once
- \#19 Delete index dialog has changed to Yes/No instead of typing 'DELETE' word
- \#20 Support _source in table view

## Version 0.4.1

- \#18 Fix error when sorting on Windows

## Version 0.4.0

- Add sorting in table view
- \#17 Convert unicode symbols
- \#16 Possibility to disconnect from ElasticSearch
- \#12 Make result table font same as editor font
- Fix checking for cluster name is unique

## Version 0.3.0

- Add ability to set background color for clusters in tree view
- \#14 Support AWS Elasticsearch Service
- \#15 Allow to set a read-only mode

## Version 0.2.3

- \#10 Fix fatal Error on invalid HTTP host
- \#11 Fix KotlinNullPointerException at MyUIUtils.getPropertiesTableHeaderColor

## Version 0.2.2

- Fix: table header constantly generates events and loads CPU.
- \#9 Support self-signed certificates

## Version 0.2.1

- \#8 Fix java.lang.NoClassDefFoundError: org/apache/commons/io/FileUtils

## Version 0.2.0

- Support horizontal request/response view
- Improve table appearance
- Support pagination
- Show field types in table header
- Support request cancelling
- Support GET with body
- Show loading spinner when request is executing
- Other small fixes and improvements

## Version 0.1.9

- \#5 Fix incorrect displaying Chinese symbols in table view
- Encode request body with UTF-8 instead of ISO 8859-1
- Fix error "Wrong line separators: '\r\n'" on Windows

## Version 0.1.8

- Fix inability to select file in SSL dialog

## Version 0.1.7

- Rename plugin to 'Elasticsearch'

## Version 0.1.6

- Improve table appearance
- Fetch clusters only on demand
- Remove auto-reload clusters
- Support JKS keystore

## Version 0.1.5

- \#3 Fix query URL encoding issue

## Version 0.1.4

- \#2 Support SSL
- Fix using PasswordSafe storage only when credentials are set

## Version 0.1.3

- \#1 Fix freezing when trying to connect to unreachable server

## Version 0.1.1

- Fix number of replicas validation

## Version 0.1.0

- Initial version
- Support connecting to Elasticsearch cluster and performing operations by REST API