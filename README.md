# CNN_Pytorch
Pick Kaggle Datasets into Google Colab.
Prerequisite:-
Kaggle Account, Google/Colab acount.

# Step 1:Kaggle API Token
Go to Your Kaggle Account after scrolling down, click on Create New API Token.
A file named kaggle.json will get downloaded containing your username and token key.

# Step 2: Upload kaggle.json into Google Drive
Create a folder named Kaggle where you will be storing your Kaggle datasets
Upload your kaggle.json file into Kaggle folder. (Remember spelling)

# Step 3: Create new colab notebook

# Step 4: Mount the drive to colab notebook
type:- from google.colab import drive
       drive.mount('/content/gdrive')
and do all the authorization code step.
then in new code section type:-

import os
os.environ['KAGGLE_CONFIG_DIR'] = "/content/gdrive/My Drive/Kaggle"
"/content/gdrive/My Drive/Kaggle is the path where kaggle.json is present in the Google Drive"

# Step 5: Change your present working directory by typing this
%cd /content/gdrive/My Drive/Kaggle
for checking use pwd command

# Step 6: Download the kaggle dataset
Go to kaggle and copy the API Command to download the dataset
for doing above, go to the dataset which you want to download, click on 3 dot which is beside new notebook and click Copy API command

after that in colab type following code(Remember using ! at the start of API command):-
!kaggle datasets download -d alessiocorrado99/animals10

check the content by using !ls command

# Step 7: Unzip your data and remove the zip file(Type this in colab)
#unzipping the zip files and deleting the zip files
!unzip \*.zip  && rm *.zip

That's it, dataset is downloaded, you can check it in drive also!!
