# Ultra-small, transparent and genetically accessible vertebrate brain with rich behavior

## Analysis of vocalizations
The code provided demonstrates the detection of vocalizations generated by *Danionella translucida* and generates a plot of the acoustic waveform and the detected vocalizations.

### System requirements
All analyses of vocalizations were performed with Python 2.7.12, Numpy 1.11.0, Scipy 0.17.0 and Matplotlib 1.5.1 on a 64-bit running Ubuntu-Linux Version 16.04. 
The script has been tested exclusively on Linux. However, we anticipate that the script is runnable on Windows, Mac without changes.

No non-standard hardware is required.

### Python
For Linux users we recommend the installation of Python and the packages mentioned above via the system's package manager and the Python package manager 'pip', respectively. 
For Windows users we recommend to use the Anaconda Python distribution available at https://www.anaconda.com/download.
Typical install time: about 30 minutes, after download. 

## Demo data
Instructions on how to run our analysis scripts on demo data are provided in the folder *vocalization analysis*. For expected output see files in the sub-folder *expected_results*. Expected run time for demo on a current standard desktop computer is a few seconds.

example data: vocalization_analysis/Fig2E_raw.wav
example script: vocalization_detection.py
example command: in the script-folder run 'python vocalization_detection.py' 



## Analysis of fish movement
The code provided analyzes video files to detect fish positions and directions, and then perform a statistical analysis of the direction distribution.

The FishTracking folder contains:
•	fish_track_analysis.m – Matlab script
•	testid.avi – 10 seconds’ video excerpt for testing purpose

### System requirements
The analysis has been run using Matlab 2017b on a MacBook Pro (Processor: 3.3 GHz Intel Core i7, RAM: 16 GB) running macOS 10.12.6. No non-standard hardware is required.

### Matlab installation guide
A free trial version of Matlab can be downloaded at https://www.mathworks.com/campaigns/products/trials.
Installation time is approximately to 30 minutes. 

### Demo
Open the fish_track_analysis.m script with Matlab, make sure the Fishtracking folder is in the current path.
Run the fish_track_analysis.m script. A window opens, double-click on testvid.avi.
After a few seconds, Matlab Figure 1 appears, click and drag the pointer to define the image area that will be analyzed (we exclude here the walls of the tank).
Upon the analysis of each frame, Figure 1 will display the background-subtracted image, with overlaid red dots (fish center positions) and blue arrows (fish directions).
Three additional figures are displayed in the end: 
-	Figure 2 shows the nearest neighbor distance histograms of the original dataset (blue) and of the shuffled dataset (red). The title indicates the result if the complete spatial randomness test.
-	Figure 3 shows the distribution of fish orientations relative to the mean one, for the original dataset.
-	Figure 4 shows the distribution of fish orientations relative to the mean one, for the shuffled dataset.
Using the previously mentioned computer, running the entire script takes about 45 seconds for the test video (250 frames).



## Cell counting 
The code provided analyzes histological brain sections to detect and count single cells. 

Thresholding value (to distinguish cells from rest) has been previously manually determined using Fiji. Brain area has been defined previously using Fiji.

The CellCounting folder contains:
•	CellCounting.m – Matlab source code
•	Slice14.tif – single brain slice image (part of the 28 slices analyzed for the paper)
•	RoiSetStackRGB.zip – ZIP archive containing brain ROI information (generated using Fiji by manually circling the brain)

### System requirements
The analysis has been run using Matlab 2017b on a MacBook Pro (Processor: 3.3 GHz Intel Core i7, RAM: 16 GB) running macOS 10.12.6. No non-standard hardware is required.

### Matlab installation guide
A free trial version of Matlab can be downloaded at https://www.mathworks.com/campaigns/products/trials.
Installation time is approximately to 30 minutes. 

### Demo
Run the CellCounting.m script. Successive processing steps (thresholding, selecting, cropping, convolving, counting) will be indicated in the command window.
In the end, the script is displaying the original image (with dark background) with red crosses overlayed, indicating the position of each detected cell. The title of the image indicates the total number of cells detected in the image within the brain region. Using the previously mentioned computer, running the entire script takes about 50 seconds.
The script can eventually be run on other images, by changing the image path at the beginning of the load section. Please note that the size of the smoothing gaussian (‘sigma’), the intensity threshold (‘thrMan’) and the ROI (‘brainArea’) would then have to be manually determined for the new images.











