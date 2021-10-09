DETR
==============================

DETR object detection using the pascal voc 2012 object detection dataset

sample images
-------------
![2008_000142](https://user-images.githubusercontent.com/76114246/136657983-0f7a6796-c02f-44c4-af03-ca704de34b97.jpg)
![2008_000196](https://user-images.githubusercontent.com/76114246/136658004-e30bb8e6-7f23-486a-a128-0efa8e2b89b2.jpg)
-------------

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
		<name>person</name>
		<pose>Frontal</pose>
		<truncated>1</truncated>
		<occluded>1</occluded>
		<bndbox>
			<xmin>271</xmin>
			<ymin>170</ymin>
			<xmax>386</xmax>
			<ymax>234</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>person</name>
		<pose>Frontal</pose>
		<truncated>1</truncated>
		<occluded>1</occluded>
		<bndbox>
			<xmin>295</xmin>
			<ymin>189</ymin>
			<xmax>328</xmax>
			<ymax>231</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>person</name>
		<pose>Frontal</pose>
		<truncated>1</truncated>
		<occluded>0</occluded>
		<bndbox>
			<xmin>206</xmin>
			<ymin>176</ymin>
			<xmax>256</xmax>
			<ymax>236</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>person</name>
		<pose>Frontal</pose>
		<truncated>0</truncated>
		<occluded>1</occluded>
		<bndbox>
			<xmin>122</xmin>
			<ymin>162</ymin>
			<xmax>198</xmax>
			<ymax>330</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>person</name>
		<pose>Frontal</pose>
		<truncated>1</truncated>
		<occluded>0</occluded>
		<bndbox>
			<xmin>457</xmin>
			<ymin>212</ymin>
			<xmax>500</xmax>
			<ymax>297</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>person</name>
		<pose>Unspecified</pose>
		<truncated>1</truncated>
		<occluded>1</occluded>
		<bndbox>
			<xmin>438</xmin>
			<ymin>173</ymin>
			<xmax>500</xmax>
			<ymax>243</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>chair</name>
		<pose>Right</pose>
		<truncated>1</truncated>
		<occluded>1</occluded>
		<bndbox>
			<xmin>351</xmin>
			<ymin>272</ymin>
			<xmax>452</xmax>
			<ymax>375</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>chair</name>
		<pose>Rear</pose>
		<truncated>0</truncated>
		<occluded>0</occluded>
		<bndbox>
			<xmin>265</xmin>
			<ymin>250</ymin>
			<xmax>353</xmax>
			<ymax>364</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>chair</name>
		<pose>Rear</pose>
		<truncated>0</truncated>
		<occluded>0</occluded>
		<bndbox>
			<xmin>189</xmin>
			<ymin>260</ymin>
			<xmax>286</xmax>
			<ymax>375</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
	<object>
		<name>diningtable</name>
		<pose>Unspecified</pose>
		<truncated>0</truncated>
		<occluded>1</occluded>
		<bndbox>
			<xmin>149</xmin>
			<ymin>224</ymin>
			<xmax>402</xmax>
			<ymax>331</ymax>
		</bndbox>
		<difficult>0</difficult>
	</object>
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
