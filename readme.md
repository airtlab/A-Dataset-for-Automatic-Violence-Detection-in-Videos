
# A Dataset for Automatic Violence Detection in Videos

This repository contains 350 video clips labelled as “non-violent” and “violent”, to be used to train and test algorithms for violence detection in videos. The non-violent clips are specifically recorded to include behaviours (hugs, claps, exulting, etc.) that can cause false positives in the violence detection task, due to fast movements and the similarity with violent behaviours.

## Data Description

The dataset is split into two main directories, “non-violent” and “violent”, labelling the included clips as showing non-violent behaviours and violent behaviours respectively.

	 violence-detection-dataset
	  ├─ non-violent
	  │   ├─ cam1 (60 .mp4 clips)
	  │   └─ cam2 (60 .mp4 clips)
	  └─ violent 
	      ├─ cam1 (115 .mp4 clips)
	      └─ cam2 (115 .mp4 clips)
		  
The directories are split into two subdirectories, “cam1” and “cam2”:
-  “non-violent/cam1” includes 60 clips representing non-violent behaviours;
-  “non-violent/cam2” includes 60 clips with the same non-violent behaviours in “non-violent/cam1” but recorded with a different camera and from a different point of view;
-  “violent/cam1” includes 115 clips representing violent behaviours;
-  “violent/cam2” includes 115 clips with the same violent behaviours in “violent/cam1” but recorded with a different camera and from a different point of view.

An additional labelling is provided in three csv files available in the main data repository directory (violence-detection-dataset):
-  “action-class-occurrences.csv” lists all the actions recorded in the clips, with the number of times each action occurs in the dataset and a label to explain if the action is violent (y) or not (n);
-  “non-violent-action-class.csv” lists the actions included in each non-violent clip;
-  “violent-action-class.csv” lists the actions included in each violent clip.

The 350 clips in the dataset are MP4 video files (H.264 codec) of an average length of 5.63 seconds, with the shortest video lasting 2 seconds and the longest 14 seconds. For all the clips, the resolution is 1920 x 1080 pixels and the frame rate 30 fps.

The clips were recorded with two cameras placed in two different spots, building a dataset with videos from two different points of view. The cameras are:
-  The front camera of the Asus Zenfone Selfie ZD551KL (13 MP, Auto Focus, f/2.2).
-  The TOPOP Action Cam OD009B (12 MP, fisheye lens 170°).

All the clips were recorded in the same room, with natural lighting conditions. The Asus Zenfone was placed in the top left corner in front of the door, while the Action Cam was placed in the top right corner on the door side. All the performed actions and behaviours were recorded with both cameras. Therefore, all the clips with the same label and name, but in different final directories (for example “non-violent/cam1/1.mp4” and “non-violent/cam2/1.mp4”) represent the same action, recorded from two different perspectives (the “cam1” directory identifies the Asus Zenfone, while the “cam2” directory identifies the Action Cam).

The clips were performed by a group of non-professional actors, varying from 2 to 4 per clip. For the violent clips, the actors were asked to simulate actions frequent in brawls, such as kicks, punches, slapping, clubbing (beating with a cane), stabbing, and gunshots. For the non-violent clips, the actors were asked to simulate actions which can result in false positives by violence detection techniques due to the speed of movements or the similarity with violent actions. Specifically, the non-violent clips include actions such as hugging, high fives and clapping, exulting, and gesticulating.

## Dataset Release Agreement

The dataset is freely released for research and educational purposes. Please cite as
- M. Bianculli, N. Falcionelli, P. Sernani, S. Tomassini, P. Contardo, M. Lombardi, A.F. Dragoni, A dataset for automatic violence detection in videos, Data in Brief 33 (2020). doi:10.1016/j.dib.2020.106587.
	 
Bibtex entry:

	 @article{Bianculli2020,
	  title = "A dataset for automatic violence detection in videos",
	  journal = "Data in Brief",
	  volume = "33",
	  pages = "106587",
	  year = "2020",
	  doi = "10.1016/j.dib.2020.106587",
	  author = "Miriana Bianculli and Nicola Falcionelli and Paolo Sernani and Selene Tomassini and Paolo Contardo and Mara Lombardi and Aldo Franco Dragoni",
	 }

The paper is open access and available here <https://www.sciencedirect.com/science/article/pii/S2352340920314682>.

## Comparative Tests on the Dataset

We compared the accuracy of 13 different neural network-based architectures on the proposed dataset. The results are published in
>P. Sernani, N. Falcionelli, S. Tomassini, P. Contardo and A. F. Dragoni, "Deep Learning for Automatic Violence Detection: Tests on the AIRTLab Dataset," in IEEE Access, vol. 9, pp. 160580-160595, 2021, doi: 10.1109/ACCESS.2021.3131315.

The paper is open access and available here <https://ieeexplore.ieee.org/document/9627980>.