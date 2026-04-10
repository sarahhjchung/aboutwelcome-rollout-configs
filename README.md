# about:welcome Rollout Configs

Source of truth for `about:welcome` rollout configurations used in Experimenter.

## Purpose

This repository maintains version controlled JSON configurations for `about:welcome` rollouts. It provides:

- **Version history** - Track what changed and when with git history
- **Single source of truth** - Reference for active rollout configurations
- **Easy rollout creation** - Copy/paste configs when creating new `about:welcome` Experimenter rollouts

## Repository Structure

```
aboutwelcome-rollout-configs/
├── README.md
├── current-rollout.json
├── rollout.py
└── archive/  # Historical configs by rollout ID
```

## How to Update

1. Replace `current-rollout.json` with the new rollout JSON from Experimenter
2. Run the script:
   ```bash
   ./rollout.py
   ```
   The script will validate the rollout ID, log any screen ID changes, and archive the previous config, and optionally commit and push.

## Related Resources

- [about:welcome in-tree defaults](https://searchfox.org/firefox-main/source/browser/components/aboutwelcome/modules/AboutWelcomeDefaults.sys.mjs)
- [about:welcome Source Docs](https://firefox-source-docs.mozilla.org/browser/components/asrouter/docs/about-welcome.html)
