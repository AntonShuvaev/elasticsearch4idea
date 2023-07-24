Change Log
----------
## 2023.2.5 (2023-07-24)
### Added
- [\#118](https://github.com/AntonShuvaev/elasticsearch4idea/issues/118) Added support for `Match Host Exec` in SSH config
### Fixed
- [\#119](https://github.com/AntonShuvaev/elasticsearch4idea/issues/119) Fixed issues with whitespace in URL
- [\#120](https://github.com/AntonShuvaev/elasticsearch4idea/issues/120) Enable 'ssh-rsa' key support in JSch
- IllegalStateException might occur in some cases

## 2023.2.4 (2023-07-12)
### Added
- [\#115](https://github.com/AntonShuvaev/elasticsearch4idea/issues/115) Support for keyboard-interactive SSH authentication
- [\#114](https://github.com/AntonShuvaev/elasticsearch4idea/issues/114) Ability to change size of table cell editing view
- [\#116](https://github.com/AntonShuvaev/elasticsearch4idea/issues/116) Store request history and connection details separately
### Changed
- [\#112](https://github.com/AntonShuvaev/elasticsearch4idea/issues/112) "Open in query console" action is now open request in persistent query console
### Fixed
- [\#117](https://github.com/AntonShuvaev/elasticsearch4idea/issues/117) "Copy index" modal does not scroll properly
- Tree nodes collapse when refreshing the tree
- "IllegalArgumentException: Wrong offsets" might occur in some cases
- "AssertionError: Wrong line separators" might occur in export preview in some cases

## 2023.2.3 (2023-06-15)
### Added
- [\#108](https://github.com/AntonShuvaev/elasticsearch4idea/issues/108) Restored the ability to open an index in the query console, in addition to the ability to open an index in the data browser.
### Fixed
- RuntimeExceptionWithAttachments might occur

## 2023.2.2 (2023-06-12)
### Fixed
- [\#107](https://github.com/AntonShuvaev/elasticsearch4idea/issues/107) Issue when index or alias contains "_search" in name

## 2023.2.1 (2023-06-12)
### Added
- Updated SSH library to support new key exchange algorithms and ED25519 keys
### Fixed
- "Algorithm negotiation fail" error might occur when establishing SSH connection

## 2023.2.0 (2023-06-06)
### Added
- The ability to save KQL queries
- Display of saved KQL queries in the query history popup
- Context help with KQL syntax
- Automatic update of the response view to show the cached response when switching between requests
- [\#104](https://github.com/AntonShuvaev/elasticsearch4idea/issues/104) The ability to zoom in on the result table
- The ability to move multi-level columns in the result table
- Display of saved requests in the request history popup
- Restoring of KQL queries from requests
- A link to the User Experience Survey in the help action group
### Changed
- Indices now open in the editor displaying only the result view, without the request view
- Favorite requests and consoles are now displayed within the cluster node
### Fixed
- The query builder no longer hides when a query is invalid
- Various minor fixes

## 2023.1.6 (2023-04-23)
### Added
- Support for Amazon OpenSearch Serverless

## 2023.1.5 (2023-04-11)
### Added
- Add ability to specify type when importing to ES version before 7
- Action to change default page size
### Changed
- Do not automatically execute queries from opened files after IDE restart
### Fixed
- Message that plugin is not registered might appear after IDE restart
- Credentials might be lost after IDE restart on Windows

## 2023.1.4 (2023-03-29)
### Fixed
- [\#101](https://github.com/AntonShuvaev/elasticsearch4idea/issues/101) Can't connect to Kibana
- ExceptionInInitializerError: NullPointerException might occur in some cases
### Added
- Ability to create Elasticsearch file from project view context menu

## 2023.1.3 (2023-03-14)
### Fixed
- [\#98](https://github.com/AntonShuvaev/elasticsearch4idea/issues/98) Do not urlencode url in the request

## 2023.1.2 (2023-03-13)
### Fixed
- [\#99](https://github.com/AntonShuvaev/elasticsearch4idea/issues/99) "indices" disappeared on some clusters


## 2023.1.1
### Added
- [\#98](https://github.com/AntonShuvaev/elasticsearch4idea/issues/98) Support whitespaces in url 

### Fixed
- [\#99](https://github.com/AntonShuvaev/elasticsearch4idea/issues/99) "indices" disappeared on some clusters
- java.lang.NullPointerException might occur in some cases


## 2023.1.0
### Added
- Recent ES files are stored and can be opened from the "Recent Files"
- Added support for 2023.1
### Changed
- ES toolwindow icon changed to the monochrome version
### Fixed
- [\#97](https://github.com/AntonShuvaev/elasticsearch4idea/issues/97) Moving tabs resets query loosing changes
- ES files are not correctly shown in "Recent Files" list


## 2022.3.4
### Added
- Ability to specify AWS config file along with credentials file
### Fixed
- [\#93](https://github.com/AntonShuvaev/elasticsearch4idea/issues/93) AWS credentials path is not saved between restarts causing NullPointerException
- [\#94](https://github.com/AntonShuvaev/elasticsearch4idea/issues/94) Error on choosing suggestion in Query Console

## 2022.3.3
### Added
- Support "routing" field in import
### Fixed
- "java.lang.VerifyError: Bad type on operand stack" may occur in some cases
- "java.lang.IndexOutOfBoundsException" may occur in some cases
- "JsonParseException Unrecognized token" may occur in some cases

## 2022.3.2
### Fixed
- "IllegalArgumentException: Argument for @NotNull parameter 'c' of com/intellij/ui/ColorUtil.toHex must not be null" might occur in some cases
- "TraceableDisposable$DisposalException: Editor is already disposed" might occur in some cases
### Added
- [\#92](https://github.com/AntonShuvaev/elasticsearch4idea/issues/92) Add "routing" field to the Bulk API export
### Changed
- Changed shortcut for "Submit changes" to "Ctrl+Shift+Enter" (was "Ctrl+Enter") to avoid conflicts with "Execute query"

## 2022.3.1
### Fixed
- Regression in 2022.3.0 where some plugin keybindings block default IDE keybindings
### Added
- [\#91](https://github.com/AntonShuvaev/elasticsearch4idea/issues/91) Added ability to choose custom color for connection
- Added help actions: Open Documentation, Open Changelog, Create GutHub Issue, Copy Email 

## 2022.3.0
### Fixed
- TraceableDisposable$DisposalException might occur in some cases
### Added
- [\#90](https://github.com/AntonShuvaev/elasticsearch4idea/issues/90) Support multiple jump hosts in SSH settings. Support host alias and ProxyJump from ssh config file.
- [\#88](https://github.com/AntonShuvaev/elasticsearch4idea/issues/88) Allow configuring plugin keymaps
- Added support for 2022.3

## 2022.2.3
### Fixed
-  [\#86](https://github.com/AntonShuvaev/elasticsearch4idea/issues/86) Nested values are not updated correctly by table editor
### Added
-  [\#84](https://github.com/AntonShuvaev/elasticsearch4idea/issues/84) Paste request from history without closing the dialog
### Changed
-  [\#84](https://github.com/AntonShuvaev/elasticsearch4idea/issues/84) Search in history dialog shows only matching requests


## 2022.2.2
### Fixed
-  [\#85](https://github.com/AntonShuvaev/elasticsearch4idea/issues/85) "IllegalArgumentException: Illegal base64 character" might occur in some cases

## 2022.2.1
### Fixed
- [\#82](https://github.com/AntonShuvaev/elasticsearch4idea/issues/82) "IllegalArgumentException: Illegal base64 character" might occur on Windows and cause the loss of state
- NullPointerException might occur in some cases
- UninitializedPropertyAccessException might occur in some cases
- IndexOutOfBoundsException: might occur in some cases


## 2022.2.0
### Added
- Show consoles in the explorer tool window
- Compatibility with IntelliJ Platform 2022.2
### Changed
- Favorites moved to the explorer tool window
### Fixed
- Field filter is reset each time the query is run


## 2022.1.10
### Added
- [\#81](https://github.com/AntonShuvaev/elasticsearch4idea/issues/81) ApiKey authorization

## 2022.1.9
### Fixed
- [\#79](https://github.com/AntonShuvaev/elasticsearch4idea/issues/79) Lost Configuration 
- Incorrect column names for fields with dots in CSV export
### Added
- Import from CSV, JSON, Dump files and copying indices
- Support gzip compression for export
- Explorer tree nodes filter
- Added task and ingest pipeline explorer tree nodes 
- Ability to send error reports to the developer

## 2022.1.8
### Fixed
- Delete document with routing not working
- Bulk update with routing not working
### Added
- Support bulk update documents in dialog window
- Ability to update or delete favorite request from editor

## 2022.1.7
### Fixed
- [\#76](https://github.com/AntonShuvaev/elasticsearch4idea/issues/76) Cannot init component state error might occur
- Fixed memory leak
### Changed
- Move favorite requests back to Bookmarks tool window
### Added
- Multilevel table header
- Create, Update, Delete documents in table
- [\#77](https://github.com/AntonShuvaev/elasticsearch4idea/issues/77) Filter indexes, aliases, templates by pattern
- Hiding empty columns in table
- "Filter fields" popup menu to hide fields in result
- Cmd+Enter shortcut for executing request
- AWS Default credential providers chain
- AWS SSO Support (Requires sso login with AWS CLI)

## 2022.1.6
### Fixed
- \#73, \#74 Added checkbox to trust insecure certificate
- \#72 Favorite requests moved to Scratches and Consoles folder
### Added
- \#69 Autocompletion for Kibana REST API

## 2022.1.5
### Fixed
- \#70 The plugin uninstalls automatically

## 2022.1.4
### Added
- Connection to Kibana or AWS OpenSearch Dashboard using them as proxy to ES
- \#66 Support triple quote multi-line strings
- Authorization with Bearer token
- \#65 Authorization with OAuth 2.0 (Client credentials and password grant types supported)
### Changed
- Username and password moved to Basic Auth at Authorization tab
### Fixed
- \#68 Search results are not displayed for ES 8
- Fields in Index Structure view are not updated immediately after show/hide action

## 2022.1.3
### Added
- Connection to Kibana or AWS OpenSearch Dashboard using them as proxy to ES
- \#66 Support triple quote multi-line strings 
- Authorization with Bearer token
- \#65 Authorization with OAuth 2.0 (Client credentials and password grant types supported) 
### Changed
- Username and password moved to Basic Auth at Authorization tab
### Fixed
- Fields in Index Structure view are not updated immediately after show/hide action

## 2022.1.2
### Added
- `Dump` extractor to export index with mappings, settings and aliases
- Autocomplete for mapping
### Changed
- Move tree nodes information panel to separate tool window
### Fixed
- \#64 ClassCastException if parent/child relations have list of children
- Fix KQL nested filter

## 2022.1.0
### Added
- \#45 Autocompletion for Aggregations
- Editors in dialogs have the first line with request to be executed 
### Changed
- Updated Elasticsearch documentation
### Fixed
- \#59 Size: 0 is ignored after switching view
- \#61 Confirm delete window while removing symbols in query input
- \#63 Login to AWS OpenSearch is not working for assume role profiles
- The error "PluginException: Cannot init component state" might occur in some cases
- The error "java.lang.NoClassDefFoundError: NotebookVisualizationUiUtilKt" might occur in some cases

## Version 1.7.1
### Added
- \#54 Support reading AWS credentials from file
- \#56 Added Delimiter-separated values (DSV) extractor
### Fixed
- com.intellij.diagnostic.PluginException when opening plugin settings 
- \#56 CSV extractor doesn't escape comma in arrays
- New line appended when executing request
- Elasticsearch files (.es) opened as plain text files
- \#55, \#57 `_geo_distance` or `_script` sorting removed from request

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