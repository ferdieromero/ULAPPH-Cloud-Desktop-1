ULAPPH Cloud Desktop - Installation Guide using the VBA Installer Tool
=============

ULAPPH Cloud Desktop installation has two phases:
- **Phase 1** - Automatic creation of Google Project ID which creates your desired https://your-server-name.appspot.com. This covers STEP 1.
- **Phase 2** - Installing the ULAPPH Cloud Desktop source codes to the Google Project ID using the Excel-based installer. This covers STEP 2 to STEP 8.

### STEP 1: Automatically create your server name or project ID in Google Cloud
* Visit https://ulapph-installer.appspot.com/compile?COM_FUN=INSTALL
	* Login using your Google or G-Suite account
	* Create your Google Project ID which can be the name of your business, your name or your pets name or accept the suggested name
	* Example: If I created "edwin-daen-vinas" as my project ID, the URL of my webtop will be: 
		* http://edwin-daen-vinas.appspot.com
* After the project ID is created in Google Cloud, you should be redirected to this page.

### STEP 2: Download the needed source codes
* Download the ULAPPH Cloud Desktop source codes which contain Golang, HTML, CSS, JS, etc
	* https://github.com/ulapph/ULAPPH-Cloud-Desktop

### STEP 3a: Download the VBA Excel installer tool
* Download the Excel file with contains macro to automate installation or upgrades
	* https://github.com/ulapph/ULAPPH-Cloud-Desktop-VBA-Installer
* Configure the installer such as the email address, Google project ID and the installation paths
* Directory Structure must be correct
* You can create a main folder such as **C:\Users\your-folder-name\ulapph**
* Create a folder under the above named **ulapph-cloud-desktop** so you will have **C:\Users\your-folder-name\ulapph\ulapph-cloud-desktop**
* Download the sources from **https://github.com/Accenture/ULAPPH-Cloud-Desktop** to the **ulapph-cloud-desktop** folder
* Configure the installer with the correct paths above
* (Later, you can configure all other credentials -- sorry no docs yet about this)

### STEP 3b: First time installer setup
* For first time users which already has a new Google Project ID...
* Once you have opened the Excel tool and VBA is enabled, we can just find & replace the existing row
* Find and replace the owner email address from **demo.ulapph@gmail.com** to your **google-email-address@gmail.com**
* Find and replace the Google Project ID from **hornriver-leader** to **your-server-name**
* Make sure to check the correct directory structure and put it in the installer
* Press F5 to install which calls appcfg.py or you can right click to access the installer menu
* Login if prompted by Ouath2 login and follow the screen instructions
* After a couple of minutes, your cloud desktop will be installed to your Google Project ID
* Note if you encountered some issues on missing libraries, execute the go get script

```
./gogetall.sh
```

### STEP 4: For existing installer, add row in the installer for new servers
* If the ULAPPH server is new, we need to add a row in the installer
* Update the row to contain the details of the new server
* Make sure you update the columns appropriately
* Press F5 to install which calls appcfg.py or you can right click to access the installer menu
* Login if prompted by Ouath2 login and follow the screen instructions
* After a couple of minutes, your cloud desktop will be installed to your Google Project ID

### STEP 5: Setup the cloud desktop start menu, sites server etc

#### Step 5a
* After installation is complete, please proceed with initial setup.
	* To setup a freshly installed desktop, you can access:
		* http://edwin-daen-vinas.appspot.com/admin-setup
	* Press the green power button to start setup. This will configure your fresh ULAPPH Cloud Desktop installation. Do this only once.
	* If you received the error "ERROR: SYSTEM_SEARCH_SETTINGS does not exist yet. Go to Admin Setup to Set Search Settings.~, please access the Admin Setup and set search settings.
		* https://your-server-name.appspot.com/admin-setup
		* Click "Set Search Settings"
		* STEP 1 must be left as is (set as N).
		* Enter below URL in STEP 2
			* https://ulapph-sites.appspot.com
		* Click Save
		* This now means that your desktop is connected to the central search server.
		
