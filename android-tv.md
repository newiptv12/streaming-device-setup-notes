# Android TV and Google TV checklist

Covers TVs and boxes running **Google TV** (Chromecast with Google TV, Google TV Streamer, Sony, TCL, Hisense and others) and older **Android TV** models.

> Menu names change between software versions and TV brands. The paths below use the current Google TV wording. On older Android TV models the same items usually sit under **Settings > Apps** or **Settings > Device Preferences** instead of **Settings > System**. If your path is different, please open an issue with your model and the menu path you see.

---

## 1. Network check

1. From the home screen, open **Settings > Network & Internet**.
2. Make sure **Wi-Fi** is on and you're connected to the right network.
3. If your TV shows **Check internet connection** (many TCL and Sony models do), run it. This confirms the TV can reach the internet, not just the router.

If the connection is missing or slow:

- Select your network, choose **Forget**, then pick it again and re-enter the password.
- Restart the router: unplug it for 30 seconds, then plug it back in.
- If your router has both bands, try the **5 GHz** network for streaming.
- Use an **Ethernet cable** if the TV or box has a port (or a USB-C Ethernet adapter for Chromecast with Google TV). Wired is almost always more stable for live TV.
- Some DNS-changing devices and ad-blocking boxes interfere with Google TV. Google's own help page suggests removing them to test.

## 2. Install from the official store

- Install apps only from the **Google Play Store** on the TV.
- To update apps: open the Play Store, select your **profile icon > Manage apps & games > Updates > Update all**.
- To keep them updated automatically: Play Store **Settings > Auto-update apps**.
- Avoid installing APK files from unknown websites. They don't get security updates and are a common cause of crashes.

## 3. Sign-in fields

Type usernames, passwords and server addresses **exactly** as your provider sent them. The usual mistakes:

| Problem | What happens | Fix |
|---|---|---|
| First letter auto-capitalised | `User123` instead of `user123` → 401 error | Check the keyboard's shift key before typing |
| Trailing space | Copy-paste adds a space at the end → 401 error | Delete the last character and retype it |
| Wrong scheme | `https://` where the provider gave `http://` (or the reverse) | Copy the scheme exactly |
| Missing port | `example.com` instead of `example.com:8080` → 404 or timeout | Include `:port` if the provider gave one |
| Letter/number mix-ups | `O` vs `0`, `l` vs `1` | Ask the provider for the details in a monospace font |

**Tip:** typing long server addresses with the remote is slow and error-prone. The **Google TV app** on your phone has a keyboard you can use instead — the phone and TV must be on the same Wi-Fi network.

For what each sign-in error means, see [`error-codes.md`](error-codes.md).

## 4. Common faults

Work through these in order. Stop as soon as the problem is fixed.

| Symptom | Try this |
|---|---|
| Video won't start or keeps freezing | **Restart:** Settings > System > Restart. Or unplug the power for 1 minute. |
| Device is frozen and the remote does nothing | Unplug the power cable, wait a few seconds, plug it back in. |
| Problems started after weeks without an update | **Settings > System > About > System update**, install anything available. |
| Only one app misbehaves | **Settings > Apps > See all apps >** select the app **> Clear cache**. Try **Clear data** only if cache didn't help — it signs you out of that app. |
| "Storage full" or apps install slowly | **Settings > System > Storage > Internal storage > Clear cached data > OK** clears the cache for all apps. Uninstall apps you don't use. |
| Picture works but no sound through a soundbar | Set **Digital audio out** to **Auto**, **PCM** or **Pass through** in the sound settings. |
| Remote stopped responding | Remove and reinsert the batteries, then check for a remote update in Settings > Remotes & Accessories. |
| Nothing else worked | **Factory reset:** Settings > System > About > Factory reset. **This erases all apps, accounts and settings.** Make sure you have your Wi-Fi password and app logins first. |

---

## Sources

- Google TV Help — [Fix problems with your Google TV device](https://support.google.com/googletv/answer/10070482)
- Google TV Help — [Fix an unresponsive Google TV device](https://support.google.com/googletv/answer/12360626)
- Chromecast Help — [Free up storage on Chromecast with Google TV](https://support.google.com/chromecast/answer/11276506)
- Sony Support — [Clear data and cache for apps on Android TV or Google TV](https://www.sony.ca/en/electronics/support/articles/00202472)
- TCL Support — [Google TV displays message: No internet connection](https://support.tcl.com/us-googletv-troubleshooting/2331802)
