# Security and File Verification

HO PC Launcher is currently distributed as a Windows installer because the app includes several required DLL files and needs a normal install/uninstall process.

The app is currently closed-source, and the Windows binaries are not code-signed yet.

## Privacy

HO PC Launcher stores its settings locally under:

`%LocalAppData%\HO_PCLauncher`

There is no cloud sync or external upload.

## SHA256 Checksums

You can verify the downloaded installer with PowerShell:

```powershell
Get-FileHash .\HO_PCLauncher_Setup_v1_0_3.exe -Algorithm SHA256
```

| File                             | SHA256                                                             |
| -------------------------------- | ------------------------------------------------------------------ |
| `HO_PCLauncher_Setup_v1_0_3.exe` | `292248ea878f5c346b047fb6d350a802b32f21d62dffd88154cc1bb16f22853c` |
| `HO_PCLauncher.exe`              | `b041b5288a887153369d7c35ffbaf0de2b7f4b03fe0a7ab251be951809cf8fa0` |

## VirusTotal Reports

For transparency, VirusTotal reports are provided for both the installer and the standalone executable.

| File                             | Result at time of checking | VirusTotal                                                                                                                          |
| -------------------------------- | -------------------------: | ----------------------------------------------------------------------------------------------------------------------------------- |
| `HO_PCLauncher_Setup_v1_0_3.exe` |                     `7/71` | [VirusTotal report](https://www.virustotal.com/gui/file/292248ea878f5c346b047fb6d350a802b32f21d62dffd88154cc1bb16f22853c/detection) |
| `HO_PCLauncher.exe`              |                     `3/58` | [VirusTotal report](https://www.virustotal.com/gui/file/b041b5288a887153369d7c35ffbaf0de2b7f4b03fe0a7ab251be951809cf8fa0/detection) |

Some antivirus engines may show generic / heuristic / machine-learning detections for unsigned Windows installers or low-reputation binaries.

The flagged files will be submitted to relevant vendors for false-positive review.
