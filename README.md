# iOS-Developer-Challenge

`version 1.6`

![Nutri-Facts! Icon](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/icon/ios/iTunesArtwork.png "Nutri-Facts!")

## Project Structure

Project was built on last Xcode Beta version, with last iOS and tested on iphone 5s. 

 - Project is using Cocoa-Pods for third party libraries, controllers or helper classes (https://cocoapods.org/)
 - Licence files are included in each cocoa-pod project (dependent on git repo)
 - For local storage I used realm db for swift (https://realm.io/docs/swift/latest/)
 - For internet, WS communication, JSON parsing I used AFNetworking (https://github.com/AFNetworking/AFNetworking)
 - Main menu is based on Persei, with some custom changes (https://github.com/Yalantis/Persei)
 - All graphs are rendered by using great of port of android charting library (https://github.com/danielgindi/ios-charts)
 - As far as in iOS in iPhone project I cannot use native formsheets, I have included perfect alternative (https://github.com/m1entus/MZFormSheetController)
 - As a background I used free parallax image and (https://github.com/michaeljbishop/NGAParallaxMotion)
 - Keyboard management in Form controller (add/edit meals) I used (https://github.com/michaeltyson/TPKeyboardAvoiding)
 - Every food cell contains tags, well presented by using (https://github.com/andreamazz/AMTagListView)
 - Colorful popup animated sliders are based on (https://github.com/alskipp/ASValueTrackingSlider)
 - UUID Generation (https://github.com/fabiocaccamo/FCUUID)
 - Floating label (https://github.com/ArtSabintsev/UIFloatLabelTextField)

## Features

### Profile Creator
![ProfileView](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/Screenshots/ProfileJPG.jpg)

* Quick User profile creation by using sliders and big flat design buttons
* Current version supports colorful weight sliders. (Colors are based on user's height -> count BMI)
* BMI RANGES:

> Severe Thinness			< 16
Moderate Thinness		16 - 17
Mild Thinness				17 - 18.5
Normal							18.5 - 25
Overweight					25 - 30
Obese Class I				30 - 35
Obese Class II				35 - 40

### Dashboard
![Dashboard](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/Screenshots/DashboardOverviewJPG.jpg)

 - Prototype of User's dashboard screen (Work in progress - Check TODO)
 - It consists of:
	 - Today graphs
		 - Daily intake of nutrients
	 - Last week bar graph
		 - Weekly intake of calories

#### History
![Dashboard History](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/Screenshots/DashboardHistoryJPG.jpg)

 - Below User's dashboard you can find feed of User's records
 - Cell in table allows to see nutrients in two views - overview and more detailed (Switched by swipping)
 - Current version supports only meal entries
	 - together with Date, Portion (stored in realmDB)

### Search
![Search Overview](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/Screenshots/SearchFoodOverviewJPG.jpg)

 - This screen is used for searching in local + remote storage of meals
 - Screen is fully responsive and every cell is expandable (in same manner than in Dashboard screen)

![Expanded cell](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/Screenshots/SearchFoodJPG.jpg)


### My Meals
![MyMeals Overview](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/Screenshots/MyMealsJPG.jpg)

 - This screen contains local storage data of saved meals
 - This meals can be easily edited by pressing pencil button or add new meal by pressing Add Custom Meal button

### Add/Edit Meal
![AddMeal](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/Screenshots/AddNewMealJPG.jpg)

 - Add/Edit Form view controller
 - Every number field is decimal keypad protected
 - Texfields are subclassed and they are showing floating labels on top

### Settings
![Settings](https://raw.githubusercontent.com/radvansky-tomas/Engineering-Challenge-iOS/master/Screenshots/SettingsJPG.jpg)

 - This screen currently contains only logout button (It clears Realm DB -> and start over)

## TODO

This app has quite big potential, so there are couple of other points what I would add in future of its development:

 - Add other WSs
 - Use public api for devices (smart scales)
 - Add other user's records -> weight
 - All strings in app are hardcoded, next step would be to replace them by nslocalized string + create lozalization.string file
 - Current solution allows users to create their own meals, but there is no option to delete them
 - App was tested only on iphone5s real device
 - Add 
