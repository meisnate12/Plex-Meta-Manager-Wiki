Configuring Radarr is optional but will allow you to send movies to a Radarr instance when they're found missing while updating a library's collections. 

A `radarr` mapping can be either in the root of the config file as global mapping for all libraries or you can specify the `radarr` mapping individually per library.

Below is a `radarr` mapping example and the full set of attributes:
```yaml
radarr:
  url: http://192.168.1.12:32788
  token: ################################
  version: v3
  quality_profile: HD-1080p
  root_folder_path: S:/Movies
  add: true
  search: false
  tag: pmm
```

| Name | Attribute | Allowed Values| Default | Required |
| :-- | :-- | :-- | :--: | :--: |
| Radarr URL | `url` | Radarr URL<br><strong>Example:</strong> http://192.168.1.12:32788 | N/A | :heavy_check_mark: |
| API Token | `token` | Radarr API Token | N/A | :heavy_check_mark: |
| Radarr Version | `version` | `v2`: for < 0.2<br>`v3`: for > 3.0 | v2 | :x: |
| Root Folder Path | `root_folder_path` | Radarr Root Folder Path To Use | N/A | :heavy_check_mark: |
| Quality Profile | `quality_profile` | Quality Profile To Use | N/A | :heavy_check_mark: |
| Add | `add` | Add missing moives found to Radarr<br><strong>boolean:</strong> true or false | false | :x: |
| Search | `search` | Search when adding missing movies to Radarr<br><strong>boolean:</strong> true or false | false | :x: |
| Tag | `tag` | Add this list or comma-separated string of tags to every movie added to Radarr | ` ` | :x: |

* The `token` can be found by going to `Radarr > Settings > General > Security > API Key`

* The `quality_profile` must be the exact name of the desired quality profile, including all spaces and capitalizations.
