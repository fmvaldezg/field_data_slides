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
download: "https://raw.githubusercontent.com/fmvaldezg/field_data_slides/main/slides.pdf"

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
  <a href="https://charlesstudy.temple.edu/calendar/workshops?&t=g&d=0000-00-00&cal%5B%5D=6197&ct%5B%5D=69157" target="_blank" class="slidev-icon-btn" title="Mapping Workshops at Temple University Libraries">
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

- 📝 Understand the **landscape of mobile data collection tools** 
- 📋 Design and deploy a **digital survey form** in **KoBoToolbox** using best practices
- 📡 Configure **offline data collection** strategies and manage **data synchronization** with desktop systems
- 📍 Integrate **GPS positioning**, **photo capture**, and **multimedia attachments** into field data workflows
- 🗺️ Prepare a **QGIS project for QField** and collect **georeferenced field observations** on a mobile device
- 🔬 Identify the **right tool for your research context** 

<br>
<br>

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

---
transition: slide-up
---

# Workshop agenda

<div class="text-sm">

| Time   | Topic                                  | Description |
|--------|----------------------------------------|-------------|
| 5 min  | Welcome & Introduction                 | Introductions, goals, participant check-in |
| 5 min  | Why Go Digital?                        | Benefits of mobile data collection over paper-based methods |
| 20 min | KoBoToolbox                            | Live demo: survey design, skip logic, validation, offline collection |
| 20 min | QField & Mobile GIS                    | Live demo: QGIS project setup, GPS integration, field data capture |
| 5 min  | Choosing the Right Tool                | Survey-driven vs. spatial workflows, combining both tools |
| 5 min  | Q&A & Wrap-Up                          | Open questions, shared resources, follow-up support |

</div>

---
transition: slide-up
---

# Why Go Digital?

<div class="grid grid-cols-2 gap-8 mt-4">

<div>

### 📄 Paper-Based Challenges
<br>

- **Transcription errors** — manual entry introduces mistakes
- **Data loss** — forms get damaged, lost, or incomplete
- **Lag time** — days or weeks before data is usable

</div>

<div>

### 📱 Digital Advantages
<br>

- **Real-time validation** — catch errors at the point of collection
- **GPS tagging** — automatic location for every record
- **Multimedia capture** — photos, audio, video in the field
- **Offline capability** — no internet? No problem

</div>

</div>

<div class="mt-8 text-center">

### Today's Toolkit

<div class="grid grid-cols-2 gap-4 mt-2">
<a href="https://www.kobotoolbox.org" target="_blank" class="border rounded-lg p-3 no-underline" style="display:flex; align-items:center; justify-content:center; background-color:rgb(107, 107, 102); border-radius:8px; cursor:pointer;">
<img src="https://raw.githubusercontent.com/kobotoolbox/docs/refs/heads/master/source/_static/images/kobologo.svg" style="width:130px; display:block; margin:auto;" alt="KoBoToolbox logo" />
</a>
<a href="https://qfield.org" target="_blank" class="border rounded-lg p-3 no-underline" style="display:flex; align-items:center; justify-content:center; background-color:rgb(107, 107, 102); cursor:pointer;">
<img src="https://qfield.org/images/qfield_for_qgis.png" style="width:130px; display:block; margin:auto;" alt="QField for QGIS logo" />
</a>
</div>

</div>

---
transition: slide-up
layout: image-right
image: /assets/intro.gif
---

# What is KoboToolbox?
An open source platform for the collection, management, and visualization of data. 

<img src="https://raw.githubusercontent.com/kobotoolbox/docs/refs/heads/master/source/_static/images/kobologo.svg" style="height:25px; background-color:#2e2e2e; padding:4px; border-radius:4px;" alt="KoBoToolbox logo" />


<br>
<br>

<div class="text-sm">

-	Build questionnaires in the web or using XLSForm
-	Translate questionnaires into multiple languages
-	Create a questions library
-	Collect data offline or online in multiple devices (mobile phones, tablets, laptops)
-	Visualize data in maps and reports
-	Download data in multiple formats (XLS, CSV, KML, ZIP, GeoJSON)
-	Share and collaborate on projects

</div>

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

---
layout: section
--- 

# Demo 1
Creating a KoboToolbox Form

<style>
.slidev-layout {
  background-image: url('public/assets/demo1.gif');
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
}

h1 {
  background-color: rgba(255, 255, 255, 0.5);
  color: #146b8c;
  padding: 1rem 2rem;
  border-radius: 12px;
  margin-bottom: 1.5rem;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(4px);
  font-weight: bold;
}

.slidev-layout p {
  background-color: rgba(255, 255, 255, 0.85);
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  margin: 0 auto;
  max-width: fit-content;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
  backdrop-filter: blur(2px);
  font-size: 2rem;
}
</style>

---
layout: iframe
url: https://umap.openstreetmap.fr/en/map/food-trucks-temple-u_1373198#17/39.979188/-75.155057
backgroundSize: contain
--- 

