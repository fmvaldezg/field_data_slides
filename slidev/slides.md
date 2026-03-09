---
theme: seriph
background: /assets/cover.jpeg
title: Field Data Collectins & Mobile GIS
class: text-center
transition: slide-left
mdc: true
duration: 60min
controls: true
presenter: false      
remote: false         
selectable: false     
monaco: false
info: false
drawings:
  enabled: false
contextMenu: false
colorSchema: light
themeConfig:
  primary: '#5d8392'
record: false
routerMode: hash
css: unocss
highlighter: shiki
download: "https://github.com/fmvaldezg/osm_for_urban_analysis/raw/main/Using%20OpenStreetMap%20for%20Urban%20Spatial%20Analysis.pdf"

---

<div class="overlay"></div>

<div class="content-wrapper">

# Field Data Collection

<span class="text-3xl">& Mobile GIS</span>

<div @click="$slidev.nav.next" class="mt-12 py-1 text-xs" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

</div>

<img 
  src="https://raw.githubusercontent.com/kobotoolbox/docs/refs/heads/master/source/_static/images/kobologo.svg" 
  class="absolute"
  style="left: 700px; top: 320px; width:130px; background-color: rgba(255, 255, 255, 0); padding: 10px; border-radius: 8px;"
  alt="Kobotoolbox logo"
/>

<img 
  src="https://qfield.org/images/qfield_for_qgis.png" 
  class="absolute"
  style="left: 700px; top: 350px; width:130px; background-color: rgba(255, 255, 255, 0); padding: 10px; border-radius: 8px;"
  alt="Qgis logo"
/>

<img 
  src="/assets/librarylogo.png" 
  class="absolute"
  style="left: 70px; top: 300px; width:300px; background-color: rgba(255, 255, 255, 0); padding: 10px; border-radius: 8px;"
  alt="OSM logo"
/>

<div class="abs-br m-6 text-xl">
  <a href="https://openstreetmap.org" target="_blank" class="slidev-icon-btn" title="Visit OpenStreetMap.org">
    <carbon:earth-filled />
  </a>
  <a href="https://library.temple.edu/services/support-for-gis-mapping" target="_blank" class="slidev-icon-btn" title="Temple University GIS Support">
    <carbon:information-filled />
  </a>
</div>

<style>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.4);
  z-index: 1;
  pointer-events: none;
}

.content-wrapper {
  position: relative;
  z-index: 2;
}

.abs-br {
  position: absolute !important;
  bottom: 0.5rem !important;
  right: 0.5rem !important;
  z-index: 10 !important;
}
</style>

---
level: 2
---

# Learning objectives


<br>
<br>

- 📝 Understand the OSM **data model**, including `nodes`, `ways`, `relations`, and the tagging schema
- ⚙️ Write **OverpassQL queries** to extract targeted urban datasets (roads, buildings, amenities, land use)
- 🧑‍💻 Use **Overpass Turbo** and **Overpass-ultra** to download and script OSM data extraction workflows
- 🗺️ Import OSM data into **QGIS** for spatial analysis and visualization
- 🌎 Create an OSM account and contribute edits using the **iD web editor**
- 🔬 Identify **research applications** of OSM data 

<br>
<br>


<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>