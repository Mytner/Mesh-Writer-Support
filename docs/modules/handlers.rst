Handlers & Utilities
====================

Emoji Database
--------------

.. py:module:: emoji_database_search

.. py:function:: load_emoji_database()

   Load the emoji database from ``emoji_database.txt``.
   
   :returns: Dictionary mapping emoji characters to metadata
   :rtype: dict

.. py:module:: common_parent_emoji_search_bar

.. py:function:: search_emojis(query)

   Search emojis based on query matching metadata fields.
   
   :param query: Search string
   :type query: str
   :returns: Dictionary of matching emojis and their data
   :rtype: dict
   
   **Searchable fields:**
   
   * Emoji name (in selected language + English fallback)
   * Category
   * Subgroup

Emoji Categories
----------------

.. py:module:: emoji_category_single_file_list

.. py:data:: EMOJI_CATEGORIES

   List of emoji category definitions with keys:
   
   * ``key``: Category identifier
   * ``name``: Display name
   * ``category_op_id``: Operator ID for category button

.. py:module:: common_parent_emoji_category_panel

.. py:function:: get_emojis_by_category(category_name)

   Get all emojis belonging to a specific category.
   
   :param category_name: Category name to filter by
   :type category_name: str
   :returns: List of emoji characters
   :rtype: list

.. py:function:: get_emoji_name(emoji, lang='en')

   Get the localized name of an emoji.
   
   :param emoji: Emoji character
   :param lang: Language code (default: 'en')
   :returns: Emoji name in specified language
   :rtype: str

SVG Handler
-----------

.. py:module:: EmojiText_Noto

.. py:class:: NotoEmojiHandler

   Handler for Noto emoji SVG files.
   
   .. py:method:: has_svg(emoji)
   
      Check if an SVG exists for the given emoji.
      
      :param emoji: Emoji character
      :returns: True if SVG available
      :rtype: bool
   
   .. py:method:: import_emoji_svg(emoji, collection_name=None)
   
      Import emoji SVG as a Blender curve object.
      
      :param emoji: Emoji character
      :param collection_name: Optional collection name for the object
      :returns: The imported object or None
