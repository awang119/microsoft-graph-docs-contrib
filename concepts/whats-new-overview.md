---
title: "What's new in Microsoft Graph"
description: "Find out what's new in Microsoft Graph APIs, SDKs, documentation, and other resources."
author: "lauragra"
ms.localizationpriority: high
---

# What's new in Microsoft Graph

Microsoft Graph provides a unified programmability model that you can use to access data in Microsoft 365, Windows, and Enterprise Mobility + Security. This article provides information about what's new in Microsoft Graph APIs, documentation, SDKs, and more.

For more detailed API-level updates, see the [Microsoft Graph API changelog](https://developer.microsoft.com/graph/changelog/).

For details about previous updates to Microsoft Graph, see [Microsoft Graph what's new history](whats-new-earlier.md).

> [!IMPORTANT]
> Features in _preview_ status are subject to change without notice, and might not be promoted to generally available (GA) status. Don't use preview features in production apps.

## October 2024: New and generally available

### Teamwork and communications | Messaging

Updated the [chatMessage: delta](/graph/api/chatmessage-delta) method to use a new endpoint that gets the list of delta messages from all chats in which a user is a participant, including one-on-one chats, group chats, and meeting chats.

## October 2024: New in preview only

### Teamwork and communications | Messaging

Updated the [chatMessage: delta](/graph/api/chatmessage-delta?view=graph-rest-beta&preserve-view=true) method to use a new endpoint that gets the list of delta messages from all chats in which a user is a participant, including one-on-one chats, group chats, and meeting chats.

### Users

Changed the following on-prem synced properties of the [user](/graph/api/resources/user?view=graph-rest-beta&preserve-view=true) resource type that were read-only in Microsoft Graph to be updatable via Microsoft Graph: 
- onPremisesDistinguishedName
- onPremisesDomainName
- onPremisesSamAccountName
- onPremisesSecurityIdentifier
- onPremisesUserPrincipalName

## September 2024: New and generally available

### Change notifications

Announced the deprecation of shared access signatures (SAS) for authenticating Event Hubs for [Microsoft Graph change notifications](/graph/change-notifications-delivery-event-hubs). We recommend using Microsoft Entra ID role-based access control (RBAC) instead. Follow the [guidance to migrate to RBAC](/graph/change-notifications-delivery-event-hubs#migrate-an-event-hub-authentication-to-microsoft-entra-id-rbac).

### Identity and access | Directory management

Removed the previously deprecated `Directory.Write.Restricted` permission from the [device](/graph/api/resources/device), [group](/graph/api/resources/group), and [user](/graph/api/resources/user) resources.

### Security | Alerts and incidents

- Use the **dnsDomain** property on [deviceEvidence](/graph/api/resources/security-deviceevidence) to get the DNS domain that a computer belongs to.
- Use the **hostName** property on [deviceEvidence](/graph/api/resources/security-deviceevidence) to get the hostname without the domain suffix.
- Use the **ntDomain** property on [deviceEvidence](/graph/api/resources/security-deviceevidence) to get a logical grouping of computers within a Microsoft Windows network.

### Security | Identities

Added the ability to [get](/graph/api/security-healthissue-get), [list](/graph/api/security-identitycontainer-list-healthissues), and [update](/graph/api/security-healthissue-update) Microsoft Defender for Identity [health issues](/graph/api/resources/security-healthissue) that represent potential issues identified within a customer's Defender for Identity configuration.

### Teamwork and communications | Messaging

- [Get all retained messages](/graph/api/channel-getallretainedmessages) across all [channels](/graph/api/resources/channel) in a [team](/graph/api/resources/team).
- [Get all retained messages](/graph/api/chat-getallretainedmessages) from all [chats](/graph/api/resources/chat) that a user is a participant in, including one-on-one chats, group chats, and meeting chats.

## September 2024: New in preview only

### Applications | Service principal

Use the **serviceManagementReference** optional property in the [applicationTemplate: instantiate](/graph/api/applicationtemplate-instantiate?view=graph-rest-beta&preserve-view=true) method to set the service tree ID for a service.

### Device and app management | Cloud PC

- Enabled the `middleEast` and `mexico` members as supported regions in the [cloudPcRegionGroup](/graph/api/resources/cloudpcsupportedregion?view=graph-rest-beta&preserve-view=true#cloudpcregiongroup-values) enumeration.
- Removed the **getShiftWorkCloudPcAccessState** method from the [cloudPC](/graph/api/resources/cloudpc?view=graph-rest-beta&preserve-view=true) resource. Going forward, use the [getFrontlineCloudPcAccessState](/graph/api/cloudpc-getfrontlinecloudpcaccessstate?view=graph-rest-beta&preserve-view=true) API.
- Use the **autopilotConfiguration** property on [cloudPcProvisioningPolicy](/graph/api/resources/cloudpcprovisioningpolicy?view=graph-rest-beta&preserve-view=true) to get or set the settings for Windows Autopilot that enable Windows 365 customers to experience it on Cloud PC.
- Use the **osVersionNumber** property on [cloudPcDeviceImage](/graph/api/resources/cloudpcdeviceimage?view=graph-rest-beta&preserve-view=true) and [cloudPcGalleryImage](/graph/api/resources/cloudpcgalleryimage?view=graph-rest-beta&preserve-view=true) resources to get the operating system version of an image.
- Introduced the [retrieveSnapshots](/graph/api/cloudpc-retrievesnapshots?view=graph-rest-beta&preserve-view=true) method on the [cloudPC](/graph/api/resources/cloudpc?view=graph-rest-beta&preserve-view=true) resource to enable you to return a list of all snapshots of a Cloud PC.

Deprecated the following methods:
- [bulkSetReviewStatus](/graph/api/manageddevice-bulksetcloudpcreviewstatus?view=graph-rest-beta&preserve-view=true); use the [cloudPcBulkSetReviewStatus](/graph/api/resources/cloudpcbulksetreviewstatus?view=graph-rest-beta&preserve-view=true) resource and its supported APIs instead.
- [List snapshots](/graph/api/virtualendpoint-list-snapshots?view=graph-rest-beta&preserve-view=true); use the [retrieveSnapshots](/graph/api/cloudpc-retrievesnapshots?view=graph-rest-beta&preserve-view=true) resource and its supported APIs instead.

### Files

- [Update the recycle bin settings](/graph/api/filestoragecontainer-update-recyclebinsettings?view=graph-rest-beta&preserve-view=true) for a [fileStorageContainer](/graph/api/resources/filestoragecontainer?view=graph-rest-beta&preserve-view=true).
- Use the `$skip`, `$top`, `$orderBy`, `$filter`, and `includeAllContainerUsers` query parameters to customize the [List permissions](/graph/api/filestoragecontainer-list-permissions?view=graph-rest-beta&preserve-view=true) operation response.
- Include all version history when you [copy a drive item](/graph/api/driveitem-copy?view=graph-rest-beta&preserve-view=true). The version history is included up to the target version setting limit.

### Identity and access | Directory management

Use the **passwordResetUri** property on [internalDomainFederation](/graph/api/resources/internaldomainfederation?view=graph-rest-beta&preserve-view=true) to get or set the URI that clients are redirected to for resetting their password.

### Identity and access | Identity and sign in

- Use the **identifierUris** property in the get and update operations of the [tenantAppManagementPolicy](/graph/api/resources/tenantappmanagementpolicy?view=graph-rest-beta&preserve-view=true) resource to get or set restrictions on vulnerable or easily compromised identifier URI formats for an application.
- Updated the return type for the **applicationRestrictions** property of the [tenantAppManagementPolicy](/graph/api/resources/tenantappmanagementpolicy?view=graph-rest-beta&preserve-view=true) resource from [appManagementConfiguration](/graph/api/resources/appmanagementconfiguration?view=graph-rest-beta&preserve-view=true) to [appManagementApplicationConfiguration](/graph/api/resources/appmanagementapplicationconfiguration?view=graph-rest-beta&preserve-view=true).
- Updated the return type for the **servicePrincipalRestrictions** property of the [tenantAppManagementPolicy](/graph/api/resources/tenantappmanagementpolicy?view=graph-rest-beta&preserve-view=true) resource from [appManagementConfiguration](/graph/api/resources/appmanagementconfiguration?view=graph-rest-beta&preserve-view=true) to [appManagementServicePrincipalConfiguration](/graph/api/resources/appmanagementserviceprincipalconfiguration?view=graph-rest-beta&preserve-view=true).
- Updated the return type for the **restrictions** property of the [appManagementPolicy](/graph/api/resources/appmanagementpolicy?view=graph-rest-beta&preserve-view=true) resource from [appManagementConfiguration](/graph/api/resources/appmanagementconfiguration?view=graph-rest-beta&preserve-view=true) to [customAppManagementConfiguration](/graph/api/resources/customappmanagementconfiguration?view=graph-rest-beta&preserve-view=true).

### Reports | Microsoft 365 usage reports

- [Get](/graph/api/reportroot-getmicrosoft365copilotusageuserdetail?view=graph-rest-beta&preserve-view=true) the most recent activity data for enabled users of Microsoft 365 Copilot apps.
- [Get](/graph/api/reportroot-getmicrosoft365copilotusercountsummary?view=graph-rest-beta&preserve-view=true) the aggregated number of active and enabled users of Microsoft 365 Copilot for a specified time period.
- [Get](/graph/api/reportroot-getmicrosoft365copilotusercounttrend?view=graph-rest-beta&preserve-view=true) the trend in the daily number of active and enabled users of Microsoft 365 Copilot for a specified time period.

### Security | Alerts and incidents

- Use the **dnsDomain** property on [deviceEvidence](/graph/api/resources/security-deviceevidence?view=graph-rest-beta&preserve-view=true) to get the DNS domain that a computer belongs to.
- Use the **hostName** property on [deviceEvidence](/graph/api/resources/security-deviceevidence?view=graph-rest-beta&preserve-view=true) to get the hostname without the domain suffix.
- Use the **ntDomain** property on [deviceEvidence](/graph/api/resources/security-deviceevidence?view=graph-rest-beta&preserve-view=true) to get a logical grouping of computers within a Microsoft Windows network.

### Security | Identities

- [Generate](/graph/api/security-sensor-regeneratedeploymentaccesskey?view=graph-rest-beta&preserve-view=true) a new deployment access key.
- [Get the deployment access key](/graph/api/security-sensor-getdeploymentaccesskey?view=graph-rest-beta&preserve-view=true) associated with a Microsoft Defender for Identity.
- [Get the sensor deployment package](/graph/api/security-sensor-getdeploymentpackageuri?view=graph-rest-beta&preserve-view=true) URL and version.

### Teamwork and communications | Calls and online meetings

Use the **isDeltaRosterEnabled** property on [incomingCallOptions](/graph/api/resources/incomingcalloptions?view=graph-rest-beta&preserve-view=true) and [outgoingCallOptions](/graph/api/resources/outgoingcalloptions?view=graph-rest-beta&preserve-view=true) to indicate whether delta roster is enabled for a call.

## Contribute to Microsoft Graph

Are there scenarios you'd like Microsoft Graph to support?

- Suggest and vote for new features by using the [Microsoft Graph Feedback Portal](https://aka.ms/graphfeedback). Some new features originate as popular requests from the developer community. The Microsoft Graph team regularly evaluates customer needs and releases new features to the beta (`https://graph.microsoft.com/beta`) and v1.0 (`https://graph.microsoft.com/v1.0`) endpoints.

- [Join](https://aka.ms/m365-dev-call) the weekly Microsoft 365 platform community call and become an active member of the Microsoft Graph community. To discover the full calendar of developer calls, visit the [Microsoft 365 and Power Platform community page](https://aka.ms/community/calls).

- [Join](https://ux.microsoft.com/Panel/M365Devs?utm_source=graphDocs) our research panel to provide your input on our developer experiences.

## Related content
- [Microsoft Graph developer blog](https://devblogs.microsoft.com/microsoft365dev/category/microsoft-graph/).
- [Microsoft Graph API changelog](https://developer.microsoft.com/graph/changelog/).
- [Microsoft Graph what's new history](whats-new-earlier.md).
