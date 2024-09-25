---
title: "Choose the right meeting type"
description: "Consider when to use online meetings API, webinar API or town hall API for Teams meetings."
author: "awang119"
ms.localizationpriority: medium
ms.subservice: "cloud-communications"
---

# Choose the right meeting type

Microsoft Teams and Microsoft Graph supports multiple types of scheduled real-time voice and video experiences. These range from ad hoc meetings suitable for a small number of participants to large structured virtual events like webinars and town halls with thousands of attendees.

The following table provides a comparison of the types of meetings that Teams and Microsoft Graph supports.
| **Meeting type**    |**Microsoft Graph resource types** | **Use cases**     |
| ------------- | ------------- | ------------- |
| [Online meeting](https://support.microsoft.com/en-us/office/meetings-in-microsoft-teams-e0b0ae21-53ee-4462-a50d-ca9b9e217b67) |[onlineMeeting](../api-reference/v1.0/resources/onlinemeeting.md) <br> [attendanceReport](../api-reference/v1.0/resources/meetingattendancereport.md) <br> [attendanceRecord](../api-reference/v1.0/resources/attendancerecord.md) |  <ul><li>Hosting a meeting for up to 1,000 participants who can be inside or outside of your organization. Everyone can interact via audio, video, chat, and screensharing. </li><li>Meetings are either scheduled, ad hoc, or channel meetings. </li></ul> |
| [Webinar](https://support.microsoft.com/en-us/office/get-started-with-microsoft-teams-webinars-42f3f874-22dc-4289-b53f-bbc1a69013e3) |[virtualEventWebinar](../api-reference/v1.0/resources/virtualeventwebinar.md) <br> [virtualEventRegistration](../api-reference/v1.0/resources/virtualeventregistration.md) <br> [virtualEventRegistrationConfiguration](../api-reference/v1.0/resources/virtualeventregistrationconfiguration.md) <br> [virtualEventRegistrationQuestion](../api-reference/v1.0/resources/virtualeventregistrationquestionbase.md) <br> [attendanceReport](../api-reference/v1.0/resources/meetingattendancereport.md) <br> [attendanceRecord](../api-reference/v1.0/resources/attendancerecord.md) <br> [virtualEventSession](../api-reference/v1.0/resources/virtualeventsession.md) <br> [virtualEventPresenter](../api-reference/v1.0/resources/virtualeventpresenter.md)|  <ul><li>Hosting a meeting where one or several experts (presenters) share their ideas or provide training to an audience (attendees inside or outside of your organization) with a maximum of 1,000 participants on the call.</li><li>Registration is needed before attendees can join the meeting.</li></ul> |
| [Town hall](https://support.microsoft.com/en-us/office/get-started-with-town-hall-in-microsoft-teams-33baf0c6-0283-4c15-9617-3013e8d4804f) | [virtualEventTownhall](../api-reference/v1.0/resources/virtualeventtownhall.md) <br> [virtualEventSession](../api-reference/v1.0/resources/virtualeventsession.md) <br> [virtualEventPresenter](../api-reference/v1.0/resources/virtualeventpresenter.md) | <ul><li>Automatic streaming event for a limited number of presenters to a large group of attendees, capping at 10,000 or 20,000 participants (with Teams Premium). </li><li>Attendees don’t need to register for the event but are invited and use Q&A to engage with presenters and organizers instead of direct interaction via chat or audio.  
</li></ul>

To learn more about the differences between each meeting type to help you choose the one that is best suited for your use case, see the [feature comparison chart](https://learn.microsoft.com/en-us/microsoftteams/meeting-webinar-town-hall-feature-comparison).  


# Related content 
- [Create or join online meetings](cloud-communications-online-meetings.md)
- [Webinar use cases](cloud-communications-virtual-events-webinar-usecases.md)
- [Town hall use cases](cloud-communications-virtual-events-townhall-usecases.md)
