# Motivation

# Methods

# How to use the machine learning model

## Step 1: Download data
Get the DEM, Satellite, Slope, and Aspect data for the region you want to use the model on (Data should be at least 10m). I recommend using https://apps.nationalmap.gov/downloader/

## Step 2: Open Google Earth Engine Code
Open the following link in a new tab for the code to generate the files that will be used for the ML model. https://code.earthengine.google.com/db48d72a0f230c4ccc0a536f3addeac3?noload=true

What you should see:
![image](https://user-images.githubusercontent.com/104661603/189474192-7d69fa3e-4f09-4da3-a9c6-9fde4da6054e.png)

IMPORTANT INFO: If you use the USGS link to download the data, the DEM data will be 10m, which is perfect. However, the satellite data will be 1m, which may make the file size too big for Google Earth Engine to import it. In that case, you may need to import the satellite data as separate GeoTiff files so that Google Earth Engine can handle the import. This won't be a problem, however, as there are instructions in the code as to how to deal with mutiple satellite files.

## Step 3: Run Code
Click the "Run" button near the top of the code tab

## Step 4: Create folder to store files
Go to Google Drive and create a folder to store your data in

What you should see:

![image](https://user-images.githubusercontent.com/104661603/189474428-b9e38c6c-bfe5-4213-b6a5-0d7601604759.png)

## Step 5: Download DEM file from GEE
Once the code has finished running, go to the Tasks tab on the right-hand side of the screen and click the "RUN" button for the DEM task. Once the button is clicked, a prompt will pop up, asking you to enter some information. In the CRS section, enter EPSG:4326. Near the bottom, enter the Google Drive folder this data should be exported to as well as the file name. Then, click "RUN" and the process should begin.

What you should see:
![image](https://user-images.githubusercontent.com/104661603/189474466-6e160ff6-d078-43e7-9cb4-39313002398b.png)

## Step 6: Download all files from GEE
Repeat Step 5 for the remaining tasks.

## Step 7: Create Chunks, Output, and MegaNumpy folders
Go to Google Drive and create 3 empty folders

Folder 1:

![image](https://user-images.githubusercontent.com/104661603/189474599-c58b5149-e2c1-44cb-b671-03403ab1be8d.png)


Folder 2:

![image](https://user-images.githubusercontent.com/104661603/189474606-999cf6c4-cb7d-48b7-8493-417c26b80f07.png)

Folder 3:

![image](https://user-images.githubusercontent.com/104661603/189577335-4c9748a2-3bbe-434e-ba46-283cd96cc7ba.png)

## Step 8: Create subfolders in Chunks folder
Go inside of the "Chunks" Folder and create four more empty folders, one for each input type(DEM, Satellite, Slope, Aspect)

What you should see:

![image](https://user-images.githubusercontent.com/104661603/189474730-fbf0e2f3-7553-46d7-bb6f-7da8e4498e50.png)

## Step 9: Download model
Check this GitHub project and find the "model.h5" file. Download that file, and save it to Google Drive.

## Step 10: Open Colab
Check this GitHub project and find the "FinalTalus.ipynb" file. Then, open it in Google Colab using the button.

Example 1:

![image](https://user-images.githubusercontent.com/104661603/189475166-ef1424a3-53a6-420d-9def-8dde339c801a.png)


Example 2:
![image](https://user-images.githubusercontent.com/104661603/189474895-3c889c88-8d9d-4a8d-aa44-85d6f8a4d9b5.png)

## Step 11: Give Colab access to Google Drive
Run the first cell (The one to import data stored in Google Drive). Do this by clicking on the cell, and then clicking on the small play button that appears on the left of the cell. Then, follow the instructions.

What you should see:

![image](https://user-images.githubusercontent.com/104661603/189475018-9116b243-3376-4b11-b9ea-df9f71c673ad.png)

## 

## Step 12: Run all code in Colab
Go through the entire file and look for the green comments. Most are instructions that will help you set up the Colab correctly. Follow all of those instructions, and then begin running each cell in order.

IMPORTANT INFO: Most of the directions are regarding finding a path to a certain Google Drive file or folder. In order to find that path, click on the files tab to the left and choose the correct drop down options to get to your folder/file. Then, click on the three dots next to the file/folder name and click "Copy path". This will copy the path name to your clipboard, so you can just paste it where required.

Example:

![image](https://user-images.githubusercontent.com/104661603/189475378-23281fc5-7a90-4041-9fda-f96988d0aeb4.png)

## Finished!
You should now have a file that displays the areas where a talus is expected to be in the output folder you previously made. It is a jpg, though, so unfortunately, there won't be any geographical data stored.
