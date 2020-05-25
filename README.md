# BuzzeBees Android Assignment 

## Deadline : (01/06/20)
## Confidental
Please don't disclose this assignment with anyone. 

## Story and Goals
We plan to launch a privilege app. Your responsibility is to create the project's base structure. It's going to be a long term project so the structure should be flexible, easy to understand and easy to be supported by your team members. Since we are making a high-quality application, we should handle all possible cases properly (no internet connection, showing loading progress)

## Your task
Your task is to create the campaign list screen. The top section shows the page's name and the bottom part shows the tabbar. Before you get the response from API, you need to show the loading progress. In case of any connection issue, you need to show a no connection screen that includes the "no connection" image, message and "try again" button. By clicking on "try again" button, it will load the data again.

[Bonus] The app should support both landscape and portrait modes. You can use the screenshots below as a reference.

**[Important]** Your final UI can look different, but it should include the same information as on the screenshots.
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
 * [Bonus] Having Kotlin Coroutine but not required
 * [Bonus] Having Koin but not required
 * [Bonus] Having Dagger but not required
 * [Bonus] Having Jetpack Components but not required
  
## Submission process
  You can use this repository while you are developing the app. 
  
  To submit the test assignment please **close the issue "Assignment Done" in "issues" tab**.
  
  We will review the code **only after you close "Assignment Done" issue**.


## Requirement

แอปพลิเคชันประกอบไปด้วย
* Login Screen
* Dashboard Screen
* Campaign List Screen
* Favourite Screen
* Detail Screen

### Dashboard Screen

เป็น Dynamic Content โดยรเรียก JSON จาก url 

https://firebasestorage.googleapis.com/v0/b/android-interview-test.appspot.com/o/dashboard.json?alt=media&token=48371953-a998-4613-8791-e00c976335a2

ประกอบไปด้วย 

* small campaign rotate
* big campaign rotate
* header
* small campaign 
* big campaign

คลิกที่ไอเทมแต่ละอันจะเปิดหน้า Detail

### Campaign List Screen

เป็น Dynamic Content โดยรเรียก JSON จาก url 

https://xxxxxxxxxxxxxx

คลิกที่ไอเทมแต่ละอันจะเปิดหน้า Detail

### Detail Screen

แสดงรายละเอียด Campaign ที่คลิกมาจากหน้า Dashboard หรือ Campaign List
สามารถกด Favourite ได้

Campaign ที่เป็น Favourite จะไปปรากฎที่หน้า Favourite Screen

### Favourite Screen

แสดงรายการ Campaign ทีเป็น Favourite
