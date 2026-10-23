# Fire TV Stick checklist

Short checklist for getting a live TV app running on a Fire TV Stick or other Fire TV device, and for the faults that come up most. Labels can differ slightly between Fire OS versions.

## 1. Network check

- [ ] Open **Settings > Network**, highlight the connected network and press **Play/Pause** on the remote. This opens the built-in network status tool, which shows whether the device reaches the router and the internet.
- [ ] On compatible models, choose **Run Speed Test** or **Advanced** in that tool for more detail.
- [ ] If an "Unable to Connect" message appears, select **Network Diagnostics** on it and follow the on-screen steps.
- [ ] Still failing: **Settings > Network > Wi-Fi**, switch it off and on again.
- [ ] Still failing: forget the network (highlight it, press **Menu**, then **Select/OK**) and reconnect with the Wi-Fi password.
- [ ] Restart the modem, then the router: unplug both for 1 minute, plug the modem in first, give it about a minute, then the router.

## 2. Install the app from the official store

- [ ] Search for the app on the Fire TV home screen and install it from the device's own app store.
- [ ] Do not install apps from links, files or websites outside the store. These notes cover store installs only.
- [ ] Keep the app updated through the store.

## 3. Sign-in fields

Most live TV apps ask for some or all of these. Use exactly what the provider sent.

| Field | Typical mistake |
|---|---|
| Username | Remote keyboard adds a capital first letter |
| Password | A trailing space copied from a message |
| Server / portal address | Missing characters, old port number, wrong `http`/`https` |

Type each field slowly. If sign-in fails, check [error-codes.md](error-codes.md) for what the code means.

## 4. Fixes for common faults

| Symptom | Try this |
|---|---|
| Everything is slow or frozen | Restart: unplug the power for 10 seconds, then plug it back in. |
| Restarts on its own or behaves erratically | Use the power cable and adapter supplied with the device, plugged into a wall outlet. Try a different outlet. |
| Running old software | **Settings > Device & Software** (older menus show a device-name entry instead) **> About > Check for System Update**. Don't unplug it while an update installs. |
| Blank screen or the TV ignores the stick | **Settings > Display & Sounds > HDMI-CEC Device Control**: turn it off, then on. Reseat the stick, or try another HDMI port or cable. |
| One app is slow, the others are fine | Open the app's entry in the installed-applications list under **Settings** and clear its cache. Menu names vary by model and software version. Clearing data instead also removes the app's sign-in. |
| Nothing above works | Factory reset (this erases all apps and settings). |

## Report a fix

Found a different menu path on your model? Open an issue with the model, the Fire OS version and the exact path.

## Sources

- Fire TV help, "Can't Connect Your Fire TV Device to Wi-Fi": https://www.amazon.com/gp/help/customer/display.html?nodeId=GYMDPRQTTLXQD7PL
- Fire TV help, "Fire TV Keeps Restarting": https://www.amazon.com/gp/help/customer/display.html?nodeId=TRq7oK4PNR2e7Sk9j1
- Fire TV help, "Fix a Blank TV Screen on Fire TV Devices": https://www.amazon.com/gp/help/customer/display.html?nodeId=202154650
