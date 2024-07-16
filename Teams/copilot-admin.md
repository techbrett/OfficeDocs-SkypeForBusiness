---
title: Admin guide to CoPilot in Teams
author: mstonysmith
ms.author: tonysmit
manager: pamgreen
ms.reviewer: elaineho
ms.date: 07/16/2024
ms.topic: article
audience: admin
appliesto: 
  - Microsoft Teams
ms.service: msteams
ms.subservice: itpro-rooms
ms.collection: 
  - M365-collaboration
  - teams-rooms-consoles
  - Tier1
f1.keywords: 
  - NOCSH                           
search.appverid: MET150
ms.localizationpriority: medium
description: Learn more about how to set up Copilot and AI-based features in Microsoft Teams.
---
# Admin guide for Teams and Copilot

When you are considering deploying Copilot and AI-based features for
your Teams users there are many things to consider. The number and type
of AI-based features is dependent on the type of license or licenses
that you assign to your Teams users, the hardware you are using for
Teams Rooms consoles, and the type of license assigned to your Microsoft
Teams Rooms consoles.

There are four separate sets of AI-based features that can be deployed
to your users when you assign a specific license for those users or
Teams Rooms consoles.

1.  **Copilot** (Copilot bot integration. Adding it to all the apps
    including Teams. Ask questions to resolve topics, catch up during
    meetings (meeting recap), organize meeting points.)
2.  **Teams Rooms** (Live transcripts and captions. Intelligent
    Speaker - identify in-room participants)
3.  **Meetings and collaboration** (Policy changes for transcription,
    captions, and recording.)
4.  **Microsoft Teams** (AI-based noise suppression and video
    optimization. Cameo overlay. Voice isolation. Speaker attribution,
    Face and voice enrollment.)

## Getting started with Copilot

