Welcome to ULAPPH Cloud Desktop!
===================


We are now releasing **ULAPPH Cloud Desktop**. It was designed to look & work like a desktop computer only that it runs in a browser such as Chrome, Opera and Firefox! It displays contents into **Windows** which can be configured via **Settings**. It can contain up to **1000 desktops** so you can organize your work easily. It automatically generates contents into **slides**, **articles**, **media** which are saved in the cloud. It can be used to **develop Javascript applications** such as for Internet of Things (IOT).  It saves data in the cloud which means no problem if you spill coffee on your device. You can just open your ULAPPH Cloud Desktop anytime, anywhere and any device such as Windows desktop, Android smartphone or tablets. 

[ULAPPH Cloud Desktop](https://www.ulapph.com/) is a web-based desktop (webtop) for online work, publishing, and development! ULAPPH is coined from word "ulap" which means cloud and PH which means it originated from the Philippines.

![http://lh3.googleusercontent.com/rdYiJWTDIf0OUVf0cAHwgEJBdKWeFnFC0OFRdoVo8-4tpzNk3MESibvzBLoLVYxZ-8W-2gS7H9o-xzJBy2VEk0bpGZ1NFg=s900](http://lh3.googleusercontent.com/rdYiJWTDIf0OUVf0cAHwgEJBdKWeFnFC0OFRdoVo8-4tpzNk3MESibvzBLoLVYxZ-8W-2gS7H9o-xzJBy2VEk0bpGZ1NFg=s900)

> **System Requirements:** To install ULAPPH Cloud Desktop you need the following:

> - Knowledge in Golang
> - Knowledge in Google App Engine, Google APIs, Google Cloud Platform
> - A Google account or G-Suite account
> - A Windows or Mac desktop with Office & VBA Excel

----------


Installation
-------------

ULAPPH Cloud Desktop installation has two phases:
- **Phase 1** - Setting up the Google Project ID which can be done automatically or manually
- **Phase 2** - Installing the ULAPPH Cloud Desktop software to the Google Project ID

### STEP 1: Automatically create your server name or project ID in Google Cloud
* Visit http://www.ulapph.com
	* Login using your Google or G-Suite account
	* Scroll down to see the App Engine Installer button
	* Click the App Engine installer button
	* Create your Google Project ID which can be the name of your business, your name or your pets name
	* Example: If I created "edwin-daen-vinas" as my project ID, the URL of my webtop will be: 
		* http://edwin-daen-vinas.appspot,com
* After the project ID is created in Google Cloud, you should be redirected to this page.

### STEP 2: Download the needed source codes
* Download the ULAPPH Cloud Desktop source codes which contain Golang, HTML, CSS, JS, etc
	* TBD

### STEP 3: Download the local installer
* Download the Excel file with contains macro to automate installation or upgrades
* Configure the installer
	* TBD

### STEP 4: Add row in the installer for new servers
* If the ULAPPH server is new, we need to add a row in the installer
* Update the row to contain the details of the new server
* Press F5 to install which calls appcfg.py
* Login if prompted by Ouath2 login and follow the screen instructions
* After a couple of minutes, your cloud desktop will be installed
* TBD

### STEP 5: Setup the cloud desktop start menu, sites server etc
* After installation, we need to setup the cloud desktop to connect to the central sites server.
	* If you have no central sites server yet, you can connect to:
		* https://ulapph-sites.appspot.com
* If you have no Start Menu yet, you may configure your desktop to connect to the central menu:
	* TBD
* Setup the desktop categories
	* TBD

### STEP 6: Access your cloud desktop
* After successful setup, you can now access:
	* **/uwm** - The main desktop
	* **/webapp** - The mobile webapp
	* **/desktops** - The listing of all desktops
	* **/contents** - The listing of contents

### STEP 7: Upgrading your desktop
* Download the latest release
	* TBD
* Open the local installer & press F5 to install/upgrade
	* TBD 

### STEP 8: Contribute your ideas and codes
* You may first test your change in your own cloud desktop
* Then request a pull request
* TBD

### ULAPPH Setup

You can setup ULAPPH Cloud Desktops as individual desktops connected to a central sites server. The central sites server will contain the shared menu, themes, monitoring, logging, etc. The central sites server and the individual cloud desktops are all running ULAPPH Cloud Desktops. 

```sequence
server1.appspot.com -> sites.appspot.com: Conntects to central server
server2.appspot.com -> sites.appspot.com: Conntects to central server
installer.appspot.com -> server1.appspot.com: Auto creates project ID
local installer -> server1.appspot.com: Installs the software to cloud
```

### Screenshots

![enter image description here](https://lh3.googleusercontent.com/oWeiwR9uf3r0N5PXLcEBYBj56ZWPdXDBx06xkdnLEzt_YGkOOdNdVCTmO6XPKxe_915vTwl3JXO4h_ANwOvdEzz_RAc8BFU=s900)

![enter image description here](https://lh3.googleusercontent.com/OGZjALz1lCM9TKHd11Hc5cEE9XuNUPIcFaYKqD7-sb4Aoresi7-S60dJXgvmQfhnQDiyTuSWR8l3Ullvst6sA_n0KUkJ0A=s900)

![enter image description here](http://lh3.googleusercontent.com/fNMF_rr2NwTBg1_dbd-bKeOPz_HAjBFtOa3HztBrE7jFS7ojnOPQ5SgJvlaA3XqZwcgJUp0j3_piDZ0ph3h0ws9gpmQ66w=s900)

![enter image description here](https://lh3.googleusercontent.com/WkV7BkGU8anaCn3OqpkRfRbBc-9k_wZVzCPQV-Rs_605F2P12tfqdC7Uv6B0yFUvSMzSol-e62679GvJsRMUb82Vi8cl=s900)
