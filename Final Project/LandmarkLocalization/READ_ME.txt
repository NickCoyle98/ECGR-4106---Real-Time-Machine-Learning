Items and their purpose:
	Python:
		CustomData.py:
			Contains a class for the Noise v.s Face dataloader and a generic binary
			classifier dataloader (used for front v.s. profile).
		csv_adjusters.py:
			a library of functions for cleansing unwanted data in a dataframe, shifting landmarks, 
			and concatenating/cleansing multiple dataframes. Also includes a function to split
			front and profile views from the master CSV and create a new CSV for each view.

	Jupyer Notebooks:
		CustomData.ipynb:
			The notebook version of the .py file.
		fix_csv.ipynb:
			The notebook version of the csv_adjusters.py file.
		create_noise_samples.ipynb:
			A notebook for generating the face v.s. no face dataset. Augments thermal images with
			noise and creates an equal amount of noise images for the "no face" class.
		FrontVsProfileTest.ipynb:
			A simple training of a simple CNN on the front vs. profile view dataset.
		NFTestRun.ipynb:
			A simple training of a simple CNN on the face vs. no face dataset.
		image_folder_to_video.ipynb:
			A script to convert a folder of images into a video.
		landmarks_test.ipynb:
			The initial attempt at landmark localization using the Pytorch tutorial.
		Shift_Landmarks_demo.ipynb:
			A script that demos the function used to shift landmarks back into correct position.
		Thermal_Landmarks_front_V2.ipynb:
			The second attempt at thermal landmark localization training for front view samples.
		Thermal_Landmarks_profile_V2.ipynb:
			The second attempt at thermal landmark localization training for profile view samples.

	Folders:
		Master: 
			Create this folder and store all images here, including thermal, rgb, .tiffs, etc
			from the UNCC thermal landmark dataset.
		Noise&Face:
			Create this folder and two subfolders "test" and "train" for storing images related to
			the Face v.s. No Face training.
		Noise&Face_CSV:
			Create this folder and the CSV related to Face v.s No Face are stored here.
		Thermal_only:
			Create this folder and place only images beginning with "N" from the UNCC thermal
			landmark dataset.
		"progress" folders:
			These folders contain images from the validation steps from the thermal landmark
			localization trainings.

	CSVs:
		Master:
			A cleansed concatenation of all landmark annotations CSVs.
		Master_front:
			Only contains front view annotations.
		Master_profile:
			Only contains profile view annotations.
		frontVSprofile:
			Contains label information for front v.s. profile view training.
		CSVs beginning with "S":
			Annotations pertaining to particular subjects, these are raw and contain errors.
			This information without error is contained in the "Master" CSV.