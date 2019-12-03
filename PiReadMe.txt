
1. First, update your Pi.

    sudo apt-get update
    sudo apt-get upgrade

2. Update Raspberry Pi firmware.

    sudo rpi-update

3. Install dependencies:
    sudo apt-get install build-essential cmake pkg-config
    sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
    sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
    sudo apt-get install libxvidcore-dev libx264-dev
    sudo apt-get install libgtk2.0-dev libgtk-3-dev
    sudo apt-get install libatlas-base-dev gfortran
    sudo apt-get install libqtgui4
    udo modprobe bcm2835-v4l2
    sudo apt-get install libqt4-test

4. Install Python 3 and Pip3:
    sudo apt-get install python3-dev
    sudo apt-get install python3-pip

5. Install Darknet
    git clone https://github.com/pjreddie/darknet.git
    cd darknet
    make

6. Compiling Darknet with OpenCV. Make sure you have openCV installed.
    Locate the "makefile" in darknet directory and change the value: 

        OPENCV=1


7. Create Virtual Environment
    python3 -m venv /path/to/new/virtual/environment

8. Activate Virtual Environment
    source ~/PATH/bin/activate

9. check python and pip versions within venv
    python --version
    pip --version 

10. Install numpy
    sudo pip3 install numpy

10. download "TestImages" and plasticClassifier.py from the GitHub repo: "https://github.com/Chadd-G/The_Dump"
    Place plasticClassifier.py and the images from "TestImage" in the same folder, within your Venv.

11. Execute the script "plasticClassifier.py" on one of the test images: 

        python3 plasticClassifier.py --image 782.jpg 

12. The script should execute in roughly 25 seconds and output a txt file with the weights, as well as a label imaged
with bounded boxes around the identified objects. 
