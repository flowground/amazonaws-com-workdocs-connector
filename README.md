# ![LOGO](logo.png) Amazon WorkDocs **flow**ground Connector

## Description

A generated **flow**ground connector for the Amazon WorkDocs API (version 2016-05-01).

Generated from: https://api.apis.guru/v2/specs/amazonaws.com/workdocs/2016-05-01/swagger.json<br/>
Generated at: 2019-07-08T14:13:30+03:00

## API Description

<p>The WorkDocs API is designed for the following use cases:</p> <ul> <li> <p>File Migration: File migration applications are supported for users who want to migrate their files from an on-premises or off-premises file system or service. Users can insert files into a user directory structure, as well as allow for basic metadata changes, such as modifications to the permissions of files.</p> </li> <li> <p>Security: Support security applications are supported for users who have additional security needs, such as antivirus or data loss prevention. The API actions, along with AWS CloudTrail, allow these applications to detect when changes occur in Amazon WorkDocs. Then, the application can take the necessary actions and replace the target file. If the target file violates the policy, the application can also choose to email the user.</p> </li> <li> <p>eDiscovery/Analytics: General administrative applications are supported, such as eDiscovery and analytics. These applications can choose to mimic or record the actions in an Amazon WorkDocs site, along with AWS CloudTrail, to replicate data for eDiscovery, backup, or analytical applications.</p> </li> </ul> <p>All Amazon WorkDocs API actions are Amazon authenticated and certificate-signed. They not only require the use of the AWS SDK, but also allow for the exclusive use of IAM users and roles to help facilitate access, trust, and permission policies. By creating a role and allowing an IAM user to access the Amazon WorkDocs site, the IAM user gains full administrative visibility into the entire Amazon WorkDocs site (or as set in the IAM policy). This includes, but is not limited to, the ability to modify file permissions and upload any file to any user. This allows developers to perform the three use cases above, as well as give users the ability to grant access on a selective basis using the IAM model.</p>

## Authorization

Supported authorization schemes:
- API Key
## Actions

### DescribeActivities
> Describes the user activities in a specified time period.<br/>

#### Input Parameters
* `Action` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### InitiateDocumentVersionUpload
<blockquote><p>Creates a new document object and version object.</p> <p>The client specifies the parent folder ID and name of the document to upload. The ID is optionally specified when creating a new version of an existing document. This is the first step to upload a document. Next, upload the document to the URL returned from the call, and then call <a>UpdateDocumentVersion</a>.</p> <p>To cancel the document upload, call <a>AbortDocumentVersionUpload</a>.</p></blockquote>

#### Input Parameters
* `Action` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeleteDocument
> Permanently deletes the specified document and its associated metadata.<br/>

#### Input Parameters
* `DocumentId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### GetDocument
> Retrieves details of a document.<br/>

#### Input Parameters
* `DocumentId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### UpdateDocument
> Updates the specified attributes of a document. The user must have access to both the document and its parent folder, if applicable.<br/>

#### Input Parameters
* `DocumentId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### GetDocumentPath
<blockquote><p>Retrieves the path information (the hierarchy from the root folder) for the requested document.</p> <p>By default, Amazon WorkDocs returns a maximum of 100 levels upwards from the requested document and only includes the IDs of the parent folders in the path. You can limit the maximum number of levels. You can also request the names of the parent folders.</p></blockquote>

#### Input Parameters
* `DocumentId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DescribeDocumentVersions
<blockquote><p>Retrieves the document versions for the specified document.</p> <p>By default, only active versions are returned.</p></blockquote>

#### Input Parameters
* `Limit` - _optional_ - Pagination limit<br/>
* `Marker` - _optional_ - Pagination token<br/>
* `DocumentId` - _required_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### AbortDocumentVersionUpload
> Aborts the upload of the specified document version that was previously initiated by <a>InitiateDocumentVersionUpload</a>. The client should make this call only when it no longer intends to upload the document version, or fails to do so.<br/>

#### Input Parameters
* `DocumentId` - _required_
* `VersionId` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### GetDocumentVersion
> Retrieves version metadata for the specified document.<br/>

#### Input Parameters
* `DocumentId` - _required_
* `VersionId` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### UpdateDocumentVersion
<blockquote><p>Changes the status of the document version to ACTIVE. </p> <p>Amazon WorkDocs also sets its document container to ACTIVE. This is the last step in a document upload, after the client uploads the document to an S3-presigned URL returned by <a>InitiateDocumentVersionUpload</a>. </p></blockquote>

#### Input Parameters
* `DocumentId` - _required_
* `VersionId` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### CreateComment
> Adds a new comment to the specified document version.<br/>

#### Input Parameters
* `DocumentId` - _required_
* `VersionId` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeleteComment
> Deletes the specified comment from the document version.<br/>

#### Input Parameters
* `DocumentId` - _required_
* `VersionId` - _required_
* `CommentId` - _required_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DescribeComments
> List all the comments for the specified document version.<br/>

#### Input Parameters
* `DocumentId` - _required_
* `VersionId` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### CreateFolder
> Creates a folder with the specified name and parent folder.<br/>

#### Input Parameters
* `Action` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeleteFolder
> Permanently deletes the specified folder and its contents.<br/>

#### Input Parameters
* `FolderId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### GetFolder
> Retrieves the metadata of the specified folder.<br/>

#### Input Parameters
* `FolderId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### UpdateFolder
> Updates the specified attributes of the specified folder. The user must have access to both the folder and its parent folder, if applicable.<br/>

