# Maintaining versioned manuals

- Root locale pages and `/versions/4.1.0/<locale>.html` include the same source
  from `_includes/manuals/4.1.0/`. Edit that source once for the current guide.
- Each manual references its version-local screenshots. Never overwrite images
  inside an archived version when preparing a later release.
- `versions/4.0.0/` preserves the five released locale sources and their 46
  referenced screenshots byte-for-byte from commit `45d90b7`. Its page version
  comes from `_config.yml` defaults, so the original front matter stays intact.
- `_data/guide_versions.yml` controls selection order, the current prepared
  guide, and release/preview labels. `_data/guide_ui.json` localizes the UI.
- Current preparation: 4.1.0 is a **preview** on `dev/main` only; production
  `origin/main` stays at `45d90b7` (4.0.0). Do not push to origin before release.
- At the actual 4.1.0 release, mark its status `released`, set `released` to
  `4.1.0`, verify on dev, then publish to origin when authorized. Existing
  Support URLs remain unchanged and serve 4.1.0; both versioned URLs remain.
- For the next guide version, add its include sources, wrapper pages and
  version-local images, point root wrappers at it, and add its version entry.
  Retain the previous version's source and assets. Bug-fix-only releases with
  unchanged usage do not require a separate manual.
- Verify all five languages on root and versioned URLs, version/language links,
  images, section anchors, search, mobile contents, light and dark appearance.
  The existing `privacy-policy.html` remains the current policy for all versions.
