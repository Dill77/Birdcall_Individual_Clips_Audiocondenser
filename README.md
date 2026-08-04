# Birdcall_Individual_Clips_Audiocondenser
This program allows the user to upload an audio clip (or an MP4) file, and uses BirdNET to create individual clips of identified birdcalls - downloadable as a .zip file at the end. Please open the code in Colab as prompted - then "run all", look for the end of the first main codeblock for the prompt to upload a file and just wait for 30-40mins ish per hour of audio uploaded. If you encounter any errors, there is a small codeblock beneath the main one with --Applying fixes--; run that cell, then restart the session and run all again.
# **How it works**
1. Program will install all dependencies(BirdNET model + audio tools), so that (hopefully!) no other downloading needs to take place!
2. Upload your audio file.
3. Run BirdNET to detect bird calls with timestamps and confidence scores (level can be manually changed pre-upload!)
4. Merge nearby detections and add a small padding so calls aren't cut short or repeated if calls have a small time lag in them
5. Export each merged segment as its own file, named with its start/end timestamp
6. Download all clips as a single .zip file
# Quick note: using 'birdnetlib', which is just the python version of the same thing Chirpity uses - to get around access issues (and the fact that Chirpity doesn't have the function of cutting audio files!) Please note that this is currently extremely slow to run, but can be cloned and run on multiple windows for different files simultaneously to make it worth it!
Apologies that the Latitude and Longitude inputs are currently bugged - leave as 'none' the identification of the bird calls is unimportant for the clipping feature to work - only its classifications will be less likely to be correct and will need manual validation.
# Note about v2:
Version 2 is identical in every way to v1, besides the added functionality to also receive a randomised selection of background audio clips (not containing the bird call). This part was added afterwards due to the need for more background clips for the retrained Perchv2 ML model epoch 2 after initial seeding for more training data!
