Operators
=========

Copy/Insert Operators
---------------------

.. py:class:: TEXT_OT_copy_emoji_COMMON

   Copy an emoji to the clipboard.
   
   :bl_idname: ``frameflow.copy_emoji``
   
   **Properties:**
   
   * ``emoji`` (StringProperty): The emoji character to copy
   * ``tooltip`` (StringProperty): Tooltip text for the button

.. py:class:: TEXT_OT_insert_emoji_COMMON

   Insert an emoji at the cursor position.
   
   :bl_idname: ``frameflow.insert_emoji``
   
   **Supported contexts:**
   
   * Text Editor: Inserts into active text block
   * View3D: Inserts into active FONT object (edit mode)
   * Geometry Nodes: Appends to string input sockets

.. py:class:: TEXT_OT_delete_emoji_panel_COMMON

   Clear the search query and clipboard.
   
   :bl_idname: ``frameflow.delete_emoji``

Category Operators
------------------

.. py:class:: TEXT_OT_emoji_back_to_categories

   Return to category selection view.
   
   :bl_idname: ``text.emoji_back_to_categories``

.. py:class:: TEXT_OT_emoji_no_svg

   Placeholder button when SVG is unavailable.
   
   :bl_idname: ``text.emoji_no_svg``

SVG Operators
-------------

.. py:class:: FRAMEFLOW_OT_import_emoji_svg

   Import an emoji's SVG as a Blender curve object.
   
   :bl_idname: ``frameflow.import_emoji_svg``
   
   **Properties:**
   
   * ``emoji`` (StringProperty): The emoji to import
   * ``tooltip`` (StringProperty): Tooltip text

Mode Operators
--------------

.. py:class:: FRAMEFLOW_OT_set_mode

   Toggle between Copy and Insert modes.
   
   :bl_idname: ``frameflow.set_mode``
   
   **Properties:**
   
   * ``mode`` (StringProperty): Either 'COPY' or 'INSERT'

Utility Operators
-----------------

.. py:class:: text_object_check_modeling_mode

   Check if active object is a text object and insert emoji.
   
   :bl_idname: ``frameflow.text_object_check_modeling_mode``
