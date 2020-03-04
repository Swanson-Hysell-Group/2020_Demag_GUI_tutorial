# PmagPy Demag GUI tutorial for the 2020 MagIC workshop

## Prior to tutorial

### Download the Pmag_GUI executable program 

Download the latest release of the PmagPy GUI software:

Mac:
https://github.com/PmagPy/PmagPy-Standalone-OSX/releases/tag/4.2.25

*The first time you open the Mac version, you need to right-click and select open. Double-clicking will not open as we are not Apple-verified developers.*

Windows:
https://github.com/PmagPy/PmagPy-Standalone-Windows/releases/tag/4.22.4

*You may need to click through a warning about unidentified developers.*

Linux:
https://github.com/PmagPy/PmagPy-Standalone-Linux/releases

Note that the software, particularly the Windows version, can take a long time to load. Be patient.

### Download this repository

Download and unpack the .zip of this repository so that you have the raw data that we will be working with.
https://github.com/Swanson-Hysell-Group/2020_Demag_GUI_tutorial/archive/master.zip

## Tutorial instructions

### Data conversion to MagIC format

In this example, we can going to convert data for one site that is a lava flow within the ca. 1084 Ma Michipicoten Island volcanics. These data were published in https://doi.org/10.1130/L580.1 with data that have been contributed to the MagIC database https://earthref.org/MagIC/11883. For the example we will work through, the data are not yet in MagIC format, but rather in the CIT lab format which includes a .sam site level file and ascii sample text files as described here: http://cires1.colorado.edu/people/jones.craig/PMag_Formats.html. While the specifics of this workflow will vary with different lab formats, this demonstration will show how Pmag_GUI can be used to convert data to MagIC format using the following steps:

1. Open the Pmag GUI executable program
2. Navigate to 2020_Demag_GUI_tutorial/data folder that has the SS21 folder and .sam file in it.
3. Click on *1. Convert magnetometer files to MagIC format* in the Pmag GUI home window
<img src="/images/Pmag_GUI_home.png" width="500"/>
4. The files that we are dealing with are CIT format. In the *step 1: choose file format* window, click the button for CIT format and then click *Import file*
<img src="/images/Convert_Step1.png" width="300"/>
5. In the PmagPy CIT file conversion window, add the SS21-.sam file and then choose the sampling particulars. Specify the sample-site naming convention to be XXXX-YY. Specify the number of terminal characters that distinguish specimen from sample (1). Enter the location name (in this case Michipicoten Island). When all of this information is entered, press ok.
<img src="/images/Convert_CIT_options.png" width="500"/>
6. Click on Go to next step in the step 1 dialog box.
7. Click OK in the *Step 2: Combine different MagIC files* box. 
8. Click OK in the *Step 3: Combine different MagIC formatted files* box. 

Following these steps, 

## Data visualization and analysis of the converted data

1. You will now be returned to the main Pmag GUI page. Click on the blue Demag GUI button to launch the visualization and analysis tools for these demagnetization data.
<img src="/images/Demag_GUI_panel.png" width="700"/>
2. Let's make fits to the high-temperature component that dominantly unblocks between 400ºC and 580ºC. To make a fit you can click add fit or double-click in the box that lists the steps. You can adjust the bounds of the fit by double-clicking in the steps box or by selecting the upper and lower bounds from the drop-down windows. You can change the name of the fit by selecting the default fit name *Fit 1*, changing the name and pressing enter. Perhaps you want to call this the **HT** (high-temperature fit) as there is also a low-temperature component.
3. Let's go through and make HT fits for all the samples in the site.
4. We can visualize fits for all the specimens in the site and calculate the Fisher mean by choosing the Display Level and the Mean Options in the upper right.
<img src="/images/Demag_GUI_site_mean.png" width="700"/>
5. Let's go through and make fits for the component that is removed at lower unblocking temperatures for all the samples in the site. We can call it the LT component.
6. Once we have made the fits, let's look at them in the Tools > Interpretation Editor view which can be helpful.

## Converting to MagIC format

1. The parameters for the least-squares fits can be saved into a lightweight file called a .redo file that specifies the bounds, the fit name, the fit type and the color. Let's save and have a look at that file.
2. To get these fits saved into MagIC format, we go to File > Save MagIC tables in Demag_GUI. We have some choices to make. In this case, it makes sense to save the directions in both geographic and tilt-corrected coordinates.
3. Once you have saved the MagIC tables out of Demag_GUI, close the Demag_GUI window which will bring you back to the Pmag_GUI window. Here you can click the green button *Create MagIC txt file for upload*.
