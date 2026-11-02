# ovf-updates

Distribution-only mirror for the **OVF Server Explorer** KNIME plugin.

This repository contains **only** the pre-built binaries and the GitHub
Pages workflow that publishes them. Source code is not included.

## Install

Point KNIME at the update site URL for your version. Detailed steps
live at:

**<https://shinwachi.github.io/ovf-updates/>**

Step-by-step guide with diagrams, for Windows, Linux and macOS:
**<https://shinwachi.github.io/ovf-updates/install.html>**

Short version, using KNIME's own wizard:

| KNIME | Update-site URL                                     |
| ----- | --------------------------------------------------- |
| 5.x   | `https://shinwachi.github.io/ovf-updates/5x/`       |
| 4.1.x | `https://shinwachi.github.io/ovf-updates/4.1.x/`    |

Add via *File > Install KNIME Extensions... > Add > Location*.

## Release process

The binaries live under `dist/`:

| Purpose                     | File                                          |
| --------------------------- | --------------------------------------------- |
| p2 update-site archive 5.x  | `ovf-serverconnector-5.x-<ver>-updatesite.zip`   |
| p2 update-site archive 4.1.x| `ovf-serverconnector-4.1.x-<ver>-updatesite.zip` |
| Dropin bundle 5.x           | `ovf-serverconnector-5.x-<ver>.zip`              |
| Dropin bundle 4.1.x         | `ovf-serverconnector-4.1.x-<ver>.zip`            |
| Installer 5.x               | `ovf-serverconnector-5.x-<ver>-installer.zip`    |
| Installer 4.1.x             | `ovf-serverconnector-4.1.x-<ver>-installer.zip`  |

To publish a new release, drop the six new zip files into `dist/`,
commit, push. The `publish-pages` workflow rebuilds the site tree and
redeploys — usually within a minute.
