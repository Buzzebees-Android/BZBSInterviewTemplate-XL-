# BuzzeBees Android Assignment 

## Deadline : (01/06/20)
## Confidential
Please don't disclose this assignment with anyone. 

## Story and Goals
We plan to launch a privileged app. Your responsibility is to create the project's base structure. It's going to be a long term project so the structure should be flexible, easy to understand, and easy to be supported by your team members.

## Your task

Your task is to create a Buzzebees privileged app. The app has two main pages, Main Page and Details Page
 
The app main page consists of 3 sub-pages, Dashboard, Campaigns, and Favorites. The top section shows the pages' name and the bottom shows a Bottom Navigation Bar. When a user clicks a campaign, it navigates to the campaign's details page. Additionally, users can change a display language by clicking the change language button on the top of the page.

To create a good user experience, before you get a response from API, you need to show loading progress. In case of any connection issues, you have to show a "no connection screen" that includes the "no connection" image, message, and "try again" button. By clicking on the button, it will load the data again.

The details page display the details of the selected campaign from the main page. It has a favourite button to mark the campaign as a favourite. You have to implement your mechanics to mark the campaign.

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
GET https://firebasestorage.googleapis.com/v0/b/android-interview-test.appspot.com/o/dashboard.json?alt=media&token=e49c0393-c604-406e-b2bd-7ba1597ca231
```

To get the campaign list, please use
```
GET https://firebasestorage.googleapis.com/v0/b/android-interview-test.appspot.com/o/campaigns.json?alt=media&token=88974393-18a9-4ae6-9a62-fded62144730
```

## Code requirements
 * The app must be written in Kotlin only
 * We prefer MVVM architecture, but you can use MVP
 * We prefer to use a dependency injection framework
 * We prefer scalable, maintainable and testable code
 * Having Unit tests would be a plus but not required
 * Having database cache would be a plus but not required
 * **[Bonus]** Using Kotlin Coroutine would be a plus but not required
 * **[Bonus]** Using Koin or Dagger as a dependency injection framework would be a plus but not required
 * **[Bonus]** Having Jetpack Components would be a plus but not required
* **[Bonus]** Having some unit test

## Application requirements
### Dashboard Screen

![Dashboard](https://bitbucket.org/Bzb_Android_Team/exam_01/raw/84adcc49398d06d0eb05b3dfc8f1cf0489274c18/pictures/Home.png)

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

Users can click the change language button to change the display language of the app.

### Campaign List Screen

![List](https://bitbucket.org/Bzb_Android_Team/exam_01/raw/84adcc49398d06d0eb05b3dfc8f1cf0489274c18/pictures/Campaigns.png)

Display a grid of campaigns. Each item displays an image, name, price using `image_url`, `name`, and `price` respectively.

By clicking a campaign, the app will navigate to Details Screen

### Detail Screen

![Details](https://bitbucket.org/Bzb_Android_Team/exam_01/raw/84adcc49398d06d0eb05b3dfc8f1cf0489274c18/pictures/Details%201.png)

Display the following details of a campaign

* Image
* Name
* Price
* Description

The heart button is a favourite button to mark this campaign as a favourite. 

### Favourite Screen

![Favorite](https://bitbucket.org/Bzb_Android_Team/exam_01/raw/84adcc49398d06d0eb05b3dfc8f1cf0489274c18/pictures/Favorite.png)

Display a grid of user favourite campaigns

By clicking an item, the app will navigate to Details Screen

## Submission process
  You can use this repository while you are developing the app. 
  
  To submit the test assignment please **close the issue "Assignment Done" in "issues" tab**.
  
  We will review the code **only after you close "Assignment Done" issue**.
