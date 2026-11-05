# LG Smart TV (webOS) checklist

Covers LG Smart TVs running **webOS**, from roughly 2014 models up to webOS 25.

> LG changes menu paths almost every year, so this file lists them by webOS version. To find yours, open **Settings > All Settings > General > About This TV** (or **Support > TV Information** on newer models). If your path is different, please open an issue with your model number, webOS version and the menu path you see.

| webOS version | Model years |
|---|---|
| webOS 24 / 25 | 2024–2025 |
| webOS 6.0 – 23 | 2021–2023 |
| webOS 5.0 | 2020 |
| webOS 4.5 and earlier | 2019 and older |

---

## 1. Network check

Open the network settings:

| webOS | Path |
|---|---|
| 6.0 – 25 | Settings > All Settings > **General > Network** > Wired Connection or Wi-Fi Connection |
| 5.0 | Settings > All Settings > **Connection > Network Connection Settings** |
| 4.5 | Settings > All Settings > **Connection** |
| 4.0 and earlier | Settings > All Settings > **Network** |

The status panel lists icons in sequence: **TV → Gateway → DNS → Internet**. An **X** shows where the connection breaks:

- **X after the TV:** the TV isn't reaching the router. Check the Wi-Fi password, or move the router closer.
- **X at Gateway:** restart the router (unplug for 30 seconds).
- **X at DNS:** the router is reachable but name lookups fail. Restart the router; if it keeps happening, ask your internet provider.
- **X at Internet:** the TV is fine; the problem is the router or your internet line. Check whether other devices are online.

Other fixes:

- Use an **Ethernet cable** if you can. Wired is almost always more stable for live TV.
- If other devices work but only the TV can't connect, LG's own help pages suggest contacting LG support.

## 2. Install from the official store

- Install apps only from the TV's own store (**LG Content Store**, shown as **Apps** on newer models). Press **Home**, open the store, and use **Search**.
- LG TVs run webOS, not Android, so Google Play apps and APK files **will not install**.
- An app update can stop working if the TV's own software is out of date. Keep both updated (see section 4).

## 3. Sign-in fields

Type usernames, passwords and server addresses **exactly** as your provider sent them. The usual mistakes:

| Problem | What happens | Fix |
|---|---|---|
| First letter auto-capitalised | `User123` instead of `user123` → 401 error | Check the on-screen keyboard's shift key before typing |
| Trailing space | Extra space at the end → 401 error | Move the cursor to the end and delete it |
| Wrong scheme | `https://` where the provider gave `http://` (or the reverse) | Copy the scheme exactly |
| Missing port | `example.com` instead of `example.com:8080` → 404 or timeout | Include `:port` if the provider gave one |
| Letter/number mix-ups | `O` vs `0`, `l` vs `1` | Ask the provider for the details in a monospace font |

**Tip:** the **Magic Remote** works as a pointer, which makes the on-screen keyboard faster than arrow keys. Most LG TVs also accept a **USB keyboard**.

For what each sign-in error means, see [`error-codes.md`](error-codes.md).

## 4. Common faults

Work through these in order. Stop as soon as the problem is fixed.

| Symptom | Try this |
|---|---|
| Apps slow, freezing, or "This app will now restart to free up more memory" | **Turn off Quick Start+**, then unplug the TV for a few minutes. With Quick Start+ on, switching off with the remote only puts the TV into a fast standby, so problems survive the restart. Location: webOS 24/25 **General > System > Additional Settings**; webOS 22/23 **General > Devices > TV Management**; older **General > Additional Settings** or directly under **General**. |
| Problems started after weeks without an update | **webOS 5.0 and later:** Settings > All Settings > **Support**, open **Software Update**, then **Check for Updates**. **webOS 4.5 and earlier:** Settings > All Settings > **General > About This TV**, then **Check for Updates**. Turn on **Allow Automatic Updates** on the same screen. |
| Only one app misbehaves | LG TVs generally have no per-app "Clear cache" button, so LG's own advice is to **delete and reinstall the app**: highlight it on the Home screen, long-press **OK** to enter edit mode, select the **X** or trash icon, then reinstall it from the store. Some newer models have a **Device Self Care** option under Support or General — use it if you see it. |
| Several apps broken and nothing above helped | **Reset to Initial Settings:** webOS 6.0–25 **General > System > Reset to Initial Settings**; webOS 5.0 **Support > Reset to Initial Settings**; webOS 4.5 and earlier **General > Reset to Initial Settings**. On webOS 24/25 you can choose **Reset all except network settings** to keep your Wi-Fi. **This erases all apps, accounts and settings.** Don't unplug the TV while it resets. |

---

## Sources

- LG Support — [How to check the internet connection status on your TV](https://www.lg.com/bd/support/product-help/CT40008099-20154863262975)
- LG Support — [How to Update Your LG TV Software and Turn On Automatic Updates](https://www.lg.com/us/support/help-library/how-to-update-your-lg-tv-software-and-turn-on-automatic-updates--20155444905539)
- LG Support — [How to fix apps that keep freezing, crashing, or won’t load](https://www.lg.com/us/support/help-library/lg-tv-how-to-fix-apps-that-keep-freezing-crashing-or-wont-load--20154996607566)
- LG Support — [Reset to initial settings](https://www.lg.com/uk/support/product-support/troubleshoot/help-library/cs-CT00008386-20155142900522/)
