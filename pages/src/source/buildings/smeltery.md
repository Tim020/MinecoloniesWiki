---
type: building
building: smeltery
layout: building
---
{% infobox_building %}
The Smeltery is where the Smelter will smelt ores into ingots.

**Hint:** The higher the level of the Smeltery, the more furnaces the Smelter will be able to use. A higher level will also have a higher chance to double and even triple the ingot output per block of ore. In 1.16, the Smelter's Strength level will sometimes determine the chance to double or triple the ingot output of ores, according to the Smeltery level. In 1.18+, the smelter applies Fortune to the ores they smelt instead. See the Smelter's page for how their strength affects the output.
{% endinfobox_building %}

## {% building %} GUI

{% building_gui_content_block_main order=1 %}
{% building_gui_content_block_craftingrecipes order=2 noteach=true noremove=true %}
{% building_gui_content_block_fuel order=3 %}
{% building_gui_content_block_stock order=4 %}
{% building_gui_content_block_itemlist order=5 header="ores" image_key="ores" image_alt="Ores" default_on=true %}
Listed here are all ore blocks the Smeltery can smelt. Turn off any ores you do not want smelted.
All coded ores (even if they come from other mods) are automatically added to this list.
If you have ores that are not on the list, they can be added to the [config file](../../source/misc/configfile).
{% endbuilding_gui_content_block_itemlist %}