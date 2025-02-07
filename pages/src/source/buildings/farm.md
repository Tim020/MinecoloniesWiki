---
type: building
building: farm
layout: building
---
{% infobox_building %}
The Farm is where the Farmer will grow crops for your colony. The crops the Farmer currently cultivates are wheat, carrots, potatoes, beets, melons, pumpkins, and most crops from other mods (as long as they have normal growth behavior). Before the Farmer can start, you will have to give the Farmer a hoe, an axe (for harvesting crops), and the crop you want to cultivate. 

The Farmer will also craft seeds, carved pumpkins, hay bales, [composted dirt](../../source/items/compost), and coarse dirt. They will only make items when they have been taught the recipes, receive a request for an item, and have the needed materials.

**Note:** The Farmer can only learn a set number of recipes based on their hut level. So:

| Hut Level | Recipes |
|-----------|---------|
| 1         | 10      |
| 2         | 20      |
| 3         | 40      |
| 4         | 80      |
| 5         | 160     |

For the Farmer to start, you will also need to place fields. Place the Field block (it looks like a scarecrow) in the plot of farmland you want the Farmer to work on and right-click on it to access its GUI. Here you will place the seed of the crop you want this specific field to cultivate. (For potatoes, carrots, and other plants without seeds, just put the raw potato/carrot/etc in the Field.) If you decide later to change the type of crop you want cultivated in that farmland, just go into the Field's GUI and switch the seed there.

<img src="../../assets/images/misc/field.png" alt="Field">
<img src="../../assets/images/gui/buildings/farm/fieldgui.png" alt="Field GUI">

You can click on the arrows to increase the size of the area the Farmer will farm. (Right-clicking will decrease the area.) The max size is 5 blocks in each direction from the Field block, or 11x11 total.

**IMPORTANT:** The Farmer will farm up to five Fields, depending on the level of the Farm. The level of the Farm is the number of Fields the Farmer can cultivate:

| Farm Level | Fields |
|------------|--------|
| 1          | 1      |
| 2          | 2      |
| 3          | 3      |
| 4          | 4      |
| 5          | 5      |

{% endinfobox_building %}

## {% building %} GUI

{% building_gui_content_block_main order=1 %}
{% building_gui_content_block_craftingrecipes order=2 %}
{% building_gui_content_block_tasks order=3 %}
{% building_gui_content_block_settings order=4 %}
{% building_gui_content_block_fields order=5 %}
{% building_gui_content_block_stock order=6 %}