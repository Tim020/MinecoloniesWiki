---
title: Research System
layout: default
---

# Research System

At the {% building university %}, {% worker researcher plural=true %} can research various upgrades to your colony. These are split into three trees: Combat, Civilian, and Technology. You access these from the second page of the University GUI.

Each column of a research tree is also the level the University needs to be to begin a research from that column. So:

| Research Tree Column | Minimum University Level |
|----------------------|--------------------------|
| 1                    | 1                        |
| 2                    | 2                        |
| 3                    | 3                        |
| 4                    | 4                        |
| 5+                   | 5                        |

You can only have one column 6 research in each of the Combat, Civilian, and Technology trees. To unlock a different column 6 research for that tree, you must undo the completed one first.

| Symbol                                                                                      | Description                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Blocked Research](../../assets/images/gui/buildings/university/research_blocked.png)      | A research can be **blocked**, either by an unfinished prerequisite research, by a completed blocking research, or because the research tree has another column 6 research already active.                                                                                                                                                  |
| ![Locked Research](../../assets/images/gui/buildings/university/research_locked.png)        | A **locked** research requires a building or buildings, or other unrelated research, before it can be started.                                                                                                                                                                                                                              |
| ![Unlocked Research](../../assets/images/gui/buildings/university/research_unlocked.png)    | An **unlocked** research has all colony and research requirements met, but requires an item or items. **These items must be in the player's inventory.**                                                                                                                                                                                    |
| ![Available Research](../../assets/images/gui/buildings/university/research_ready.png)      | An **available** research is ready to begin. Clicking the title of the research will consume the items from the player's inventory and start the research.                                                                                                                                                                                  |
| ![Progressing Research](../../assets/images/gui/buildings/university/research_progress.png) | A **progressing** research is being worked on currently. This research will show its current progression and a rough estimate of the remaining time to completion. A progressing research can be canceled by clicking the research title and then clicking the Cancel pop-up. Cancelling a research will **not** refund the material costs. |
| ![Complete Research](../../assets/images/gui/buildings/university/research_complete.png)    | A **complete** research has been fully unlocked by your University. Its effects have been applied to the colony and colonists.                                                                                                                                                                                                              |
| ![Exclusive Research](../../assets/images/gui/buildings/university/research_or.png)         | Some researches are **exclusive**, requiring such extreme focus that they aren't compatible with each other. Only one research from a specific **or** selection may be learned in a colony at a time.                                                                                                                                       |
| ![Undo Research](../../assets/images/gui/buildings/university/research_undo.png)            | Some completed researches may be **undone** if they block another research in some way, do not have a completed research that depends on them, and are not marked with a redstone torch as irreversible. Undoing a research does *not* refund the research costs and consumes the displayed item.                                           |

<span id="top-anchor"></span>

## Below is a description of each of the researches:

**Note:** Researches below are *not* cumulative unless stated otherwise.

{% for research_tree in site.data.research.trees %}
- [{{ research_tree[1].name }}]({{ "#" | append: research_tree[1].name | downcase }})
{% endfor %}

<hr/>

{% for research_tree in site.data.research.trees %}
{% assign research_tree_name = research_tree[1].name %}
### {{ research_tree[1].name }}
[Back to top](#top-anchor)

{% if research_tree[1].description != null and research_tree[1].description != "" %}
{{ research_tree[1].description }}
{% endif %}

{% assign chains = research_tree[1].chains %}
{% include research/recurse.html tree=research_tree_name chains=chains %}

<hr/>
{% endfor %}
