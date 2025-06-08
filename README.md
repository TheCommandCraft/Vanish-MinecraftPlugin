# Vanish++
<div align="center">

**The ultimate vanish solution for modern Minecraft servers.**

![License](https://img.shields.io/badge/license-Custom-blue?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/TheCommandCraft/Vanish-MinecraftPlugin?style=for-the-badge)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/TheCommandCraft/Vanish-MinecraftPlugin?style=for-the-badge)

</div>

Vanish++ provides a clean, robust, and feature-rich way to manage vanished players on your server. Designed with performance and stability in mind, it's the perfect tool for staff who need to observe without being seen. From faking join/leave messages to silent container opening, Vanish++ handles all the small details to create a seamless and immersive stealth experience.

With instant, asynchronous saving, your vanished players' states are always safe, even through server crashes, all without causing any server lag.

---

## ✨ Features

<details>
<summary><b>🛡️ Core Vanish Functionality</b></summary>

- **Toggle Vanish:** Players with permission can become completely invisible to normal players using `/vanish`.
- **Vanish Other Players:** Staff can vanish other players using `/vanish <player>`.
- **Persistent Vanish:** A player's vanished state is saved instantly and persists through server restarts, crashes, and logouts.
- **On-Join Re-Vanish:** Players who log off while vanished will automatically be put back into vanish when they rejoin.
</details>

<details>
<summary><b>🎭 Visibility & Immersion</b></summary>

- **Complete Invisibility:** Vanished players are hidden from the tab list, the server list player count (on ping), and are physically invisible.
- **See Permission:** Players with the `vanishpp.see` permission can see vanished players, their tab list prefix, and receive special notifications.
- **Vanish Prefix:** Vanished players have a configurable `[VANISHED]` prefix in the tab list, visible only to staff.
- **Action Bar Indicator:** Vanished players see a persistent, configurable message on their action bar to remind them they are hidden.
- **Fake Join/Leave Messages:** When a player vanishes, a "Player left the game" message is shown to normal players. When they unvanish, a "Player joined the game" message is shown. This uses the server's own translatable messages for maximum immersion across all languages.
- **Silent Join/Quit:** Staff with `vanishpp.see` receive discreet "silent join/quit" messages when a vanished player connects or disconnects.
- **Staff Notifications:** Staff are notified when another staff member uses the `/vanish` command on someone.
</details>

<details>
<summary><b>👻 Gameplay Integration & Stealth</b></summary>

- **Block Trigger Prevention:** Vanished players will not trigger pressure plates, tripwires, or sculk sensors.
- **Silent Chests:** Opening chests and other containers does not play the opening/closing animation for other players.
- **Mob Spawning:** Vanished players do not affect mob spawning or mob caps around them.
- **Silent Advancements:** Advancement announcement messages are hidden from normal players when earned by a vanished player.
- **Silent Death Messages:** Death messages from vanished players are hidden from normal players.
- **Hidden Chat:** Chat messages sent by a vanished player are only visible to other players with the `vanishpp.see` permission and are formatted with the vanish prefix.
</details>

<details>
<summary><b>🚀 Technical & Performance Features</b></summary>

- **Asynchronous Saving:** Configuration and vanish data are saved to disk on a separate thread the moment a player's state changes, ensuring no data loss from crashes and no lag on the main server thread.
- **Robust State Management:** The plugin correctly handles edge cases like server restarts or crashes while a player is vanished, preventing glitched states (e.g., a visible player with a vanish prefix).
- **Dynamic Permission Updates:** When a player is opped or de-opped, their ability to see vanished players is updated instantly without requiring a rejoin.
- **High Performance:** Designed to be lightweight and have a minimal impact on server performance.
</details>

<details>
<summary><b>🔧 Configuration</b></summary>

- **Fully Configurable:** Nearly every feature, from messages and prefixes to gameplay effects, can be enabled, disabled, or customized in the `config.yml` file.
- **Clear Data Separation:** The `config.yml` has a clear, decorative header separating user-configurable settings from the plugin's internal data storage to prevent accidental edits.
</details>

---

## 📋 Commands

| Command | Description | Permission |
| :--- | :--- | :--- |
| `/vanish` or `/v` | Toggles your own vanish state. | `vanishpp.vanish` |
| `/vanish <player>` | Toggles another player's vanish state. | `vanishpp.vanish.others` |

---

## 🔒 Permissions

| Permission | Description | Default |
| :--- | :--- | :--- |
| `vanishpp.vanish` | Allows using `/vanish` on oneself. | `op` |
| `vanishpp.vanish.others` | Allows using `/vanish` on other players. | `op` |
| `vanishpp.see` | Allows seeing vanished players, their chat, and special notifications. | `op` |

---

## ⚙️ Setup & Configuration

### Requirements
- **Java 17** or newer
- **Paper** (or a Paper fork like Purpur) for Minecraft 1.20.x or newer.
  - *This plugin is **not** compatible with Spigot or Bukkit due to its use of modern Paper APIs.*

### Installation
1.  Download the latest release from the **Releases page**.
2.  Drop the `Vanishpp.jar` file into your server's `plugins` folder.
3.  Start or restart your server.
4.  All configuration options can be found and modified in the generated `plugins/Vanishpp/config.yml` file.

---

## 🐞 Bug Reports & Suggestions

Have a feature request or found a bug? Please **open an issue** on this repository. Your feedback is greatly appreciated!

Please note that as this is a closed-source project, code contributions via Pull Requests cannot be accepted at this time.

## 📄 License

This is a closed-source project. All rights are reserved.

The compiled plugin is provided for use under the terms of the custom license. You may not copy, modify, or redistribute the software unless explicitly allowed. Please see the [**LICENSE**](LICENSE) file for the full terms of use.
