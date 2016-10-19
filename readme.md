S5K4EC fixed driver for linux
=============================

This is S5K4EC driver (for Pine camera) with some fix to work in linux.

Working window sizes (guvcview tested) in VIDEO_MODE:
- QSXGA: 2592x1936
- QXGA: 2048x1536
- 1080P: 1920x1080
- UXGA: 1280x960
- 720P: 1280x720
- VGA: 640x480

Usage
=====

- remove any previously loaded driver, type in the command line:


	sudo modprobe -r -f vfe_v4l2

	sudo modprobe -r -f s5k4ec


- load the driver


	sudo modprobe s5k4ec

	sudo modprobe vfe_v4l2


-  or put it in /etc/modules 

	edit and write the lines in this order:


	sudo modprobe s5k4ec

	sudo modprobe vfe_v4l2


* known issues

	pulling the images with a v4l2 capture image was possible for the following win sizes:

	UXGA: 1280x960

	720P: 1280x720

	VGA: 640x480

	this needs to be investigated, but does not seem to be driver issue because guvcview gets video from all available win sizes.

	

This was tested with guvcview and cap, you can try motion and see if it works as expected.

History Log:
* initial commit, fix

