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

# Furnace Upgrades

### Features

* Upgrade each attribute of your furnace;
* Supports different oven types;
* It is possible to define default attributes for all ovens on the server;
* You can set a default value for all base ovens (replacing quicksmelt);
* You can enable/disable any features you want;
* Option to keep attributes when removing the furnace;
* Option to auto split ores;
* Automatic fuel calc based on the upraded oven attributes;
* Now **BBQ** and **Campfire** can also be improved;
* Option so that only the furnace owner can upgrade it;
* Option so that only owner's teammates can upgrade it;
* A new completely redesigned UI;

### Demonstration

{% embed url="https://www.youtube.com/watch?v=AK0ZHEaHd5g" %}

### Permissions

`furnaceupgrades.use` - This is the **unique permission**. required for all players to upgrade furnaces

### Configuration

```json
{
  "General Settings": {
    "Only the owner can upgrade the furnace": true,
    "Only teammates can upgrade the furnace": false,
    "Keep attributes when removing": true,
    "Maintain the same speed for split items.": false
  },
  "Currency Settings": {
    "Currency type (0 - Scrap | 1 - Economics | 2 - Server Rewards)": 0,
    "Currency item (if the currency type is '0')": {
      "Short name": "scrap",
      "Skin ID": 0
    }
  },
  "Visual Settings": {
    "Use chat messages": true,
    "Notification plugin (0 - None | 1 - Toastify | 2 - Notify)": 1,
    "Toastify notification ID": "success",
    "Notify notification type": 0,
    "Upgrade effect (empty = disabled)": "assets/bundled/prefabs/fx/build/promote_stone.prefab"
  },
  "UI Settings": {
    "Disable status panel": false,
    "Upgrade button": {
      "Anchor": "0.5 0 0.5 0",
      "Offset": "400 109.5 480 141.5",
      "Background color": "0.45 0.63 0.19 1",
      "Font size": 13
    },
    "Status panel": {
      "Anchor": "0.5 0 0.5 0",
      "Offset": "193 17 420 103",
      "Background color": "0 0 0 0.25",
      "Font size": 12
    }
  },
  "Features Settings": {
    "Smelting speed multiplier": true,
    "Fuel speed": true,
    "Resource output multiplier": true,
    "Charcoal multiplier": true,
    "Auto split cookables": true,
    "Auto add fuel": true
  },
  "Default Settings": {
    "Smelting speed": 1.0,
    "Fuel speed": 1.0,
    "Resource output multiplier": 1.0,
    "Charcoal multiplier": 1.0
  },
  "Upgrades Settings": {
    "furnace": {
      "Smelting speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        },
        {
          "Cost": 200,
          "Multiplier": 3.0
        }
      ],
      "Fuel speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Resource output multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Charcoal multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ]
    },
    "furnace.large": {
      "Smelting speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        },
        {
          "Cost": 200,
          "Multiplier": 3.0
        }
      ],
      "Fuel speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Resource output multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Charcoal multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ]
    },
    "electric.furnace": {
      "Smelting speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        },
        {
          "Cost": 200,
          "Multiplier": 3.0
        }
      ],
      "Fuel speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Resource output multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Charcoal multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ]
    },
    "legacyfurnace": {
      "Smelting speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        },
        {
          "Cost": 200,
          "Multiplier": 3.0
        }
      ],
      "Fuel speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Resource output multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Charcoal multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ]
    },
    "campfire": {
      "Smelting speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        },
        {
          "Cost": 200,
          "Multiplier": 3.0
        }
      ],
      "Fuel speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Resource output multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Charcoal multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ]
    },
    "bbq": {
      "Smelting speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        },
        {
          "Cost": 200,
          "Multiplier": 3.0
        }
      ],
      "Fuel speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Resource output multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Charcoal multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ]
    },
    "small.oil.refinery": {
      "Smelting speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        },
        {
          "Cost": 200,
          "Multiplier": 3.0
        }
      ],
      "Fuel speed": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Resource output multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ],
      "Charcoal multiplier": [
        {
          "Cost": 100,
          "Multiplier": 2.0
        }
      ]
    }
  },
  "Version": {
    "Major": 2,
    "Minor": 0,
    "Patch": 3
  }
}
```
