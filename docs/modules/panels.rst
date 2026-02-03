Panels
======

Base Panels
-----------

.. py:class:: PARENT_PT_COMMON_Panel

   Base panel class providing common UI elements for all Mesh Writer panels.
   
   Located in: ``common_parent_UI_panel.py``

.. py:class:: EMOJI_SEARCH_BAR_PT_COMMON

   Search bar panel with emoji search functionality.
   
   Located in: ``common_parent_emoji_search_bar.py``
   
   **Features:**
   
   * Search input field
   * Copy/Insert mode toggle buttons
   * Clear button
   * SVG options checkbox (View3D only)
   * Search results grid

.. py:class:: TEXT_PT_emoji_category_panel

   Base panel for emoji category browsing.
   
   Located in: ``common_parent_emoji_category_panel.py``
   
   **Features:**
   
   * 2-column category button grid
   * 4-column emoji grid per category
   * Back navigation

View3D Panels
-------------

Panels in ``view3d_main_panel.py``:

* ``VIEW3D_PT_parent_panel`` - Main parent panel
* ``VIEW3D_EMOJI_CATEGORIES_PT_COMMON`` - Emoji categories
* ``VIEW3D_MATH_SYMB_PT_COMMON`` - Math symbols
* ``VIEW3D_SUP_SUB_SCRIPT_PT_COMMON`` - Super/subscript characters

Text Editor Panels
------------------

Panels in ``text_editor_main_panel.py``:

* ``TEXT_EDITOR_PT_parent_panel`` - Main parent panel
* ``TEXT_EDITOR_EMOJI_CATEGORIES_PT_COMMON`` - Emoji categories

Geometry Nodes Panels
---------------------

Panels in ``geo_nodes_main_panel.py``:

* ``GEO_NODES_PT_parent_panel`` - Main parent panel
* ``GEO_NODES_EMOJI_CATEGORIES_PT_COMMON`` - Emoji categories
* ``GEO_NODES_MATH_SYMB_PT_COMMON`` - Math symbols

.. note::
   SVG import is disabled in Geometry Nodes as SVG curves don't work in that context.
