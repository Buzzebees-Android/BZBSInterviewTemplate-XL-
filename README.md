# BuzzeBees Android/Flutter Assignment 

## Confidential
Please don't disclose this assignment with anyone. 

## Story and Goals
We plan to launch a privileged app. Your responsibility is to create the project's base structure. It's going to be a long term project so the structure should be flexible, easy to understand, and easy to be supported by your team members.

## Your task

Your task is to create a Buzzebees privileged app. The app has two main pages, Main Page and Details Page
 
The app main page consists of 5 sub-pages, Dashboard, Campaigns, Collect Point, Favorites and My Account. The top section shows the pages' name and the bottom shows a Bottom Navigation Bar. When a user clicks a campaign, it navigates to the campaign's details page.

The details page display the details of the selected campaign from the main page. It has a favourite button to mark the campaign as a favourite. You have to implement your own mechanics to mark the campaign.

Since we are making a high-quality application, we should handle all possible cases properly (no internet connection, showing loading progress, support screen rotation, error handling)

## Design

Please refer to this link
```
https://www.figma.com/file/F5bUJNmMG4XwXucXfad1xW/Buzzebees-Android-Test?node-id=0%3A1
```
Your final UI can look different from the design, but it should include the same information we provided.

## API details

To get the dashboard, please use 
```
curl --location 'https://firebasestorage.googleapis.com/v0/b/android-interview-test.appspot.com/o/dashboard.json?alt=media&token=7ce93fe2-7f99-46fa-88ac-5a1e0e123bb0'
```

To get the campaign list, please use
```
curl --location 'https://firebasestorage.googleapis.com/v0/b/android-interview-test.appspot.com/o/campaigns.json?alt=media&token=13af3b54-6b36-416c-a42d-483f0acea6ad'
```

## Code requirements
 * The app must be written in Kotlin (for Android) or Dart (for Flutter)
 * We prefer MVVM architecture, but you can use MVP/MVC
 * We prefer scalable, maintainable and testable code
 * **[Bonus for Android]** Using Kotlin Coroutine
 * **[Bonus for Android]** Using Koin or Hilt as a dependency injection framework
 * **[Bonus for Android]** Having Jetpack Compose
 * **[Bonus for Flutter]** State Management
 * **[Bonus]** Having local database
 * **[Bonus]** Having some unit test

## Application requirements
### Dashboard Screen

![Dashboard](https://github.com/Buzzebees/BZBSInterviewTemplate/blob/master/screenshots/Home.png?raw=true)

The dashboard is a list of dashboard objects. Each dashboard object has its `type` to determine how they are rendered on the screen.

In this project, you will work with the following types of the dashboard:

Type | Size | Description
--- | --- | ---
campaign | small | Display a square image using `image_url`, other properties can be ignored.
campaign | medium | Display a rectangular image using `image_url`, other properties can be ignored.
header | - | Display a simple text using `name`.
campaign_rotate | big | Display a horizontally rotatable pager of dashboards. It contains `subcampaigndetails` which is a list of dashboards to be displayed.
campaign_rotate | small | Display a horizontal list of dashboards. Like a big campaign_rotate, it contains `subcampaigndetails`. This dashboard cannot be rotated.

By clicking a dashboard item, the app will navigate to Details Screen.

### Campaign List Screen

![List](https://github.com/Buzzebees/BZBSInterviewTemplate/blob/master/screenshots/Campaigns.png?raw=true)

Display a grid of campaigns. Each item displays an image, name, price using `image_url`, `name`, and `price` respectively.

By clicking a campaign, the app will navigate to Details Screen.

### Collect Points Screen

Display user's barcode and qr code. This is a static page

### Favourite Screen

![Favorite](https://github.com/Buzzebees/BZBSInterviewTemplate/blob/master/screenshots/Favorite.png?raw=true)

Display a grid of user's favourite campaigns.

By clicking an item, the app will navigate to Details Screen.

### My Account Screen

Display user information and other menus. This is a static page

### Detail Screen

![Details](https://github.com/Buzzebees/BZBSInterviewTemplate/blob/master/screenshots/Details%201.png?raw=true)

Display the following details of a campaign

* Image
* Name
* Price
* Description
* Favorite Button
* Redeem Button

By clicking the favorite button, you add a campaign to user's favorite campaigns.
The redeem button do nothing.

## Submission process
  You can use this repository while you are developing the app. 
  
  To submit the test assignment please **close the issue "Assignment Done" in "issues" tab**.
  
  We will review the code **only after you close "Assignment Done"**.
