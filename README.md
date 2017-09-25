# OpenSourceTractor_CV
The computer vision software for the open source tractor developed by the open-source ecology

The code is written in python and with the aid of the open computer vision library, open CV2 in python.

It is intended to be downloaded on Raspberry Pi Zero W equipped with a Pi Cam.

The big picture of the code functionality is that it should be able to predict the correct orientation the tractor should follow. it should be able to detect multiple "white" (I guess it needs to be changed to a florecent color) markers digged in the ground to determine the orientation it needs to follow, and to be able to weed the row of plants efficiently. To eliminate the effect of fidelity in recognition, the camera should be installed over a gimbal free for the roll and pitch, but not the yaw angle.

After determining the orientation, the RPi needs to be compare the data with the gyroscope readings to make sure that the tractor is on the right track.

In regards to the gyroscope, it needs to be calibrated at the beginning of the field with special markers, and then the rest of the field should follow this calibration. Knowing that the tractor is solar powered, and that it can not finish the field in a single day, we are expecting the system to be able to store the information about its position and and orientation at the end of each session to recoved on the beginning of the next session.

A feature that can be added later on is a perspective trasform of the the camera readings to form a Top-view, 2D map of the field.
