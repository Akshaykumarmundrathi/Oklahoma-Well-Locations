
````markdown
# 🛢️ Oklahoma Well Locations Extraction and Map

## 📌 Project Overview

This project automates the **extraction of well location information** from Oklahoma well report PDFs.  
It parses metadata such as **County, Section, Township, Range**, and **GPS coordinates** from the reports, then generates:

- 📄 A structured **Excel/CSV** file with all extracted data  
- 🗺️ An **interactive Folium map (HTML)** showing well locations visually  

This helps geologists, data analysts, and environmental researchers efficiently visualize and analyze well data across the state.

---

## 🏆 Features

✅ Automated PDF parsing and structured data extraction  
✅ Robust coordinate extraction from embedded **randymajors.org** URLs  
✅ Clean tabular output for easy data analysis in Excel or Power BI  
✅ Interactive Folium web map with clickable, clustered markers  
✅ Simple deployment and hosting via **GitHub Pages**

---

## 🛠️ Tech Stack

| Component | Technology |
|------------|-------------|
| **Language** | Python 3 |
| **Libraries** | PyMuPDF (`fitz`), pandas, regex, folium, tqdm |
| **Visualization** | Folium + Leaflet (auto-generated HTML/JS) |
| **Storage & Hosting** | CSV/Excel output, GitHub Pages for map hosting |

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Akshaykumarmundrathi/Oklahoma-Well-Locations.git
cd Oklahoma-Well-Locations
````

---

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

> Or manually install the essentials:
>
> ```bash
> pip install PyMuPDF pandas openpyxl folium tqdm
> ```

---

### 3️⃣ Place the Input PDF

Copy your well report PDF (e.g.,
`PDFs_Well_Location_20250523_140405.pdf`) into the project root folder.

---

### 4️⃣ Run the Extraction Script

```bash
python oklahoma_well_location_map.py
```

This will generate:

* `oklahoma_wells_text_extract_with_latlon.csv` → structured well data
* `oklahoma_wells_map.html` → interactive map

---

## 📊 Visualization

Once the script finishes:

* Open the generated **`.html`** map in your web browser
* Click on any marker to view:

  * Report name
  * County, Section, Township, Range
  * Latitude & Longitude
  * Direct link to RandyMajors map

Example marker popup:

```
Report Name: 03711572_L L BERRYHILL
County: Creek
Section: 16 | Township: 17 N | Range: 12 E
Lat: 35.951526 | Lon: -96.036915
```

---

## 🌐 Hosting on GitHub Pages

To publish your interactive map online:

1. Rename your map file to `index.html`
2. Commit and push it to the repository root
3. Enable **GitHub Pages**:
   *Settings → Pages → Branch: main → / (root) → Save*
4. Your map will be live at
   `https://<your-username>.github.io/Oklahoma-Well-Locations/`

---

## ⚠️ Limitations

* Some reports may miss data due to **inconsistent PDF layouts**
* Coordinates appear **only if** a valid `randymajors.org` link exists
* Regex patterns may need fine-tuning for other report templates
* Very large PDFs could require extra memory/time during parsing

---

## 🧠 Example Project Structure

```
Oklahoma-Well-Locations/
│
├── oklahoma_well_location_map.py         # Main extraction + mapping script
├── PDFs_Well_Location_20250523_140405.pdf # Input PDF
├── oklahoma_wells_text_extract_with_latlon.csv # Output CSV
├── oklahoma_wells_map.html               # Generated Folium map
├── requirements.txt
└── README.md
```

---

## 🤝 Contributing

Contributions, suggestions, and pull requests are welcome!
If you encounter parsing issues, please share a sample snippet or pattern —
together, we can improve the extraction robustness across various PDF formats.

---

## 👨‍💻 Author

**Akshay Kumar Mundrathi**
📍 Oklahoma State University
📧 [akshaykumarmundrathi@gmail.com](mailto:akshaykumarmundrathi@gmail.com)
💼 [LinkedIn](https://www.linkedin.com/in/akshaykumarmundrathi)

---

### ⭐ If you find this project useful, don’t forget to **star** the repository!

```

---

Would you like me to also write a matching `requirements.txt` for your repo (exact pip dependencies for this project)? It’ll make setup easier for others who clone it.
```
