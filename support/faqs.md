---
description: FAQs to assist you with using Cider.
---

## How to Find the Application Data Directory

The location of your application data varies depending on your operating system.
* For Windows-based operating systems, the path is `%APPDATA%/Cider/`
* For Linux users, the AppData can be found in `.config/Cider/`.
* For macOS the path is `Library/Application Support/Cider/`.

***

## MPRIS Integration Information

For those who are using Linux and intend on using a script to display song information, you can utilise the cider MPRIS integration with the `org.mpris.MediaPlayer2.cider` or cider identifier. If you wish to find out more about MPRIS, visit the [arch wiki page](https://wiki.archlinux.org/title/MPRIS).

***

## Why is my Discord RPC status not appearing?

Try the following if Discord Rich Presence is not appearing on Discord.

<details>
<summary>Activity Status Message</summary>

***
Make sure that 'Display current activity as a status message' is enabled in your Activity Status category in the Discord settings.
Cider will not appear as a game, so do not manually add it.

![Discord Activity Status Message](https://i.imgur.com/3znfOMh.png)

</details>

<details>
<summary>Snapcraft Store Issues</summary>

***
If you are using Discord from the Snap Store, you are advised to install from a different source (Discords Website or using another package manager).
The Snap Store version of Discord is known to have issues with DiscordRPC.
</details>

<details>
<summary>Permissions</summary>

***
Ensure that you are running Discord on a level that is below Cider. If Discord is being elevated, Cider will be unable to connect.
Furthermore, **ensure that Discord is started first**. Cider has to connect to Discord and this is only done on Cider's launch. So make sure Discord is started before Cider.
</details>

***

## Cider on Wayland

If you experience issues when running Cider on the Linux Wayland Desktop Server, pass the following arguments when launching the app:
`--enable-features=UseOzonePlatform --ozone-platform=wayland`

***

## Cannot Cast on my Network (Windows)

For issues when attempting to cast your music, do the following:
1. Open Control Panel
2. Click Network and Internet
3. Click Network and Sharing centre
4. Click Change Advanced Sharing Settings on the left-hand side
5. Expand the Guest or Public list and turn on both options.
6. Restart your PC