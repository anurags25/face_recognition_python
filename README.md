# Face Recognition w/ Python

## Methodology:

webcam_recognize.py consists of 3 functions: 
>train(), get_webcam() and recognize_faces().

The train() function looks for sample images in test_images/, loads them, normalizes them w/ dlib and saves the encodings extracted using OpenFace to a list (known_face_encodings) with the name person in the image in the corresponding index of another list (known_face_names).

The get_webcam() function simply returns the reference to the default webcam using OpenCV.

Recognize_faces() iterates through every alternate frame of the webcam stream, scales it down to 1/4th size for faster processing. In every processed frame, the face is recognized and encoded extracted much like in the train() method. This encoding is then compared to previously extracted (i.e. "known") encodings by calculating the Euclidean distance between the candidate encoding and all the faces in our dataset.

## Resources:
OpenCV
dlib (pip install dlib)
face_recognition (pip install face_recognition)

## Usage:
(Make sure the 'test_images' child directory is set up)

$pip install dlib

$pip install face_recognition

$python3 webcam_recognize.py

## Demo:
{The link is password protected}

https://vimeo.com/285331937

password: InternshipTask@AbsoluteFace.xyz
