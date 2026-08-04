# LightFogURP documentation

LightFogURP renders lightweight volumetric fog in the Universal Render Pipeline through a renderer feature and a Volume override.

## Setup

1. Select the active URP Renderer asset.
2. Add the `Volumetric Fog` renderer feature.
3. Create or select a Global Volume in the scene.
4. Add the volumetric fog override to its Volume Profile.
5. Enable the override and tune the fog values for the scene.

The renderer feature requests the depth input used by the fog pass. If the result is missing or incomplete, confirm that the active URP asset and renderer allow a depth texture.

## Samples

The package includes:

- **2D Sample** for layered or side-view scenes.
- **3D Sample** for perspective scenes.
- **Utilities Sample** with supporting prefabs and assets.

Import samples from the package details panel in the Unity Package Manager.

## Rendering notes

- The effect is designed for URP and does not support the Built-in Render Pipeline or HDRP.
- Fog is controlled through the Volume system, so local and global Volume blending can be used normally.
- Camera type and post-processing settings can affect whether the pass is enqueued.
- Keep the fog cost appropriate for the target platform and render scale.

## Troubleshooting

### Fog does not render

- Confirm that the renderer feature is added to the renderer used by the camera.
- Confirm that the Volume affects the camera and the override is enabled.
- Check that post-processing is enabled for the camera and renderer configuration.
- Check depth texture support in the active URP asset.

### Fog is visible in one camera only

Verify that every camera uses a renderer containing the feature and is affected by the intended Volume layer mask.

### Materials or shaders are missing

Reimport the package and confirm the hidden fog shaders are included. Avoid renaming package shader assets without updating the renderer feature.

## Package requirements

- Unity 2021.3 or newer.
- Universal Render Pipeline 12.1.16 or a compatible version supplied by the Editor.