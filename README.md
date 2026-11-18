# KimiLM engines

Programs that KimiLM (a desktop app for AI agents that run on your own computer) downloads after it is installed,
built here from pinned upstream sources. This repository is public so that every installed copy of KimiLM can
fetch them.

## Music engine

KimiLM makes music on the user's computer with ACE-Step 1.5 through
[acestep.cpp](https://github.com/ace-step/acestep.cpp) (MIT licence). Its authors publish no ready-made programs,
so the workflow **Build music engine** builds `ace-lm` and `ace-synth` for Windows from the commit in `pins.json`
and publishes them as a release of this repository (`acestep-windows-x64.zip`).

- `pins.json` holds the upstream repository, the commit and the release tag. Keep it equal to `acestep_repo`,
  `acestep_commit` and `music_engine_tag` in KimiLM's `engine/dva/versions.json`.
- Run it once per pin: **Actions → Build music engine → Run workflow** (tick the box to also build for graphics
  cards).
- KimiLM then installs it from Sound → Voices & models → Music on this computer → Install.

Nothing here is an app release.
