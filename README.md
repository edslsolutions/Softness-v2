# MacType Profile: Softness v2

A font rendering profile for **MacType**, designed to deliver maximum visual smoothness, eliminate the harsh jaggedness typical of standard ClearType, and ensure comfortable extended reading on Windows.

---

## 📋 Key Features

* **Balanced Smoothness:** Gradual, soft glyph contours without compromising clarity or legibility.
* **Subtle Depth with Shadow:** Discreet drop-shadow effect providing gentle contrast against light and translucent backgrounds.
* **Typographic Fidelity:** Preserves the native font weights and geometry (`NormalWeight=0`, `BoldWeight=0`, `ItalicSlant=0`), avoiding artificial font thickening.
* **Generous Cache:** Increased memory allocation for font tables and glyph bitmaps, preventing stutter and visual glitches during multi-window navigation.
* **Stability & Isolation:** Incorporates recommended application exclusions (Chromium/DirectWrite apps) and system safeguards (`dwm.exe`, `explorer.exe`).

---

## 🔍 Parameter Breakdown

| Category | Key Parameters | Configured Behavior |
| :--- | :--- | :--- |
| **Rendering** | `HintingMode (3)`, `AntiAliasMode (-1)` | Full hinting and default FreeType antialiasing |
| **Weight & Geometry** | `NormalWeight (0)`, `BoldWeight (0)`, `ItalicSlant (0)` | Native font weight and slant preserved |
| **Gamma & Contrast** | `GammaMode (0)`, `GammaValue (0.1)`, `Contrast (1.0)` | Subtle tonal curve with neutral contrast |
| **Subpixel Filtering** | `LcdFilter (1)`, `TextTuning (20)` | Minimized color fringing with edge clarity enhancement |
| **Visual Effects** | `Shadow (5,5,90,...)` | Subtle shadow with 5px offset and 90% transparency |
| **Graphics Engine** | `DirectWrite (0)` | DirectWrite hooking disabled for optimal stability |
| **Memory Management** | `CacheMaxFaces (256)`, `CacheMaxSizes (~12 MB)`, `CacheMaxBytes (~11.5 MB)` | High glyph capacity retained in memory |
| **Compatibility** | `[UnloadDll]`, `[exclude]` | Windows desktop protection and bypass for modern browsers/Electron apps |

---

## 🚀 Installation & Setup

1. Copy the `Softness v2.ini` file into your MacType configuration directory:
   * Typically: `C:\Program Files\MacType\ini` (or `C:\Program Files (x86)\MacType\ini`).
2. Launch the **MacType Wizard**.
3. Select your preferred loading method (**Service Mode** or **Registry Mode** recommended).
4. Choose the **Softness v2** profile from the list.
5. Click **Finish** / **Apply**.
6. Sign out and back into Windows (or restart your computer) to apply the changes across all supported processes.

---

## 💡 Fine-Tuning Tips

* **High-DPI / 2K / 4K Displays:**  
  If display scaling is set above 100% and text appears too thick or bold, reduce `RenderWeight` from `10.0` down to `2.0` – `5.0`.
* **Flat Look (Disable Shadow):**  
  If you prefer a completely flat rendering style without depth, set `Shadow=0,0,0,0x0,0,0x0`.
