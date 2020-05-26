# BuzzeBees Android Assignment 

## Deadline : (01/06/20)
## Confidential
Please don't disclose this assignment with anyone. 

## Story and Goals
We plan to launch a privileged app. Your responsibility is to create the project's base structure. It's going to be a long term project so the structure should be flexible, easy to understand, and easy to be supported by your team members. Since we are making a high-quality application, we should handle all possible cases properly (no internet connection, showing loading progress, support screen rotation, error handling)

## Your task

Your task is to create a Buzzebees privileged app. The app has two main pages, Main Page and Details Page
 
The app main page consists of 3 sub-pages, Dashboard, Campains, and Favorites. The top section shows pages' name and the bottom shows a Bottom Navigation Bar. When user click a campaign, it naviagte to the campaign's details page. Before you get a response from API, you need to show a loading progress. In case of any connection issue, you have to show a no connection screen that includes the "no connection" image, message, and "try again" button. By clicking on the "try again" button, it will load the data again.

The details page display the details of selected campaign from the main page. It has a favorite button to mark the camapaign as favorite. You have to implement you own mechanics to mark the camapaign


**[Bonus]** The app should support both landscape and portrait modes. You can use the screenshots below as a reference.

**[Important]** Your final UI can look different from the design, but it should include the same information as on the screenshots.
```
https://www.figma.com/file/F5bUJNmMG4XwXucXfad1xW/Untitled?node-id=0%3A1
```

## API details

To get the dashboard, please use 
```
GET https://firebasestorage.googleapis.com/v0/b/android-interview-test.appspot.com/o/dashboard.json?alt=media&token=48371953-a998-4613-8791-e00c976335a2
```

To get the campaign list, please use
```
GET https://firebasestorage.googleapis.com/v0/b/android-interview-test.appspot.com/o/dashboard.json?alt=media&token=48371953-a998-4613-8791-e00c976335a2
```

## Code requirements
 * The app must be written in Kotlin only
 * We prefer MVVM architecture, but you can use MVP
 * We prefer to use a dependency injection framework
 * We prefer scalable, maintainable and testable code
 * Having Unit tests would be a plus but not required
 * Having database cache would be a plus but not required
 * **[Bonus]** Having Kotlin Coroutine but not required
 * **[Bonus]** Having Koin but not required
 * **[Bonus]** Having Dagger but not required
 * **[Bonus]** Having Jetpack Components but not required

## Application requirements
### Dashboard Screen

The dashboard is a list of dashboard objects. Each dashboard object has its `type` to determine how they are rendered on the screen.

In this project, you will work with the folowing types of the dashboard:

Type | Size | Description
--- | --- | ---
campaign | small | Display a square image using `image_url`, other properties can be ignored.
campaign | medium | Display a rectangular image using `image_url`, other properties can be ignored.
header | - | Display a simple text using `name`.
campaign_rotate | big | Display a horizontal rotatable pager of dashboards. It contains `subcampaigndetails` which is a list of dashboards to be displayed.
campaign_rotate | small | Display a horizontal list of dashboards. Like a big campaign_rotate, it contains `subcampaigndetails`. This dashboard cannot be rotated

By clicking a dashboard item, the app will navaigate to Details Screen

### Campaign List Screen

Display a grid of dashboard items. Each items displays and image, name, price using `image_url`, `name`, and `price` respectively.

By clicking a dashboard item, the app will navaigate to Details Screen

### Detail Screen

Display the following details of a campaign

* Image
* Name
* Price
* Description

The heart button is a favorite button to mark this campaign as favorite. 

### Favourite Screen

Display a grid of user favorite campaigns

By clicking an item, the app will navaigate to Details Screen


## Submission process
  You can use this repository while you are developing the app. 
  
  To submit the test assignment please **Pull requests in "Pull request" tab**.
  
  We will review the code **only after you Pull request**.
