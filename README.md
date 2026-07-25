# Bliss
<img src="https://github.com/X0nk/Bliss-Shader/assets/122314734/873c788c-5a48-46c0-9fb5-eac57b4ffa27" width="100%" height="100%">
I always loved chocapic's shaders, and how customizeable it was. But i wanted MORE.
i eventually started tweaking the shader, adding settings, breaking stuff, and after a while wanted to impose my own visual style onto the shader.
i wanted to emphasize a varying scene, where the lighting isn't always the same whenever or wherever you are.

### SPECIAL THANKS:
+ Chocapic13, for the base shader
+ WoMspace, for spending alot of time creating a DOF overhaul
+ Null, for doing a huge amount of work creating the voxel floodfill colored lighting
+ Emin, and Gri573, for teaching me how to stop alot of light leaking
+ RRe36 and Sixthsurge, for the great ideas to steal
### [Come join my discord server!](https://discord.gg/8nVt56H9zH)
### [Want to support me? Consider donating](https://ko-fi.com/xonkdev)
# RELEASE VERSIONS, STABLE VERSIONS, AND UNSTABLE VERSIONS
`Release versions` are uploaded when the stable version is... stable enough, and has enough changes to warrant a release. These are the versions uploaded to Modrinth or Curseforge. The release versions are not the very latest version.

`Stable versions` are not the absolute newest versions, but they are more stable, and are released regularly to be tested by anyone. **Please report any issues you find.**

`Unstable versions` are the ABSOLUTE latest versions, and are released very frequently and are likely to have bugs and issues or missing features. When this branch reaches a stable enough state, it is merged into the Stable branch. **Please report any issues you find.**
## How to download the `stable` version:
 - locate the `green "code" button` on this page. this button is NOT in the `releases` page.
 - click the `green "code" button` and select `"download zip"`.
 - once the zip file finishes downloading, install it like a normal shader. you do NOT need to unzip/extract/decompress.
## How to download the `unstable` version:
 - locate the `"branch switcher"` drop-down menu on the top-left area of this page.
 - select the `"Unstable"` branch. <img width="917" height="326" alt="image" src="https://github.com/user-attachments/assets/9dc00c07-9fcd-4934-b069-cbe5ac224c78" />
 - after doing the above, locate the `green "code" button` on this page. this button is NOT in the `releases` page.
 - click the `green "code" button` and select `"download zip"`.
 - once the zip file finishes downloading, install it like a normal shader. you do NOT need to unzip/extract/decompress.
## How to download the `release` version:
 - locate the `"Releases"` tab on the right side of this page.
 - find the release version you want to download. locate the files attactched to it, and download the file named similar to `"Bliss_(version)_chocapic13_shaders_edit.zip"`
 - once the zip file finishes downloading, install it like a normal shader. you do NOT need to unzip/extract/decompress.

## Advanced Materials (BSL-style SEUS/Old PBR & labPBR emission for entities)
This fork adds two settings, just like in BSL shaders, under
**Shader Options -> Resource Pack Support -> Materials / Advanced Materials**:

- **Advanced Materials** (on/off) - enables reading `"_s"` specular textures on entities
  (player skins, mobs, armor) and on the first-person hand.
- **Material Format** (`labPBR 1.3` / `SEUS/Old PBR`, default = `SEUS/Old PBR`):
  - `SEUS/Old PBR` - the **blue channel** of the `"_s"` texture is emission. Alpha is ignored.
  - `labPBR 1.3` - the blue channel is emission too, but it is disabled for hard-coded
    (HCM) metals that use an alpha of 230 or higher.

Example use: put a skin texture called `Electro` and an `Electro_s` texture in the same
folder of your resource pack, paint the parts that should glow **blue** on the `_s` image,
and those parts of the character will glow. The `_s` texture must actually be loaded by the
game (OptiFine/CEM, or Iris together with a mod such as ETF/EMF), exactly like in BSL.
Glow strength and curve can be tuned in **Resource Pack Support -> Emissives**
(`Emission Multiplier` / `Emission Curve`).
