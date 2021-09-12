---
layout: default
title: Edit a dashboard
nav_order: 3
parent: Creating and Editing Dashboards (Panels)
has_children: false
has_toc: false
---

# How to edit a dashboard ?

A dashboard usually represent some visualization or table of some sort. GrimoireLab allows
you to execute the following queries in regards to your dashboard.

## Edit panel's title

Editing a dashboard's title is simple.
- Steps
    1. Click on `Edit` in the navigation bar of GrimoireLab.

   ![edit navigation](../assets/edit_nav.png)

    2. Click on the `Settings` icon of the dashboard. This will open a dropdown.

    ![edit](../assets/edit.png)

    3. Click on `Customize panel` and change your dashboard's panel.

    ![customize](../assets/customize.png)

## How to arrange your panels

GrimoireLab provides you with the ability to move and display your panels in any order you
want.

- Steps
  1. Look for the "Edit" button and click it.

     ![edit](../assets/edit_button.png)

  2. Once you've done the above, edit mode will be active. You can then drag any panels
     around and arrange it in any way you want.

     ![dragging panels](../assets/drag.gif)

## Edit visualization

In order to edit a visualization and save it, you need to be [logged
in.](https://vsevagen.github.io/grimoirelab-tutorial/docs/dashboards/dashboard-access/#how-to-login)
- Steps
    1. Click on `Edit` in the navigation bar of GrimoireLab.
    2. Click on the `Settings` icon of the dashboard. This will open a dropdown.
    3. Click on `Edit Visualization`.
    4. Change/Add your
       [Metrics](https://vsevagen.github.io/grimoirelab-tutorial/docs/dashboard/create-visualization/#metrics)
       and
       [Buckets](https://vsevagen.github.io/grimoirelab-tutorial/docs/dashboard/create-visualization/#buckets)
       and press the play button to visualize it.
    5. Once satisfied, `Save` your visualization.


**Note**: Refer to [how to create a
visualization](https://vsevagen.github.io/grimoirelab-tutorial/docs/dashboards/new-dashboard/)
to understand the editing interface.

## How to change the color of visualizations

Some visualizations make use of graphs, charts and tables to represent data. In order to
represent the different data, several contrasting colors are used.

- Steps
  1. Find the panel in which you want to change the color.
  2. Every panel that makes use of colors will have the sample color and the data it
     represents on the right side of the panel. In the case it is not visible, click on
     the arrow key on the right side of the panel. 

     ![color selection](../assets/color.png)

  3. Once you've clicked on the sample color, a palette of colors will be displayed. You
     just have to choose your preferred color. 

     ![color palette](../assets/color_palette.png)


##  Remove visualization from dashboard

For this action, you need to [logged
in](https://vsevagen.github.io/grimoirelab-tutorial/docs/dashboards/dashboard-access/#how-to-login) as
well.
- Steps
    1. Click on `Edit` in the navigation bar of GrimoireLab.
    2. Click on the `Settings` icon of the dashboard. This will open a dropdown.
    3. Click on `Delete from dashboard`.
    4. Press on `Save` in the navigation bar to save it.

**Note**: Deleting a dashboard removes it from dashboards but the dashboard would still be
available in your visualizations lists. In case you want to remove a dashboard entirely,
[refer to this
section](https://vsevagen.github.io/grimoirelab-tutorial/docs/dashboard/remove-dashboard/)