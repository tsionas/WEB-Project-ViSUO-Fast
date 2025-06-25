# Simple Geometry Visibility Tool (SGVT)
Produced by UCLouvain, BE under the Wind Energy for Brussels (WEB) Project, co-financed by Innoviris.
### Overview
The **Simple Geometry Visibility Tool (SGVT)** was developed within ArcGIS Pro using **Model Builder** and is designed for **parametrized visibility analysis (VA)** of multiple **Small Urban Objects (SUOs)** from multiple **observation points (OPs)**. 

Using **line-of-sight (LOS) calculations**, SGVT determines whether each SUO is visible from each OP. The tool provides both **analytical outputs** and **descriptive statistics** characterizing visibility relations across the study area.

### Motivation
Cities are composed not only of large structures such as buildings but also of Small Urban Objects (SUOs)—including street furniture, signage, and small-scale monuments—which, despite their modest size, contribute significantly to the visual perception of the urban landscape. SGVT enables fast and maasive  **Visibility Analysis (VA)** for SUO with true-3D analytical methods as **point locations**. 

### Features
- **Automated visibility analysis** using **LOS** calculations
- **Flexible observation point generation** (along paths, around outlines, or grid-based areas)
- **Customizable vertical positioning** (relative to terrain elevation from **DEM**)
- **SUO representation with optimized selection criteria**
- **Visibility metrics**, including:
  - Overall Visibility (OV)
  - SUO Visibility (SUOV)
  - OP Visibility (OPV)
  - Geometric attributes (viewing distance, azimuth, elevation angle)
- **Advanced filtering and classification** for directional analysis
- **Open-source and scalable for urban research**

### How It Works
1. **Input Requirements**
   - A set of **observation points (OPs)**
   - Locations of **Small Urban Objects (SUOs)**
   - A 3D model of the **urban environment** contaning occluding objects such as buildings, trees etc. (Digital Surface Model)

2. **LOS Calculation**
   - For each **OP-SUO pair**, a **LOS** is constructed.
   - If the **LOS intersects an occluding object**, visibility is recorded as **false**; otherwise, it is **true**.
   - Each **LOS** is has as attributes the viewing:
     - **Distance (Length)**
     - **Azimuth (horizontal angle from the North to the SUO)**
     - **Vertical angle (elevation angle to SUO)**

3. **Visibility Metrics**

   The examined OP and SUO are copied and descriptive statistics are added at each OP from all the visible SUO and at each SUO from all OP with visibility.  
   - **Overall Visibility (OV)**: proportion of visible LOS relative to total LOS
   - **SUO Visibility (SUOV)**: number of OPs from which an SUO is visible
   - **OP Visibility (OPV)**: number of SUOs visible from an OP
   - **Directional Classification**: Standard or custom bins (e.g., N-E-S-W)

### Installation
One needs to load the toolbox (.tbx file) to ArcGIS Pro from the Catalog.

#### Prerequisites
- ArcGIS Pro with **Model Builder**

#### Setup
1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo/SGVT.git
