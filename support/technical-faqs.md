---
description: >-
  The main FAQs for those who wish to learn more about Cider's code base or wish
  to integrate it with their system.
---

# Technical FAQs

<details>

<summary>Cider Media Player Information (MPRIS - Linux)</summary>

For those who are using Linux and intend on using a script to display song information, you can utilise the cider MPRIS integration with the `org.mpris.MediaPlayer2.cider` or cider identifier. If you wish to find out more about MPRIS, visit the [arch wiki page](https://wiki.archlinux.org/title/MPRIS).

</details>

<details>

<summary>Running Cider for Development</summary>

While we encourage the use of the `dist` command in the compiling documentation, the main command that is useful for testing most functionality of the app is with the following commands:

* &#x20;`start`&#x20;
  * This launches the app using normal electron and building the JS from Typescript.
* `start-renderer`
  * This launches the app using normal electron but does not build new build files. (Build would need to be run previously, but if no changes have been made to the backend this command would work fine.)

Both these commands allow the app to launch with the notable limitation on macOS and Windows of no playback. Linux playback works in an uncompiled state.

</details>
