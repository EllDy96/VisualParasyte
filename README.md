# Synesthetic

## What is Synesthetic?

The goal of Synesthetic is to create a colorful and dynamic visual representation of a rhythmic musical piece. The user is required to upload an audio file containing of a rhythmic recording, e.g. a drum recording. A rhythmic analysis then is performed on the track, which separates the contributions of the different periodicities present in the rhythm, so that each periodicity can give a separate contribution to the visualization. This makes Synesthetic an informative tool for rhythm visualization. We encourage the user to upload polyrhythmic and polymetric tracks for a more interesting visual experience.

## How does this "colorful representation" actually look?

We chose to take inspiration from the famouse painter Piet Mondrian. We imagined our representation as a Mondrian-like composition which reacts to the rhythmic events by vibrating, pulsating in color, and so on. We prepared a demo which shows you the representation based on drum track of "Sound of Muzak" by Porcupine Tree.   

[![](http://img.youtube.com/vi/CIWOzm0pQt0/0.jpg)](http://www.youtube.com/watch?v=CIWOzm0pQt0 "")


## Give me some implementative details!

The code of Synesthetic is divided into two main parts:
1. Backend (implemented in Python): receives the audio track uploaded by the user, performs the rhythmic analysis and stores a compact representation of the rhythmic content inside a JSON file. Polyrhythms and polymeters are supported. Both the audio track and the JSON file are then retrieved by the frontend.
2. Frontend (implemented in JavaScript): takes in the data generated by the backend and generates the representation. The various animations of the representation are triggered in sync with the rhythmic events of the musical piece.

Python and Javascript are integrated using Flask, which instantiates a web server (see https://flask.palletsprojects.com/en/1.1.x/installation/ and https://palletsprojects.com/p/flask/)

## How to run Synesthetic / I want to know more details about the code!
To run synesthetic, you'll have to instantiate the Flask server, either locally on a server. Please follow the instructions located in the README of the src/ folder. The README also contains further details of the implementation, to make your journey through the code even easier.
