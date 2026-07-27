# Birdcall_Individual_Clips_Audiocondenser
This program allows the user to upload an audio clip (or an MP4) file, and uses BirdNET to create individual clips of identified birdcalls - downloadable as a .zip file at the end
# **How it works**
1. Program will install all dependencies(BirdNET model + audio tools), so that (hopefully!) no other downloading needs to take place!
2. Upload your audio file.
3. Run BirdNET to detect bird calls with timestamps and confidence scores (level can be manually changed pre-upload!)
4. Merge nearby detections and add a small padding so calls aren't cut short or repeated if calls have a small time lag in them
5. Export each merged segment as its own file, named with its start/end timestamp
6. Download all clips as a single zip.
# Quick note: using 'birdnetlib', which is just the python version of the same thing Chirpity uses - to get around access issues (and the fact that Chirpity doesn't have the function of cutting audio files!)
