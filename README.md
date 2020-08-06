# Net Worth
The Net Worth data file consists of three types of entries. Entries are some value in the player's profile that will contribute to their net worth. Direct entries are values that will be directly added (ie coins). Tiered entries have a value associated per tier and accumulate from all previous values. Tiered entries also have an offset that will be added to the value read from the location. The value will be mapped to the index in the array. In the event the index is out of bounds, the sum will stand as all previous values up until there is no more data. Single purchase entries are entries that can be purchase one time for a set amount of coins.

## Naming
All entries for each type are named beginning with `stats`, followed by the name of the game, followed by the category the entry belongs to in the hypixel shop menu (If it is a part of 2 categories like "Kits & Perks" and "Normal Kits" for the Armorer kit in skywars, only use the most relevant category. It would be "Normal Kits" in this case.), finally followed by the name of the entry. (everything is lower case)
Here are some examples: `stats.hungergames.advancedkits.astronaut`, `stats.skywars.normalkits.armorer`, `stats.bedwars.victorydances.dragonrider`.

## Contributing
If you would like to contribute, please add entries and open a pull request.

## Example
Example for each type of entry:
```
{
   "direct": [
        "stats.arcade.coins"
    ],
    "tiered": {
        "hungergames": {
            "advancedkits": {
                "astronaut": {
                    "offset": 1,
                    "values": [
                        0,
                        80,
                        400,
                        1000,
                        3000,
                        12000,
                        50000,
                        100000,
                        250000,
                        1000000
                    ]
                }
            }
        }
    },
    "single": {
        "bedwars": {
            "projectiletrails": {
                "firework": 25000
            }
        }
    }
}
```

