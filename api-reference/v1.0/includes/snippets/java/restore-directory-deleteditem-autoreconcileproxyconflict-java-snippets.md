---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

// Code snippets are only available for the latest version. Current version is 6.x

GraphServiceClient graphClient = new GraphServiceClient(requestAdapter);

com.microsoft.graph.directory.deleteditems.item.restore.RestorePostRequestBody restorePostRequestBody = new com.microsoft.graph.directory.deleteditems.item.restore.RestorePostRequestBody();
restorePostRequestBody.setAutoReconcileProxyConflict(true);
var result = graphClient.directory().deletedItems().byDirectoryObjectId("{directoryObject-id}").restore().post(restorePostRequestBody);


```