---
description: The main Frequently Asked Questions for Cider application support.
---

# FAQ

{% hint style="info" %}
This is essential knowledge for the debugging process, please read these before creating an issue.
{% endhint %}

<details>

<summary>How to find the Application Data Directory</summary>

The location of your application data varies depending on your operating system.

* For users on Windows using the GitHub release, the path is `%APPDATA%/Cider/`
* For users of the Microsoft Store release of Cider, the path is `/Program Files/WindowsApps/**Cider**`
* For Linux users, the AppData can be found in `~/.config/Cider/`.
* For macOS the path is `Library/Application Support/Cider/`.

</details>

## Why is my DiscordRPC status not appearing?

Try the following if Discord Rich Presence is not appearing on Discord.&#x20;

<details>

<summary>Discord Desktop Client Only</summary>

Ensure you only have the Discord desktop client, not the web client open. As Cider is not directly connected to Discord we cannot have your status showing when not connected to Cider directly through Discord's Rich Presence functionality.

</details>

<details>

<summary>Activity Status Message</summary>

Make sure that 'Display current activity as a status message' is enabled in your Activity Status category in the Discord settings. Cider will not appear as a game, so do not manually add it.

<img src="https://i.imgur.com/3znfOMh.png" alt="Discord Activity Status Message" data-size="original">

</details>

<details>

<summary>Snapcraft Store Issues</summary>

If you are using Discord from the Snap Store, you are advised to install from a different source (Discords Website or using another package manager). The Snap Store version of Discord is known to have issues with DiscordRPC.

</details>

<details>

<summary>Permissions and Elevation</summary>

Ensure that you are running Discord on a level that is below Cider. If Discord is being elevated, Cider will be unable to connect. Furthermore, **ensure that Discord is started first**. Cider has to connect to Discord and this is only done on Cider's launch. So make sure Discord is started before Cider.

</details>

## Cannot Cast on my Network (Windows)

For issues when attempting to cast your music, do the following:

1. Open Control Panel
2. Click Network and Internet
3. Click Network and Sharing centre
4. Click Change Advanced Sharing Settings on the left-hand side
5. Expand the Guest or Public list and turn on both options.
6. Restart your PC
