---
layout: post
title: "Advanced Settings of Application for iOS SDK and Showcase app"
date: 2016-11-15
comments: true
tags: beacon iOS SDK showcase management
---


#Advanced Settings of Application for iOS SDK and Showcase app.

> This is a description for the advance settings of application on management platform.

 1. [Settings for iOS SDK : The settings are used to configure the behaviours of iOS SDK](http://sensorberg-dev.github.io/2016/11/Advanced-Settings-of-Application-for-iOS-SDK-and-Showcase-app/#settings-for-ios-sdk)
 2. [Settings for iOS Showcase app : The settings to change all colour and font styles of iOS 'Showcase' app.](http://sensorberg-dev.github.io/2016/11/Advanced-Settings-of-Application-for-iOS-SDK-and-Showcase-app/#settings-for-showcase)

<!--more-->
  

----------  


##Settings for iOS SDK

> Following keys are used to configure the behaviour of iOS SDK  

|key|type|description|
|---|---|---|---|
|monitoringDelay|number (seconds)|time interval to fire beacon exit event when beacon is disappeared.|
|postSuppression|number(seconds)|time interval to send statistic and conversion data to Sensorberg platform|
|resolverURL|string|endpoint of beacon management platform|
|customBeaconRegions|key-value hash table|custom beacon uuid to detect beacons in given beacon region. This setting enables scanning beacons which are not include in any associated campaigns.|
|---|---|---|---|
  
Example:  

```json
{
	"monitoringDelay" : 120,
	"postSuppression" : 300,
	"resolverURL" :  "https://manage.sensorberg.com",
	"customBeaconRegions" : {
			 "B9407F30-F5F8-466E-AFF9-25556B57FE6D" : "Custom0",
			 "F7826DA6-4FA2-4E98-8024-BC5B71E0893E" : "Custom1",
			 "2F234454-CF6D-4A0F-ADF2-F4911BA9FFA6" : "Custom2"
		 }
}
```


##Settings for Showcase

> There is a special setting only for 'Showcase'.
> With following theme property you can change all colour and font styles of 'Showcase' app.  
  

|key|type|description|
|---|---|---|---|
|theme|[Theme Object](#theme-object)||change theme of Showcase app|
|---|---|---|---|

Example :  

```json
{
	"theme" : {
		"navigationBarColor":"#00AAFF",
		"navigationBarLogoImage" : "http://www.sensorberg.com/logo.png",
		"navigationBarLogoColor" : "#FFFFFF"
	}
}
```

###Theme Object

|key|type|description|
|---|---|---|---|
|navigationBarColor|[color string](#color-string)| Color for top navigation bar|
|navigationBarTitleFont|[font object](#font-object)|Font for screen titles on top navigation bar|
|navigationBarTitleColor|[color string](#color-string)|Color for screen titles on top navigation bar|
|navigationBarLogoImage|image url string|Icon image on left top of top navigation bar|
|navigationBarLogoColor|[color string](#color-string)|Image tint color for the icon image on left top of top navigation bar|
|tabBarColor|[color string](#color-string)|Color for bottom tab bar|
|tabBarSelectedItemColor|[color string](#color-string)|Color of selected item on botom tab bar.|
|tableViewSectionHeaderTextFont|[font object](#font-object)|Font for all tableview section headers|
|tableViewSectionHeaderTextColor|[color string](#color-string)|Text color for all tableview section headers|
|switchColor|[color string](#color-string)|color of UISwitch|
|switchOnColor|[color string](#color-string)|color of UISwitch when switch is on|
|switchThumbTintColor|[color string](#color-string)|thumb color of UISwitch|
|baseTableViewCellTitleTextFont|[font object](#font-object)|title text font of UITableViewCell|
|baseTableViewCellTitleTextColor|[color string](#color-string)|title text color of UITableViewCell|
|baseTableViewCellDetailTextFont|[font object](#font-object)|detail text font of UITableViewCell|
|baseTableViewCellDetailTextColor|[color string](#color-string)|detail text color of UITableViewCell|
|historyCellTitleTextFont|[font object](#font-object)|title text font of notification history|
|historyCellTitleTextColor|[color string](#color-string)|title text color of notification history|
|historyCellDetailTextFont|[font object](#font-object)|detail text font of notification history|
|historyCellDetailTextColor|[color string](#color-string)|detail text color of notification history|
|historyCellContentBackgroundColor|[font object](#font-object)|background color of notification history item|
|beaconCellTitleTextFont|[font object](#font-object)|Beacon name text font on scanner screen|
|beaconCellTitleTextColor|[color string](#color-string)|Beacon name text color on scanner screen|
|beaconCellDetailTextFont|[font object](#font-object)|Beacon major minor text font on scanner screen|
|beaconCellDetailTextColor|[color string](#color-string)|Beacon major minor text color on scanner screen|
|---|---|---|---|

Example :   

```json
{
	"navigationBarColor":"#RRGGBB",
	"navigationBarTitleFont ":  {
		"fontName" : "Helvetica",
		"fontSize" : 21
	},
	"navigationBarTitleColor" : "#FFFFFF",
	"navigationBarLogoImage" : "http://www.sensorberg.com/logo.png",
	"navigationBarLogoColor" : "#FFFFFF"
}
```

###Font Object :

|key|type|
|---|---|
|fontName|string|
|fontSize|number|
|---|---|

Example :   

```json
"navigationBarTitleFont" : 
{
	"fontName" : "Helvetica",
	"fontSize":21
}
```

###Color String 

:  "#RRGGBB"  formated string

Example :   

```json
"navigationBarLogoColor" : "#FF5500"
```
