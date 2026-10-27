# Maintaining versioned manuals

- Root locale pages and `/versions/4.1.0/<locale>.html` include the same source
  from `_includes/manuals/4.1.0/`. Edit that source once for the current guide.
- Each manual references its version-local screenshots. Never overwrite images
  inside an archived version when preparing a later release.
- `versions/4.0.0/` preserves the five released locale sources and their 46
  referenced screenshots byte-for-byte from commit `45d90b7`. Its page version
  comes from `_config.yml` defaults, so the original front matter stays intact.
- `_data/guide_versions.yml` controls selection order and the current guide.
  `_data/guide_ui.json` localizes the current/past version labels.
- Dev shows the final publication display: the current guide is labeled
  “Published” and older guides “Previous version”. There is no preview status
  or preview notice; publication timing is controlled by which remote is used.
- Current preparation: 4.1.0 is on `dev/main` only; production `origin/main`
  stays at `45d90b7` (4.0.0). Do not push to origin before release.
- At the actual 4.1.0 release, publish the verified dev guide to origin when
  authorized, without a separate label/status change. Existing Support URLs
  remain unchanged and serve 4.1.0; both versioned URLs remain available.
- For the next guide version, add its include sources, wrapper pages and
  version-local images, point root wrappers at it, and add its version entry.
  Retain the previous version's source and assets. Bug-fix-only releases with
  unchanged usage do not require a separate manual.
- Verify all five languages on root and versioned URLs, version/language links,
  images, section anchors, search, mobile contents, light and dark appearance.
  The existing `privacy-policy.html` remains the current policy for all versions.
