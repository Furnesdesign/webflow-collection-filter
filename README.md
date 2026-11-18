# Webflow Collection Filter

Live search and multi-dropdown filtering for Webflow Collection Lists.

## Install

Paste into **Site settings → Custom code → Footer code** (or a page's *Before `</body>` tag*):

```html
<script src="https://cdn.jsdelivr.net/gh/Furnesdesign/webflow-collection-filter@1/collection-filter.min.js"></script>
```

## Versions

Releases are git tags using semantic versioning (`v1.0.0`, `v1.0.1`, `v1.1.0`, `v2.0.0` …).

| Link | Gets |
| --- | --- |
| `@1` | Newest 1.x.x — bug fixes and new features, never breaking changes. **Use this on sites.** |
| `@1.0.0` | Exactly that version, never changes. |
| `@main` | Latest commit. For testing only – never on live sites. |

- **Patch** (`1.0.1`): bug fix. **Minor** (`1.1.0`): new optional feature. Both reach every `@1` site automatically.
- **Major** (`2.0.0`): renamed attributes or changed behaviour. Sites stay on `@1` until you change their link.
- jsDelivr caches `@1` for a while. To roll out a release right away, open
  `https://purge.jsdelivr.net/gh/Furnesdesign/webflow-collection-filter@1/collection-filter.min.js` (and `collection-filter.js`).

### Releasing a new version

1. Update the version in the header comment of `collection-filter.js`.
2. Commit and push.
3. Tag and push the tag:
   ```
   git tag v1.0.1
   git push origin v1.0.1
   ```

## Attributes

| Element | Attribute |
| --- | --- |
| Collection List | `data-filter="list"` |
| Collection Items | `data-filter="item"` |
| Result count (optional) | `data-filter="count"` |
| Live search input | `data-filter-live-search="*"` |
| Searchable text inside items | `data-filter-source="live-search"` |
| Tags inside items | `data-filter-source-tag="{{slug}}"` |

### Dropdowns

| Element | Attribute |
| --- | --- |
| Wrapper | `data-filter-dropdown="wrapper"` |
| Toggle button | `data-filter-dropdown="button"` |
| Toggle label | `data-filter-dropdown="toggle-label"` |
| Toggle tag (default `display: none`) | `data-filter-dropdown="toggle-tag"` |
| Toggle tag label | `data-filter-dropdown="toggle-tag-label"` |
| Toggle tag close | `data-filter-dropdown="toggle-tag-close"` |
| Dropdown list | `data-filter-dropdown="list"` |
| Tag items | `data-filter-dropdown-tag="{{slug}}"` |
| Check icon | `data-filter-dropdown="icon-checked"` |
| Uncheck icon | `data-filter-dropdown="icon-unchecked"` |
| Tag label | `data-filter-dropdown="label"` |
