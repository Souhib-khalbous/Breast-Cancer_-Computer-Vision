We split th0 preprocessing operation to 5 stips and each step has its own directory 

# Stage 1

1. Run Preprocessing.ipynb to save all dcm images in one folder , change input_folder with your input path,
output_path with path that point to folder 1 as in code

2. convert dcm to png files, chnage png_output variable with path that point to folder 2 (as inside code)

3. change image_folder variable with path that point ot folder 2 (like inside code), to create the csv file 
change the path of output_csv (it should be in the same root of Preprocessing.ipynb)

4. in Negative to Positive step change the input_folder variable with path that point to folder 2 (like inside the code)
change the output_folder variable to folder that point to folder 3 (in the same root of Preprocessing.ipynb)

5. Resize step: change the input_dir to path that point to folder 3, set the output_dir variable to folder 4

# Stage 2
A- run Calcification_Loaing.ipynb
    1. change the model_path variable with model path
    2. change TEST_PATH variable with path that point to folder 4
    3. create csv file and change csv_file variable with root of directory file (as inside the code) 
    this csv file contain the main sizes of images before resizing
    4. in *Create the Final CSV file for the Calcification* step chnage the csv_file variable to save the calssification model results
B- run Mass_Loading.ipynb
    1. change the model_path variable with model path
    2. change TEST_PATH variable with path that point to folder 4
    3. create csv file and change csv_file variable with root of directory file (as inside the code) 
    this csv file contain the main sizes of images before resizing
    4. in *Create the Final CSV file for the Calcification* step chnage the csv_file variable to save the calssification model results

# Stage 3
 Take the JSON file from the Classification (BI-RADS type clssification team)
    1. Define the path of the Kitle's CSV file in kitle_csv_path
    2. Define the path of the Kalsifikasyon's CSV file in kalsifikasyon_csv_path
    3. Define the path of the JSON file of the Calcification's team.
    4. Create a path for the updated JSON's file.