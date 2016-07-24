# ULAPPH-Cloud-Desktop
A repository of resources being used by ULAPPH Cloud Desktop - a golang cloud desktop running on Google Appengine. The source code of ULAPPH Cloud Desktop is not yet open-source but you can find it's documentation in the link below.
http://ulapph-public-1.appspot.com/articles?TYPE=ARTICLE&DOC_ID=3&SID=TDSARTL-3

# To point your Start Menu to Github
Go to Admin Setup, edit your System Top List Menu to include the line below on the very first line:

    #GET_REMOTE_DATA: https://raw.githubusercontent.com/edwindvinas/ULAPPH-Cloud-Desktop/master/ULAPPH%20Cloud%20Desktop%20System%20Start%20Menu

This will make sure your Start Menu gets the latest from Github.

# To create a generic autocomplete list

For site guests or when Start Menu cannot be fetched, point GITURL_AUTOCOMP_LIST to an autocomplete list in Github.

    GITURL_AUTOCOMP_LIST    https://raw.githubusercontent.com/edwindvinas/ULAPPH-Cloud-Desktop/master/AUTOCOMPLETE/general

If you want to refer to a different link, inform the administrator so we can update your installation.
