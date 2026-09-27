# LDFCD: A Cross-Resolution Geological Disaster Change Detection Dataset

**LDFCD** (Landslide and Debris Flow Change Detection) is a heterogeneous-sensor cross-resolution change detection dataset for geological disaster monitoring. It contains real pre/post-disaster image pairs across two disaster types, kept in their **original unregistered state** to reflect real-world conditions.

---

## 📁 Dataset Structure

<pre>


The dataset contains two subsets. Each subset follows the same three-folder structure:

LDFCD/

├── Landslide/ # 48 image pairs

│ ├── A/ # Pre-disaster images (Landsat-8, 30 m)

│ ├── B/ # Post-disaster images (high-resolution, ~10 m)

│ └── label/ # Binary change masks (0: unchanged, 255: changed)

│

└── DebrisFlow/ # 40 image pairs

├── A/ # Pre-disaster images (Landsat-8, 30 m)

├── B/ # Post-disaster images (high-resolution, ~10 m)

└── label/ # Binary change masks (0: unchanged, 255: changed)


</pre>

sql_more

> **Note:** The data provided here are the **original image pairs
> before augmentation**. In our experiments, we divided the data
> into training / validation / test splits at the event level to
> prevent data leakage. Details are described in the paper.

---

## 📊 Dataset Overview

| Subset | Image Pairs | Pre-disaster Sensor | Post-disaster Sensor | Registration |
|---|---|---|---|---|
| LDFCD-Landslide | 48 | Landsat-8 (30 m) | High-resolution (~10 m) | Unregistered |
| LDFCD-DebrisFlow | 40 | Landsat-8 (30 m) | High-resolution (~10 m) | Unregistered |

**Key characteristics:**
- **Heterogeneous sensors**: image pairs come from different sensors with a native resolution ratio of approximately 3×, without any artificial downsampling
- **Unregistered**: pairs are retained in their original unregistered state, posing a realistic and challenging alignment problem
- **High-steep terrain**: all scenes are located in steep mountainous areas in southwestern China, prone to geological disasters

---

## 🌍 Geographic Coverage

The dataset covers **59 geological disaster events** (landslides and debris flows) in southwestern China, including events triggered by the 2008 Wenchuan earthquake, the 2013 Ya'an earthquake, and subsequent rainfall-induced secondary disasters.

Representative locations include Beichuan (北川), Caopo Township (草坡乡), Jiuzhaigou (九寨沟), and the Jinsha River (金沙江) region.



📬 Contact
If you encounter any issues with the dataset or the GEE tool, please
contact us:

Zhi Li — m15732638213@163.com
Bug reports and suggestions are also welcome via
GitHub Issues.

📜 License
This dataset is released under the Creative Commons Attribution 4.0 International License (CC BY 4.0). You are free to share and adapt the material for any purpose, provided appropriate credit is given.

🙏 Acknowledgements
Post-disaster high-resolution imagery is obtained from ref38—please replace with the propercitation.


