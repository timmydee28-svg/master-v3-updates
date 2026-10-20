# master_v3 framework updates

This repository holds **release packages only**. It has no source code.

Each release (tag `vX.Y.Z`) has these files attached:

| File | What it is |
|---|---|
| `manifest.json` | List of files and their hashes, plus release notes |
| `manifest.sig` | RSA signature over the manifest |
| `framework-X.Y.Z.zip.enc` | The framework code, encrypted with AES-256-GCM |
| `framework-X.Y.Z-offline.zip` | The three files above in one file, for servers with no internet |

The packages are encrypted. Only installed systems hold the key that opens them,
so downloading them from here gives you nothing readable. Installed systems also
refuse any release that the framework's release key did not sign.

## Updating a system

Go to **Admin → Framework Updates**. With **Where updates come from** set to
*Automatic* or *GitHub*, the system finds new releases here by itself. No dev
portal or access token is needed.

For a server with no internet, download `framework-X.Y.Z-offline.zip` from the
release page and drop it on **Install from a file**.
