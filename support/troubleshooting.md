---
description: Some useful steps to resolving your issues.
---

Troubleshooting can be done in a series of ways. Below is a list of the current methods you can troubleshoot issues with the application.

## **Clean Installation**
* A clean installation can be done by doing the following guide associated with your operating system:

{% hint style="warning" %}
Note: This will remove your login state, settings and followed artists.
{% endhint %}

***

<details>
<summary>Windows</summary>

1. Uninstall the `Cider` application using the control panel.
2. Delete the following folders: 
   * `%appdata%/Cider` (*If its present*)
   * `%LOCALAPPDATA%\Programs\cider` (*If its present*)
   * `%LOCALAPPDATA%\cider-updater` (*If its present*)
3. Reinstall `Cider`.
</details>

***

<details>
<summary>Linux</summary>

1. Uninstall the `Cider` application using your system uninstaller.
2. Delete the `.config/Cider` folder. (*If its present*)
3. Reinstall `Cider`.
</details>

***

<details>
<summary>macOS</summary>

1. Delete the `Cider.app` file from your Applications folder.
2. Delete the `Library/Application Support/Cider` folder. (*If its present*)
3. Reinstall `Cider`
</details>