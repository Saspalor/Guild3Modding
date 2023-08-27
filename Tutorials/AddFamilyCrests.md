# Tutorial: Adding Shields for More Family Crests in The Guild 3

In *The Guild 3*, you can enhance family crests by incorporating additional shields with unique designs. This guide will guide you through the process of introducing new shields into the game using the provided instructions.

### 1. Prepare Your Shield Images:

Before you begin adding new family crests, ensure that you have the shield images you intend to use. Place these images in the following filepaths:

- **Shield Colors:** `media/userinterface/icons/shields/color`
  - Typically used for most cases.
- **Small Outline Shields:** `media/userinterface/icons/shields/smalloutline`
  - Utilized, for instance, alongside the names of dynasty members.

Ensure that your shield images are appropriately sized (squared, e.g. 512px or 256px) and formatted (.png) to meet the game's requirements.

### 2. Edit the `FamilyCrestDescsDefault.oc` File:

To define your new family crests, you'll need to modify the `FamilyCrestDescsDefault.oc` file located in `media/base/guild3`. This file defines the crest and links to other files, including the in-game color for all the family crests in the game. Here's an example of how to add a new crest:

```cpp
Crests44 extend FamilyCrestDesc
{
    Id = 33; // Should correspond to the filename of your image.
    TextureName = "Shield33"; // Requires further investigation.
    CrestColor = array{0.855, 0.149, 0.133}; // Define the ingame color using RGB values.
},
```

- `Id`: Select a unique numerical ID for your crest.
- `TextureName`: `"Shield33"` is likely related to a texture file (e.g., for the flag during conquest).
- `CrestColor`: Set the crest color using RGB values (values ranging from 0 to 1).

### 3. Texture for Dynasty Flag:

*Further investigation needed; this section is left out for now (potentially until we can extract images from .oppc files)*

### 4. Entry and Definition in Extended Glyph Sheet:

To ensure that your new family crest displays correctly in the game, you may need to create an entry and definition in the extended glyph sheet. This entails specifying the position and dimensions of your shield image within the glyph sheet, which can be found in the main game files.

### 5. Testing:

After implementing these changes, save the `FamilyCrestDescsDefault.oc` file and any other relevant files. Launch the game and create or select a family to check if your new crest is available. If you encounter any issues, thoroughly review your code, file paths, and image formats.

**TL;DR:**

1. Prepare shield images and place them in the specified folders.
2. Modify the `FamilyCrestDescsDefault.oc` file to define new crests.
3. You may need to work on textures for dynasty flags.
4. Create an entry and definition in the extended glyph sheet for proper display.
5. Test your changes in the game to ensure they work.


Following these steps, you should be able to incorporate new shields for family crests in *The Guild 3*. Happy modding!
