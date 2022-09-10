# How to use the machine learning model

## Step 1: 
Get the DEM, Satellite, Slope, and Aspect data for the region you want to use the model on (Data should be at least 10m). I recommend using https://apps.nationalmap.gov/downloader/

## Step 2: 
Click on the following link for the code to generate the files that will be used for the ML model. https://code.earthengine.google.com/db48d72a0f230c4ccc0a536f3addeac3?noload=true

What you should see(for the most part):
![image](https://user-images.githubusercontent.com/104661603/189474192-7d69fa3e-4f09-4da3-a9c6-9fde4da6054e.png)

IMPORTANT INFO: If you use the USGS link to download the data, the DEM data will be 10m, which is perfect. However, the satellite data will be 1m, which may make the file size too big for Google Earth Engine to import it. In that case, you may need to import the satellite data as separate GeoTiff files so that Google Earth Engine can handle the import. This won't be a problem, however, as there are instructions in the code as to how to deal with mutiple satellite files.

## Step 3: 
Click the "Run" button near the top of the code tab

## Step 4:
Go to Google Drive and create a folder to store your data in

Example:

![image](https://user-images.githubusercontent.com/104661603/189474428-b9e38c6c-bfe5-4213-b6a5-0d7601604759.png)

## Step 5: 
Once the code has finished running, go to the Tasks tab on the right-hand side of the screen and click the "RUN" button for the DEM task. Once the button is clicked, a prompt will pop up, asking you to enter some information. In the CRS section, enter EPSG:4326. Near the bottom, enter the Google Drive folder this data should be exported to as well as the file name. Then, click "RUN" and the process should begin.

Example:
![image](https://user-images.githubusercontent.com/104661603/189474466-6e160ff6-d078-43e7-9cb4-39313002398b.png)

## Step 6: 
Repeat Step 5 for the remaining tasks.

## Step 7:
Go to Google Drive and create 2 empty folders

Folder 1:

![image](https://user-images.githubusercontent.com/104661603/189474599-c58b5149-e2c1-44cb-b671-03403ab1be8d.png)


Folder 2:

![image](https://user-images.githubusercontent.com/104661603/189474606-999cf6c4-cb7d-48b7-8493-417c26b80f07.png)

## Step 8:
Go inside of the "Chunks" Folder and create four more empty folders, one for each input type(DEM, Satellite, Slope, Aspect)

Example:

![image](https://user-images.githubusercontent.com/104661603/189474730-fbf0e2f3-7553-46d7-bb6f-7da8e4498e50.png)

## Step 9:
Check this GitHub project and find the "FinalTalus.ipynb" file. Then, open it in Google Colab using the button.

Example:
![image](https://user-images.githubusercontent.com/104661603/189474895-3c889c88-8d9d-4a8d-aa44-85d6f8a4d9b5.png)

## Step 10:
Run the first cell (The one to import data stored in Google Drive). Do this by clicking on the cell, and then clicking on the small play button that appears on the left of the cell

Example:
![image](https://user-images.githubusercontent.com/104661603/189475018-9116b243-3376-4b11-b9ea-df9f71c673ad.png)

## Step 11:
Go through the entire file and look for the green comments. Most are instructions that will help you set up the Colab correctly. Follow all of those instructions, and then begin running each cell in order.

## Finished!
You should now have a file that displays the areas where a talus is expected to be.
