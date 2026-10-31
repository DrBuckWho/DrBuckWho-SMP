# DrBuckWho SMP: player setup

Everything you need to play on the DrBuckWho SMP server: a ready-made modpack for **Minecraft Java Edition 1.21.1 (NeoForge)** with shaders, a performance mod and the server's own economy mod. Setup takes about 10 minutes.

> You need a Minecraft **Java Edition** account (a Microsoft account that owns the game). Prism Launcher is free.

## Step by step

### 1. Install Prism Launcher
1. Go to **<https://prismlauncher.org/download/>** and download the installer for your system (on Windows pick the **Setup / installer** version).
2. Run it and open Prism Launcher. A first-run wizard appears; keep the defaults. Prism downloads the right Java (Java 21) by itself, so you do **not** need to install Java.

### 2. Sign in with your Microsoft account
1. Click the **profile icon** in the top right, then **Manage Accounts**, then **Add Microsoft**.
2. Follow the sign-in steps (a code and a Microsoft page). Close the window when it shows your account name.

### 3. Download the pack
Download **`DrBuckWho-SMP-1.13.0.mrpack`** from the **[latest release](https://github.com/DrBuckWho/DrBuckWho-SMP/releases/latest)** (or from the [`pack`](https://github.com/DrBuckWho/DrBuckWho-SMP/tree/main/pack) folder in this repo). Do **not** unzip it.

### 4. Import it into Prism
1. In Prism click **Add Instance**, choose **Import**, click **Browse** and pick the `.mrpack` file, then **OK**.
   (Or just drag the file onto the Prism window.)
2. Wait while Prism downloads Minecraft, NeoForge, the mods and the shader pack. This takes a few minutes the first time.
3. A new instance called **DrBuckWho-SMP-1.13.0** appears in your list.

### 5. Give it enough memory
1. Right-click the instance, choose **Edit**, then **Settings**, then **Java**.
2. Tick **Memory** and set **Maximum memory** to **4096 MB**. If your computer has 16 GB of RAM or more, **6144 MB** is better.

### 6. Launch
Double-click the instance. The first start takes a couple of minutes while the game loads the mods and compiles the shaders. Later starts are faster.

### 7. Shaders
The pack comes with **Complementary Reimagined** shaders already switched on, using Iris and Sodium.
- To turn shaders off or change them: **Options → Video Settings → Shader Packs**.
- If the game is slow, choose **(off)** there, or open **Shader Pack Settings** and pick a lower **Profile**. Lowering the render distance helps too.
- On a laptop or an old graphics card, start with shaders off.

### 8. Join the server
1. In Minecraft click **Multiplayer**, then **Add Server**.
2. Enter the server address that DrBuckWho gave you and click **Done**, then join.

## What is in the pack

| Mod | What it does |
| --- | --- |
| **DrBuckWho SMP** (our mod) | The server economy, homes, random teleport, auto chests and more (see below) |
| [Sodium](https://modrinth.com/mod/sodium) | Much better performance |
| [Iris Shaders](https://modrinth.com/mod/iris) | Loads shader packs |
| [Complementary Reimagined](https://modrinth.com/shader/complementary-reimagined) (shader pack) | Better lighting and graphics |
| [JEI](https://modrinth.com/mod/jei) | Shows every recipe and item (press **R** or **U** on an item) |
| [KubeJS](https://modrinth.com/mod/kubejs) and [Rhino](https://modrinth.com/mod/rhino) | The enchanted-resource recipes |

Sodium, Iris, JEI, KubeJS, Rhino and the shaders are **downloaded from Modrinth by Prism** when you import the pack. They are not stored in this repository. The pack has **no minimap** on purpose.

## What you can do on the server

| Command or key | What it does |
| --- | --- |
| `/market` | Buy and sell items at the market |
| `/ah` | Player auction house (sell the item in your hand with `/ah sell <price>`) |
| `/stock` | Stock market simulator |
| `/gamble` | Casino: coin flip and blackjack |
| `/sell`, `/buy`, `/balance` | Quick selling, buying and your balance |
| `/home` | Save up to 20 homes and teleport to any of them. The last home you go to is your respawn point |
| `/rtp` | Teleport to a random spot in the world |
| **H** | Town portal: go to your bed (or spawn) and leave a portal to come back through. Change the key under **Controls → DrBuckWho SMP** |

Crafted items:
- **Auto-Condenser Chest**: chest + crafting table. Turns what is inside into enchanted items.
- **Auto-Sell Chest**: emerald + chest. Sells what is inside; open it and press **Claim** to collect the money.
- **Autocrafter V2**: crafter + diamond block. Set a recipe once, fill it with hoppers, craft with a redstone pulse.
- **Portable Beacon**: netherite block + lead. Its powers work from your inventory.
- **Replant** enchantment: a rare drop from farmer villagers. Hoes with it replant crops.

## Updating the pack

When a new version is released:
1. Download the new `.mrpack` from the [latest release](https://github.com/DrBuckWho/DrBuckWho-SMP/releases/latest) and import it again (step 4). It becomes a new instance.
2. Launch the new one. Once it works, right-click the old instance and **Delete** it.

Your worlds and items live on the server, so there is nothing to copy. Your video settings and key bindings do not move across by themselves; to keep them, copy `options.txt` from the old instance's `minecraft` folder into the new one's (right-click the instance, choose **Folder**, then open the `minecraft` folder).

## Troubleshooting

- **"Java 21 is required" or Java errors**: open Prism **Settings → Java** and turn on automatic Java download, or pick a Java 21 entry from the list. Then launch again.
- **You get kicked on joining ("mod mismatch" or similar)**: your pack is out of date. Download the newest `.mrpack` and import it (see *Updating*).
- **The game crashes at start-up**: update your graphics drivers. If it still crashes, open the instance folder (right-click the instance, choose **Folder**, then open the `minecraft` folder), open `config/iris.properties` in Notepad, change `enableShaders=true` to `enableShaders=false`, save and launch again.
- **The import stalls or fails**: close the window and import again. Prism keeps the files it already downloaded.
- **Low FPS**: see step 7, and lower the render distance in **Options → Video Settings**.

## Versions

| | |
| --- | --- |
| Pack | 1.13.0 |
| Minecraft | 1.21.1 |
| NeoForge | 21.1.252 (the server runs a newer 21.1 build and works with it) |

This is a private server project and is not affiliated with Mojang or Microsoft. Minecraft is a trademark of Mojang AB.
