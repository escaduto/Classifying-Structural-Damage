Comparative Assessment of High-Resolution Satellite-Based Building Footprint Extraction Methods
Erica Scaduto (escaduto@ucdavis.edu ) , Yuhan Huang (yuhhuang@ucdavis.edu) 

I. Overview and Related Work 
	Automatic extraction of building footprints from high resolution imagery can aid in environmental and disaster management by integrating its spatiotemporal distribution patterns within risk assessments and urban planning efforts. However, deriving a reliable and efficient building extraction method has presented challenges mainly due to regional differences in development type (e.g. rural vs metropolitan), as well as the sheer varieties in building characteristics (e.g. color, shape, materials) (Li et al. 2019). 
Over the past decade, studies have implemented object-based image analysis to extract information from high resolution satellite and aerial imagery including road/buildings, land use, palm tree identification, and etc. Methods include segmentation algorithms (Belgiu and Dragut 2014), machine learning classifiers (AdaBoost, RF, SVM) (Chen et al. 2018), as well as deep learning-based methods (Long, Darrell, and Fully 2015). The use of auxiliary data in combination with multispectral satellite imagery has also been utilized, including public GIS datasets from OpenStreetMap, and Google Maps (Li et al. 2019). 

II. Proposed Work
2.1 Objective
We intend to compare different machine learning algorithms for image classification to develop a general method for building extraction from high-resolution remote sensing images.

2.2 Datasets
There are a number of annotated datasets, including SpaceNet, SAT-6 airborne, and Open Cities AI datasets which offer ready-to-use labelled training/testing data across various regions, and spatial/spectral resolutions (Table 1). Furthermore, the use of OpenStreetMap GIS data along with NAIP imagery via GEE is also an option (depending on our ROI). The building footprint from OSM can be converted into a single-band binary image (0: non-building 1: building). Further investigation on coverage/quality may be needed. 

2.3 Methods & Model Selection:
Unsupervised: K-means, spectral clustering, hierarchical  clustering, shift invariance feature transform(SIFT), simple linear iterative clustering (SLIC) segmentation, Felzenszwaib segmentation...
Supervised: two trajectories: pixel-based and object-based (objects from segmentation)
KNN, maximum likelihood, SVM, random forest, XGBoost, random walker segmentation, simple 2-layer ANN…
Deep learning methods: Mask R-CNN...
