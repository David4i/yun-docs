# Military Airfield

## Description

As soon as the event starts, several troops (NPCs) are spawned to defend an hackable crate that will be delivered by the CH47. This crate may contain a lot of loot, so the troops have the duty to defend it. For this purpose, there is a variety of troops such as snipers, close-range shooters, and long-range shooters.

If a player manages to initiate the hacking of the crate, all the airfield troops will be relocated to a combat position. In other words, all troops that you haven't seen yet or that are hidden will be moved to the center of the airfield to defend the crate. After a few minutes, a plane will be sent with supply drops containing weapons to assist the troops in defense. However, airborne troops will also be dispatched from the plane to parachute down and aid in defending the crate.

If the crate is looted, all troops will be destroyed, leaving only the crates, supply drops, and bodies to be looted by intruders.

## Demonstration

{% embed url="https://youtu.be/I3T8vDe-gTA" %}

## Commands

{% hint style="info" %}
The command can be changed in the config file.
{% endhint %}

`/ma start` to start the event\
`/ma stop` to stop the event\
`/ma position` to get the current position based in the airfield monument (used to config)

> **Console commands:**
>
> `ma start` to start the event\
> `ma stop` to stop the event

## **Permissions**

`militaryairfield.admin` to access all commands

## API

```csharp
// Called when the event starts
private void OnMilitaryAirfieldEventStarted();

// Called when the event ends
private void OnMilitaryAirfieldEventEnded(BasePlayer? lootedBy);
```

## Configuration