[Microsoft Copilot for Microsoft 365](https://www.microsoft.com/microsoft-365/blog/2023/03/16/introducing-microsoft-365-copilot-a-whole-new-way-to-work) is an AI-powered productivity tool that uses large language models (LLMs) and integrates your data with the Microsoft Graph and Microsoft 365 Apps.

Microsoft Copilot for Microsoft 365 provides the ability for users to find and access their content through natural language prompting. Copilot ensures data security and privacy by adhering to existing obligations and integrating with your organization\'s policies. To get the most out of Copilot, you should consider optimizing data and content for Search, to ensure optimal secure access. To learn more about privacy with Microsoft Copilot for Microsoft 365, see [Data, Privacy, andSecurity for Microsoft Copilot for Microsoft 365](/copilot/microsoft-365/microsoft-365-copilot-privacy).

Copilot features for Excel, Word, PowerPoint, and OneNote will work seamlessly for users who have multiple Microsoft accounts (work/school account or personal account) signed into a single Windows session when one of those accounts has a Copilot Pro or Copilot for Microsoft 365 license assigned. For example, when a user on their work machine with a Copilot for Microsoft 365 license opens a document from their personal OneDrive, they'll be able to use Copilot in the document. Or when a
Copilot Pro user signs in on their work device with their Microsoft account (MSA), they'll be able to use Copilot with Office files stored on their OneDrive or in SharePoint document libraries.

Microsoft Copilot for Microsoft 365 ensures data security and privacy by adhering to existing obligations and integrating with your organization's policies. It utilizes your Microsoft Graph content with the same access controls as other Microsoft 365 services. To learn more about privacy with Microsoft Copilot for Microsoft 365, see [Data, Privacy, and Security for Microsoft Copilot for Microsoft 365](/copilot/microsoft-365/microsoft-365-copilot-privacy).

## Requirements for Copilot in M365

The integration of Microsoft Copilot for Microsoft 365 and Microsoft 365 Apps enables Copilot experiences to take place inside individual apps, such as Word, PowerPoint, Teams, Excel, Outlook, and more. As a result of this integration, the requirements for using Microsoft Copilot for Microsoft 365 are nearly identical to the requirements for using Microsoft 365 Apps.

To see more videos on [CoPilot, see Microsoft Mechanics -- Podcast](<https://www.youtube.com/playlist?list=PLXtHYVsvn_b8MTl8mD8FBJIB_cSGkEaT9>).

Learn more: [Service Descriptions for Copilot\]([/copilot/microsoft-365/microsoft-365-copilot-requirements](https://learn.microsoft.com/copilot/microsoft-365/microsoft-365-copilot-requirements).

### Provisioning users to use AI-based features in Teams

After you've prepared your organization for Copilot, you can manage your Microsoft 365 licenses from the Microsoft 365 admin center. You can assign licenses to individual users or to groups of users, as well as reassign licenses to other users depending on the level of AI support that would be needed.

In Teams, there are four types of licenses that you can assign. First, you must assign at least one user license to your users (depending on what features you want available to your Teams users). Second, to take advantage of all of the AI-based features you must assign a Microsoft Teams Pro license to each Teams Rooms console in your organization.

Here is a feature comparison between each of the user licenses that youmust assign:

### Feature vs license comparison

+-----------------+-----------------+-----------------+-----------------+
| Feature         | Microsoft Teams | Microsoft Teams | Copilot for     |
|                 |                 | Premium         | Microsoft 365   |
+=================+:===============:+:===============:+:===============:+
| AI-based noise  | Yes             |                 |                 |
| suppression     |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| AI-based video  | Yes             |                 |                 |
| optimization    |                 |                 |                 |
| (brightness and |                 |                 |                 |
| backgrounds)    |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Suggested       | Yes             |                 |                 |
| replies         |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Live meeting    | Yes             |                 |                 |
| captions and    |                 |                 |                 |
| transcript      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Cameo video     | Yes             |                 |                 |
| overlay on      |                 |                 |                 |
| screen share    |                 |                 |                 |
| and PowerPoint  |                 |                 |                 |
| Live            |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Real-time       |                 | Yes             |                 |
| translation of  |                 |                 |                 |
| meeting         |                 |                 |                 |
| captions and    |                 |                 |                 |
| transcript      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Intelligent     |                 | Yes             | Yes             |
| recap (after    |                 |                 |                 |
| meeting) --     |                 |                 | **NOTE:**       |
| standardized AI |                 |                 | Coming soon to  |
| notes and AI    |                 |                 | Copilot         |
| tasks           |                 |                 | license.        |
+-----------------+-----------------+-----------------+-----------------+
| Intelligent     |                 | Yes             | Yes             |
| recap (after    |                 |                 |                 |
| meeting) --     |                 |                 |                 |
| video, speaker, |                 |                 |                 |
| chapter markers |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Ask any         |                 |                 | Yes             |
| question during |                 |                 |                 |
| meeting?        |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| How did the     |                 |                 | Yes             |
| team react to   |                 |                 |                 |
| the proposal?   |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Does this       |                 |                 | Yes             |
| plan's timeline |                 |                 |                 |
| have any        |                 |                 |                 |
| conflicts?      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Create a table  |                 |                 | Yes             |
| with pros and   |                 |                 |                 |
| cons.           |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Other:          |                 |                 | Yes             |
| Microsoft       |                 |                 |                 |
| Copilot UX      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Other:          |                 |                 | Yes             |
| AI-powered web  |                 |                 |                 |
| groundling and  |                 |                 |                 |
| Microsoft 365   |                 |                 |                 |
| Graph           |                 |                 |                 |
| groundling      |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Other:          |                 |                 | Yes             |
| Microsoft       |                 |                 |                 |
| Copilot and     |                 |                 |                 |
| Copilot Studio  |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+
| Other: Copilot  |                 |                 | Yes             |
| in core         |                 |                 |                 |
| Microsoft 365   |                 |                 |                 |
| app             |                 |                 |                 |
+-----------------+-----------------+-----------------+-----------------+

Learn more: [Set up Copilot in Microsoft 365](/copilot/microsoft-365/microsoft-365-copilot-setup).

For business users, a user must have a Microsoft 365 Business Basic, Business Standard, Business Premium, E3, E5, F1, or F3 subscription, along with a Microsoft Copilot for Microsoft 365 subscription.

To assign and manage licenses, you can use the Microsoft 365 admin center.

1. Sign in to the Microsoft 365 admin center and go to **Billing** > **Licenses** > select **Copilot for Microsoft 365**.
2. In the product details page, assign licenses to users andmanage their access to Copilot and other apps and services.

Learn more:[Assign licenses for Copilot](/copilot/microsoft-365/microsoft-365-copilot-enable-users)

### Updating Microsoft Teams Rooms

Microsoft Teams Rooms supports speaker recognition in meeting transcripts. However, in working with Copilot, Teams Rooms not only enhances the overall meeting experience and enables better support for collaboration, it works together with Copilot to make meeting transcripts better by adding support for meeting summaries and intelligent recap.

To support these features, you want to verify that all Teams Rooms consoles:

- Updated and have the hardware to support speaker recognition.
- Resource account has a Teams Rooms Pro license assigned to it. For more information on licensing, see [Overview of Teams Rooms licensing](/microsoftteams/rooms/rooms-licensing) .

To assign a Microsoft Teams Rooms Pro license, you can use the Microsoft 365 admin center.

1. Sign in to the Microsoft 365 admin center and go to **Users** >
    **Active users** > Select the **resource account** you created
    earlier.
2. In the right pane, select **Licenses and Apps**.

Learn more: [Certified Hardware\]([/microsoftteams/rooms/certified-hardware?tabs=Windows](https://learn.microsoft.com/microsoftteams/rooms/certified-hardware?tabs=Windows) and [Release notes](/microsoftteams/rooms/rooms-release-note?tabs=Windows).

### Copilot across Microsoft Teams

You can make Copilot available to users in Microsoft Teams. This way
you, your teammates, and your broader organization can interact with it
when you assign a Copilot license to a user.  When you add Copilot to
Microsoft Teams, some of your data, such as copilot content and end-user
chat content, is shared with Microsoft Teams.

By buying the Copilot licenses, adding it to Microsoft Teams, and
connecting the bot, it enables features that can be used by end users
including adding a bot to teams and channels so they can interact with
it, and be able to use Copilot:

-   During a meeting to summarize discussion points, including who said
    what and any action items in real time. Transcription must be turned
    on.

-   To catch up on what was missed in the meeting. They will see and
    select the Copilot icon from the meeting controls and a meeting
    summary will appear in the right side of the meeting window.

-   After the meeting is done. Copilot can help wrap up a meeting with
    clear next steps. They will also have other options including a
    meeting recap, action items listed, follow-up questions, main items
    that are discussed, and meeting notes.

When you add Copilot in Microsoft Teams, you can:

-   Add Copilot to Microsoft team channels, teams, meetings, and chats.

-   Customize your Copilot's appearance in Microsoft Teams.

-   Install the Copilot app for yourself in Microsoft Teams.

-   Share Copilot\'s installation link with other users so they can
    install it.

-   Show the Copilot app in Microsoft Teams app store.

-   Download the pregenerated Teams app manifest to distribute it within
    your Microsoft Teams tenant.

In Microsoft Teams, you can [Add Copilot to Microsoft
teams](https://learn.microsoft.com/microsoftteams/platform/bots/how-to/conversations/channel-and-group-conversations?tabs=dotnet).
When you add Copilot, team members can @mention the Copilot bot in any
team channels, and all teammates will see the response from the bot.

**Learn more:**
\[Bots\]([/microsoftteams/platform/bots/how-to/conversations/channel-and-group-conversations?tabs=dotnet](https://learn.microsoft.com/microsoftteams/platform/bots/how-to/conversations/channel-and-group-conversations?tabs=dotnet))

Also, after you add Copilot to Teams, any user, who installs Copilot
from the [Teams app
store](https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams#install-a-copilot-as-an-app-in-microsoft-teams) or
the \[installation
link\](/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams#share-a-link-so-others-can-install-the-copilot0,
will:

-   Have the option to add Copilot to a channel they own.

-   Have the option to add Copilot to group and meeting chats in
    Microsoft Teams.

**Learn more:** \[Add a bot to Microsoft
Teams\]([/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams](https://learn.microsoft.com/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams))

## Admin set up

Within your organization there are several settings that you will either
need to turn on (they are off by default) or verify that they are turned
on to let end users get the full advantages of Copilot in Microsoft
Teams. Settings like transcriptions, captioning, recording, voice
isolation, voice enrollment are a few of the settings that you will want
to set up or turn on for your end users in your organization.

### Turning on Copilot for your Teams users

After you have added CoPilot to Teams, you will need to turn it on,
enable transcriptions, and meeting recordings for your end users. By
turning it on, users will see the Copilot icon and options but
transcription for meetings will also need to be turned on as well.

To turn on Copilot for your Teams users.

-   In the [Teams admin center](https://admin.teams.microsoft.com/), go
    to **Meetings** from the navigation pane \> **Meeting Policies**.
    Either select an existing policy or create a new one.
    Select **On** or **On only with retained transcript** from the
    dropdown for the **Copilot** setting.

You can use PowerShell to turn this on:

**\
***Set-CsTeamsMeetingPolicy -Identity \<policy name\> -Copilot Enabled*

**Learn more:** \[Meeting
transcription\]([/microsoftteams/copilot-teams-transcription](https://learn.microsoft.com/en-us/microsoftteams/copilot-teams-transcription))

### Noise suppression

Noise suppression is identifying non human voices or noise in an
environment and then minimizing or completely eliminating them from an
audio stream. Part of the AI processes for voice isolation is telling
the difference between background chatter in a café and a user is simply
listening in and if they also want to be heard clearly if they are
speaking in the meeting from their laptop.

Noise suppression of background noise is turned on by default when you
install the Microsoft Teams app but their microphone must also support
it. If it does, noise suppression of background noise will significantly
reduce the amount of background noise from a meeting participant and it
will greatly enhance the microphone's audio quality.

![A screenshot of a black screen Description automatically
generated](media/image1.png){width="3.35419072615923in"
height="1.7864709098862641in"}

However, if you want to also isolate or have Teams be able to tell the
difference between background nose and a human's voice, you will need
have user then set up a voice profile and enable voice isolation in the
Teams app.

### Enable voice isolation

You can manage how voice and face profiles are used to turn off voice
Isolation for users to enhance noise and voice background reduction
admins can switch off voice isolation with PowerShell in the meeting
policy or users can turn it on themselves in the Teams app.

**Learn more:** \[Manage voice isolation for your
users\]/microsoftteams/voice-isolation)

Voice isolation is on by default in an organization. Check to make sure
that it's turned on and if it isn't, you can use PowerShell to turn it
on for all of your users.

*Set-CsTeamsMeetingPolicy -Identity Global -VoiceIsolation Enabled*

Each user must set up a voice profile to turn it on in their Teams app.
This can be turned off or on either before or during a meeting.

![A screenshot of a computer Description automatically
generated](media/image2.png){width="3.117985564304462in"
height="1.4899048556430445in"}

### Manage meeting transcription and captions

Transcription allows users to play back meeting recordings with closed
captions and review important discussion items in the transcript.
Transcription and captions help create inclusive content for viewers. It
also helps Copilot to create meeting summaries, recaps, action items,
and other features.

To turn on Copilot for your Teams users.

In the [Teams admin center](https://admin.teams.microsoft.com/) go to
**Meetings** \> select **Meeting Policies**. Either select an existing
policy or create a new one. On the meeting policy page, under
**Recording & transcription**, turn on **Meeting recording**. This
setting is off by default.

**Note**: Under **Recording & transcription**, there are several other
recording options that are available for you to set. Review all of the
settings to ensure that they meet the needs of your organization.

You can use PowerShell to turn this on:

*Set-CsTeamsMeetingPolicy -Identity \<policy name\> --
AllowTranscription \$true*

**Learn more:** \[Meeting
transcription\]([/microsoftteams/meeting-transcription-captions](https://learn.microsoft.com/en-us/microsoftteams/meeting-transcription-captions))

### Turn on Live captioning

Teams has built-in closed captioning you can turn on from the meeting
controls. Live captions can make your meeting more productive
and inclusive for participants who are deaf or hard-of-hearing,
have different levels of language proficiency, or the meeting
participant is in a noisy place during a meeting will all benefit from
live captions.

Live captions and transcriptions can show you the text of a conversation
in a Teams meeting. They can help you keep records or better understand
what others are saying during a meeting.

It is available in the desktop version of the Teams app but users can
set transcription and captioning options under **Settings** \>
**Captions and transcripts** in the Teams app.

![A screenshot of a black screen Description automatically
generated](media/image3.png){width="3.5954330708661417in"
height="1.837665135608049in"}

**Learn more:** \[Live
transcriptions\](<https://support.microsoft.com/office/view-live-transcription-in-microsoft-teams-meetings-dc1a8f23-2e20-4684-885e-2152e06a4a8b>)

If your organization is using OneDrive for Business and SharePoint for
meeting recordings, you should turn on **Allow transcription** in the
Teams meeting policy and turn on the **Always show live captions in
meeting** in the Teams app and encourage your users to start
transcription in every meeting. This will make captions available in the
post-meeting recording when it's generated by Copilot as well.

In the [Teams admin center](https://admin.teams.microsoft.com/),
Under **Meetings**, select **Meeting Policies**. Either select an
existing policy or create a new one. On the meeting policy page, under
**Recording & transcription**, set **Live captions** to **Off, but
organizers and co-organizers can turn them on**.

You can use PowerShell to turn this on:

*Set-CsTeamsMeetingPolicy -Identity \<policy name\> --
AllowTranscription \$true*

### Turn on Live transcriptions

By default, transcripts are shown in the language spoken during a
meeting or event. Live translated transcription allows your users to
translate the meeting or event transcript into the language they\'re
most comfortable with.

You can use a new meeting policy you create or use the Global (Org-wide
default) policy to turn this on using the Teams admin center or
PowerShell.

To turn on Live transcription, **Transcription** but be set to **On**
first.

In the [Teams admin center](https://admin.teams.microsoft.com/), under
**Meetings**, select **Meeting Policies**. Either select an existing
policy or create a new one. On the meeting policy page, under
**Recording & transcription**, turn on **Meeting recording**. This
setting is off by default.

You can use PowerShell to turn this on:

*Set-CsTeamsMeetingPolicy -Identity \<policy name\> -Copilot Enabled --
AllowTranscription \$true*

**Learn more:** \[Meeting transcription and
captions\](/microsoftteams/meeting-transcription-captions)

### Turn on meeting recording

Recording meetings is optional, however, there are many cases that you
will want to allow meetings to be recorded. Meeting recordings as you
imagine is recording a stream of audio and video for a meeting, but in
the case with CoPilot, it is used to help generate meeting summaries,
recaps, and other information after the meeting has ended. When a
meeting is recorded:

-   It gets uploaded to OneDrive (private meetings) or SharePoint
    (channel meetings).

-   People invited to the meeting have permissions to the recording
    (guests and external attendees can view the recording only if the
    recording is explicitly shared with them).

-   Microsoft Purview compliance features apply to the meeting recording
    files the same as with other files.

-   It\'s linked in the chat for the meeting.

-   It\'s displayed in the Recordings and Transcripts tab for the
    meeting in Teams calendar.

-   It\'s added to various file lists across Microsoft 365: Shared with
    me, office.com, Recommended, Recent, etc.

-   Microsoft 365 Search indexes it.

There\'s also an option for recordings to have automatic transcription,
so that users can play back meeting recordings with closed captions and
review important discussion items in the transcript.

You can use a new meeting policy you create or use the Global (Org-wide
default) policy to turn this on using the Teams admin center or
PowerShell.

In the [Teams admin center](https://admin.teams.microsoft.com/),
under **Meetings** \> **Meeting policies**. Select the policy that you
want to edit. Turn **Meeting recording** On or Off.

You can use PowerShell to turn this on:

*Set-CsTeamsMeetingPolicy -Identity \<policy name\> -AllowCloudRecording
Enabled*

**Learn more:** [\[Meeting
recording\](/microsoftteams/meeting-recording?tabs=meeting-policy](https://learn.microsoft.com/en-us/microsoftteams/meeting-recording?tabs=meeting-policy))

### Turn it on so speakers will be identified in meetings

In meeting transcripts, live transcripts, captions and in meeting recaps
using Copilot, you will want users to be able to identify the person
that is talking during the meeting. By default, this is turned on at the
organization level (Global (Org-wide default) policy), but in the case
you want to turn this off for another part of your organization, you can
create a new meeting policy.

You can use PowerShell to set this:

*Set-CsTeamsMeetingPolicy -Identity Global -SpeakerAttributionMode
automatic*

**Speaker Attribution Modes**:

> **Automatic**: In this mode, Teams automatically detects and
> attributes the speaker based on audio input. It identifies who is
> speaking and displays their name next to their audio stream.
>
> **Manual**: In manual mode, the meeting organizer or participants can
> manually attribute the speaker by selecting their name from the
> participant list.
>
> **Off**: Disabling speaker attribution means that Teams won't display
> speaker names next to audio streams.

You can optionally tell users to go verify that it's turned on by going
to in the Teams app to **Settings** \> **Captions and transcripts** \>
**Automatically identify me in meeting captions and transcripts** and
make sure it's turned on.

![](media/image4.png){width="4.030641951006125in"
height="1.6751279527559055in"}

### Turn on voice and face enrollment

Admins can turn on or off voice and face enrollment for specific users,
or groups using the [Team meeting
policy](https://learn.microsoft.com/en-us/powershell/module/teams/set-csteamsmeetingpolicy).
You can use a new meeting policy you create or use the Global (Org-wide
default) policy to turn this on using the Teams admin center or
PowerShell.

By default, voice and face enrollment is disabled for all users in the
organization, but admins can change this setting using PowerShell.

To use PowerShell to turn this on:

*Set-CsTeamsMeetingPolicy -Identity Global -EnrollUserOverride Enabled*

To enable or disable voice and face enrollment for specific users,
admins can either assign a custom meeting policy to the users or use the
following PowerShell cmdlet.

You can use PowerShell to apply the setting to a custom policy:

*Grant-CsTeamsMeetingPolicy -Identity -PolicyName -EnrollUserOverride
Enabled*

**Note:** There isn't a way to set this in Teams admin center.

**Learn more:** [\[Voice
recognition\](/microsoftteams/rooms/voice-recognition](https://learn.microsoft.com/en-us/microsoftteams/rooms/voice-recognition))

### Set up voice and face recognition profiles

Tell your users to set up a voice profile in the Teams app. Each person
who will be attending in the meeting room (as opposed to remotely) sets
up their digital voice profile in the system so that they will be
identified in the transcription. 

1.  Go to your profile picture select **More options**  ![Microsoft
    Teams more options
    icon](media/image5.png){width="0.20833333333333334in"
    height="0.20833333333333334in"}  \> **Settings **and look
    under **Language** and make sure that your Teams language is set
    to **English**.** **You can enroll your voice profile in EN-US,
    EN-GB, EN-CA, EN-AU, IE (Indian English), or NZE (New Zealand
    English).

2.  Under **Settings** again, select **Recognition **and then **Create
    voice profile.**

3.  On the next screen, select the microphone, select **Create voice
    profile** and read the text that is in the box.

![A screenshot of a computer Description automatically
generated](media/image6.png){width="3.820774278215223in"
height="2.3361417322834646in"}

If have turned on Face profiles in your organization, the **Create face
profile** button will be available to end users. By selecting the
button, they can set up their face profile that will be used in
meetings.

**Learn more:** \[Identify in-room meeting
participants\]([/office/use-microsoft-teams-intelligent-speakers-to-identify-in-room-participants-in-a-meeting-transcription-a075d6c0-30b3-44b9-b218-556a87fadc00#bkmk_setupvoiceprofile](https://support.microsoft.com/en-us/office/use-microsoft-teams-intelligent-speakers-to-identify-in-room-participants-in-a-meeting-transcription-a075d6c0-30b3-44b9-b218-556a87fadc00#bkmk_setupvoiceprofile))

### Set up and use Microsoft Teams Intelligent Speakers to identify in-room participants in a meeting transcription (Optional)

If your organization\'s [Microsoft Teams
Rooms](https://rooms.microsoft.com/) are equipped with Intelligent
Speakers, you can hold meetings where in-room participants can be
identified in live transcription. During the meeting, all participants
can then easily see who's saying what, and the post-meeting transcript
identifies both remote and in-room attendees.

**Learn more:** \[Identify in-room meeting
participants\]([/office/use-microsoft-teams-intelligent-speakers-to-identify-in-room-participants-in-a-meeting-transcription-a075d6c0-30b3-44b9-b218-556a87fadc00#bkmk_setupvoiceprofile](https://support.microsoft.com/en-us/office/use-microsoft-teams-intelligent-speakers-to-identify-in-room-participants-in-a-meeting-transcription-a075d6c0-30b3-44b9-b218-556a87fadc00#bkmk_setupvoiceprofile))

### Enable Intelligent Speaker user recognition

Voice profile data can be used in any meeting with an Intelligent
Speaker. See [Teams meetings
policies](/microsoftteams/rooms/voice-and-face-recognition) and
the [PowerShell meeting
cmdlets](/microsoftteams/teams-powershell-overview) for information on
the meeting settings.

You can use PowerShell to turn this on:

*Set-CsTeamsMeetingPolicy -Identity PolicyName
-roomAttributeUserOverride Attribute -AllowTranscription \$true*

## Connect to the Microsoft Copilot Dashboard

If you have assigned a Copilot license to your users, you can use the
Copilot Dashboard. The Microsoft Copilot Dashboard provides actionable
insights to help your organization get ready to deploy AI, drive
adoption based on how AI is transforming workplace behavior, and measure
the impact of Copilot.

Some of the dashboard's metrics and functionalities are available to any
customer with a Microsoft 365 or Office 365 subscription for business or
enterprise. Learn about these features in [Connect to the Microsoft
Copilot Dashboard for Microsoft 365
customers](https://learn.microsoft.com/viva/insights/org-team-insights/copilot-dashboard).

If you have access to the Copilot Dashboard, you can find it in
the [Teams or web
app](https://insights.cloud.microsoft/#/CopilotDashboard).

1.  Open the Teams app on desktop or the web. If you have the Viva
    Insights app pinned, select it from the left bar.

If you don't have the Viva Insight app pinned, select the ellipses on
the left. Then in the search field, enter Microsoft Viva Insights, and
select it.

2.  On the left navigation panel, select Copilot Dashboard.

3.  To learn more about the data in the dashboard, refer
    to [Interpreting the dashboard
    data](https://learn.microsoft.com/en-us/viva/insights/org-team-insights/copilot-dashboard#interpreting-the-data).

If you need to let individual users access the Copilot Dashboard:

In the [Microsoft 365 admin
center](https://admin.microsoft.com/adminportal/home?#/viva/insights):

To enable access for new report users:

1.  Go to the **Settings** tab and select **Microsoft Viva**,
    then **Viva Insights**. You need to enter your credentials if
    you\'re not already signed in.

2.  Under **Viva Insights** in Microsoft 365, select **Manage settings**
    for viewing the Copilot dashboard.

3.  Select **Add users**.

4.  Search for the people you\'d like to add and select them from the
    list.

5.  At the bottom, select **Add**.

**Learn more:** [\[Copilot
Dashboard\](/viva/insights/org-team-insights/copilot-dashboard](https://learn.microsoft.com/en-us/viva/insights/org-team-insights/copilot-dashboard))


