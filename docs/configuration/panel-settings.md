---
layout: docs
title: Panel Settings
description: Tune up your IDE's look and feel.
group: configuration
toc: true

previous:
  url: '/docs/configuration/tab-settings'
  title: Tab Settings
next:
  url: '/docs/configuration/component-settings'
  title: Component Settings

colors:
  - name: default
    color: '#1E272C'
    light: false
  - name: darker
    color: '#1A1A1A'
    light: false
  - name: lighter
    color: '#F4F4F4'
    light: true
  - name: palenight
    color: '#202331'
    light: false
---

These settings control the customization of various parts of the IDE, such as the tool windows, status bar, icons or  the components' colors.
{:class='title'}

### Contrast Mode

The contrast mode allows you to add more contrast between the IDE's panels and components for better visualizing.

{% include figure.html content="/screens/noContrast.png" caption="Without Contrast enabled" %}
{% include figure.html content="/screens/withContrast.png" caption="With Contrast enabled" %}

The parts that are affected by the contrast change are:
- The project tree
- The settings tree
- Inactive tabs
- Input, Search and number controls
- Dropdowns
- Lists and Tables

#### Color Palette

{% for color in page.colors %}
{% include color.html color=color %}
{% endfor %}


### Hide File Icons

This option allows you to _completely hide_ the file icons from the IDE. This means from the _Project Tree_, Tabs, Dialogs and everything. This does not remove folders, though.

{% include figure.html content="/screens/hideFileIcons.png" caption="Hide File Icons" %}

This feature depends on the [Material File Icons]({{ site.baseurl }}/docs/configuration/component-settings#material-file-icons)

**Note**: This feature takes precedence over default file icons providers and the plugin's own one. However some plugins, such as the _PHP_ or _Python_ plugins, may have an even greater precedence, meaning that you will still see icons from these plugins.
{:class='card-panel'}

----
### Custom sidebar height

Following Material Design principles, this plugin is adding more padding to many of the components used in the IDE, such as Tables, Lists and Tree. This setting will allow you to override this behavior and specify a custom line height in your tree views, such as the _Project View_ and the _Settings View_.

The allowed values are between **18** and **30** in order to keep the IDEs within reasonable sizes. The default value when unchecked is **28**.

<div class="masonry">

{% include figure.html content="/screens/regularLineHeight.png" caption="Regular Line Height" %}

{% include figure.html content="/screens/paddedLineHeight.png" caption="Padded Line Height" %}

</div>

----
### Custom tree indent

Another tree views' feature is the ability to customize the indentation of the items. This might be useful for projects that have a lot of nesting levels and do not want unnecessary scrolling.

The allowed values vary between **2** and **8**, with the default being **4**.
<div class="masonry">

{% include figure.html content="/screens/condensedView.png" caption="Condensed indent (2)" %}

{% include figure.html content="/screens/dilatedView.png" caption="Dilated indent (8)" %}

</div>

----
### Compact Statusbar

The IDE's Status Bar went through a redesign as well, removing all borders and giving more padding on the top and bottom. This setting allows you to revert back to the default "_compact_" design.


{% include figure.html content="/screens/expandedStatusbar.png" caption="Padded Status Bar" %}

{% include figure.html content="/screens/compactStatusbar.png" caption="Compact Status Bar" %}

**Note**: Because of how the status bar was implemented, the padding can only be given at the start of the application, meaning that when opening multiple projects the status bar automatically reverts to its default, compact state regardless of the settings.
{:class='card-panel'}

----
### Compact Table Cells

Just like the status bar, table cells, table headers and list views were also given more padding to resemble more like Material Design's equivalents.

This setting allows you to revert to the old, "_compact_" style. This can be useful if you have lots of items and don't want to scroll endlessly.

----
### Bold Directories

This setting allows you to set directories in the _Project View_ in **bold**. This could be useful to immediately differentiate between files and directories (default off).

{% include figure.html content="/screens/boldDirectories.png" caption="Bold directories" %}

----
### Custom Accent Color

This setting controls the [current accent color](custom-accents.md) used throughout the app.

Accent color is used in many places such as:
- Quick documentation
- Parameter Info
- Links and bold texts in documentation panels
- Text, number and password boxes border
- Dropdowns border
- Checkboxes and Radio Buttons fill color
- etc...

While a set of predefined accent colors are available in the [Accent Color Chooser](actions.md), this setting allows you to set your own custom color.

{% include figure.html content="/screens/accentChooser.png" caption="Accent Color Chooser" %}

----
### Notes

- Contrast color is also used inside "striped tables", independently of the setting.
- Tree views settings work in all tree views, even views such as "Project Structure" or "Remote Host"
- Compact Statusbar only works if there are only one open instance of the IDE


