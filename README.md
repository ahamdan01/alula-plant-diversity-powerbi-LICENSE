# AlUla Plant Biodiversity & Geographic Distribution Dashboard

An interactive Power BI dashboard that maps, tracks, and analyzes the biodiversity and density of wild plant species across various reserves and locations in the AlUla region, Saudi Arabia. This project transforms raw ecological data into a visual story, supporting environmental sustainability aligned with Saudi Vision 2030.

View Images:
<img width="1922" height="1080" alt="لقطة الشاشة 2026-06-21 224755" src="https://github.com/user-attachments/assets/aa6ff580-4dfe-488c-8748-5cabcfd3e281" />
<img width="1922" height="1081" alt="لقطة الشاشة 2026-06-21 224820" src="https://github.com/user-attachments/assets/348ac597-32bf-4120-83a5-91cb8ac8e545" />
<img width="1922" height="1083" alt="لقطة الشاشة 2026-06-21 224701" src="https://github.com/user-attachments/assets/055616ce-c038-4055-b545-d5722aeeecc0" />
<img width="1923" height="1077" alt="لقطة الشاشة 2026-06-21 224728" src="https://github.com/user-attachments/assets/00ee63f7-e576-4558-a1c0-f622f3efabdc" />



---

## 🗺️ Project Overview & Visual Preview
This dashboard visualizes the geographic distribution of plant families and species in AlUla using a 3D terrain-mapped interface. 

*   **Data Source:** National Open Data Platform (Provided by the Royal Commission for AlUla - RCU).
*   **Core Objective:** To identify the most dense flora zones, discover the most prominent plant families (e.g., *Asteraceae*), and provide an intuitive UX for researchers and environmentalists.

---

## 🛠️ Tech Stack & Skills Demonstrated
*   **Business Intelligence:** Microsoft Power BI Desktop
*   **Data Engineering / ETL:** Power Query M-Language
*   **Geospatial Visualization:** Azure Maps (3D Columns)
*   **UI/UX Design:** Custom Button Slicers, Harmonious Themed Palettes

---

## ⚙️ The Data Pipeline & Engineering Journey (ETL)

A significant amount of data engineering was performed within **Power Query** to elevate this from raw data into a production-ready dashboard:

1. **Structural Transformation (Unpivot):** The original source dataset structured locations horizontally as columns. I executed an **Unpivot** transformation to normalize the matrix into a clean, row-oriented tabular format suitable for relational database modeling.
2. **Geographical Mapping (Geocoding):** Built a custom geospatial lookup table featuring precise **Latitude & Longitude** coordinates for each surveyed oasis/reserve to successfully enable 3D mapping layers.
3. **Advanced Text Cleaning:** Standardized inconsistent location records using **Trim** and manual text normalization (*Replace Values*) to achieve a 100% relational join match between the main survey table and the coordinates table.
4. **Data Integrity & Filtering (Handling NaNs):** Addressed a critical logical bug where raw records falsely inflated metrics. Discovered a hidden status attribute and implemented an optimized filter layer to extract only true positive instances (`Present`), completely omitting erroneous `NA/NaN` placeholders.

---

## 🎨 Dashboard Design & Visual Storytelling

*   **3D Geospatial Layer:** Built using **Azure Maps**, where the exact column height corresponds to the `Plant Record` (Count) over AlUla's actual terrain elevation.
*   **Themed Visual Identity:** The color scheme is meticulously chosen to match AlUla's natural environment and branding—blending rich **Terracotta (Warm Clay)** for core data elements with a soft, clean **Beige** background for sleek UI cards.
*   **Modern UI Controls:** Replaced standard dropdowns with Power BI's latest **Button Slicers** (configured with customized default, hover, and selection states) for web-like tactile navigation.

---

## 📁 Repository Structure
*   project is saved using the modern **Power BI Project (.pbip)** format, decomposing the report into human-readable, trackable text files for optimal version control:
*   `📁 alula-plant-diversity-powerbi.Report/` : Contains the UI/UX visual layers, page configurations, theme custom properties, and button slicer layouts.
*   `📁 alula-plant-diversity-powerbi.Dataset/` : Holds the data model configuration, relationship schemas, Power Query M-Language steps, and DAX expressions.
*   `📄 alula-plant-diversity-powerbi.pbip` : The main Power BI project launch file.
*   `📁 Data/` *(Optional)*: Contains the coordinate lookup tables and external metadata.
*   `📄 .gitignore` : Optimized to exclude local user caches, database instances, and private developer configs (`.pbi/`).
*   `📄 LICENSE` : MIT License.
---

## 💡 Key Insights Uncovered
*   **Asteraceae** stands out as the most dominant and heavily recorded plant family in the surveyed regions, crossing over 100 verified observations.
*   **Harrat Uwayrid** and **Sharaan** represent high-density biodiversity hotspots compared to other surveyed locations.

---

## 👤 Author
*   **Abdulrahman Hamdan**
*   https://www.linkedin.com/in/abdulrahman-hamdan-0b3b36a5/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3Bqz4QoRrMTmSqpmyMTMVzBg%3D%3D
