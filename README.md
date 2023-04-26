# Corne-ish Zen Custom Configuration

![Corne-ish Zen Logo](zenlogo.png)

> **Warning**
>
> If you have a Corne-ish Zen from round 3 of the group buy (delivered after October 2022) you should use the the config repo for V2 PCBs, available at [LOWPROKB/zmk-config-zen-2](https://github.com/LOWPROKB/zmk-config-zen-2) instead of this one!

This repo is the official configuration of the Corne-ish Zen low profile wireless mechanical keyboard. Use it to develop your own keymap and easily build your own ZMK firmware to run on your Corne-ish Zen. These steps will get you using your keymap on your keyboard in the fastest time possible. It uses the GitHub Actions feature to build your firmware online, rather than setting up a complex tool chain on your local computer.
If you are looking to dig deeper into ZMK and develop new functionality, it is recommended to follow the steps of installing ZMK as found on the official ZMK documentation site (linked below).

**Note:** This process is temporary, and will be used until such time that the Corne-ish Zen board definition is merged into ZMK Main.

## Resources
- The [official ZMK Firmware GitHub](https://github.com/zmkfirmware/zmk) repository. View the keymaps for other boards and shields as a starting point for your keymap.
- The [official ZMK Documentation](https://zmk.dev/docs) web site. Find the answers to many of your questions about ZMK Firmware.
- The [official ZMK Discord Server](https://discord.gg/8cfMkQksSB). Instant conversations with other ZMK developers and users. Great technical resource!

## Instructions
1. Log into, or sign up for, your personal GitHub account.
2. Fork this repository to your local computer, and then push it to your GitHub personal account. ([instructions](https://docs.github.com/en/get-started/quickstart/fork-a-repo))
3. Edit the keymap file(s) to suit your needs
4. Commit and push your changes to your personal repo. Upon pushing it, GitHub Actions will start building a new version of your firmware with the updated keymap.

## Firmware Files
To locate your firmware files...
1. log into GitHub and navigate to your personal config repository you just uploaded your keymap changes to.
2. Click "Actions" in the main navigation, and in the left navigation click the "Build" link.
3. Select the desired workflow run in the centre area of the page (based on date and time of the build you wish to use). You can also start a new build from this page by clicking the "Run workflow" button.
4. After clicking the desired workflow run, you should be presented with a section at the bottom of the page called "Artifacts". This section contains the results of your build, in a file called "firmware.zip"
5. Download the firmware zip archive and extract the two .uf2 files. They are named according to which side they need to be flashed to.
6. Flash the firmware to your keyboard by double-clicking the reset button to put the it in bootloader mode. A window should pop up showing the contents of the storage on the keyboard. Drag and drop the correct .uf2 file into the window. When the upload is complete the window will close and the keyboard will exit bootloader mode.

Your keyboard is now ready to use.

