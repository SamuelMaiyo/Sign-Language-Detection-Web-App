# sign-language-detection-web-app
This is simple web app that allows sign detection and translation to text and to speech at the click of a button.

#Hand Detection and Tracking
Mediapipe is used to track the key points on the human hand. This model precisely localizes 21 3D hand-knuckle coordinates i.e., x, y, z-axis, inside the detected hand regions.

# Sign Extraction
After hand detection and tracking, this model is passed over the dataset. Considering the American Sign Language dataset, we have a to z alphabets. The detection model is passed over every alphabet directory containing images. The model compares the obtained landmark points with all the letters of the alphabet and determines the one with the highest probability. Once the model extracts the feature and determines the alphabet with the highest probability, the landmarks turn green

# Conversion to Text and Speech
The label with the highest probability is recognized to be the predicted label and is displayed as text in the OpenCV feed. The recognized letters and words are converted into the corresponding speech using the pyttsx3 library.

# Web application Integration
A web application was created using flask. This creates a user-friendly interface where users can be able to access the sign language translation system easily. The web application was linked with system in the back-end and with a click of a button, the system will start running and display an OpenCV window.
