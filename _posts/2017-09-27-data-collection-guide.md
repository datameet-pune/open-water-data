---
layout:     post
title:      Guide to collection of Crop data points
author:     Craig D
tags: 		how-to
subtitle:  	
category:  how-to
---
<!-- Start Writing Below in Markdown -->

Table of Contents
===================
  * [Goals of data collection](##Goals-of-data-collection)
  * [Open Camera App](##Open-Camera-App)
    * [Installation](###Installation)
    * [Change the default settings of Open Camera](###Change-the-default-settings-of-Open-Camera)
  * [Travel to field sites](##Travel-to-field-sites)
    * [GPS](##GPS)
    * [Click and confirm photo](##Click-and-confirm-photo)
  * [Upload photos and rename](##Upload-photos-and-rename)
  * [Email](##Email)
  
# Goals of data collection
Out goal of this data collection exercise is to develop a crop database that can be used to teach a training/testing set for applying Machine Learning to open source satellite imagery. The database would need to have three main variables. Crop name, GPS lat,long of a field where the crop is currently growing and a photo of the crop itself. <br>

The data once collected will look something like this<br>

| Crop | Latitude | Longitude | Date of Photo | Photo |
| ---- | -------- | --------- | ------------- | ----- |
| Rice | 18.53173 | 73.53651  | Sep 24th,2017 |![rice](/img/oc-image-rice.jpg)|

If any of you are traveling outside your city and can get us a few data points your help would be much appreciated. Else if you know friends living outside the cities who can help us please do forward this to them! 

# Data collection steps
## Open Camera App
### Installation
Search Google Play Store for the Open Camera App and install. See image below.
![open-camera-play-store](/img/oc-play-store.PNG)

### Change the default settings of Open Camera
Open the app once installed open it and click on its settings button<br>
![open-camera-find-settings](/img/oc-find-settings.png)        ![open-camera-settings](/img/oc-settings.png)<br><br>

Find 'Photo settings' and change settings to 'Stamp photos'<br>
![open-camera-photo-settings](/img/oc-photo-settings.png)<br><br>

Find 'Location settings' and Click the ☑ for all three options<br>
![open-camera-location-settings](/img/oc-location-settings.png)<br>

## Travel to field sites
Once the settings for the app have been fixed you can travel to field sites. Please choose sites where you can identify the crops. Alternatively at some sites you may find a farmer who can tell you the name of the crop, this would also work.
### GPS
Turn on the GPS on your phone. It is important for accuracy that the GPS is turned on at least 2-3 minutes before taking the first photo. When the GPS signal is obtained you will see a yellow light when taking the image, see below
![open-camera-gps-ready](/img/oc-gps-ready.png)<br>

### Click and confirm photo
You may now take a photo of the field. When taking a photo do try to get a clear picture in which some part of the background is also visible.<br>
Once you have clicked find the photo and confirm whether the GPS Latitude, Longitude, angle and timestamp are all visible.
![open-camera-photo-confirm](/img/oc-photo-confirm.jpg)<br>

## Upload photos and rename
When you are back home connect your phone to a laptop via USB and download the folder of photos you have taken. They will be in the DCIM > OpenCamera folder on your phone.<br>
Rename all the photos by adding the name of the crop to the filename. If the filename is XYZ and the crop is rice you can rename it as XYZ_rice. <br>
This is especially important for crops that are less common and hard to recognize from a photo. If you take many photos it may be useful to also take a notebook and write down the name of the crop in each photo so you don't forget.

## Email
Once all the photos have been renamed with the name of the crops please upload to Google Drive or Dropbox and email them to pune@datameet.org

We appreciate your contributions and will give attribution to you on our web page. Thank you!

