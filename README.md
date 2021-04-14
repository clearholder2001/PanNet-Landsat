# PanNet-Landsat
Implementation of PanNet by Chainer. Landsat 8 images are used in this repository.  

|Original RGB (resolution: 30m)|Pansharpened by PanNet (resolution: 15m)|
|---|---|
|![overview](imgs/gdal_merged_original.png)|![overview](imgs/pansharpened_by_pannet.png)|  

Original RGB image is created by gdal_merge. Both images are screenshots of QGIS on my laptop.

### Architecture of PanNet
![overview](imgs/architecture.png)

### Demo on Google Colab
Please see [examples/demo_on_colab.ipynb](https://github.com/oyam/PanNet-landsat/blob/master/examples/demo_on_colab.ipynb)

### References
* PanNet: A deep network architecture for pan-sharpening   http://openaccess.thecvf.com/content_iccv_2017/html/Yang_PanNet_A_Deep_ICCV_2017_paper.html

### Environment Setup for Windows
```
python -m pip install --upgrade pip setuptools wheel
pip install .\dependency\GDAL-3.1.4-cp36-cp36m-win_amd64.whl
pip install .\dependency\rasterio-1.1.8-cp36-cp36m-win_amd64.whl
pip install chainercv
pip install -r .\requirements.txt
```
Copy .\dependency\cv2.cp36-win_amd64.pyd .\dependency\opencv_world452.dll to Lib\site-packages