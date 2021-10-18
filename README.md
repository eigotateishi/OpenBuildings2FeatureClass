# OpenBuildings2FeatureClass
This script is to convert the CSV file(s) of [Google Open Buildings](https://sites.research.google/open-buildings/) to a Feature Class.

## How to use
This script uses ArcPy modules, so your environment should have ArcPy library. Simply, load the script to your Tool Box on your ArcGIS Pro project and run it. The target Open Buildings CSV file must be stored in the folder where the script is located.

When you want to test the script with a small chunk of a full CSV, change the code:
### TO TEST THE CODE with a small chunk of data:
#df_test = df_conf.iloc[0:100, :].copy()
#df_test.reset_index(inplace=True, drop=True)

## NOTE

* Each CSV file can contain a huge amount of geometries (+10 million), so it is highly recommended to limit the geographical scope of your CSV file. This [download region polygons](https://colab.research.google.com/github/google-research/google-research/blob/master/building_detection/open_buildings_download_region_polygons.ipynb#scrollTo=fwxfj3B1qUWu) tool developed by the Open Buildings Google team will help you to define the target geographical extent when you download the CSV file.
* Process time: Approximately 0.5 million geometries / about X hours with Windows 10 - AMD Ryzen 9 3900X 12-Core Processor 3.79 GHz, 32GB RAM.
* The data could contain invalid geometries (basically 'EMPTY' geometries). These invalid geometries will be automatically removed from the resulted feature class.
