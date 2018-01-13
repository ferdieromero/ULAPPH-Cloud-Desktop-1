ULAPPH Cloud Desktop - Javascript Programmers Guide
===================


This is a guide for Javascript Programmers.

----------

Summary of UWM Hidden Parameters
-------------

Item     | Value
-------- | ---
TBD		 | TBD
TBD		 | TBD

Accessing UWM Hidden Parameters
-------------

When you access /uwm desktop, you will have access to the hidden parameters.

#### <i class="icon-file"></i> desktop

This contains the name of the desktop such as uwm1, uwm2, desktop0 etc.

#### <i class="icon-file"></i> dName

This contains the desktop name such as Main Desktop or Desktop0

#### <i class="icon-file"></i> aUser

This is the email address of the user.

#### <i class="icon-file"></i> tok

This is the JWT token of the current session.

#### <i class="icon-file"></i> host

This is the complete URL of the cloud desktop.

#### <i class="icon-file"></i> mode

This is the mode of the cloud desktop.

#### <i class="icon-file"></i> ringtone

This is the ringtone of the cloud desktop.

#### <i class="icon-file"></i> dispAds

This is the flag to display advertisements.

#### <i class="icon-file"></i> scheme

This determines if http or https.

#### <i class="icon-file"></i> ushare

This is the flag if desktop is shared.

#### <i class="icon-file"></i> isMobile

This is the flag if desktop or mobile.

#### <i class="icon-file"></i> uwms

TBD

#### <i class="icon-file"></i> TITLE

Title of the uwm.

#### <i class="icon-file"></i> jwt

The long JWT token string.

#### <i class="icon-file"></i> aep

The Google App Engine project.

#### <i class="icon-file"></i> sss

The sites server being used.

#### <i class="icon-file"></i> snm

The flag if sound is on or off.

#### <i class="icon-file"></i> X-AppEngine-Country

The country of origin of request.

#### <i class="icon-file"></i> X-AppEngine-Region

The region origin of request.

#### <i class="icon-file"></i> X-AppEngine-City

The city origin of request.

#### <i class="icon-file"></i> X-AppEngine-CityLatLong

The longitude and latitude origin of request.

#### <i class="icon-file"></i> U-Referer

The referrer  origin of request.


Summary of Local Storage Parameters
-------------

Item     | Value
-------- | ---
TBD		 | TBD
TBD		 | TBD

Accessing Local Storage Parameters
-------------

When you access /uwm desktop, you will have access to the local storage parameters.

#### <i class="icon-file"></i> fingerprint

This contains the unique fingerprint of the browser.

#### <i class="icon-file"></i> uwm-1, uwm-2, uwm-n

This contains the currently opened ULAPPH desktops.


Summary of Javascript Functions
-------------

Item     | Value
-------- | ---
TBD		 | TBD
TBD		 | TBD

Accessing Javascript Functions
-------------

When you access /uwm desktop, you will have access to the built-in Javascript functions

#### <i class="icon-file"></i> uwmArrWin()

This re-arranges the windows of the desktops. Executing this twice will make the desktop appears tiled.


Summary of Other Functions
-------------

Item     | Value
-------- | ---
TBD		 | TBD
TBD		 | TBD

Customizing the desktop
-------------

You can customize the desktop via some Javascript codes. You can add these codes inside the UWM settings.

#### <i class="icon-file"></i> Set desktop wallpaper

This sets the desktop wallpaper to a fix image.

``
<script>    
    setTimeout(function(){
    	var rn = document.getElementById("ranid");
    	rn.value = "pause";
        var bgImgUrl = "https://lh3.googleusercontent.com/5-KY9yZgOBEaS5d-f7fS7SYbMDRA3UPW1Ppgp_-oraPuqyP0FUZCKQoHzi-dF5qiLm9h7xuuzzbEiKnGhFZ9pKl9_UK4Og=s1500";
        document.getElementById("DEFAULT_WALLPAPER").value = bgImgUrl;
        document.getElementById('page').style.backgroundImage = "url(" + bgImgUrl + ")";    
    }, 10000);
</script>
``

