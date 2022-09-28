# volumio-plugins-sources
Volumio plugins source code for Volumio 3

You want to write a plugin to extend Volumio, or before sending a Pull Request, please have a look [here](https://developers.volumio.com)

# What's this?

This fork of the volumio sources adds a plugin that allow to change the playlist with NFC tags.

# How to install the plugin

- Go to the Volumio Test Player by visiting the following url: `http://volumio.local/dev/` or `http://<volumio-ip-address>/dev`
- Enable `Plugins Test Mode` and `SSH`
- Connect to Volumio via SSH via `ssh volumio@volumio.local` or `ssh volumio@<volumio-ip-address>` using password `volumio`
- In the SSH client, clone this repository by executing `git clone https://github.com/gaelgubian/volumio-plugins-sources`
- Navigate to the plugin's folder by executing `cd volumio-plugins-sources/nfc_reader`
- Execute the command `volumio plugin install` and wait for it to finish
  (Volumio 2.x will hang on "Finalizing installation", but the plugin has already been installed successfully; just hit CTRL-C and continue to the next step)
- Close the SSH connection
- In the Volumio web interface, go to `Plugins` -> `Installed Plugins` and enable the plugin
- Restart Volumio

# Updating the plugin

- Connect to Volumio via SSH via `ssh volumio@volumio.local` or `ssh volumio@<volumio-ip-address>` using password `volumio`
- Go into the `volumio-plugins-sources` folder by executing `cd volumio-plugins-sources`
- Execute `git pull`
- Go into the `nfc_reader` folder by executing `cd nfc_reader`
- Execute `volumio plugin refresh`
- Execute `volumio vrestart` or `reboot`
