---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# TC Levels

### Features

* Reduce the decay damage by tick;
* Upgrade the authorizations limit;
* Upgrade the building grade limit;
* Upgrade the storage capacity of the cupboard;
* Unlock some deployable items;
* Upgrade the stack size limit of the cupboard;
* Set a default building grade for the server;
* Modify the default decay;
* Keep the cupboard attributes when remove;

Make your server fun ^u^

### Permissions

The plugin has a unique permission, which allows the player to use the cupboard upgrade: _`tclevels.use`_

### F.A.Q

1. **How many items can be blocked? and which?**\
   You can block unlimited items and all items must be deployable or they will not be blocked.
2. **Which area will be checked when i place my cupboard**\
   The entire privilege area will be checked. But you can also disable checks in the configuration file.
3. **Could it cause conflict with any plugin?**\
   Yes, but i am providing an API for the plugin so that other developers can integrate with it, so if there is a conflict, just go to the developer's plugin support and ask them to integrate it. Also if it is possible for me to integrate it from my plugin, i will do so without any problem.

### Demonstration

{% embed url="https://www.youtube.com/watch?v=MXIjWa_Js1k" %}

### API

```cs
// Gets the current cupboard allowed building grade limit
// If the cupboard isn't provided, it will return the default building grade limit of the config;
private BuildingGrade.Enum GetBuildingGradeLimit(BuildingPrivlidge? cupboard);

// Gets the current cupboard decay multiplier
// If the cupboard isn't provided, it will return the default decay multiplier of the config;
private float GetDecayMultiplier(BuildingPrivlidge? cupboard);

// Gets the current cupboard authorization limit
// If the cupboard isn't provided, it will return the default auth limit of the config;
private int GetAuthLimit(BuildingPrivlidge? cupboard);

// Gets the current cupboard storage capacity
// If the cupboard isn't provided it will throw an exception;
private int GetCapacity(BuildingPrivlidge cupboard);

// Gets a list of the cupboard blocked items
// If the cupboard isn't provided it will return all locked items listed in the config;
private List<string> GetLockedItems(BuildingPrivlidge? cupboard);
```

### Configuration

```json
{
  "General Options": {
    "Can only the owner update the cupboard?": false,
    "Keep the cupboard attributes into the item when removing it with a removal tool?": true,
    "Allow placement with locked items placed before": false,
    "Allow placement with the base already with a building grade?": false,
    "Block the building grade bigger than the default without a cupboard?": true,
    "Block placement of locked items without a cupboard?": false,
    "Disable chat messages?": false,
    "Notifications plugin (0 = disabled | 1 = Toastify | 2 = Notify)": 1,
    "Sync your notifications ID with below keywords": {
      "Error": "error",
      "Success": "success",
      "Info": "success"
    },
    "Effect when upgrade": "assets/bundled/prefabs/fx/build/promote_stone.prefab",
    "Effect when unlock a item": "assets/bundled/prefabs/fx/item_unlock.prefab",
    "Error effect": "assets/prefabs/weapons/toolgun/effects/repairerror.prefab"
  },
  "Features Options": {
    "Enable decay reducer": true,
    "Enable authorizations limit": true,
    "Enable cupboard capacity": true,
    "Enable building grade limit": true,
    "Enable cupboard stack size multiplier": true
  },
  "Currency Options": {
    "Currency type (0 = Economics | 1 = Server Rewards | 2 = Item)": 2,
    "Currency item (change only if currency type is set to item)": {
      "Short name": "scrap",
      "Skin ID": 0
    }
  },
  "Cupboard Defaults": {
    "Default cupboard authorizations limit": 1,
    "Default cupboard capacity": 6,
    "Default building grade limit (0 = twigs | 1 = wood | 2 = stone | 3 = metal | 4 = top tier)": 1,
    "Default decay multiplier (less than 1.0 = Decay slower | bigger than 1.0 = Decay faster)": 1.0,
    "Default cupboard stack size multiplier": 1.0
  },
  "UI Options": {
    "Button anchor": ".5 0 .5 0",
    "Button offset": "400 596 572 616",
    "Modal background color": "0.96 0.92 0.88 .08"
  },
  "Upgrade Options": {
    "Cupboard capacity": [
      {
        "Cost": 500,
        "Capacity": 16
      },
      {
        "Cost": 800,
        "Capacity": 24
      },
      {
        "Cost": 500,
        "Capacity": 29
      }
    ],
    "Building grade (0 = Twigs | 1 = Wood | 2 = Stone | 3 = Metal | 4 = Top Tier)": [
      {
        "Cost": 200,
        "Grade level": 2
      },
      {
        "Cost": 400,
        "Grade level": 3
      },
      {
        "Cost": 800,
        "Grade level": 4
      }
    ],
    "Authorization limit": [
      {
        "Cost": 100,
        "Max authorizations": 2
      },
      {
        "Cost": 200,
        "Max authorizations": 4
      }
    ],
    "Reduce decay (0 to 100%)": [
      {
        "Cost": 100,
        "Reduce amount": 10.0
      },
      {
        "Cost": 300,
        "Reduce amount": 30.0
      },
      {
        "Cost": 500,
        "Reduce amount": 50.0
      },
      {
        "Cost": 800,
        "Reduce amount": 80.0
      },
      {
        "Cost": 2000,
        "Reduce amount": 100.0
      }
    ],
    "Stack size multiplier": [
      {
        "Cost": 400,
        "Multiplier (2 = 2x the vanilla stack)": 1.25
      },
      {
        "Cost": 1000,
        "Multiplier (2 = 2x the vanilla stack)": 2.0
      },
      {
        "Cost": 2000,
        "Multiplier (2 = 2x the vanilla stack)": 3.0
      }
    ],
    "Items that need to be unlocked (shortname: price)": {
      "furnace": 50,
      "electric.furnace": 200,
      "box.wooden.large": 100,
      "door.hinged.toptier": 300,
      "electric.solarpanel.large": 50,
      "door.double.hinged.toptier": 300,
      "wall.external.high.stone": 200,
      "gates.external.high.stone": 200,
      "wall.frame.garagedoor": 300,
      "wall.window.bars.toptier": 150,
      "bed": 100,
      "workbench3": 500
    }
  },
  "Version": {
    "Major": 1,
    "Minor": 2,
    "Patch": 0
  }
}
```
