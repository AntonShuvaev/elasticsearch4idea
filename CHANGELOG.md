Change Log
----------
## Version 0.5.1
- Add search by request history
- \#23 Fix: Unable to parse unicode value: cm_c


## Version 0.5.0
- \#13 Support Global / Project cluster configurations
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