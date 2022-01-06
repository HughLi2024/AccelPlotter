# AccelPlotter
AccelPlotter is a Python script that plots the acceleration of cars in the mobile racing game Asphalt 9: Legends. The script takes in game footage and analyses the speedometer and timer in the top right corner of the screen. By using OCR technology, the speed and time are recognised and graphed out.
Note: Use slowed down game footage to achieve more accurate results. [iGameGod](https://iosgods.com/repo/) is an iOS jailbreak package that can be used to slow down the game

## Technologies
This project is created with:
* Python 3.6
* [Pandas](https://pypi.org/project/pandas/)
* [OpenCV](https://pypi.org/project/opencv-python/)
* [ImageHash](https://pypi.org/project/ImageHash/)
* [Pillow](https://pypi.org/project/Pillow/)
* [NumPy](https://pypi.org/project/numpy/)
* [Google Cloud](https://pypi.org/project/google-cloud/) [Vision API](https://cloud.google.com/vision/)
* [Matplotlib](https://pypi.org/project/matplotlib/)

## Google Cloud Vision API
This script utilises Google Cloud's Vision OCR API to recognise characters in images.
1. [Sign up for Google Cloud](https://console.cloud.google.com/) and enable billing. [The first 1000 images per month are free](https://cloud.google.com/vision/pricing)
2. [Create a project and select Vision API](https://cloud.google.com/resource-manager/docs/creating-managing-projects)
3. [Create a service account](https://cloud.google.com/docs/authentication/getting-started) and download the JSON key
4. [Setup and initialize the Google Cloud SDK](https://cloud.google.com/sdk/docs/install)
Follow this in-depth [tutorial](https://cloud.google.com/vision/docs/ocr#set-up-your-gcp-project-and-authentication) if any issues are encountered

## Setup
To run this script:
1. Open Terminal and navigate to the local repository
2. [Set the environmental variable](https://cloud.google.com/docs/authentication/getting-started#setting_the_environment_variable) `GOOGLE_APPLICATION_CREDENTIALS`
3. Run main.py `python3 main.py`
4. Enter the directory path to the input video
5. Enter the video filename
6. Enter a project title
7. After the video frames have been split, a prompt will ask "Please manually verify if the following information is correct regarding the first frame". Verify if the information is correct, and enter "y" or "n"
8. After the video frames have been analysed by the OCR library, a prompt will ask "Please review and edit the generated spreadsheet and press ENTER to plot the data." Manually check and edit the generated spreadsheet in the created project folder, then press ENTER in the Terminal prompt
9. A graph will generated within the project folder

## Sample
- [Demo1](https://github.com/HughLi2024/accelplotter/tree/main/Demo1) is a the end result of the program by inputting a 31s gameplay video
- [Demo2](https://github.com/HughLi2024/accelplotter/tree/main/Demo2) is a the end result of the program by inputting a 1m52s gameplay video. Note that the OCR is unable to accurately determine the speed in all frames. The spreasheet was manually checked and edited. [Demonstration](https://user-images.githubusercontent.com/72953426/148393233-f7643d00-036f-4b40-9b83-3b45c8167977.mov)

## References
https://stackoverflow.com/a/33399711
https://stackoverflow.com/a/63003020
https://cloud.google.com/vision/docs/ocr

