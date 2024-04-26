# sys-clk Config Manager - simple sys-clk config manager

Manage your sys-clk configs.

For example, one with power efficient handheld clocks for maximum battery and one with higher handheld clocks for max performance at the cost of battery life.

## Features
- **Change profile**: Will change the current sys-clk config.ini you are using. Based on the current profile you are on, it will copy the current config to that profile slot to save any edits you have made and then switch to the config.ini for the selected profile. This way you can switch to the OC profile, adjust any clocks in sys-clk, then switch to Eco, your OC profile will be saved automatically and your Eco profile loaded. You just can switch between configs and make changes in sys-clk as needed. Profile switches take effect immediately in sys-clk.

### Manual Settings
Use this submenu to perform manual actions

**Discarding current config and switching to a profile** will skip the step of saving any current changes made in sys-clk and just switch to the last saved config for any profile. For example, if you were on the Eco profile and changed a bunch of settings, but they weren't really working out, you can just switch to another profile and discard any changes to your Eco profile. When you switch back to the Eco profile, it will be whatever it used to be before you made any changes.

You can also discard current and use the same profile you are already on. For example, you're on the OC profile and want to try some different OC clocks in some games, but after making some changes, you found that your old clocks worked better, just `Discard current and use OC` and your latest changes will be reverted back to your saved OC profile.

**Copying current changes to a specific profile** - these options will completely overwrite any of the saved configs with your current sys-clk config.ini. For example if you load your OC profile and then select `Copy current to Test` it will completely wipe out any settings for any games you've set in that `Test` config slot and overwrite it with all of the config for all of the games you've set in your OC profile. It does not switch the current profile you are using.

- **Discard current and use OC**: will copy `/config/sys-clk/OC_config/config.ini` to `/config/sys-clk/config.ini` and refresh active profile
- **Discard current and use Eco**: will copy `/config/sys-clk/Eco_config/config.ini` to `/config/sys-clk/config.ini` and refresh active profile
- **Discard current and use Test**: will copy `/config/sys-clk/Test_config/config.ini` to `/config/sys-clk/config.ini` and refresh active profile
- **Copy current to OC**: will copy `/config/sys-clk/config.ini` to `/config/sys-clk/OC_config/config.ini`
- **Copy current to Eco**: will copy `/config/sys-clk/config.ini` to `/config/sys-clk/Eco_config/config.ini`
- **Copy current to Test**: will copy `/config/sys-clk/config.ini` to `/config/sys-clk/Test_config/config.ini`

## Getting Started

### Installation
 - [Ultrahand Overlay](https://github.com/ppkantorski/Ultrahand-Overlay) is required
 - Download the .zip file from the [latest release](https://github.com/Bikkies/sys-clk-Config-Manager/releases/latest)
 - Extract the zip file to your sd card

### Initial setup
None of the below steps are required to start using the tool, but you can follow them if you want to start with config already in place for each profile.

1. Create these directories on your SD card. If these folders do not exist, they will be created when you first switch profiles or use a manual option to copy config.
  - `/config/sys-clk/OC_config/`
  - `/config/sys-clk/Eco_config/`
  - `/config/sys-clk/Test_config/`

3. Copy your desired `config.ini` files from `/config/sys-clk/config.ini` into the specific folders.
