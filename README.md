Welcome to ULAPPH Cloud Desktop!
===================


**ULAPPH Cloud Desktop** is a cloud desktop that runs in a browser such as Chrome, Opera and Firefox! It contains Javascript windowing system which displays contents in multiple **Windows**. The desktop can be configured to contain up to **1000 desktop categories** so you can organize your work your personal, business and any information. It automatically generates contents into **slides**, **articles**, and **media** which are automatically saved in the Google cloud. It can be used to **develop Javascript applications** such as for Internet of Things (IOT) or execute **Golang** codes.  It saves data in the cloud which means your cloud desktop is available anytime, anywhere and any device. It works in laptops, desktops, Android/IOS devices as long as they have Chrome, Opera or Firefox browsers -- no installation required except the X-Frame-Ignore extension and Cross Origin extension. 

[ULAPPH Cloud Desktop](https://www.ulapph.com/) is a web-based desktop (webtop) for your online work, publishing, and development! ULAPPH is coined from word "ulap" which means cloud and PH which means it originated from the Philippines.

![http://lh3.googleusercontent.com/rdYiJWTDIf0OUVf0cAHwgEJBdKWeFnFC0OFRdoVo8-4tpzNk3MESibvzBLoLVYxZ-8W-2gS7H9o-xzJBy2VEk0bpGZ1NFg=s900](http://lh3.googleusercontent.com/rdYiJWTDIf0OUVf0cAHwgEJBdKWeFnFC0OFRdoVo8-4tpzNk3MESibvzBLoLVYxZ-8W-2gS7H9o-xzJBy2VEk0bpGZ1NFg=s900)

> **System Requirements (part 1):** To install ULAPPH Cloud Desktop you need the following:
> - A Google account or G-Suite account
> - A Windows or Mac desktop with Office & VBA Excel
> - A Chrome, Opera or Firefox browser in laptop, desktop or mobile

> **System Requirements (part 2):** To customize ULAPPH Cloud Desktop you need the following:

> - Knowledge in Golang programming https://golang.org
> - Knowledge in Google App Engine, Google APIs, Google Cloud Platform
> - A Google account or G-Suite account
> - A Windows or Mac desktop with Office & VBA Excel
> - A Chrome, Opera or Firefox browser in laptop, desktop or mobile

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
		* http://edwin-daen-vinas.appspot.com
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
* After installation is complete, please proceed with initial setup.
	* To setup a freshly installed desktop, you can access:
		* http://edwin-daen-vinas.appspot.com/admin-setup
	* Press the green power button to start setup
	* If you received the error "ERROR: SYSTEM_SEARCH_SETTINGS does not exist yet. Go to Admin Setup to Set Search Settings.~, please access the Admin Setup and set search settings.
		* https://hornriver-leader.appspot.com/admin-setup
		* Click "Set Search Settings"
		* STEP 1 must be left as is (set as N).
		* Enter below URL in STEP 2
			* https://ulapph-sites.appspot.com
		* Click Save
		* This now means that your desktop is connected to the central search server.
* If you have no Start Menu yet, you may configure your desktop to connect to the central menu:
	* By default, your desktop will connect to the common start menu
	* To personalize it, perform the following steps:
		* Go to Admin Setup (/admin-setup)
		* Click "Edit System Top List Menu"
		* Enter the following text in the editor
			* #GET_REMOTE_DATA: http://ulapph-sites.appspot.com/media?FUNC_CODE=PLAY&MEDIA_ID=7&SID=TDSMEDIA-7
			* This means we will connect to the common menu stored in the sites server
		* If you can't edit, make sure to check that the Read Only option is unchecked
		* Once saved, click the "Update Media" icon
			* File title: System Start Menu
			* File desc: System Top List Menu
		* Click the link "Set as SYSTEM Top List Menu"
		* Close the window
		* Click the reload icon in the main desktop toolbar
* Setup the desktop categories
	* By default, your desktop will not contain any desktop categories which can be up to 1000 desktops
	* To personalize it, perform the following steps:
		* Go to Admin Setup (/admin-setup)
		* Click "Edit Categories List"
		* Enter the below sample categories
			#<Basic Desktops>
				  <option value="desktop0">0:My Ulap</option>
				  <option value="desktop1">1:Life</option>
				  <option value="desktop2">2:Education</option>
				  <option value="desktop3">3:Career</option>
				  <option value="desktop4">4:Personal</option>
				  <option value="desktop5">5:Ancestry</option>
				  <option value="desktop6">6:Awards</option>
				  <option value="desktop7">7:Inventions</option>
				  <option value="desktop8">8:Research</option>
				  <option value="desktop9">9:Toastmasters</option>
				  <option value="desktop10">10:Teaching</option>
				  <option value="desktop11">11:Companies</option>
				  <option value="desktop12">12:Travels</option>
				  <option value="desktop13">13:Books</option>
				  <option value="desktop14">14:Government</option>
				  <option value="desktop15">15:Citizenship</option>
				  <option value="desktop16">16:Certifications</option>
				  <option value="desktop17">17:Societies</option>
				  <option value="desktop18">18:Mentors</option>
				  <option value="desktop19">19:Tips&Tricks></option>
				  <option value="desktop20">20:Legacy</option>
			#</Basic Desktops>
			#
			#<Anything>
				  <option value="desktop1000">1000:Anything Under the Sun</option>
			#</Anything>
		* If you can't edit, make sure to check that the Read Only option is unchecked
		* If you just copied the above, make sure to outdent to make the first column of texts starts at the first column of editor
			* You may highlight all and press Shift + Tab
			* Then Save the editor
			* You should be directed to the"Add Desktops" screen
			* Clicking the link in third column will launch that desktop category
		* Once saved, click the "Update Media" icon
			* File title: Categories List
			* File desc: Desktop Categories List
		* Click the link "Set as Categories List"
		* Close the window
		* Click the reload icon in the main desktop toolbar

### STEP 6: Access your cloud desktop links
* After successful setup, you can now access:
	* **http://edwin-daen-vinas.appspot.com/uwm** - The main desktop
	* **http://edwin-daen-vinas.appspot.com/webapp** - The mobile webapp
	* **http://edwin-daen-vinas.appspot.com/desktops** - The listing of all desktops
	* **http://edwin-daen-vinas.appspot.com/contents** - The listing of contents
* You may use the toolbar to access the above main screens
	* Click the desktop icon to list all desktops
	* Click the globe icon to launch the website
	* Click the ULAPPH start menu to expand the menu (try launching the apps)

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
