# ovf-updates

Distribution-only mirror for the **OVF Server Explorer** KNIME plugin.

This repository contains **only** the pre-built binaries and the GitHub
Pages workflow that publishes them. Source code is not included.

## Install

Point KNIME at the update site URL for your version. Detailed steps
live at:

**<https://shinwachi.github.io/ovf-updates/>**

Short version:

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

To publish a new release, drop the four new zip files into `dist/`,
commit, push. The `publish-pages` workflow rebuilds the site tree and
redeploys — usually within a minute.
