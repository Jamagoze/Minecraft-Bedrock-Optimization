# Contributing to Minecraft-Bedrock-Optimization

Thanks for helping improve Bedrock performance without hurting visuals!

## Reporting issues

Please include:
- Device model, SoC/GPU, RAM, and Android version
- Minecraft Bedrock version (e.g. 1.26.51)
- Which pack(s) you used: resource pack, behavior pack, or both
- What happened vs. what you expected
- FPS before and after, if you measured it
- Screenshots of any visual problems

## Suggesting changes

1. Fork the repo and create a branch from `main`
2. Make your change and test it in-game on a real device
3. Open a pull request describing what changed and why

## Testing checklist

- Pack imports without errors and shows up in Settings → Storage / Global Resources
- `manifest.json` version info matches the targeted game version
- World loads and plays normally with the pack enabled
- Note FPS or load-time differences on low-RAM devices (3–4GB)
- No visual regressions (lighting, textures, UI)

## Guidelines

- Keep pull requests small and focused on one change
- Don't upload Mojang/Microsoft assets (vanilla textures, game files); only your own modified or original content
- Be respectful and constructive

## License

By contributing, you agree your contributions are licensed under the same license as this project.