#### Input Parameters
* `FolderId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeleteFolderContents
> Deletes the contents of the specified folder.<br/>

#### Input Parameters
* `FolderId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DescribeFolderContents
<blockquote><p>Describes the contents of the specified folder, including its documents and subfolders.</p> <p>By default, Amazon WorkDocs returns the first 100 active document and folder metadata items. If there are more results, the response includes a marker that you can use to request the next set of results. You can also request initialized documents.</p></blockquote>

#### Input Parameters
* `Limit` - _optional_ - Pagination limit<br/>
* `Marker` - _optional_ - Pagination token<br/>
* `FolderId` - _required_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### GetFolderPath
<blockquote><p>Retrieves the path information (the hierarchy from the root folder) for the specified folder.</p> <p>By default, Amazon WorkDocs returns a maximum of 100 levels upwards from the requested folder and only includes the IDs of the parent folders in the path. You can limit the maximum number of levels. You can also request the parent folder names.</p></blockquote>

#### Input Parameters
* `FolderId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DescribeGroups
> Describes the groups specified by the query. Groups are defined by the underlying Active Directory.<br/>

#### Input Parameters
* `Action` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### GetCurrentUser
> Retrieves details of the current user for whom the authentication token was generated. This is not a valid action for SigV4 (administrative API) clients.<br/>

#### Input Parameters
* `Action` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DescribeRootFolders
<blockquote><p>Describes the current user's special folders; the <code>RootFolder</code> and the <code>RecycleBin</code>. <code>RootFolder</code> is the root of user's files and folders and <code>RecycleBin</code> is the root of recycled items. This is not a valid action for SigV4 (administrative API) clients.</p> <p>This action requires an authentication token. To get an authentication token, register an application with Amazon WorkDocs. For more information, see <a href="https://docs.aws.amazon.com/workdocs/latest/developerguide/wd-auth-user.html">Authentication and Access Control for User Applications</a> in the <i>Amazon WorkDocs Developer Guide</i>.</p></blockquote>

#### Input Parameters
* `Action` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DescribeNotificationSubscriptions
> Lists the specified notification subscriptions.<br/>

#### Input Parameters
* `OrganizationId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### CreateNotificationSubscription
<blockquote><p>Configure Amazon WorkDocs to use Amazon SNS notifications. The endpoint receives a confirmation message, and must confirm the subscription.</p> <p>For more information, see <a href="https://docs.aws.amazon.com/workdocs/latest/developerguide/subscribe-notifications.html">Subscribe to Notifications</a> in the <i>Amazon WorkDocs Developer Guide</i>.</p></blockquote>

#### Input Parameters
* `OrganizationId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeleteNotificationSubscription
> Deletes the specified subscription from the specified organization.<br/>

#### Input Parameters
* `OrganizationId` - _required_
* `SubscriptionId` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### GetResources
> Retrieves a collection of resources, including folders and documents. The only <code>CollectionType</code> supported is <code>SHARED_WITH_ME</code>.<br/>

#### Input Parameters
* `Action` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeleteCustomMetadata
> Deletes custom metadata from the specified resource.<br/>

#### Input Parameters
* `ResourceId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### CreateCustomMetadata
> Adds one or more custom properties to the specified resource (a folder, document, or version).<br/>

#### Input Parameters
* `ResourceId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeleteLabels
> Deletes the specified list of labels from a resource.<br/>

#### Input Parameters
* `ResourceId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### CreateLabels
> Adds the specified list of labels to the given resource (a document or folder)<br/>

#### Input Parameters
* `ResourceId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### RemoveAllResourcePermissions
> Removes all the permissions from the specified resource.<br/>

#### Input Parameters
* `ResourceId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DescribeResourcePermissions
> Describes the permissions of a specified resource.<br/>

#### Input Parameters
* `ResourceId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### AddResourcePermissions
> Creates a set of permissions for the specified folder or document. The resource permissions are overwritten if the principals already have different permissions.<br/>

#### Input Parameters
* `ResourceId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### RemoveResourcePermission
> Removes the permission for the specified principal from the specified resource.<br/>

#### Input Parameters
* `ResourceId` - _required_
* `PrincipalId` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DescribeUsers
<blockquote><p>Describes the specified users. You can describe all users or filter the results (for example, by status or organization).</p> <p>By default, Amazon WorkDocs returns the first 24 active or pending users. If there are more results, the response includes a marker that you can use to request the next set of results.</p></blockquote>

#### Input Parameters
* `Limit` - _optional_ - Pagination limit<br/>
* `Marker` - _optional_ - Pagination token<br/>
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### CreateUser
> Creates a user in a Simple AD or Microsoft AD directory. The status of a newly created user is "ACTIVE". New users can access Amazon WorkDocs.<br/>

#### Input Parameters
* `Action` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeleteUser
> Deletes the specified user from a Simple AD or Microsoft AD directory.<br/>

#### Input Parameters
* `UserId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### UpdateUser
> Updates the specified attributes of the specified user, and grants or revokes administrative privileges to the Amazon WorkDocs site.<br/>

#### Input Parameters
* `UserId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### DeactivateUser
> Deactivates the specified user, which revokes the user's access to Amazon WorkDocs.<br/>

#### Input Parameters
* `UserId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

### ActivateUser
> Activates the specified user. Only active users can access Amazon WorkDocs.<br/>

#### Input Parameters
* `UserId` - _required_
* `Version` - _required_
* `X-Amz-Content-Sha256` - _optional_
* `X-Amz-Date` - _optional_
* `X-Amz-Algorithm` - _optional_
* `X-Amz-Credential` - _optional_
* `X-Amz-Security-Token` - _optional_
* `X-Amz-Signature` - _optional_
* `X-Amz-SignedHeaders` - _optional_

## License

**flow**ground :- Telekom iPaaS / amazonaws-com-workdocs-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