{% code lineNumbers="true" %}
```json
{
  "General settings": {
    "Chat command": "ma",
    "Using AlphaLoot or CustomLoot": false,
    "Allow PVP in the event area? (if you are using TruePVE plugin)": false,
    "Use chat messages": true,
    "Use GUI countdown": true
  },
  "Map marker settings": {
    "Use map marker": true,
    "Radius": 2.5,
    "Color": "#000000",
    "Outline color": "#ff0000",
    "Opacity": 0.75,
    "Icon type (0 - Circle | 1 - Triangle)": 1,
    "Icon index": 4,
    "Icon color (0 - Yellow | 1 - Blue | 2 - Green | 3 - Red | 4 - Purple | 5 - Cyan)": 3,
    "Text": "MILITARY AIRFIELD EVENT"
  },
  "Notifications settings": {
    "Notications type (0 - None | 1 - GameTip | 2 - Toastify | 3 - Notify)": 1,
    "GameTip style (0 - Blue normal | 1 - Red normal | 2 - Blue long | 3 - Blue short | 4 - Server event)": 4,
    "Toastify notification ID": "info",
    "Notify notification type": 0
  },
  "Event settings": {
    "Event duration (seconds)": 3600.0,
    "Auto start enabled": true,
    "Auto start cooldown min (seconds)": 7200.0,
    "Auto start cooldown max (seconds)": 3600.0,
    "Start only at the night": true,
    "Interval before troop relocation after crate starts to be hacked (seconds)": 15.0,
    "Interval to call the plane after troop relocation (seconds)": 30.0,
    "Show zone sphere": true,
    "Sphere color (0 - Black | 1 - Blue | 2 - Green | 3 - Purple | 4 - Red)": 4,
    "Patrol NPCs": [
      {
        "Roam position": "(-38.47, 0.30, 56.64)",
        "Roam range": 10.0,
        "Relocation position": "(-23.69, 0.30, -14.40)",
        "Weapon": {
          "Short name": "rifle.lr300",
          "Skin ID": 3074330534
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "rifle.lr300",
            "Skin ID": 3074330534
          },
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(-27.00, 0.30, 25.98)",
        "Roam range": 10.0,
        "Relocation position": "(-8.65, 0.30, -15.07)",
        "Weapon": {
          "Short name": "rifle.lr300",
          "Skin ID": 3074330534
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "rifle.lr300",
            "Skin ID": 3074330534
          },
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(5.41, 0.30, 53.21)",
        "Roam range": 10.0,
        "Relocation position": "(0.96, 0.30, 0.77)",
        "Weapon": {
          "Short name": "rifle.semiauto",
          "Skin ID": 2884741877
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "rifle.semiauto",
            "Skin ID": 2884741877
          },
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(17.01, 0.30, 33.88)",
        "Roam range": 10.0,
        "Relocation position": "(15.37, 0.30, 8.87)",
        "Weapon": {
          "Short name": "rifle.semiauto",
          "Skin ID": 2884741877
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "rifle.semiauto",
            "Skin ID": 2884741877
          },
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(57.82, 0.30, 53.20)",
        "Roam range": 10.0,
        "Relocation position": "(55.93, 0.30, -18.10)",
        "Weapon": {
          "Short name": "rifle.ak",
          "Skin ID": 2833821724
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "rifle.ak",
            "Skin ID": 2833821724
          },
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(57.31, 0.30, 32.35)",
        "Roam range": 10.0,
        "Relocation position": "(30.45, 0.31, -10.98)",
        "Weapon": {
          "Short name": "rifle.ak",
          "Skin ID": 2833821724
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "rifle.ak",
            "Skin ID": 2833821724
          },
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(46.74, 0.29, -84.86)",
        "Roam range": 10.0,
        "Relocation position": "(43.39, 0.30, -46.70)",
        "Weapon": {
          "Short name": "smg.thompson",
          "Skin ID": 796687275
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "smg.thompson",
            "Skin ID": 796687275
          },
          {
            "Amount": {
              "Min": 25,
              "Max": 75
            },
            "Chance": 1.0,
            "Short name": "ammo.pistol",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(6.07, 3.30, -84.80)",
        "Roam range": 10.0,
        "Relocation position": "(-17.05, 0.30, -55.56)",
        "Weapon": {
          "Short name": "smg.thompson",
          "Skin ID": 796687275
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "smg.thompson",
            "Skin ID": 796687275
          },
          {
            "Amount": {
              "Min": 25,
              "Max": 75
            },
            "Chance": 1.0,
            "Short name": "ammo.pistol",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(-38.04, 3.30, -78.29)",
        "Roam range": 10.0,
        "Relocation position": "(-39.46, 0.30, -38.40)",
        "Weapon": {
          "Short name": "smg.mp5",
          "Skin ID": 839819171
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "smg.mp5",
            "Skin ID": 839819171
          },
          {
            "Amount": {
              "Min": 25,
              "Max": 75
            },
            "Chance": 1.0,
            "Short name": "ammo.pistol",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(-76.04, 0.31, 33.72)",
        "Roam range": 10.0,
        "Relocation position": "(-38.29, 0.29, 10.79)",
        "Weapon": {
          "Short name": "smg.mp5",
          "Skin ID": 839819171
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "smg.mp5",
            "Skin ID": 839819171
          },
          {
            "Amount": {
              "Min": 25,
              "Max": 75
            },
            "Chance": 1.0,
            "Short name": "ammo.pistol",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(-74.95, 0.09, -80.66)",
        "Roam range": 10.0,
        "Relocation position": "(-22.57, 0.30, -49.01)",
        "Weapon": {
          "Short name": "shotgun.spas12",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "shotgun.spas12",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 7,
              "Max": 21
            },
            "Chance": 1.0,
            "Short name": "ammo.shotgun",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(-12.76, 3.30, -79.25)",
        "Roam range": 10.0,
        "Relocation position": "(-4.19, 1.80, -69.42)",
        "Weapon": {
          "Short name": "shotgun.spas12",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "shotgun.spas12",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 7,
              "Max": 21
            },
            "Chance": 1.0,
            "Short name": "ammo.shotgun",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(-11.57, 3.29, -91.24)",
        "Roam range": 10.0,
        "Relocation position": "(-0.21, 0.30, -40.07)",
        "Weapon": {
          "Short name": "shotgun.spas12",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "coffeecan.helmet",
            "Skin ID": 2715609678
          },
          {
            "Short name": "roadsign.jacket",
            "Skin ID": 2715608631
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2655671015
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2891379321
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2891377798
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.25,
            "Short name": "shotgun.spas12",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 7,
              "Max": 21
            },
            "Chance": 1.0,
            "Short name": "ammo.shotgun",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(-47.64, 21.40, -88.16)",
        "Roam range": 8.0,
        "Relocation position": "(-37.84, 21.41, -79.27)",
        "Weapon": {
          "Short name": "rifle.l96",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "metal.facemask",
            "Skin ID": 2105454370
          },
          {
            "Short name": "metal.plate.torso",
            "Skin ID": 2105505757
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2090790324
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2080975449
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2080977144
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 2090776132
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.15,
            "Short name": "rifle.l96",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 5,
              "Max": 30
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.5,
            "Short name": "weapon.mod.small.scope",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.15
      },
      {
        "Roam position": "(108.67, 14.90, 26.31)",
        "Roam range": 8.0,
        "Relocation position": "(109.14, 14.89, 17.50)",
        "Weapon": {
          "Short name": "rifle.l96",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "metal.facemask",
            "Skin ID": 2105454370
          },
          {
            "Short name": "metal.plate.torso",
            "Skin ID": 2105505757
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2090790324
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2080975449
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2080977144
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 2090776132
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.15,
            "Short name": "rifle.l96",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 5,
              "Max": 30
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.5,
            "Short name": "weapon.mod.small.scope",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.15
      },
      {
        "Roam position": "(-126.34, 18.04, 40.72)",
        "Roam range": 8.0,
        "Relocation position": "(-114.04, 0.24, 3.85)",
        "Weapon": {
          "Short name": "rifle.l96",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "metal.facemask",
            "Skin ID": 2105454370
          },
          {
            "Short name": "metal.plate.torso",
            "Skin ID": 2105505757
          },
          {
            "Short name": "burlap.gloves",
            "Skin ID": 2090790324
          },
          {
            "Short name": "hoodie",
            "Skin ID": 2080975449
          },
          {
            "Short name": "roadsign.kilt",
            "Skin ID": 2649381460
          },
          {
            "Short name": "pants",
            "Skin ID": 2080977144
          },
          {
            "Short name": "shoes.boots",
            "Skin ID": 2090776132
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.15,
            "Short name": "rifle.l96",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 5,
              "Max": 30
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.5,
            "Short name": "weapon.mod.small.scope",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.15
      }
    ]
  },
  "CH47 settings": {
    "Landing position": "(6.22, 0.30, -37.33)",
    "NPCs (Max 12)": [
      {
        "Roam position": "(16.39, 0.30, -16.70)",
        "Roam range": 10.0,
        "Relocation position": "(-45.65, 0.30, -14.88)",
        "Weapon": {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "lmg.m249",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "hazmatsuit.arcticsuit",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.35,
            "Short name": "hazmatsuit.arcticsuit",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(-18.08, 0.28, -34.13)",
        "Roam range": 10.0,
        "Relocation position": "(-6.87, 0.31, -45.43)",
        "Weapon": {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "lmg.m249",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "hazmatsuit.arcticsuit",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.35,
            "Short name": "hazmatsuit.arcticsuit",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(5.64, 0.31, -52.90)",
        "Roam range": 10.0,
        "Relocation position": "(12.16, 0.31, -51.93)",
        "Weapon": {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "lmg.m249",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "hazmatsuit.arcticsuit",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.35,
            "Short name": "hazmatsuit.arcticsuit",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      },
      {
        "Roam position": "(22.73, 0.31, -42.57)",
        "Roam range": 10.0,
        "Relocation position": "(24.41, 0.31, -35.30)",
        "Weapon": {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "lmg.m249",
          "Skin ID": 0
        },
        "Attire": [
          {
            "Short name": "hazmatsuit.arcticsuit",
            "Skin ID": 0
          }
        ],
        "Droppable loot": [
          {
            "Amount": {
              "Min": 10,
              "Max": 50
            },
            "Chance": 1.0,
            "Short name": "ammo.rifle",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 2
            },
            "Chance": 1.0,
            "Short name": "syringe.medical",
            "Skin ID": 0
          },
          {
            "Amount": {
              "Min": 1,
              "Max": 1
            },
            "Chance": 0.35,
            "Short name": "hazmatsuit.arcticsuit",
            "Skin ID": 0
          }
        ],
        "Attack range multiplier": 1.0
      }
    ],
    "Crate settings": {
      "Hack duration (Min 60s)": 420.0,
      "Total items": {
        "Min": 8,
        "Max": 10
      },
      "Items": [
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle.explosive",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle.incendiary",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle.hv",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "ammo.rocket.basic",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "door.double.hinged.toptier",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "door.hinged.toptier",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "wall.window.bars.toptier",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "metal.facemask",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "metal.plate.torso",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "explosives",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "explosive.timed",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "weapon.mod.lasersight",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "weapon.mod.small.scope",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.ak",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.bolt",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "hmlmg",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smg.mp5",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "jacket",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "heavy.plate.helmet",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "heavy.plate.jacket",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "heavy.plate.pants",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smgbody",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "riflebody",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 2,
            "Max": 4
          },
          "Chance": 1.0,
          "Short name": "techparts",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 5,
            "Max": 6
          },
          "Chance": 1.0,
          "Short name": "metalpipe",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "targeting.computer",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "cctv.camera",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 15,
            "Max": 25
          },
          "Chance": 1.0,
          "Short name": "metal.refined",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "supply.signal",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "floor.ladder.hatch",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "floor.triangle.ladder.hatch",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "gates.external.high.stone",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "wall.external.high.stone",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "wall.frame.cell.gate",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "wall.frame.cell",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "wall.frame.garagedoor",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "shutter.metal.embrasure.a",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "shutter.metal.embrasure.b",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "wall.window.glass.reinforced",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "roadsign.gloves",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "coffeecan.helmet",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "hoodie",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "nightvisiongoggles",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "roadsign.kilt",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "shoes.boots",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "hazmatsuit",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "roadsign.jacket",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "barricade.concrete",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "barricade.metal",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "computerstation",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "drone",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "elevator",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "furnace.large",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "trap.landmine",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "locker",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "modularcarlift",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "small.oil.refinery",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smart.alarm",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smart.switch",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "storage.monitor",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.battery.rechargable.large",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.battery.rechargable.medium",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.counter",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.hbhfsensor",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.laserdetector",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.furnace",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.andswitch",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electrical.memorycell",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.random.switch",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.rf.broadcaster",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.rf.receiver",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.fuelgenerator.small",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "industrial.crafter",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "powered.water.purifier",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "electric.teslacoil",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "waterpump",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "ptz.cctv.camera",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "searchlight",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "water.catcher.large",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "generator.wind.scrap",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "parachute",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "autoturret",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rf.detonator",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "largemedkit",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "syringe.medical",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rf_pager",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "grenade.smoke",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "weapon.mod.extendedmags",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "weapon.mod.holosight",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "weapon.mod.muzzleboost",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "weapon.mod.muzzlebrake",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "chainsaw",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "grenade.f1",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "flamethrower",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "grenade.flashbang",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "homingmissile.launcher",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "grenade.molotov",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "pistol.python",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rocket.launcher",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "axe.salvaged",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "icepick.salvaged",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "shotgun.pump",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "pistol.semiauto",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.semiauto",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smg.2",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "longsword",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smg.thompson",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "horse.armor.roadsign",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "horse.shoes.advanced",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 12,
            "Max": 12
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 15,
            "Max": 15
          },
          "Chance": 1.0,
          "Short name": "ammo.pistol",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.lr300",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "pistol.m92",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "shotgun.spas12",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 8,
            "Max": 12
          },
          "Chance": 1.0,
          "Short name": "ammo.shotgun",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.l96",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "weapon.mod.8x.scope",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.m39",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "pistol.prototype17",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "shotgun.m4",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 8,
            "Max": 12
          },
          "Chance": 1.0,
          "Short name": "ammo.shotgun.slug",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "aiming.module.mlrs",
          "Skin ID": 0
        }
      ]
    }
  },
  "Plane settings": {
    "Height": 15.0,
    "Speed": 125.0,
    "Supply drop": {
      "Amount (max 8)": {
        "Min": 2,
        "Max": 4
      },
      "Total items": {
        "Min": 4,
        "Max": 6
      },
      "Items": [
        {
          "Amount": {
            "Min": 5,
            "Max": 5
          },
          "Chance": 1.0,
          "Short name": "gears",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 5,
            "Max": 6
          },
          "Chance": 1.0,
          "Short name": "metalpipe",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 5,
            "Max": 5
          },
          "Chance": 1.0,
          "Short name": "sheetmetal",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 4,
            "Max": 5
          },
          "Chance": 1.0,
          "Short name": "techparts",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 140,
            "Max": 160
          },
          "Chance": 1.0,
          "Short name": "scrap",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 32,
            "Max": 40
          },
          "Chance": 1.0,
          "Short name": "metal.refined",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "coffeecan.helmet",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "bucket.helmet",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "jacket.snow",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "riot.helmet",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "hoodie",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "pants",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "roadsign.jacket",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "roadsign.kilt",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "roadsign.gloves",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "shotgun.pump",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 8,
            "Max": 12
          },
          "Chance": 1.0,
          "Short name": "ammo.shotgun",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.semiauto",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 35,
            "Max": 50
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smg.2",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 20,
            "Max": 20
          },
          "Chance": 1.0,
          "Short name": "ammo.pistol",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smg.thompson",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "smg.mp5",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "shotgun.spas12",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "pistol.m92",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.m39",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "rifle.lr300",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "pistol.prototype17",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 10,
            "Max": 10
          },
          "Chance": 1.0,
          "Short name": "ammo.pistol.fire",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 10,
            "Max": 10
          },
          "Chance": 1.0,
          "Short name": "ammo.pistol.hv",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 8,
            "Max": 8
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle.incendiary",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 10,
            "Max": 10
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle.hv",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 8,
            "Max": 8
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle.explosive",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 4,
            "Max": 4
          },
          "Chance": 1.0,
          "Short name": "ammo.shotgun.slug",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 4,
            "Max": 8
          },
          "Chance": 1.0,
          "Short name": "ammo.shotgun.fire",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "chainsaw",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "jackhammer",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 2,
            "Max": 4
          },
          "Chance": 1.0,
          "Short name": "grenade.f1",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "explosive.satchel",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 1
          },
          "Chance": 1.0,
          "Short name": "explosive.timed",
          "Skin ID": 0
        }
      ]
    },
    "NPCs": {
      "Amount (max 8)": {
        "Min": 4,
        "Max": 6
      },
      "Weapon": {
        "Short name": "hmlmg",
        "Skin ID": 0
      },
      "Attire": [
        {
          "Short name": "jumpsuit.suit",
          "Skin ID": 0
        },
        {
          "Short name": "hat.gas.mask",
          "Skin ID": 0
        }
      ],
      "Droppable loot": [
        {
          "Amount": {
            "Min": 10,
            "Max": 50
          },
          "Chance": 1.0,
          "Short name": "ammo.rifle",
          "Skin ID": 0
        },
        {
          "Amount": {
            "Min": 1,
            "Max": 2
          },
          "Chance": 1.0,
          "Short name": "syringe.medical",
          "Skin ID": 0
        }
      ],
      "Attack range multiplier": 1.0
    }
  },
  "Debug mode": false,
  "Plugin version": {
    "Major": 0,
    "Minor": 1,
    "Patch": 3
  }
}
```
{% endcode %}
