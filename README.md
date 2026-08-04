<div align="center">

# LightFogURP

Lightweight volumetric fog for the Universal Render Pipeline.

[![Release](https://img.shields.io/github/v/release/Natteens/com.natteens.lightfogurp?style=flat-square)](https://github.com/Natteens/com.natteens.lightfogurp/releases)
[![Unity](https://img.shields.io/badge/Unity-2021.3%2B-000000?style=flat-square&logo=unity)](https://unity.com)
[![URP](https://img.shields.io/badge/URP-12.1.16%2B-555555?style=flat-square)](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@12.1/manual/index.html)
[![License](https://img.shields.io/github/license/Natteens/com.natteens.lightfogurp?style=flat-square)](LICENSE.md)

</div>

LightFogURP adds configurable volumetric fog through a URP renderer feature and the Unity Volume system. It is intended as a small, direct effect rather than a complete atmospheric simulation.

## Features

- Renderer Feature integration for URP.
- Volume-based fog controls.
- Separate 2D and 3D samples.
- No runtime setup framework required.

## Installation

Add the package through `Window > Package Manager > Add package from git URL`:

```text
https://github.com/Natteens/com.natteens.lightfogurp.git
```

Or add it to `Packages/manifest.json`:

```json
{
  "dependencies": {
    "com.natteens.lightfogurp": "https://github.com/Natteens/com.natteens.lightfogurp.git"
  }
}
```

The URP dependency is declared by the package.

## Quick start

1. Add the `Volumetric Fog` feature to the active URP Renderer.
2. Create a Global Volume.
3. Add the volumetric fog override to its profile.
4. Enable the override and adjust the fog settings.

Samples can be imported from the Package Manager.

## Documentation

Setup details and troubleshooting are available in [Documentation](Documentation~/index.md).

## License

MIT. See [LICENSE.md](LICENSE.md).