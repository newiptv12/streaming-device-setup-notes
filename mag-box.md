# MAG set-top box checklist

Covers Infomir **MAG** boxes running the standard Linux-based **Embedded Portal**, such as MAG250, 254, 256, 322, 324, 349, 351 and similar models.

> **Android-based MAG models** (for example MAG424 and MAG524) work like an Android TV box instead: see [`android-tv.md`](android-tv.md) for those. Menu names can also differ if your box runs custom firmware from a previous seller. If your path is different, please open an issue with your model and the menu path you see.

MAG boxes work differently from Smart TVs and streaming sticks:

- There is **no app store**. The box loads a **portal** (a server address) from your provider.
- Sign-in is usually done with the box's **MAC address**, not a username and password.
- Most settings live under **Settings > System settings**. Pressing **Setup** (or **Set**) on the remote opens the same menu.

---

## 1. Network check

1. Open **Settings > System settings > Network info** to see whether the box has an IP address and is connected.
2. To change the connection, open **System settings > Network** and choose **Wired (Ethernet)** or **Wireless (Wi-Fi)**.

If the connection is missing or slow:

- **Use the Ethernet port.** MAG boxes are designed for wired connections, and many models need an external USB adapter for Wi-Fi. A cable is the single biggest fix for buffering.
- Restart the router: unplug it for 30 seconds, then plug it back in.
- If **Network info** shows no IP address, check that the cable clicks into both the box and the router, and try a different router port.
- If the box is connected but the portal won't load, see section 3: the portal address is the usual cause.

## 2. Software comes from Infomir only

There's nothing to install from a store; the portal software is built into the box. What matters is keeping the box's own firmware up to date and official.

- **Update from the box:** Settings > System settings > **Software update** > set **Update method = HTTP** > **Verify (OK)** > **Update (F1)**.
  The default update address on factory firmware is `http://update.infomir.com/mag/<model>/imageupdate`, where `<model>` is your model number (for example `322`).
- **Don't switch the box off or unplug the network cable during an update.** The box restarts on its own when it finishes.
- **Second-hand boxes:** some sellers load custom firmware that blocks resets or updates. If a factory reset doesn't fully restore the box, reload the official Infomir firmware for your model.
- Only install firmware from Infomir's own servers or your provider. Firmware files from random websites can permanently break the box.

## 3. Sign-in fields

### MAC address

Most providers activate your box by its **MAC address**. Find it on the **sticker on the bottom of the box** or under **System settings > Device info** (shown as *About*, or *Network info* on some versions). It looks like `00:1A:79:xx:xx:xx`. Send it to the provider exactly as shown, and wait for them to confirm it's activated before entering the portal.

### Portal URL

1. Open **Settings > System settings > Servers > Portals**.
2. Fill in **Portal 1 name** (any label) and **Portal 1 URL** (exactly as your provider sent it). Press **KB** on the remote to bring up the on-screen keyboard.
3. Press **OK** to save, then go back and choose **Restart portal** (or reboot the box).

Common mistakes:

| Problem | What happens | Fix |
|---|---|---|
| Typo in the portal URL | Blank screen, "Page loading error" or the box falls back to the Embedded Portal | Re-type it slowly; check every `/` and `.` |
| Missing `/c/` or trailing slash | Portal fails to load | Copy the ending exactly, e.g. `…/c/` |
| Wrong scheme or port | `https://` instead of `http://`, or a missing `:port` | Copy both exactly as given |
| MAC not activated yet | Portal loads but shows an error or no channels | Confirm with the provider that your MAC is registered |
| Wrong MAC sent | Same as above | Read the MAC from the box's menu, not from memory |

For what each error code means, see [`error-codes.md`](error-codes.md).

## 4. Common faults

Work through these in order. Stop as soon as the problem is fixed.

| Symptom | Try this |
|---|---|
| Channels freezing or the portal stuck loading | **Restart portal** from System settings, or **reboot** the box: unplug the power for 30 seconds. |
| Portal doesn't load after a restart | Check **Network info** (section 1), then re-check the portal URL and MAC activation (section 3). |
| Problems started after a long time without an update | Run a **Software update** (section 2). |
| Picture fits badly or has black bars | Settings > System settings > **Video** and set the resolution and output mode to match your TV. |
| Box behaves strangely after changing settings | **Reset settings** from the Embedded Portal's system settings. You'll need to enter the portal URL again. |
| Box won't boot or nothing else worked | **Factory reset** from the **System Recovery Utility** (bootloader) menu: select **Default Settings** and confirm with **Yes**. On most models you open this menu by holding **Menu** on the remote while the box powers on. **This erases all settings, including your portal.** |

---

## Sources

- Infomir Wiki — [External portal loading](https://wiki.infomir.eu/eng/set-top-box/stb-linux-webkit/embedded-portal/external-portal-loading)
- Infomir Wiki — [Software update MAG322/324/349/351](https://wiki.infomir.eu/eng/set-top-box/stb-linux-webkit/mag322-324-349-351/software-update-mag322-324-349-351)
- Infomir Wiki — [System Recovery Utility MAG322/324/349/351](https://wiki.infomir.eu/eng/set-top-box/stb-linux-webkit/mag322-324-349-351/system-recovery-utility-mag322-324-349-351)
- Infomir Wiki — [MAG245/250/254/255/270/275 overview](https://wiki.infomir.eu/eng/stb-webkit/mag245-250-254-255-270-275)
