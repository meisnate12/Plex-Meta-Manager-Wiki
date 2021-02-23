Configuring Sonarr is optional but will allow you to send shows to a Sonarr instance when they're found missing while updating a library's collections.

A `sonarr` mapping can be either in the root of the config file as global mapping for all libraries or you can specify the `sonarr` mapping individually per library.

Below is a `sonarr` mapping example and the full set of attributes:
```YAML
sonarr:
  url: http://192.168.1.12:32789
  token: ################################
  version: v3
  quality_profile: HD-1080p
  root_folder_path: S:/Shows
  add: true
  search: false
  tag: pmm
```

| Name | Attribute | Allowed Values| Default | Required |
| :-- | :-- | :-- | :--: | :--: |
| Sonarr URL | `url` | Sonarr URL<br><strong>Example:</strong> http://192.168.1.12:32788 | N/A | :heavy_check_mark: |
| API Token | `token` | Sonarr API Token | N/A | :heavy_check_mark: |
| Sonarr Version | `version` | `v2`: for < 0.2<br>`v3`: for > 3.0 | v2 | :x: |
| Root Folder Path | `root_folder_path` | Sonarr Root Folder Path To Use | N/A | :heavy_check_mark: |
| Quality Profile | `quality_profile` | Quality Profile To Use | N/A | :heavy_check_mark: |
| Add | `add` | Add missing shows found to Sonarr<br><strong>boolean:</strong> true or false | false | :x: |
| Search | `search` | Search when adding missing shows to Sonarr<br><strong>boolean:</strong> true or false | false | :x: |
| Tag | `tag` | Add this list or comma-separated string of tags to every show added to Sonarr | ` ` | :x: |

* The `token` can be found by going to `Sonarr > Settings > General > Security > API Key`

* The `quality_profile` must be the exact name of the desired quality profile, including all spaces and capitalizations.