---
layout: iframe-right
url: https://umap.openstreetmap.fr/en/map/participants-map_1373673
level: 2
---

# Try it out

Take a look at the sample form for the live map:

[Go to the form](https://ee.kobotoolbox.org/x/d8Kn8EGg)

Or scan the QR code:

<img src="/assets/qr-code.png" style="width:200px;" />

---
layout: image-right
level: 2
image: /assets/demo2.gif
backgroundSize: contain
---

# Your turn

<v-clicks>

1. Go to [https://www.kobotoolbox.org/](https://www.kobotoolbox.org/)
2. Create an account (use the *Global KoboToolbox Server*)
3. Start a new project
4. Add all types of questions to your form
5. Preview your form
6. Deploy your form when ready
7. Share the link with participants or collect data yourself
8. Analyze your data with reports and maps
9. Download your data
</v-clicks>


---
layout: image-right
level: 2
image: /assets/demo2.gif
backgroundSize: contain
---

# Tips and Tricks

- Always **preview** your form 
- Test the form in different devices
- Use alternative languages
- Try out different layouts
- Create the form using XLSForm
- Save the form as an app in your phone/tablet
- Test the form offline (if needed)
- Download the data in different formats
- Configure a REST service to share live updates

---
layout: default
level: 2
---

# Additional Resources
<br>
<br>
<br>

<div class="grid grid-cols-3 gap-8 text-center">
<div>
<a href="https://academy.kobotoolbox.org/" target="_blank">KoboToolbox Academy</a>
<br><br>
<img src="/assets/academy.png" style="width:250px; display:block; margin:auto;" />
</div>
<div>
<a href="https://community.kobotoolbox.org/" target="_blank">KoboToolbox Community</a>
<br><br>
<img src="/assets/community.png" style="width:250px; display:block; margin:auto;" />
</div>
<div>
<a href="https://support.kobotoolbox.org/" target="_blank">KoboToolbox Help Center</a>
<br><br>
<img src="/assets/helpcenter.png" style="width:250px; display:block; margin:auto;" />
</div>
</div>

---
layout: section
--- 

# Demo 2
QField

<style>
.slidev-layout {
  background-image: url('public/assets/demo3.gif');
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
}

h1 {
  background-color: rgba(255, 255, 255, 0.5);
  color: #146b8c;
  padding: 1rem 2rem;
  border-radius: 12px;
  margin-bottom: 1.5rem;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(4px);
  font-weight: bold;
}

.slidev-layout p {
  background-color: rgba(255, 255, 255, 0.85);
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  margin: 0 auto;
  max-width: fit-content;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
  backdrop-filter: blur(2px);
  font-size: 2rem;
}
</style>

---
transition: slide-up
layout: image-right
image: /assets/demo4.gif
---

# What is QField?
QField is an open-source application that allows painless fieldwork and synchronisation with your local QGIS projects.

<img src="https://raw.githubusercontent.com/opengisch/QField/master/images/icons/qfield_logo.png" style="height:75px; padding:4px; border-radius:4px;" alt="QField logo" />

<br>

<div class="text-sm">

-	Use it in online and offline
-	Link to external databases
-	Export from QGIS with the QFieldSync Plugin
-	QField is available for Android and iOS devices
-	Optimised data collection outside

</div>

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

---
layout: image-right
level: 2
image: /assets/demo4.gif
backgroundSize: contain
---

# Your turn

<v-clicks>

1. Download [QGIS](https://qgis.org/)
2. Create your project in QGIS
3. Download the [QField Plugin](https://docs.qfield.org/get-started/tutorials/get-started-qfs/) 
4. Download QField on your mobile device (Phone or Tablet)
5. Export the project to your device
6. Use QField Cloud to synchronize (if needed)
7. Go out and map
8. Update your QGIS project files
</v-clicks>

---
layout: default
level: 2
---

# Additional Resources
<br>
<br>
<br>

<div class="grid grid-cols-3 gap-8 text-center">
<div>
<a href="https://docs.qfield.org/how-to/" target="_blank">QField Docs</a>
<br><br>
<img src="/assets/docs.png" style="width:250px; display:block; margin:auto;" />
</div>
<div>
<a href="https://community.kobotoolbox.org/" target="_blank">QGIS user groups</a>
<br><br>
<img src="/assets/usergroups.png" style="width:250px; display:block; margin:auto;" />
</div>
<div>
<a href="https://support.kobotoolbox.org/" target="_blank">QField Cloud</a>
<br><br>
<img src="/assets/cloud.png" style="width:250px; display:block; margin:auto;" />
</div>
</div>

---
layout: image
transition: slide-up
image: /assets/workshoppromo.png
--- 

--- 
layout: end
---

Contact us at:\
felipe.valdez@temple.edu \
<br>
Visit our guides:\
https://guides.temple.edu/gis-mapping

<style>
.slidev-layout.end {
  background: linear-gradient(135deg, rgb(164, 30, 53) 0%, rgb(149, 56, 71) 100%);
}
</style>