# Samsung Smart TV (Tizen) checklist

Covers Samsung Smart TVs running **Tizen**, roughly 2016 models onward.

> Samsung moves menus around between model years. The paths below use the **2020-and-later** layout (Settings > All Settings > …) and list the older path in brackets where it differs. If your path is different, please open an issue with your model number (on the sticker on the back, or under Settings > Support > About This TV) and the menu path you see.

---

## 1. Network check

1. Press **Home**, go to **Settings > All Settings > Connection > Network > Network Status**.
   *(Older models: Settings > General > Network > Network Status.)*
2. The screen shows three icons: **TV → router → internet**. Blue dots mean that link works, a red **X** shows where it breaks.
   - **X between TV and router:** the TV isn't reaching your Wi-Fi.
   - **X between router and internet:** the TV is fine; the problem is the router or your internet line.

If the connection is missing or slow:

- Restart the router: unplug it for 30 seconds, then plug it back in.
- **Reset Network:** Settings > All Settings > Connection > Network > **Reset Network**, then reconnect with **Open Network Settings**.
- Some older Samsung models only support **2.4 GHz** Wi-Fi. If your 5 GHz network doesn't appear, connect to the 2.4 GHz one.
- Use an **Ethernet cable** if you can. Wired is almost always more stable for live TV.
- To test the whole chain at once, run **Smart Hub Connection Test**: Settings > All Settings > Support > Device Care > **Self Diagnosis** > Smart Hub Connection Test. It checks the gateway, DNS and Samsung's servers separately and tells you which step fails.

## 2. Install from the official store

- Install apps only from the TV's own **Apps** store (Home > **Apps**). Samsung TVs run Tizen, not Android, so Google Play apps and APK files **will not install**.
- Keep apps updated: in **Apps**, open **Settings** (gear icon) and turn on **Auto Update**.
- If an app is not in the store for your region or model year, a website claiming to "install it anyway" is not a safe workaround.

## 3. Sign-in fields

Type usernames, passwords and server addresses **exactly** as your provider sent them. The usual mistakes:

| Problem | What happens | Fix |
|---|---|---|
| First letter auto-capitalised | `User123` instead of `user123` → 401 error | Check the on-screen keyboard's shift key before typing |
| Trailing space | Extra space at the end → 401 error | Move the cursor to the end and delete it |
| Wrong scheme | `https://` where the provider gave `http://` (or the reverse) | Copy the scheme exactly |
| Missing port | `example.com` instead of `example.com:8080` → 404 or timeout | Include `:port` if the provider gave one |
| Letter/number mix-ups | `O` vs `0`, `l` vs `1` | Ask the provider for the details in a monospace font |

**Tip:** most Samsung Smart TVs accept a **USB keyboard**. Plugging one in makes long server addresses much easier to type correctly than the remote.

For what each sign-in error means, see [`error-codes.md`](error-codes.md).

## 4. Common faults

Work through these in order. Stop as soon as the problem is fixed.

| Symptom | Try this |
|---|---|
| Apps slow, freezing or not loading | **Cold boot:** hold the remote's **Power** button until the TV turns off and back on (about 5 seconds). Or unplug the TV for 1 minute. A normal "off" only puts the TV in standby. |
| Problems started after weeks without an update | Settings > All Settings > **Support > Software Update > Update Now**. Don't turn the TV off while it installs. |
| Whole TV feels sluggish | Settings > All Settings > Support > **Device Care > Start Device Care**. This scans the TV and frees memory. |
| Only one app misbehaves | Settings > All Settings > Support > Device Care > **Manage Storage** > select the app > **View Details > Clear Cache**. Use **Clear Data** only if cache didn't help — it signs you out of that app. *(2019 models: Support > Self Diagnosis > TV Device Manager.)* |
| The app is still broken | Delete it (Manage Storage > select app > **Delete**) and reinstall it from **Apps**. |
| Several apps broken or missing | **Reset Smart Hub:** Settings > All Settings > Support > Device Care > Self Diagnosis > **Reset Smart Hub**, default PIN **0000**. *(2016–2018: Support > Self Diagnosis > Reset Smart Hub.)* This signs you out of every app and removes apps you installed, so have your logins ready. It can't be run from inside an app — switch to Live TV or an HDMI input first. |
| Nothing else worked | **Factory reset:** Settings > All Settings > **General & Privacy > Reset**, PIN **0000**. *(Older: Settings > General > Reset.)* **This erases all apps, accounts and settings.** Use it last. |

---

## Sources

- Samsung Support — [How to verify network status on your Samsung TV](https://www.samsung.com/ca/support/tv-audio-video/verify-network-status-on-your-samsung-tv/)
- Samsung Support — [How to do Smart Hub Connection Test in Samsung TV](https://www.samsung.com/in/support/tv-audio-video/how-to-do-smart-hub-connection-test-in-samsung-tv/)
- Samsung Support — [Clear App Cache and Data on your Samsung TV](https://www.samsung.com/au/support/tv-audio-video/clear-app-cache-and-data-on-your-samsung-tv)
- Samsung Support — [Reset the Smart Hub on your Samsung TV](https://www.samsung.com/au/support/tv-audio-video/reset-smart-hub-samsung-tv)
- Samsung Support — [Apps freezing, not loading, missing or crashing](https://www.samsung.com/us/support/troubleshooting/TSG10000062)
- Samsung Support — [How to reset your Samsung TV](https://www.samsung.com/ca/support/tv-audio-video/reset-my-samsung-tv/)
