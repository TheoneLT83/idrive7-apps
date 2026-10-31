# Waze on cluster

The CarPlay map (Waze, Apple Maps or Google Maps) on the instrument cluster of an iDrive 7
car, by Robert Nisipeanu, from
[robertnisipeanu/idrive-apps](https://github.com/robertnisipeanu/idrive-apps) at
`0fa0cd23b22064cc44e6075658aea8f8d3c78203`. Install **Waze on cluster** from the Store: it
installs the Waze tool and the cluster renderer first.

**For now the map is stable only with the cluster display's assisted driving view set to
"Deactivated"** (the car's cluster display settings). The app says so in the first row of its page.

| Folder | |
|---|---|
| `robertn_waze_cluster/` | the iDrive app (Enable map, Disable map, status, the tools' log), a source package the head unit builds; 0.3.1 adds the note above |
| `cluster-render/` | the cluster renderer 0.1.0, as published there (`cluster-render@0.1.0.tgz`, sha256 `16961ee7…`) |
| `waze-on-cluster/` | the Waze tool 0.5.0, as published there (`waze-on-cluster@0.5.0.tgz`, sha256 `49e19742…`) |
| `source/` | the two tools' source at that commit (`make target` builds them in Docker) |

The tools need the Store's deploy tool 0.7.0 or newer (the Waze tool's activate and
deactivate hooks), which the Store installs first.

GPL-3.0-or-later (`LICENSE`); cluster-render's client parts are MPL-2.0
(`cluster-render/LICENSES`). Details in `source/*/README.md`.
