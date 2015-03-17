# Game Data Description

Description of the data formats used to describe an entire game.

Formats
-------

Below are the various formats used to describe a game.

### Sprite

As detailed in [sprite-exporter][], we will store sprites as a [JSON][json] file with the following format

```json
{
  "columns": 15,
  "rows": 10,
  "palette": ["rgba(0,0,0,1)", "rgba(255,0,0,1)"],
  "pixels": [
    [[0, 0], [1, 0], [2, 0]],
    [[12, 9], [13, 9], [14, 9]]
  ]
}
```

### Sprite map

Sprite maps are a combination of two files

1. An image file, e.g. `trees.png`.
2. Corresponding meta-data, e.g. `trees.json`


```json
{
  "info": {
    "description": "Trees and assorted shrubbery",
    "width": 640, "height": 480
  },
  "sprites": {
    "Oak Tree Foliage": { "x": 0, "y": 0, "width": 100, "height": 100 },
    "Oak Tree Stem": { "x": 40, "y": 100, "width": 20, "height": 80 },
    "Oak Tree Roots": { "x": 20, "y": 180, "width": 60, "height": 20 }
  }
}
```

### Game

```json
{
  "levels": [
    {
      "sections": [
        {
          "layers": [
            {
              "objects": [
                { "x": 37, "y": 51, "spritemap": "trees.json", "key": "Oak Tree Foliage" },
                { "x": 37, "y": 200, "spritemap": "clams.json", "key": "mossy heap of clams" }
              ]
            }
          ]
        }
      ]
    }
  ]
}
```

[sprite-exporter]: https://github.com/Chair-of-Indefinite-Studies/sprite-exporter