#### Step 5b
* If you have no Start Menu yet, you may configure your desktop to connect to the central menu
	* By default, your desktop will connect to the common start menu
	* To personalize it, perform the following steps:
		* Go to Admin Setup (/admin-setup)
		* Click "Edit System Top List Menu"
		* Enter the following text in the editor
			* #GET_REMOTE_DATA: http://ulapph-sites.appspot.com/media?FUNC_CODE=PLAY&MEDIA_ID=7&SID=TDSMEDIA-7
			* This means we will connect to the common menu stored in the central sites server
		* If you can't edit, make sure to check that the Read Only option is unchecked
		* Once saved, click the "Update Media" icon
			* File title: System Start Menu
			* File desc: System Top List Menu
		* Click the link "Set as SYSTEM Top List Menu"
		* Close the window
		* Click the reload icon in the main desktop toolbar
		
#### Step 5c
* Setup the desktop categories
	* By default, your desktop will not contain any desktop categories. You can define up to 1000 desktops!
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
				  <option value="desktop21">21:Golang-Programming</option>
			#</Basic Desktops>
			#
			#<Anything>
				  <option value="desktop500">500:My-Hobbies</option>
				  <option value="desktop1000">1000:Anything Under the Sun</option>
			#</Anything>
		* If you can't edit, make sure to check that the Read Only option is unchecked
		* If you just copied the above, make sure to outdent to make the first column of texts starts at the first column of editor
			* You may highlight all and press Shift + Tab
			* Then Save the editor
			* You should be directed to the "All Desktops" screen
			* Clicking the link in third column will launch that desktop category
		* Once saved, click the "Update Media" icon
			* File title: Categories List
			* File desc: Desktop Categories List
		* Click the link "Set as Categories List"
		* Close the window
		* Click the reload icon in the main desktop toolbar

### STEP 6: Access your cloud desktop links
* Install browser extensions
	* For Chrome, here are the two extenstions that you need to install:
		* Allow-Control-Allow-Origin (https://chrome.google.com/webstore/detail/allow-control-allow-origi/nlfbmbojpeacfghkpbjhddihlkkiljbi?utm_source=chrome-app-launcher-info-dialog)
		* Ignore X-Frame headers (https://chrome.google.com/webstore/detail/ignore-x-frame-headers/gleekbfjekiniecknbkamfmkohkpodhe?utm_source=chrome-app-launcher-info-dialog)
	* For Firefox, here are the add-ons you need to install:
		* CORS Everywhere (https://addons.mozilla.org/en-US/firefox/addon/cors-everywhere/?src=search)
		* Ignore X-Frames Options (https://addons.mozilla.org/en-US/firefox/addon/ignore-x-frame-options/?src=search)
	* For Opera, you need to download the following extensions and install to Opera
		* Force CORS (https://github.com/edwindvinas/ForceCORS)
		* Force Embed (https://github.com/edwindvinas/force-embed)
	* For Edge/IE/Safari - no extensions available!

* After successful setup, you can now access:
	* **http://your-server-name.appspot.com/uwm** - The main desktop
	* **http://your-server-name.appspot.com/webapp** - The mobile webapp
	* **http://your-server-name.appspot.com/desktops** - The listing of all desktops
	* **http://your-server-name.appspot.com/contents** - The listing of contents
* You may use the toolbar to access the above main screens
	* Click the desktop icon to list all desktops
	* Click the globe icon to launch the website
	* Click the ULAPPH start menu to expand the menu (try launching the apps)

### STEP 7: Upgrading your desktop
* Download the latest source codes
	* https://github.com/ulapph/ULAPPH-Cloud-Desktop
* Open the local installer & press F5 to install/upgrade
	* https://github.com/ulapph/ULAPPH-Cloud-Desktop-VBA-Installer

### STEP 8: Customizing the source codes
* You may customize the cloud desktop and test your change in your own cloud desktop
	* Update the golang codes in **main.go** (this is the single Golang program that controls everything)
	* Update the static codes in **static** folder
* Then request a pull request if you want to contribute your changes
