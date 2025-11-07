# 🎮 rbylua - Pokémon RBY Shiny Hunting Scripts

## ⚠️ Project Status

**This is an actively maintained project.** Although there have been years between development cycles, I continue to work on and improve these scripts. 

**Important Note:** These scripts are not guaranteed to work reliably due to their dependency on emulator behavior. Script functionality can vary based on:
- Emulator version and configuration
- VBA-M version (currently developed for VBA-M rr 23.6)
- Game version and ROM characteristics
- Timing and frame-perfect execution

If you encounter issues, please report them or try adjusting script parameters.

## 📝 Overview

A collection of Lua scripts designed for automated shiny hunting in Pokémon Red, Blue, and Yellow games using VBA-M emulator. These scripts automate the process of finding shiny Pokémon by monitoring game memory and automating repetitive hunting actions.

**Compatibility:** Works primarily with VBA-M rr 23.6

## 🚀 Features

### Main Script Categories

#### 🎁 Gift Bot (`giftbot.lua`)
- Automates shiny hunting for gift Pokémon
- DVs (Individual Values) are generated after prompting to nickname your Pokémon
- Position cursor over "no" (nicknames not yet supported) and run the script
- **Valid for:** Starters, fossils, in-game gifts (Eevee, Lapras, etc.) and game corner prizes

#### 🗿 Stationary Bot (`stationarybot.lua`)
- Automates shiny hunting for stationary Pokémon encounters
- DVs are generated when the battle begins
- Interact with the sprite, stop at the cry text before the battle and run the script
- **Valid for:** Snorlax, Zapdos, Articuno, Moltres, Mewtwo, Electrode/Voltorb in Power Plant

#### 🎣 Fishing Bots (`fishingbots/` directory)

**autospecie_fishingbot.lua** - Automatic Species Detection
- New shiny finder method
- Select your rod, position cursor over "use" and run the script
- Script automatically selects the first Pokémon found
- Optimized for discovering any shiny species

**fishbot.lua** - Manual Species Configuration
- Species is generated first, then the IVs
- Edit the script for desired species by changing the index number
- Index numbers: [Bulbapedia - Pokémon Index (Generation I)](http://bulbapedia.bulbagarden.net/wiki/List_of_Pok%C3%A9mon_by_index_number_(Generation_I))
- Edit script to view non-shiny Pokémon IVs (Edit "local op")
- Select your rod, position cursor over "use" and run the script

#### 🔍 Nature Check (`party_checker.lua`)
- Non-automated script to display Pokémon nature and shinyness
- Shows what nature the Pokémon will have when transferred through Pokébank
- **Note:** Nature is based on experience points - gaining experience changes nature
- Rewritten version of Collector Togami's script with game version autocheck and more compact code

#### 📊 In-Game Trade Scripts (`InGameTrades/` directory)
- Automates shiny hunting for in-game trades
- Run the script before the last input before animation (typically at "connect your link cable" text)
- **Recommended:** Use InGameTrade.lua instead of giftbot for better IV handling
- DVs are fixed for received Pokémon through in-game trades

#### 🆔 TID Script (`beta/` - Experimental)
- Edit script for desired TID in decimal format
- Run with cursor over "New Game" in main screen

#### 🌲 Wild Pokémon Script (`beta/wild.lua` - Requires IPS Patch)
- For use with [IPS patches](https://www.reddit.com/r/pokemonrng/comments/6e8kvm/ips_patches_pokemon_red_blue_with_fixed_rng_and/)
- Credits to Aligateur for patch development

## 📦 Repository Structure

```
rbylua/
├── README.md                    # This file
├── giftbot.lua                 # Gift Pokémon hunting script
├── party_checker.lua           # Nature and shinyness checker
├── stationarybot.lua           # Stationary encounter script
├── tidbot.lua                  # TID setting script
├── InGameTrades/               # In-game trade scripts
│   ├── InGameTrade.lua         # Main trade hunting script
│   ├── LegesFigure11_igtbot.lua # Specific trade variant
│   ├── Readme.md               # Trade script documentation
│   └── Zep715_igtbot.lua       # Alternate trade script
├── fishingbots/                # Fishing automation scripts
│   ├── autospecie_fishingbot.lua # Auto species detection
│   ├── fishbot.lua             # Manual species configuration
│   └── README.md               # Fishing script documentation
└── beta/                       # Experimental scripts
    └── wild.lua                # Wild Pokémon hunting (IPS patch)
```

## 🛠️ Installation & Usage

### Prerequisites
1. VBA-M emulator (rr 23.6 recommended)
2. Pokémon Red, Blue, or Yellow ROM
3. Lua scripting support in VBA-M

### Setup
1. Download the desired `.lua` script file
2. Open VBA-M emulator
3. Load your Pokémon ROM
4. In VBA-M: Tools → Lua Script → Open Script
5. Select the desired `.lua` file
6. Position your in-game cursor as specified by the script
7. Run the script

### Script Execution
- Most scripts require specific cursor positioning before execution
- Follow the individual script documentation for precise positioning
- Monitor the emulator console for script feedback

## ⚙️ Configuration

### Editing Scripts
- Most scripts include editable parameters at the top
- Species hunting: Edit index numbers in fishing bot scripts
- TID hunting: Edit desired TID value in tidbot.lua
- Comment out lines to disable specific checks or behaviors

### VBA-M Configuration
- Ensure Lua support is enabled
- Configure emulator speed settings for optimal performance
- Test scripts with frame limiter ON for consistent behavior

## 📌 Known Issues & Limitations

### Emulator Dependency
- Scripts rely on emulator accuracy and frame timing
- Different VBA-M versions may behave differently
- Custom ROM patches may cause compatibility issues

### Script Reliability
- Scripts may occasionally fail to detect shinies or game events
- Timing issues can occur with slower computers
- Some edge cases in game logic may not be handled

### Workarounds
- Restart the script if detection fails
- Ensure optimal emulator performance settings
- Try alternative script versions (different methods) if one fails

## 🔗 Credits & Attribution

- **zaksabeast** - For updating the scripts for Pokébank 1.3 transporter compatibility
- **Collector Togami** - For original nature check script and shiny discovery methods
- **Aligateur** - For IPS patch development for wild Pokémon RNG
- **zep715** - Original fork maintainer

## 🤝 Contributing

If you discover:
- Scripts that don't work with specific game versions
- Improvements to shiny detection methods
- New hunting opportunities in the games
- Better ways to handle emulator timing

Please open an issue or submit a PR!

## 📄 License

This project is provided as-is for educational and research purposes.

---

**Last Updated:** Actively maintained | See git history for change log

**Support:** If you encounter issues, ensure you're using VBA-M rr 23.6 and try alternative script versions before reporting bugs.
