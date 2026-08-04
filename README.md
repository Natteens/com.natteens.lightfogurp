<div align="center">

# LightFogURP

**Give a URP scene depth and atmosphere without installing an entire weather system.**

A focused volumetric fog effect built around a Renderer Feature and the Unity Volume workflow.

[![Release](https://img.shields.io/github/v/release/Natteens/com.natteens.lightfogurp?sort=semver&label=release&style=flat-square)](https://github.com/Natteens/com.natteens.lightfogurp/releases)
[![Unity](https://img.shields.io/badge/Unity-2021.3%2B-000000?style=flat-square&logo=unity)](https://unity.com)
[![URP](https://img.shields.io/badge/URP-12.1.16%2B-555555?style=flat-square)](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@12.1/manual/index.html)
[![License](https://img.shields.io/github/license/Natteens/com.natteens.lightfogurp?style=flat-square)](./LICENSE.md)

[Overview](#a-small-effect-with-a-clear-job) · [Installation](#installation) · [Setup](#quick-setup) · [Documentation](#documentation)

</div>

---

## A Small Effect With a Clear Job

LightFogURP adds volumetric fog to the normal URP rendering path. It does not replace the lighting
pipeline or introduce a separate environment framework: add the feature, place a Volume and tune the
look from the same tools already used by URP projects.

That narrow scope makes it suitable for scenes that need visible light volume, distance separation
or a denser atmosphere without taking on the configuration surface of a full sky and weather stack.

<table>
<tr>
<td width="50%"><strong>URP-native setup</strong><br><sub>The effect enters the renderer through a standard Scriptable Renderer Feature.</sub></td>
<td width="50%"><strong>Volume controls</strong><br><sub>Fog settings live in a Volume override and can participate in the usual profile workflow.</sub></td>
</tr>
<tr>
<td width="50%"><strong>2D and 3D examples</strong><br><sub>Import the samples that match the project instead of reverse-engineering a finished scene.</sub></td>
<td width="50%"><strong>No runtime framework</strong><br><sub>There is no manager, service locator or required bootstrap beyond URP configuration.</sub></td>
</tr>
</table>

## Installation

Requires Unity **2021.3** or newer with URP. The compatible URP dependency is declared by the
package.

In the Package Manager, choose **Add package from git URL** and paste:

```text
https://github.com/Natteens/com.natteens.lightfogurp.git
```

Or declare it in `Packages/manifest.json`:

```json
{
  "dependencies": {
    "com.natteens.lightfogurp": "https://github.com/Natteens/com.natteens.lightfogurp.git"
  }
}
```

Pin a release tag for stable project installs.

## Quick Setup

1. Open the active URP Renderer asset.
2. Add the **Volumetric Fog** Renderer Feature.
3. Create a Global Volume or reuse an existing one.
4. Add the volumetric fog override to its profile.
5. Enable the properties you want to control and shape the effect for the scene.

The **2D**, **3D** and **Utilities** samples are available from the Package Manager.

## Documentation

Detailed renderer setup, Volume controls, sample notes and troubleshooting are kept in
[Documentation](./Documentation~/index.md). The main README stays intentionally focused on the
package and the shortest path to seeing it work.

See the [changelog](./CHANGELOG.md) for release history.

## License

MIT. See [LICENSE.md](./LICENSE.md).
