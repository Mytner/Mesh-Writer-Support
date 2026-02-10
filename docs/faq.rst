Frequently Asked Questions
===========================

.. contents:: Table of Contents
   :local:
   :depth: 1

----

**Q: Why do some Unicode characters (e.g. certain symbols) not appear?**

Mesh Writer is an evolving library with more than three thousand Unicode characters. Not all Unicode characters are currently supported, especially rare or complex glyphs. Support for additional Unicode symbols will be expanded in future updates.

----

**Q: In Object Mode, why do some imported SVGs look black or distorted?**

This is due to how Blender natively imports SVG files. All the layers (curves) are stacked on one another which may look as if the SVGs are distorted or not colored properly.

Some SVGs contain complex fills, strokes, or transforms that Blender may convert imperfectly into curves. Additionally, Blender imports SVGs at a very small default scale, which can exaggerate visual artifacts.

To address this, Mesh Writer applies a default scale of 10, making SVGs immediately visible and easier to work with.

----

**Q: I can't see the SVG after importing it. Why?**

Blender's native SVG import places the geometry at a very small scale and aligns it on the XY plane, making it easy to miss.

Mesh Writer automatically scales imported SVGs by 10×, so they are visible right away.

----

**Q: Why do some icons look different when converted from Text?**

Blender's Text objects rely on an internal font-to-curve conversion system. Some Unicode icons and icon-font glyphs use highly complex paths or overlapping shapes, which Blender may simplify or restructure during conversion. This can cause subtle distortions or visual differences.

For maximum fidelity, especially with complex icons, using the Import SVG workflow is recommended. SVG files follow a more explicit path definition pipeline and generally preserve the original shape more accurately.

----

**Q: Why is my object's "Origin" far away from the actual mesh?**

SVGs often carry the canvas coordinates from the software they were created in (like Illustrator or Inkscape). To fix this, right-click the object in the 3D viewport and select **Set Origin → Origin to Geometry**.

----

**Q: Some emojis show "NA" instead of an SVG. Why?**

Mesh Writer currently parses emoji data using the Noto Emoji dataset. Not all emojis have SVG counterparts available yet, so some appear as NA. Future versions will expand coverage to include more SVGs.

----

**Q: Why are colored emojis not included?**

Colored emojis are intentionally excluded to keep the UI clean, lightweight, and consistent inside Blender.

If you have a specific use case that requires colored emojis, please submit a feature request and it can be considered for a future patch.

----

**Q: Why do Mesh Writer's emojis in Blender look different from those on my phone or computer?**

Different platforms use different emoji fonts and rendering systems (for example, Apple Emoji, Segoe UI Emoji, or Noto Color Emoji).

Mesh Writer uses the Noto Emoji set, which follows Google's design language. Additionally, unlike standard Unicode characters, there is no single universal SVG or visual standard for emojis, so their appearance naturally varies across platforms.

----

**Q: Is this a Blender bug or a Mesh Writer bug?**

The way Blender's native text, font, or SVG import systems work often lead to some visual problems. Mesh Writer builds on top of these systems and does not modify Blender's internal conversion logic.

----

**Q: Can I fix distorted icons manually?**

Yes. After conversion, you can adjust curve handles, fill mode, or convert to mesh and clean up topology manually.

----

**Q: Why are some icons heavier / thinner than expected?**

Font glyphs may contain variable stroke weights or rely on font hinting, which Blender does not fully support. SVG imports preserve stroke intent more reliably.

----

**Q: Does Mesh Writer modify Blender's SVG or Text engine?**

No, as of now. Mesh Writer works on top of Blender's existing systems and does not alter Blender's internal import or text pipelines.

----

**Q: Why is my converted text not appearing in the 3D viewport?**

Check that:

1. You're in the correct viewport shading mode
2. The object isn't hidden or on a disabled layer
3. The text object has actual content/characters
4. Your camera/view position allows you to see the object location

----

**Q: Can I animate text with Mesh Writer?**

Mesh Writer converts text to static geometry. For animation, you can:

1. Animate the mesh object itself (position, rotation, scale)
2. Use Geometry Nodes on the converted mesh
3. Keep it as a Text object and use Blender's native text animation features before conversion

----

**Q: Why are emojis in Blender not colored and sometimes split apart unlike their SVG counterpart?**

*(Example: 🧘‍♂️ SVG appears as 🧘 ♂ Text and looks less detailed)*

**Emoji sequences:** Some emojis (like 🧘‍♂️) are made up of multiple Unicode characters joined together with special rules (ZWJ sequences). Blender's text editor and text object's system doesn't natively support these, so it displays them as separate glyphs.

Also, Blender's text system only supports black-and-white outline fonts. Color emojis rely on special font formats (used by browsers and operating systems) that Blender does not render. As a result, emojis appear monochrome and less detailed.

Simple, single-character emojis (😀 ❤️ 🔥) render more reliably. Compound emojis with gender, skin tone, or profession modifiers (👨‍🚀 👩‍⚕️ 🏃‍♀️) will likely break.

**Recommended:** Use their SVG counterpart.



**Q: How to create a frame in node editor?**
Open a Shader Node Editor (Same for Geometry and Compositor node editors)
: Press N -- Go to the Mesh Writer tab
To create a frame or comment:
Use the "Create Frame ➕" button

**Q: To create a frame for a node or nodes:**
Select your node or nodes
Use the "Insert Frame ☐" button
A frame will be created at the mouse cursor location.

**Q: How to use the text editor in the node editor?**
Click on the "Open Text Editor" button to open the text editor.
You can use the editor just like any text editor to add multiline text.


**Q: How to change the text format to bold or italic?**
You can change the text format to bold or italic using the buttons 🅱️ Bold Live and 𝑰 Italic Live.


**Q: How to change the Name/Label/Color?Font size?**
To edit these properties, you do these just as you would with any regular frame node in Blender:
Name, label and color select the frame and go to the Node tab in the sidebar (N key) and
--> Label : Click on the label field to edit the label text. The label is a secondary name that appears on the frame node and can be different from the data block name.
--> Name: Click on the name field to edit the data block name. This is the internal name used for referencing the frame in scripts and data management. It must be unique among all data blocks.
--> Color: The color option will change the frame color.
--> Font Size: Select the frame and go to the Node tab in the sidebar (N key) and adjust the font size under Properties.

**Q: How to resize the frame?**
Simply select the frame and use the standard Blender node resizing handles to adjust its size.

**Still got queries? Open an `Issue <https://github.com/abhi-01/FrameFlow-Blender/issues>`_ on GitHub.**



