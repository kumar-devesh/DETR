DETR
==============================
![image](https://user-images.githubusercontent.com/76114246/139389001-ae0e25c5-e0f2-474b-b01a-9acb0bbb7751.png)
DETR object detection model formulates the problem of object detection as a direct set prediction problem effectively removing the need for hand designed components like a non max supression or anchor box generation that explicitly encode the knowledge of the task. It uses a transformer encoder-decoder based architecture to output set predictions in parallel. 

![image](https://user-images.githubusercontent.com/76114246/139389968-eb79aee6-467e-4ef3-89b8-183ff2f9a09d.png)

Transformer architecture
-----------------------
The transformer architecture is slightly different from [Vaswani et al](https://arxiv.org/abs/1706.03762) and uses a positional encoding at each encoder and decoder layer.
![image](https://user-images.githubusercontent.com/76114246/139390148-31410e20-5305-43ef-87b5-c2c44025d8b3.png)


Loss Function
--------------------
The loss functions used are a giou loss for bounding box, a negative log likelihood loss for class predictions and an L1 loss for the predicted and ground truth boxes.

Dataset
---------------------
The DETR model is being trained on the Pascal VOC 2012 object detection dataset with 20 classes and around 5000 train and validation images.

sample images
-------------
2008_000142          |  2008_000196
:-------------------------:|:-------------------------:
![2008_000142](https://user-images.githubusercontent.com/76114246/136657983-0f7a6796-c02f-44c4-af03-ca704de34b97.jpg)  |  ![2008_000196](https://user-images.githubusercontent.com/76114246/136658004-e30bb8e6-7f23-486a-a128-0efa8e2b89b2.jpg)

sample annotation file:
----------------------
```
<annotation>
	<folder>VOC2012</folder>
	<filename>2008_000041.jpg</filename>
	<source>
		<database>The VOC2008 Database</database>
		<annotation>PASCAL VOC2008</annotation>
		<image>flickr</image>
	</source>
	<size>
		<width>500</width>
		<height>375</height>
		<depth>3</depth>
	</size>
	<segmented>0</segmented>
	<object>
		<name>pottedplant</name>
		<pose>Unspecified</pose>
		<truncated>0</truncated>
		<occluded>0</occluded>
		<bndbox>
			<xmin>54</xmin>
			<ymin>189</ymin>
			<xmax>84</xmax>
			<ymax>214</ymax>
		</bndbox>
		<difficult>1</difficult>
	</object>
	<object>
		<name>person</name>
		<pose>Rear</pose>
		<truncated>1</truncated>
		<occluded>0</occluded>
		<bndbox>
			<xmin>358</xmin>
			<ymin>188</ymin>
			<xmax>469</xmax>
			<ymax>359</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
</annotation>
```
----------------------

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
"# DETR" 
