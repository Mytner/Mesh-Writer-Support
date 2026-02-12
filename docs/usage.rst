Usage Guide
===========

Emoji Search
------------

1. Type in the search bar to find emojis by name or category
2. Select **Copy** or **Insert** mode:
   
   * **Copy**: Copies emoji to clipboard
   * **Insert**: Inserts directly into active text object or node

3. Click on an emoji to copy/insert it

Emoji Categories
----------------

1. Expand the **Emojis** panel
2. Click a category button (e.g., "Smileys & Emotion")
3. Browse emojis in a 4-column grid
4. Click **← Back** to return to categories

SVG Import (View3D Only)
------------------------

1. Check **Show SVG Options** in the search panel
2. Emojis with available SVGs show an asterisk (*)
3. Click the SVG button to import as a curve object

.. note::
   SVG import only works in View3D, not in Geometry Nodes.

**All SVG files are scaled by 10 by default for better visual clarity. 
Ensure to check on it in case you feel to change it.**

Working with Text Objects
-------------------------

In View3D:

1. Select a Text object
2. Use **Insert** mode
3. Click an emoji to insert at cursor position

In Geometry Nodes:

1. Select a String node
2. Use **Insert** mode  
3. Click an emoji to append to the string input


Working with the Text Editor:
----------------

**Using the text editor in the node editor:**
Click on the "Open Text Editor" button to open the text editor.
You can use the editor just like any text editor to add multiline text.

**Changing the text format to bold or italic:**
You can change the text format to bold or italic using the buttons 🅱️ Bold Live and 𝑰 Italic Live.


Frame Creation and Management:
----------------
**Creating a frame.**
Open a Shader Node Editor (Same for Geometry and Compositor node editors)
: Press N -- Go to the Mesh Writer tab
To create a frame or comment:
Use the "Create Frame ➕" button

**Creating a frame for a node or nodes:**
Select your node or nodes
Use the "Insert Frame ☐" button
A frame will be created at the mouse cursor location.

**Note:** 

Each frame creation results in a data block named "_MW". 

This stores your text and formatting. Any frame created via Mesh Writer will have a data block ending with "_MW". You can change it if you want.

All data blocks are saved automatically, you do not need to save them manually.

To delete a frame and its data block, simply delete the frame node. The data block will be deleted automatically.


Language Selection
------------------

Change the emoji name language in the **Help/Settings** panel to see tooltips in your preferred language.
