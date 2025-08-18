
## Anaconda on MacOS

### Optional: Uninstall older versions

On MacOS, I first removed the previous installation using:

    Open Finder and Go to the Applications folder.
    Move the Anaconda Navigator to the trash and empty the trash.

I then had to remove the anaconda3 folder using:

    cd /opt
    sudo rm -rf anaconda3

### Install new Anaconda using Command Prompt

I installed Anaconda manually using:

    curl -O https://repo.anaconda.com/archive/Anaconda3-2024.10-1-MacOSX-arm64.sh
    cd /opt
    bash Anaconda3-2024.10-1-MacOSX-arm64.sh

