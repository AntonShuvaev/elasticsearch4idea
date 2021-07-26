# Elasticsearch Plugin for IntelliJ IDEA

[![Version](https://img.shields.io/jetbrains/plugin/v/org.elasticsearch4idea.svg)](https://plugins.jetbrains.com/plugin/org.elasticsearch4idea)
[![Downloads](https://img.shields.io/jetbrains/plugin/d/org.elasticsearch4idea.svg)](https://plugins.jetbrains.com/plugin/org.elasticsearch4idea)

https://plugins.jetbrains.com/plugin/14512-elasticsearch
https://intellij-elasticsearch.com/

## Documentation

### Add cluster
Click `Add Cluster` button on the explorer toolbar and fill in information:

#### General

![](https://plugins.jetbrains.com/files/14512/592-page/855b5a46-7ac0-42a5-b29e-f865b33e83e3)

- *Settings level*: `Project` for the current project  or `Global` for all projects
- *Name*: a label for the cluster. You can select a color for highlighting tabs and indices tree.
- *URL*: host and port to connect
- *User*: (optional) username for basic auth
- *Password*: (optional) password for basic auth
- *Read-only*: If selected, then all requests except GET require confirmation in Yes/No dialog

#### SSH

![](https://plugins.jetbrains.com/files/14512/592-page/19638c32-4e41-44b4-9139-14c807ad6e5a)

- *Use SSH tunnel*: If selected, then the connection is through SSH tunnel
- *Host*: Host of the remote server
- *Port*: Port of the remote server
- *User name*: username for SSH connection
- *Local port*: port on the local machine. If empty then it will be selected dynamically
- *Auth type*: `Password` to connect with a password, `Key pair` to connect with key pair, `OpenSSH config and authentication agent` to use SSH keys that are managed by a credentials helper application (for example, Pageant on Windows or ssh-agent on macOS and Linux)

Note: When you use SSH tunnel, the URL specified in`General` tab is the URL of the Elasticsearch node for the remote server. So, if you use SSH tunnel to Elasticsearch node URL will be `localhost:{port}`.

#### AWS

![](https://plugins.jetbrains.com/files/14512/592-page/48e3ccab-b86b-4f89-ba4e-caa616a7e289)

If you use AWS Elasticsearch service with enabled [request signing](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-request-signing.html) you need to specify AWS keys and region to send signed requests.

## REST API

Some useful REST API requests available in context menu of clusters and indices:

![](https://plugins.jetbrains.com/files/14512/592-page/5756e125-cb6d-4fa6-acae-21ba123c846a)

![](https://plugins.jetbrains.com/files/14512/592-page/3fd5f624-d0a6-4230-b5ac-995d5fd1fe76)


For executing any REST API request click `Open Rest Console` button on the explorer toolbar, then specify request method, body, URL, and click `Execute request` on the editor toolbar 

![](https://plugins.jetbrains.com/files/14512/592-page/0cbbb9c8-3245-4bc9-a46e-eaa06483daff)

You can browse request history by clicking `Browse Request History` button on the editor toolbar.

## Data browser

For search and CRUD operations click `Open Data Browser` button on the explorer toolbar or double click on an index in the explorer tree

![](https://plugins.jetbrains.com/files/14512/592-page/6ef7512b-e8c7-440c-a834-f144f60b811a)

#### Index pattern 
At the top of the screen is the index pattern text field where you can specify index name, index pattern with wildcard, or indices names separated by a comma.

#### Request body
At the left part of the screen, you can see the request body editor. The request body can be changed manually or it will be changed automatically with actions: pagination, sorting, hiding/showing fields, filtering with Kibana Query Language. Press `⌃ + Enter` to execute the request. The request body panel can be hidden by clicking `Show/Hide Request` button on the editor toolbar or `⌘ + P`. Also, you can change the orientation of the request body panel and response panel in `Settings -> View Position` on the editor top toolbar.

#### Query DSL Autocomplete
Start typing a name of a property or field and code completion will popup automatically as you type. Or you can open a popup with  `⌃Space`.
![](https://plugins.jetbrains.com/files/14512/592-page/97873866-f65c-4d63-9e62-3f80f3594f5a)


#### Response view
There are two views for search response: `Table` and `Text` you can select one in `Settings -> View Mode` on the editor top toolbar.

<img src="https://plugins.jetbrains.com/files/14512/592-page/8e3e4879-8837-4283-b3f0-316bb18feb1f" width="500" />
<img src="https://plugins.jetbrains.com/files/14512/592-page/86a6de6d-c9db-4215-a5cc-dab90a688764" width="500" />

#### Search with Kibana Query Language
You can use the search text field under the toolbar for searching with [Kibana Query Language](https://www.elastic.co/guide/en/kibana/current/kuery-query.html). 
![](https://plugins.jetbrains.com/files/14512/592-page/61132698-d47f-4a71-b667-db313a4d6e70)

Input query and press `Enter`. KQL query will be transformed to Elasticsearch Query replacing `query` in the Request Body, then the request will be executed. Found matches are highlighted in the response view based on Elasticserach highlight functionality that is also applied to the request body.

#### Index structure
You can see the fields of indices in the index structure view. There are two ways to open the index structure view. First is the built-in `Structure` view that can be opened by `⌘ + 7`. The second is the modal view that can be opened by click on the `Index structure` button on the toolbar or `⌘ + F12`.

![](https://plugins.jetbrains.com/files/14512/592-page/6ddfe856-f172-4cd1-b316-841cccef4b4a)

#### Sorting and Hiding fields

You can sort by field or hide/show some fields using the Index structure view.

![](https://plugins.jetbrains.com/files/14512/592-page/181ffde8-0aa4-41bd-bd23-0c25f24cc793)

In the `Table` response view it is also possible to sort by clicking on the column header and hide columns in the header context menu.

#### Creating new documents

To create a new document click `Add New Document` button on the toolbar or press `⌘ + N`.

![](https://plugins.jetbrains.com/files/14512/592-page/dd8aedd5-feff-4c8b-957a-689e96b7323f)

Select the `index` and input `id` and `routing` if it is necessary and input the document body. The `Refresh` option adds `refresh=true` query parameter to the request. See the documentation of [refresh](https://www.elastic.co/guide/en/elasticsearch/reference/7.11/docs-refresh.html). The `Create` option adds `op_type=create` query parameter for "put-if-absent" behavior.

#### Updating documents

In the `Table` view select the row that you want to update. In `JSON` view put the cursor at any line of the search hit that you want to update. Then click `Update Document` button on the toolbar or press `⌘ + B`.

![](https://plugins.jetbrains.com/files/14512/592-page/b1742e51-9211-445a-980e-70bb2c1d8e7a)

The update API supports passing a partial document, which is merged into the existing document. To fully replace an existing document, use the `Add New Document` with unselected `Create` checkbox.

#### Deleting documents

In the `Table` view select the row that you want to delete. In `JSON` view put the cursor at any line of the search hit that you want to delete. Then click `Delete Document` button on the toolbar or press `Delete`.

### Favorites
You can add your favorite search and REST API requests to favorites. When you want to save your current request click `Add  To Favorites` button on the toolbar or press `F3`. 

![](https://plugins.jetbrains.com/files/14512/592-page/47906b6e-8233-4177-9a28-3c320c7dfeed)

- *Name* - name for request
- *Group* - name for a group of favorite requests (optional)
- *Level* - save favorites for all projects or current project
- *Open for* - open request only with selected cluster or any cluster. For the second option, the cluster is taken from the open editor or from the context menu of the cluster tree.
- *Perform request after opening* - if selected then request will be immediately performed after opening request editor

Saved requests are displayed in `Favorites` or the context menu of the cluster tree.

![](https://plugins.jetbrains.com/files/14512/592-page/38cab71a-a040-42aa-82ab-cbef5b0ed8fc)  ![](https://plugins.jetbrains.com/files/14512/592-page/2780b2ae-636b-45bd-91af-04697d45bdd6)

You can open your favorite requests by double click on an item in the `Favorites` view. If the request was saved for a certain cluster it will be opened in a new tab for this cluster. If the request was saved for `Any cluster` it will be opened in a new tab for the same cluster as in the opened request editor. If there is no opened editor the request will not be opened.

Also, you can open favorite requests from the context menu of the cluster tree. There will be available only those requests that were saved for this cluster or for `Any cluster`.

You can edit and delete your favorite requests in the `Favorites` view.

### Preferences
Open  **Preferences | Tools | Elasticsearch**  to configure plugin options.

![](https://plugins.jetbrains.com/files/14512/592-page/e7e8a57b-52b8-4c0e-9e01-11b649a7fd5f)

### Comming soon

- Autocompletion for aggregations
