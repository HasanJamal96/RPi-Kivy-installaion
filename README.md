# RPi-Kivy-installaion

Update RPi

	$ sudo apt-get update && sudo apt-get -y upgrade
	$ sudo reboot
	$ sudo nano /etc/apt/sources.list
  
At the end of file, add the APT sources for Gstreamer:

	deb http://vontaene.de/raspbian-updates/ . main
	
  
Now run these commands

	$ gpg --keyserver pgp.mit.edu --recv-keys 0C667A3E
	$ gpg -a --export 0C667A3E | sudo apt-key add -
	
if above 2 commands didnot work use the following
	
	$ gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv 9A2FD067A2E3EF7B
	$ gpg -a --export 9A2FD067A2E3EF7B | sudo apt-key add -

	
	$ sudo apt-get update
	
	$ sudo apt-get -y install pkg-config libgl1-mesa-dev libgles2-mesa-dev \
  	python3-pygame python3-setuptools libgstreamer1.0-dev git-core \
  	gstreamer1.0-plugins-{bad,base,good,ugly} \
  	gstreamer1.0-{omx,alsa} python3-dev
 
	$ sudo apt-get install libsdl2-dev libsdl2-image-dev libsdl2-mixer-dev libsdl2-ttf-dev
	
	$ sudo apt-get install python3-pip

  	$ python3 -m pip install --upgrade --user Cython==0.29.10 pillow

	$ sudo pip3 install cython pygments docutils
	
	$ git clone https://github.com/kivy/kivy
	$ cd kivy
	$ python3 setup.py build
	$ sudo python3 setup.py install
	
	
	$ nano ~/.kivy/config.ini
	
In modules section add

	cursor=1
