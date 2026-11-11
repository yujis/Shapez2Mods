# ⏩ Fast Forwarder for Shapez 2

Time is efficiency. **Fast Forwarder** is a quality-of-life mod for Shapez 2 that puts time control directly at your fingertips. 

Whether you need to pause and plan your next massive blueprint, or accelerate time to wait for shapes to reach the Vortex, this mod provides a clean, native-looking toolbar to manage the game's simulation speed on the fly.

Requires **Shapez 2 1.2+**. The mod uses the game's native mod loader — **BepInEx and Harmony are not required**.

## ✨ Key Features

* **Click-and-Go Interface:** No console commands, no hidden hotkeys. A dedicated toolbar sits neatly in the top right of your screen.
* **Five Speed Tiers:**
    * `II` **Pause (0x):** Completely freeze the simulation to think, build, or troubleshoot without pressure.
    * `>` **Normal (1x):** Standard vanilla gameplay speed.
    * `>>` **Fast (5x):** Speed things up a bit.
    * `>>>` **Very Fast (10x):** Great for testing new production lines.
    * `>|` **Ultra (25x):** Skip the waiting game and fill your milestones instantly.
* **Immersive Design:** The UI is crafted to blend smoothly with the Shapez 2 aesthetic, featuring the game's signature orange highlight to clearly indicate your active speed setting.
* **Pause Sync:** The highlighted speed follows the game's own pause toggle.

## 🛠️ Installation

### Recommended Method (Mod Manager)
The easiest way to install and keep the mod updated is by using **r2modman** or the **Thunderstore Mod Manager**. Simply search for "FastForwarder" and click Install.

### Manual Method
1. Download the latest release of `FastForwarder.zip`.
2. Extract the `FastForwarder` folder into the game's mods directory:
    * **Windows:** `%USERPROFILE%\AppData\LocalLow\tobspr Games\shapez 2\mods\`
    * **macOS:** `~/Library/Application Support/com.tobspr.shapez-2/mods/`
3. Launch the game. The UI will appear automatically once you load into a save.

The resulting layout looks like this:

```
mods/
└── FastForwarder/
    ├── manifest.json
    └── FastForwarder.dll
```

## 🔨 Building

Requires the .NET SDK 8.

```bash
# Windows (default Steam path can be overridden with -p:Shapez2Dir=...)
dotnet build FastForwarder/FastForwarder.csproj -c Release \
  -p:Shapez2Dir="C:\Program Files (x86)\Steam\steamapps\common\shapez 2"

# macOS
dotnet build FastForwarder/FastForwarder.csproj -c Release \
  -p:ManagedDir="/Applications/shapez 2.app/Contents/Resources/Data/Managed"
```

The build output (`FastForwarder.dll` + `manifest.json`) is placed in
`FastForwarder/bin/Release/`.

## ⚠️ Notes
* Running the game at `25x` speed on extremely large and complex factories may cause temporary performance drops or lag spikes depending on your PC's hardware. 
* The mod does not modify save games and does not disable achievements.

## 🤝 Credits
* **Original Creator:** This mod is a heavily modified and fixed fork of the original [TimeController](https://github.com/urakkaamyx/Shapez2Mods-TimeController) mod created by **Urakka**. All core concepts belong to them.
* **Improvements:** Fixed unpausing bugs, prevented UI duplication, and redesigned the interface to match the Shapez 2 native aesthetic.
* **Maintained by:** yujis
