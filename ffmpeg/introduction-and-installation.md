# FFmpeg

FFmpeg is a free and open-source software project consisting of a suite of libraries and programs for handling video, audio, and other multimedia files and streams.

FFmpeg is not needed in general although it is required for AirPlay Casting support.

For a guide on Installation, pick your OS and follow the instructions.

<details>

<summary>Windows</summary>

## Download

1. Head over to [FFmpeg's Official Website](https://ffmpeg.org/) and download the latest version.
2. If you have downloaded a ZIP file (.zip, .7z, etc.), Create a folder named `FFmpeg` in the `C:\` drive and extract it there.

## Installation

1. Open Control Panel and look for `Edit the system environment variables` and open it. You can also search for it in the search bar or settings.
2. Head across to Environment Variables if not already in it.
3. Locate Path under User variables and double click it.
4. Click on the New button and add the folder location in which you extracted FFmpeg.
5. Once done, click on the Ok button and now you can close it.

You've now successfully downloaded and installed FFmpeg installed on your windows machine.

</details>

<details>

<summary>Linux</summary>

## Installation of FFmpeg on Ubuntu and Linux Mint

Open a new terminal (CTRL+ALT+T) and then run the following commands.

    ```
    $ sudo apt update
    $ sudo apt install ffmpeg
    $ ffmpeg -version
    ```

## Installation of FFmpeg on Debian

FFmpeg should be installed on Debian by default and can also be installed by running the following commands.

    ```
    $ sudo apt update
    $ sudo apt install ffmpeg
    $ ffmpeg -version
    ```

## Installation of FFmpeg on CentOS and RHEL

Installation of FFmpeg on CentOS and RHEL requires you to enable EPEL and RPM Fusion repository on the system using the following commands.

    Enable EPEL using the following command

    ```
    # yum install epel-release
    ```

    Enable RPM Fusion using the following command.

    ```
    -------------- On CentOS & RHEL 8.x --------------
    # yum localinstall --nogpgcheck https://download1.rpmfusion.org/free/el/rpmfusion-free-release-8.noarch.rpm https://download1.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-8.noarch.rpm

    -------------- On CentOS & RHEL 7.x --------------
    # yum localinstall --nogpgcheck https://download1.rpmfusion.org/free/el/rpmfusion-free-release-7.noarch.rpm https://download1.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-7.noarch.rpm

    -------------- On CentOS & RHEL 6.x --------------
    # yum localinstall --nogpgcheck https://download1.rpmfusion.org/free/el/rpmfusion-free-release-6.noarch.rpm https://download1.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-6.noarch.rpm
    ```

    You can now install FFmpeg by running the following command.

    ```
    # yum install ffmpeg ffmpeg-devel
    # ffmpeg -version
    ```

## Installation of FFmpeg on Fedora

You are required to enable RPM Fusion to install FFmpeg. Run the following command below to install FFmpeg.

    ```
    $ sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
    $ sudo dnf install ffmpeg ffmpeg-devel
    $ ffmpeg -version
    ```

## Installation of FFmpeg on Arch Linux

Install FFmpeg by running the following command.

    ```
    $ sudo pacman -S ffmpeg
    $ yay -S ffmpeg-git
    $ yay -S ffmpeg-full-git
    $ ffmpeg -version
    ```

## Installation of FFmpeg on openSUSE

Install FFmpeg by running the following command.

    ```
    -------------- On openSUSE Tumbleweed --------------
    $ sudo zypper addrepo -cfp 90 'https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/' packman
    $ sudo zypper refresh
    $ sudo zypper install --from packman ffmpeg
    $ ffmpeg -version

    -------------- On openSUSE Leap --------------
    $ sudo zypper addrepo -cfp 90 'https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Leap_$releasever/' packman
    $ sudo zypper refresh
    $ sudo zypper install --from packman ffmpeg
    $ ffmpeg -version
    ```

You've now successfully downloaded and installed FFmpeg installed on your Linux machine.

</details>

<details>

<summary>MacOS</summary>

## Download

1. Head over to [FFmpeg's Official Website](https://ffmpeg.org/) and download the latest version.
2. If you have downloaded a ZIP file (.zip, .7z, etc.), Create a folder named `audio-orchestrator-ffmpeg` in your home folder and a sub-folder named `bin` inside of it. Extract the files in the `bin` folder you've just created.

## Installation

1. Double click on the `ffmpeg` file and open it.
2. If you are prompted with an error message saying "ffmpeg can’t be opened because it is from an unidentified developer", click on the “OK” button.
   1. Go to System Preferences > Security and Privacy and click on the General tab.
   2. At the bottom of the window you will see a message saying that ffmpeg was blocked. Click "Open Anyway".
      1. If you do not see this message in the General tab, double-click ffmpeg again.
      2. You may have to click the "unlock" button and enter your password to be able to click "Open Anyway".
3. If you are prompted with an error message saying “ffmpeg is from an unidentified developer. Are you sure you want to open it?”, click "Open".
4. If a terminal window pops up, Keep it open until you see a confirmation message saying you can close the terminal.

You've now successfully downloaded and installed FFmpeg installed on your macOS machine.

</details>

Now that you have FFmpeg installed on your operating system, you have to provide the location of FFmpeg to Cider in order for it to use it.

1. Go to Cider Settings
2. Head over to Advanced tab.
3. Under Experimental section, Provide FFmpeg's location.
