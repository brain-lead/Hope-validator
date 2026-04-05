# 📡 Hope Phone Intelligence v1.0

**Advanced Phone Number Intelligence Suite — Carrier Detection, Line Type Classification, Location Mapping & Smart Number Generation**

Developed by **Brain Lead** — [@brain_lead](https://t.me/brain_lead)

---

> ⚠️ **THIS IS PROPRIETARY, CLOSED-SOURCE SOFTWARE.**
> Unauthorized copying, distribution, modification, reverse engineering, decompilation, or disassembly of this software is strictly prohibited. All rights reserved.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Supported Countries](#-supported-countries)
- [Tabs & Modules](#-tabs--modules)
  - [Carrier Lookup](#-carrier-lookup)
  - [Line Type Checker](#-line-type-checker)
  - [Location Lookup](#-location-lookup)
  - [Combined Lookup](#-combined-lookup)
  - [Number Generator](#-number-generator)
- [Output Formats](#-output-formats)
- [Filtering & Export](#-filtering--export)
- [Auto-Save System](#-auto-save-system)
- [Licensing](#-licensing)
- [System Requirements](#-system-requirements)
- [Installation](#-installation)
- [Getting Started](#-getting-started)
- [FAQ](#-faq)
- [Disclaimer](#%EF%B8%8F-disclaimer)
- [Contact & Support](#-contact--support)

---

## 🔍 Overview

Hope Phone Intelligence is a desktop application that provides real-time phone number intelligence. It identifies the **carrier/operator**, **line type** (Mobile, Landline, VoIP), and **geographic location** for phone numbers across 60+ countries.

For the United States, Canada, and the United Kingdom, the application uses a high-performance **offline database** containing 370,000+ prefix records for instant lookups with no API dependency. For all other supported countries, lookups are performed via the integrated `phonenumbers` library.

The built-in **Number Generator** can produce bulk phone numbers filtered by area code, carrier, state, and line type — ideal for telecommunications research, data validation, and number plan analysis.

---

## ✨ Features

### Core Intelligence
- **Carrier Detection** — Identify the telecom operator for any phone number (Verizon, AT&T, T-Mobile, Vodafone, EE, etc.)
- **Line Type Classification** — Determine if a number is Mobile, Landline, VoIP, or Unknown
- **Location Mapping** — Resolve numbers to city and state/province (US/Canada) or country-level location
- **Combined Analysis** — Run all three lookups simultaneously with multi-dimensional filtering

### Number Generation
- **Manual Mode** — Generate numbers by area code, prefix, and count for any country
- **Smart Gen Mode** — Generate numbers filtered by specific carrier, state/region, and line type (US/Canada/UK)
- **Line Type Filtering** — Include or exclude Mobile, Landline, VoIP, and Unknown types during generation

### Data & Performance
- **Offline Database** — 200,000+ US, 44,000+ Canada, and 126,000+ UK prefix records
- **Bulk Processing** — Handle hundreds of thousands of numbers per session
- **Progress Tracking** — Real-time progress bar and statistics during processing
- **Carrier Normalization** — Automatically groups subsidiaries under parent carriers (e.g., Cellco Partnership → Verizon, New Cingular → AT&T, Omnipoint → T-Mobile)

### Export & Save
- **Cross-Tab Export** — Send filtered results from any tab to any other tab for further analysis
- **Auto-Save** — Automatically saves results organized by carrier, line type, or location
- **Manual Save** — Save all results or only filtered/visible rows
- **Multiple Formats** — Save as plain text (numbers only) or CSV with full details

### Interface
- **Dark Theme UI** — Professional dark interface optimized for extended use
- **Color-Coded Results** — Green (Mobile), Yellow (Landline), Purple (VoIP), Red (Not Found)
- **Responsive Layout** — Resizable window with minimum 800×600, scales to any screen size
- **Country Selector** — Searchable dropdown with 60+ countries, dynamically updates all tabs

---

## 🌍 Supported Countries

### Full Offline Database (Instant Lookups)
| Country | Prefix Records | Data Includes |
|---------|---------------|---------------|
| 🇺🇸 United States | 200,000+ | Carrier, Line Type, City, State |
| 🇨🇦 Canada | 44,000+ | Carrier, Exchange Area, Province |
| 🇬🇧 United Kingdom | 126,000+ | Carrier, Line Type |

### Phonenumbers Library (60+ Countries)
Carrier detection, line type, and location via the `phonenumbers` library for:

🇦🇺 Australia · 🇩🇪 Germany · 🇫🇷 France · 🇮🇹 Italy · 🇪🇸 Spain · 🇳🇱 Netherlands · 🇧🇪 Belgium · 🇨🇭 Switzerland · 🇦🇹 Austria · 🇸🇪 Sweden · 🇳🇴 Norway · 🇩🇰 Denmark · 🇫🇮 Finland · 🇵🇱 Poland · 🇨🇿 Czech Republic · 🇮🇪 Ireland · 🇵🇹 Portugal · 🇬🇷 Greece · 🇭🇺 Hungary · 🇷🇴 Romania · 🇧🇬 Bulgaria · 🇭🇷 Croatia · 🇷🇸 Serbia · 🇮🇳 India · 🇵🇰 Pakistan · 🇧🇩 Bangladesh · 🇱🇰 Sri Lanka · 🇳🇵 Nepal · 🇦🇫 Afghanistan · 🇨🇳 China · 🇯🇵 Japan · 🇰🇷 South Korea · 🇹🇼 Taiwan · 🇭🇰 Hong Kong · 🇸🇬 Singapore · 🇲🇾 Malaysia · 🇮🇩 Indonesia · 🇹🇭 Thailand · 🇻🇳 Vietnam · 🇵🇭 Philippines · 🇧🇷 Brazil · 🇲🇽 Mexico · 🇦🇷 Argentina · 🇨🇴 Colombia · 🇨🇱 Chile · 🇵🇪 Peru · 🇻🇪 Venezuela · 🇿🇦 South Africa · 🇳🇬 Nigeria · 🇰🇪 Kenya · 🇪🇬 Egypt · 🇲🇦 Morocco · 🇩🇿 Algeria · 🇸🇦 Saudi Arabia · 🇦🇪 UAE · 🇶🇦 Qatar · 🇰🇼 Kuwait · 🇮🇱 Israel · 🇹🇷 Turkey · 🇷🇺 Russia · 🇺🇦 Ukraine · 🇰🇿 Kazakhstan · 🇳🇿 New Zealand

---

## 🗂 Tabs & Modules

### 🏢 Carrier Lookup

Identifies the telecom carrier/operator for each phone number.

- **Input**: Paste or load phone numbers (one per line)
- **Output**: Number + Carrier name
- **Filter**: Filter results by specific carrier
- **Auto-Save**: Automatically saves results split by carrier (e.g., `results/carrier/verizon.txt`, `results/carrier/att.txt`)
- **Carrier Normalization**: Subsidiaries and legacy names are automatically mapped to parent carriers:
  - Cellco Partnership, Alltel, GTE, Bell Atlantic → **Verizon**
  - Cingular, Pacific Bell, BellSouth, New Cingular → **AT&T**
  - Metro PCS, Omnipoint, Suncom, Aerial, Powertel → **T-Mobile**
  - Nextel → **Sprint**
  - And more for UK carriers (Vodafone, EE, O2, Three, etc.)

### 📶 Line Type Checker

Classifies each phone number by its line type.

- **Input**: Paste or load phone numbers
- **Output**: Number + Type (Mobile, Landline, VoIP, Unknown)
- **Filter**: Filter by line type
- **Statistics**: Shows breakdown count for each type
- **Auto-Save**: Saves split by type (e.g., `results/type/mobile.txt`, `results/type/landline.txt`)

### 📍 Location Lookup

Resolves the geographic location of each phone number.

- **Input**: Paste or load phone numbers
- **Output**: Number + Location (City, State for US/Canada)
- **Filter**: Filter by location name
- **Auto-Save**: Saves split by location (e.g., `results/location/new_york_ny.txt`, `results/location/atlanta_ga.txt`)

### 🔗 Combined Lookup

Runs carrier, line type, and location lookups simultaneously.

- **Input**: Paste, load, or use the built-in Quick Generate feature
- **Output**: Number + Carrier + Type + Location (4 columns)
- **Multi-Filter**: Independent filter dropdowns for Carrier, Type, Location, and Valid/Unknown status
- **Include Toggles**: Choose which lookups to include (Carrier, Line Type, Location)
- **Quick Gen**: Built-in area code generator — enter area codes, prefix, and count, then click "Gen & Run" to generate and analyze in one step
- **Auto-Save**: Saves by carrier under `results/combined/`

### 🔢 Number Generator

Generates bulk phone numbers with two modes:

#### Manual Mode (All Countries)
- **Area Codes**: Enter comma-separated area codes, or leave empty to auto-select from database
- **Prefixes**: Optional NXX prefixes to constrain generation
- **Count**: Number of phone numbers to generate
- **Format**: Choose output format from dropdown
- **Line Type Filter**: Checkboxes to include/exclude Mobile, Landline, VoIP, Unknown (US/Canada/UK only)

#### Smart Gen Mode (US / Canada / UK)
- **Carrier Filter**: Generate numbers only for a specific carrier (e.g., Verizon, AT&T, T-Mobile, Vodafone, EE)
- **State/Region Filter**: Generate numbers only from a specific state or province
- **Line Type Filter**: Generate only Mobile, Landline, or VoIP numbers
- **Count**: Number of phone numbers to generate

#### Export
Generated numbers can be exported directly to any lookup tab:
- 🔗 Combined
- 🏢 Carrier
- 📶 Line Type
- 📍 Location

---

## 📐 Output Formats

The format dropdown dynamically updates based on the selected country:

### US / Canada (+1)
| Format | Example |
|--------|---------|
| `XXXXXXXXXX` | `2015551234` |
| `+1XXXXXXXXXX` | `+12015551234` |
| `1XXXXXXXXXX` | `12015551234` |
| `(XXX) XXX-XXXX` | `(201) 555-1234` |
| `XXX-XXX-XXXX` | `201-555-1234` |

### UK (+44)
| Format | Example |
|--------|---------|
| `XXXXXXXXXXX` | `7911123456` |
| `+44XXXXXXXXXXX` | `+447911123456` |
| `0XXXXXXXXXXX` | `07911123456` |

### Other Countries
| Format | Example |
|--------|---------|
| `XXXXXXXXXXX` | Raw digits |
| `+[code]XXXXXXXXXXX` | With country code |
| `0XXXXXXXXXXX` | With leading zero |

---

## 🔀 Filtering & Export

### Filtering
Every lookup tab has a filter dropdown that updates dynamically after each run. Select a specific carrier, line type, or location to show only matching rows. The Combined tab has independent filters for all three dimensions plus a Valid/Unknown radio selector.

### Cross-Tab Export
Every lookup tab (Carrier, Line Type, Location) includes export buttons in the results panel:
- **🔗 Combined** — Send visible numbers to Combined tab
- **📍 Location** — Send visible numbers to Location tab
- **📶 Line Type** — Send visible numbers to Line Type tab
- **🏢 Carrier** — Send visible numbers to Carrier tab

Export respects the current filter — if you filter to "Verizon" and export, only Verizon numbers are sent.

### Save Options
- **💾 Save Results** — Save all results to a file
- **💾 Save Filtered** — Save only the currently visible/filtered rows
- **Save numbers only** — Checkbox to save just phone numbers (one per line) or full details
- **CSV support** — Save as `.csv` for spreadsheet import

---

## 💾 Auto-Save System

Results are automatically saved to organized folders after each lookup:

```
results/
├── carrier/
│   ├── verizon.txt
│   ├── att.txt
│   ├── t_mobile.txt
│   └── sprint.txt
├── type/
│   ├── mobile.txt
│   └── landline.txt
├── location/
│   ├── new_york_ny.txt
│   ├── atlanta_ga.txt
│   └── silver_spring_md.txt
├── combined/
│   ├── combined_verizon.txt
│   └── combined_att.txt
└── generator/
    └── generated.txt
```

The auto-save path is configurable per tab via the "Auto-save to:" field.

---

## 🔑 Licensing

Hope Phone Intelligence uses a hardware-bound license system.

### Trial Mode
- Available for evaluation purposes
- Limited to **50,000 numbers** per session
- Trial banner displayed in the header

### Pro License
- **Unlimited** number processing and generation
- All features unlocked
- License is bound to your hardware (one device per license)
- Purchase via [@brain_lead on Telegram](https://t.me/brain_lead)

### License Activation
1. Click the **🔑 Activate** button in the trial banner, or
2. Enter your license key in the activation dialog
3. License is validated and bound to your system

### License Binding Reset
If you need to move your license to a new machine:
- The application automatically detects binding conflicts on startup
- A reset dialog will appear allowing you to unbind from the previous system
- After reset, the license is reactivated on your current machine

> ⚠️ **Each license is for ONE user only.** If multiple users are detected using the same license, the license may be permanently revoked.

---

## 💻 System Requirements

| Requirement | Minimum |
|-------------|---------|
| **OS** | Windows 10/11 (64-bit) |
| **RAM** | 4 GB |
| **Disk** | 200 MB free space |
| **Display** | 800×600 minimum resolution |
| **Internet** | Required for license validation and updates |

---

## 📦 Installation

### Windows (Compiled Executable)
1. Download `gui.exe` from the authorized distribution channel
2. Place it in a folder with the included `data/` directory and `config/` directory
3. Run `gui.exe`
4. Activate your license when prompted

### Directory Structure
```
hope-validator/
├── gui.exe                  # Main application
├── config/
│   └── settings.json        # Application settings
├── data/                    # Offline databases (required)
├── database/                # License storage (auto-created)
└── results/                 # Output files (auto-created)
```

> ⚠️ Do not modify, move, or delete files in the `data/` directory. The application requires these files for offline lookups.

---

## 🚀 Getting Started

1. **Launch** the application
2. **Select your country** from the 🌍 dropdown in the header
3. **Choose a tab** based on what you need:
   - Need carrier info? → 🏢 Carrier tab
   - Need line types? → 📶 Line Type tab
   - Need locations? → 📍 Location tab
   - Need everything? → 🔗 Combined tab
   - Need to generate numbers? → 🔢 Generator tab
4. **Input numbers** by pasting into the text area or clicking 📂 Load to import from a file
5. **Click ▶ Run** to process
6. **Filter** results using the dropdown
7. **Export** to other tabs or **Save** to file

### Quick Workflow Example
1. Go to **🔢 Generator** → Enter area codes `201, 301, 404` → Set count to `100000` → Click ⚡ Generate
2. Click **🔗 Combined** export button → Numbers are sent to Combined tab
3. In Combined tab, click **▶ Run** → All numbers are analyzed
4. Filter by **Carrier: VERIZON** and **Type: Mobile**
5. Click **💾 Save Filtered** → Save only Verizon mobile numbers

---

## ❓ FAQ

**Q: Can I use this offline?**
A: Lookups for US, Canada, and UK work fully offline. Other countries require the `phonenumbers` library. License validation requires internet on first launch.

**Q: How accurate is the carrier data?**
A: The offline database is sourced from official NPA-NXX assignment records. Accuracy depends on the data source and does not account for number porting (numbers transferred between carriers).

**Q: Can I process numbers from multiple countries at once?**
A: Select the target country from the dropdown before running. To process multiple countries, run separate batches for each.

**Q: What happens if my trial expires?**
A: Trial mode has a 50,000 number limit per session. Contact [@brain_lead](https://t.me/brain_lead) to purchase a Pro license.

**Q: Can I move my license to a new computer?**
A: Yes. The application will detect the binding conflict and offer a self-service reset option. Each license supports one active device at a time.

**Q: The application says "AUTH FAILED" — what do I do?**
A: Check your internet connection. If the issue persists, contact [@brain_lead](https://t.me/brain_lead) for support.

---

## ⚖️ Disclaimer

**IMPORTANT: PLEASE READ THIS DISCLAIMER CAREFULLY BEFORE USING THIS SOFTWARE.**

By downloading, installing, or using Hope Phone Intelligence (hereinafter referred to as "the Software"), you acknowledge that you have read, understood, and agree to be bound by the following terms:

### Purpose
The Software is provided for **educational, experimental, research, and legitimate business purposes only**. It is designed to assist in lawful telecommunications analysis, number plan research, and data validation activities conducted with proper authorization and consent.

### No Warranty
THE SOFTWARE IS PROVIDED **"AS IS"**, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS, COPYRIGHT HOLDERS, OR DEVELOPER BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT, OR OTHERWISE, ARISING FROM, OUT OF, OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### User Responsibility
You, the user, are **solely and entirely responsible** for your use of the Software and any consequences arising from such use. This includes, but is not limited to:

- **Complying with ALL applicable local, state, national, and international laws**, regulations, and industry standards related to your use of the Software, including but not limited to data privacy laws (GDPR, CCPA, TCPA, etc.), electronic communications regulations, anti-spam legislation, and telecommunications regulations.
- **Obtaining and maintaining explicit, documented consent** from all recipients or affected parties before sending any communications, performing any lookups, or taking any actions using data obtained through the Software.
- **Ensuring the accuracy and legality** of the content or actions performed using the Software.
- **Adhering to the terms of service** and acceptable use policies of any third-party services, providers, or platforms you interact with.
- **Protecting your own credentials, data, and systems** from unauthorized access.

### Prohibited Uses
The Software shall **NOT** be used for:
- Any illegal, fraudulent, or malicious activity
- Harassment, stalking, or invasion of privacy
- Unsolicited communications (spam) in violation of applicable laws
- Any activity that violates the Telephone Consumer Protection Act (TCPA), CAN-SPAM Act, GDPR, or equivalent legislation in your jurisdiction
- Circumventing telecommunications regulations or carrier terms of service
- Any purpose that could cause harm to individuals, organizations, or telecommunications infrastructure

### Data Accuracy
The developer makes **no guarantees** regarding the accuracy, completeness, or timeliness of the data provided by the Software. Phone number assignments, carrier information, and location data may change without notice. Number portability means that carrier information may not reflect the current service provider. Users should independently verify any critical data.

### Hardware Authorization
The Software incorporates a Hardware ID (HWID) authorization mechanism. You acknowledge that this feature is in place to manage access to the Software and that unauthorized use, redistribution, or circumvention of this mechanism is strictly prohibited.

### Intellectual Property
This Software is **proprietary and closed-source**. All intellectual property rights, including but not limited to copyrights, trademarks, trade secrets, and patents, are owned by the developer. You are granted a limited, non-exclusive, non-transferable license to use the Software subject to these terms. You may NOT:
- Copy, reproduce, or distribute the Software
- Modify, adapt, translate, or create derivative works
- Reverse engineer, decompile, disassemble, or attempt to derive the source code
- Remove, alter, or obscure any proprietary notices or labels
- Sublicense, rent, lease, or lend the Software to any third party

### Indemnification
By using the Software, you agree to **indemnify, defend, and hold harmless** the developer (Brain Lead) from and against any and all claims, liabilities, damages, losses, costs, expenses, or fees (including reasonable attorneys' fees) arising from:
- Your use or misuse of the Software
- Your breach of this Disclaimer or any applicable law
- Any third-party claims related to your use of the Software
- Any data breach or security incident resulting from your use of the Software

### Limitation of Liability
IN NO EVENT SHALL THE DEVELOPER BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, CONSEQUENTIAL, OR PUNITIVE DAMAGES, INCLUDING BUT NOT LIMITED TO LOSS OF PROFITS, DATA, USE, GOODWILL, OR OTHER INTANGIBLE LOSSES, RESULTING FROM YOUR USE OF OR INABILITY TO USE THE SOFTWARE, REGARDLESS OF WHETHER THE DEVELOPER HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

### Governing Law
This Disclaimer shall be governed by and construed in accordance with applicable laws. Any disputes arising from the use of this Software shall be resolved through appropriate legal channels.

### Acceptance
**By downloading, installing, launching, or using the Software in any way, you indicate that you have read, understood, and agreed to ALL terms of this Disclaimer.** If you do not agree to these terms, you must immediately cease all use of the Software and delete all copies in your possession.

---

## 📞 Contact & Support

| Channel | Link |
|---------|------|
| **Telegram** | [@brain_lead](https://t.me/brain_lead) |
| **Purchase License** | [@brain_lead](https://t.me/brain_lead) |
| **Bug Reports** | [@brain_lead](https://t.me/brain_lead) |

---

**Hope Phone Intelligence v1.0** — Built by **Brain Lead**

© 2025 Brain Lead. All Rights Reserved. Unauthorized distribution is prohibited.
