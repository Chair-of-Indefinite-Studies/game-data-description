# Game Data Description

Description of the data formats used to describe an entire game.

Formats
-------

Below are the various formats used to describe a game.

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

