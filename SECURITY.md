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

VirusTotal results can change over time as vendors update their detections and the set of participating engines changes.

Last checked: June 13, 2026

| File                             | Result at time of checking | VirusTotal                                                                                                                          |
| -------------------------------- | -------------------------: | ----------------------------------------------------------------------------------------------------------------------------------- |
| `HO_PCLauncher_Setup_v1_0_3.exe` |                     `5/69` | [VirusTotal report](https://www.virustotal.com/gui/file/292248ea878f5c346b047fb6d350a802b32f21d62dffd88154cc1bb16f22853c/detection) |
| `HO_PCLauncher.exe`              |                     `3/58` | [VirusTotal report](https://www.virustotal.com/gui/file/b041b5288a887153369d7c35ffbaf0de2b7f4b03fe0a7ab251be951809cf8fa0/detection) |

Based on the current Microsoft review status, VirusTotal results, and the nature of the remaining detections, there is currently no evidence that these files are malicious.

The remaining detections are from a small number of engines and appear to be generic, heuristic, or machine-learning based detections. These results should be interpreted with caution and are not sufficient on their own to establish that the files are malware.

Most major antivirus engines currently report the files as undetected.

## False-Positive Review Status

The following files were submitted to Microsoft Security Intelligence for false-positive review on June 11, 2026.

As of June 13, 2026, Microsoft reports no positive detection from its scanners for `HO_PCLauncher.exe`. Microsoft also noted that it has no telemetry indicators for the submitted file. The final determination is still pending.

| File                             | SHA256                                                             | Status                                                                                |
| -------------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| `HO_PCLauncher_Setup_v1_0_3.exe` | `292248ea878f5c346b047fb6d350a802b32f21d62dffd88154cc1bb16f22853c` | Submitted to Microsoft, in progress                                                   |
| `HO_PCLauncher.exe`              | `b041b5288a887153369d7c35ffbaf0de2b7f4b03fe0a7ab251be951809cf8fa0` | Microsoft reports no positive detection; final determination pending                  |

I will update this page when Microsoft completes the review.
