# List of System Bloatware Packages to Uninstall from Realme UI Using ADB

> **Disclaimer:** Removing system apps can impact your device's performance or functionality. Proceed with caution and only uninstall apps you are certain are unnecessary. **This guide is for educational purposes only!**

---

## 🚀 Getting Started

### 1. **Set Up ADB on Your Computer**

ADB (Android Debug Bridge) lets you communicate with your device directly from your computer, and it’s an essential tool for uninstalling system bloatware. 

1. Install ADB on your computer if you haven’t already. You can [download it here](https://developer.android.com/studio/releases/platform-tools).
2. Enable **Developer Options** on your device by going to `Settings > About phone > Build number` and tapping it multiple times.
3. Enable **USB Debugging** in `Settings > Developer Options`.

### 2. **Connect Your Device**

1. Connect your Realme device to your computer via USB.
2. Open a terminal or command prompt.
3. Type the following command to ensure ADB recognizes your device:

   ```bash
   adb devices
   ```

   > You should see your device listed. If prompted, authorize the connection on your phone.

---

## 🔍 Finding & Uninstalling Bloatware Packages

1. **List all installed packages on your device:**

   ```bash
   adb shell pm list packages
   ```

2. **Search for a specific package:**

   Replace `<keyword>` with the app name you’re looking for (e.g., `facebook` or `gamecenter`):

   ```bash
   adb shell pm list packages | grep <keyword>
   ```

3. **Uninstall a package:**

   Replace `<package_name>` with the actual package name you want to remove (e.g., `com.facebook.app`):

   ```bash
   adb shell pm uninstall -k --user 0 <package_name>
   ```

   > ⚠️ **Note:** Uninstalling certain system packages may lead to instability or reduced functionality of your device.

4. **Reinstall a package (if needed):**

   If you want to reinstall any uninstalled package, you can use:

   ```bash
   adb shell cmd package install-existing <package_name>
   ```

---

## 📄 Bloatware Packages in Realme

Here’s a list of packages you may consider uninstalling, along with their commands. This package list is specifically tailored for the Realme RMX2085 running RealmeUI 2 but is expected to be compatible with other versions as well.
| App/Service                         | Package Name                              | Uninstall Command                                                       |
|-------------------------------------|-------------------------------------------|-------------------------------------------------------------------------|
| Facebook App                        | `com.facebook.app`                        | `adb shell pm uninstall -k --user 0 com.facebook.app`                  |
| Realme Game Center                  | `com.oppo.gamecenter`                     | `adb shell pm uninstall -k --user 0 com.oppo.gamecenter`               |
| Realme App Market                   | `com.oppo.market`                         | `adb shell pm uninstall -k --user 0 com.oppo.market`                   |
| Realme Browser                      | `com.coloros.browser`                     | `adb shell pm uninstall -k --user 0 com.coloros.browser`               |
| Hot Apps                            | `com.opos.cs`                             | `adb shell pm uninstall -k --user 0 com.opos.cs`                       |
| Phone Manager                       | `com.coloros.phonemanager`                | `adb shell pm uninstall -k --user 0 com.coloros.phonemanager`          |
| HeyTap Cloud                        | `com.heytap.cloud`                        | `adb shell pm uninstall -k --user 0 com.heytap.cloud`                  |
| HeyTap Pictorial                    | `com.heytap.pictorial`                    | `adb shell pm uninstall -k --user 0 com.heytap.pictorial`              |
| HeyTap User Center                  | `com.heytap.usercenter`                   | `adb shell pm uninstall -k --user 0 com.heytap.usercenter`             |
| Google Search                       | `com.google.android.googlequicksearchbox` | `adb shell pm uninstall -k --user 0 com.google.android.googlequicksearchbox` |
| OK Google Hotword Enrollment        | `com.android.hotwordenrollment.okgoogle`  | `adb shell pm uninstall -k --user 0 com.android.hotwordenrollment.okgoogle` |
| Google Assistant                    | `com.google.android.apps.googleassistant` | `adb shell pm uninstall -k --user 0 com.google.android.apps.googleassistant` |
| Google Lens                         | `com.google.ar.lens`                      | `adb shell pm uninstall -k --user 0 com.google.ar.lens`                |
| HeyTap Browser                      | `com.heytap.browser`                      | `adb shell pm uninstall -k --user 0 com.heytap.browser`               |
| Finshell                            | `com.finshell.fin`                        | `adb shell pm uninstall -k --user 0 com.finshell.fin`                 |
| Realme Video                        | `com.coloros.video`                       | `adb shell pm uninstall -k --user 0 com.coloros.video`                |
| ORoaming                            | `com.redteamobile.roaming`                | `adb shell pm uninstall -k --user 0 com.redteamobile.roaming`         |
| Google Keep                         | `com.google.android.keep`                 | `adb shell pm uninstall -k --user 0 com.google.android.keep`          |
| Google Maps                         | `com.google.android.apps.maps`            | `adb shell pm uninstall -k --user 0 com.google.android.apps.maps`     |
| Gmail                               | `com.google.android.gm`                   | `adb shell pm uninstall -k --user 0 com.google.android.gm`            |
| Google Photos                       | `com.google.android.apps.photos`          | `adb shell pm uninstall -k --user 0 com.google.android.apps.photos`   |
| Google Calendar                     | `com.google.android.calendar`             | `adb shell pm uninstall -k --user 0 com.google.android.calendar`      |
| Realme Store                        | `com.realmestore.app`                     | `adb shell pm uninstall -k --user 0 com.realmestore.app`              |
| HeyTap Music                        | `com.heytap.music`                        | `adb shell pm uninstall -k --user 0 com.heytap.music`                 |
| Realme Sound Recorder               | `com.coloros.soundrecorder`               | `adb shell pm uninstall -k --user 0 com.coloros.soundrecorder`        |
| Realme Calculator                   | `com.coloros.calculator`                  | `adb shell pm uninstall -k --user 0 com.coloros.calculator`           |
| Realme Weather                      | `com.coloros.weather2`                    | `adb shell pm uninstall -k --user 0 com.coloros.weather2`             |
| Realme Community                    | `com.realmecomm.app`                      | `adb shell pm uninstall -k --user 0 com.realmecomm.app`               |
| Realme Alarm Clock                  | `com.coloros.alarmclock`                  | `adb shell pm uninstall -k --user 0 com.coloros.alarmclock`           |
| Realme Compass                      | `com.coloros.compass2`                    | `adb shell pm uninstall -k --user 0 com.coloros.compass2`             |
| Realme File Manager                 | `com.coloros.filemanager`                 | `adb shell pm uninstall -k --user 0 com.coloros.filemanager`          |
| Google Pay                          | `com.google.android.apps.nbu.paisa.user`  | `adb shell pm uninstall -k --user 0 com.google.android.apps.nbu.paisa.user` |
| YouTube                             | `com.google.android.youtube`              | `adb shell pm uninstall -k --user 0 com.google.android.youtube`       |
| Glance                              | `com.glance.internet`                     | `adb shell pm uninstall -k --user 0 com.glance.internet`              |
| Android Auto                        | `com.google.android.projection.gearhead`  | `adb shell pm uninstall -k --user 0 com.google.android.projection.gearhead` |
| Digital Wellbeing                   | `com.google.android.apps.wellbeing`       | `adb shell pm uninstall -k --user 0 com.google.android.apps.wellbeing` |
| Realme Game Space                   | `com.coloros.gamespaceui`                 | `adb shell pm uninstall -k --user 0 com.coloros.gamespaceui`          |

---
> **Important Warning:** Do not remove **'com.heytap.themestore'** and **'com.coloros.weather.service'** as this may cause the System UI to enter an infinite loop. The only solution to this issue is to perform a factory reset via recovery mode..
---
## ⚙️ Additional Commands

- **Check if a package is installed:**

  ```bash
  adb shell pm path <package_name>
  ```

- **Reboot your device after uninstalling multiple apps (optional):**

  ```bash
  adb reboot
  ```

---

## 📢 Important Notes

- Some apps may have dependencies on other system functions. Double-check before uninstalling critical system apps.
- If you encounter issues, you can always **reinstall the app** using the reinstall command provided.

---

Happy decluttering!
