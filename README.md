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
Download **`DrBuckWho-SMP-2.7.2.mrpack`** from the **[latest release](https://github.com/DrBuckWho/DrBuckWho-SMP/releases/latest)** (or from the [`pack`](https://github.com/DrBuckWho/DrBuckWho-SMP/tree/main/pack) folder in this repo). Do **not** unzip it.

### 4. Import it into Prism
1. In Prism click **Add Instance**, choose **Import**, click **Browse** and pick the `.mrpack` file, then **OK**.
   (Or just drag the file onto the Prism window.)
2. Wait while Prism downloads Minecraft, NeoForge, the mods and the shader pack. This takes a few minutes the first time.
3. A new instance called **DrBuckWho-SMP-2.7.2** appears in your list.

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
2. Enter the server address `drbuckwho.com` and click **Done**, then join.

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
| `/market` | The market. Anyone can switch it (button at the top) between the **Live market** and the **DrBuckWho SMP market**, a player-run order market: place a buy order (item, amount, price per item), sell into other players' orders, and collect what you bought from a chest window with **Collect purchases** |
| `/ah` | Auction house. In the DrBuckWho SMP market it holds players' own listings (one slot of items at a price you choose; sell the item in your hand with `/ah sell <price>`) |
| `/market` | The market. Anyone can switch it (button at the top) between the **Live market** (3% fee on buys and sells, paid by the server bank) and the **DrBuckWho SMP market**, a player-run order market: place a buy order (item, amount, price per item), sell into other players' orders (3% fee from the seller), and collect what you bought from a chest window with **Collect purchases** |
| `/ah` | Auction house (5% fee from the seller). In the DrBuckWho SMP market it holds players' own listings (one slot of items at a price you choose; sell the item in your hand with `/ah sell <price>`) |
| `/stock` | **Player stocks.** Every player is a stock of 1,000 shares of themselves. List part of yourself (up to 49%), trade shares on an order book, and earn dividends from other players' market income and casino profit. The **Server Index (SIDX)** pays holders a share of every fee the server collects, instantly |
| `/gamble` | Casino: coin flip and blackjack, backed by the server bank |
| `/sell`, `/buy`, `/balance` | Quick selling, buying and your balance. Your inventory panel, the sell window and each Auto-Sell Chest can sell to the **best price** (default: players' buy orders that pay more than the live market first, then the live market), only the **live market**, or only **players' buy orders**. Click the small button to change it |
| `/bank` | The server bank's balance. Everything in the economy is closed: the bank only gains money from fees and losses and only loses it by paying live-market sales, new-player money and casino wins |
| `/bankadmin` | Server owner only: the bank dashboard (money flow, runway, mint and burn) |
| `/home` | Save up to 20 homes and teleport to any of them. The last home you go to is your **active home**: it is where you respawn if you die. The world spawn and beds are never used. With no home you respawn at the spot of your last `/rtp` |
| `/rtp` | Teleport to a truly random spot anywhere in the world. Spots are prepared in the background ahead of time, so it is instant |
| `/pay <player> <amount>` | Send money to a player who is online (`1500`, `2.5k` and `3m` all work). You pay a 1% fee on top; the receiver gets the full amount |
| `/tpa <player>`, `/tpahere <player>` | Ask to teleport to a player, or ask them to come to you. They answer with `/tpaccept` or `/tpdeny` (or the chat buttons); `/tpcancel` cancels yours |
| `/help` | Lists these commands and the custom items |
| **H** | Town portal: go to your active home and leave a portal behind. Step through the portal at home to return to where you pressed H; both portals then disappear. Change the key under **Controls → DrBuckWho SMP** |

Crafted items:
- **Auto-Condenser Chest**: chest + crafting table. Turns what is inside into enchanted items.
- **Auto-Sell Chest**: emerald + chest. Sells what is inside; open it and press **Claim** to collect the money.
- **Autocrafter V2**: crafter + diamond block. Set a recipe once, fill it with hoppers, craft with a redstone pulse. If the same item is in several cells it is shared evenly between them.
- **Order Chest**: book + emerald block + chest. Pick an item and a price and fund it with money from your balance; it keeps a buy order open for as much as fits inside, and buys from the live market instead when that is cheaper. It only spends the funds you put in.
- **Magnetic Conveyor**: leather + iron ingots + redstone (3 leather on top; iron, redstone, iron below; makes 6). A rail-like belt for dropped items: it pulls items from a block around onto its middle, carries them, ramps up or down one block, turns, and drops them off the end (or into a chest in front).
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
| Pack | 2.7.2 |
| Minecraft | 1.21.1 |
| NeoForge | 21.1.252 (the server runs a newer 21.1 build and works with it) |

This is a private server project and is not affiliated with Mojang or Microsoft. Minecraft is a trademark of Mojang AB.

## Distant terrain

The pack includes **Distant Horizons** (far terrain out to 256 chunks, set to its highest quality) plus ModernFix, FerriteCore, Lithium, ImmediatelyFast and Entity Culling for speed. Normal chunk range is 16. It also works in single player: the pack includes the chunk-generation mods (C2ME, Chunky) so a local world generates just as fast, and the JJThunder terrain datapack can be added to a new world's `datapacks` folder. Give the game plenty of memory: in Prism open the instance, Settings, Java, and set the maximum memory to 10-12 GB if your PC has the RAM.
