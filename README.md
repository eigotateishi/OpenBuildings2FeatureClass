# OpenBuildings2FeatureClass
This script is to convert the CSV file(s) of [Google Open Buildings](https://sites.research.google/open-buildings/) to a Feature Class.

**How to use:**
This script uses ArcPy modules, so your environment should have ArcPy library. Simply, load the script to your Tool Box on your ArcGIS Pro project and run it. The target Open Buildings CSV file must be stored in the folder where the script is located.

**NOTE:**

(1) Each CSV file can contain a huge amount of geometries (+10 million), so it is highly recommended to limit the geographical scope of your CSV file. This [tool](https://colab.research.google.com/github/google-research/google-research/blob/master/building_detection/open_buildings_download_region_polygons.ipynb#scrollTo=fwxfj3B1qUWu) developed by the Open Buildings Google team will help you to define the target geographical extent when you download the CSV file.

(2) Process time: Approximately 0.5 million geometries / about X hours with Windows 10 - AMD Ryzen 9 3900X 12-Core Processor 3.79 GHz, 32GB RAM.
