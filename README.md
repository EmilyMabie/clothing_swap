# clothing_swap
A web-based local clothing swap intended to connect people with clothes and combat fast fashion.

![alt text](https://github.com/EmilyMabie/clothing_swap/blob/main/Screen%20Shot%202021-08-25%20at%201.13.27%20PM.png)

## **Project Title:** Madison Clothing Swap
### **Project Description:** A web-based local clothing swap intended to connect people with clothes and combat fast fashion in Madison, Wi.
[Wireframe Link](https://balsamiq.cloud/spvylua/p9ev1ek)

**Features List:**
*  Use of Django templating engine
*  User can create object to database, read, view, retrieve these objects from the database, and (if they are the creator) edit and delete objects
*  Log and Registration with validations
*  Application includes protected route (user must be in session to view)
*  Application features static content (CSS, images, JS)
*  Created data must be validated (events cannot be in the past, clothing swaps must be within the bounds of the City of Madison)
*  Map API
*  Email generation using SendGrid's SMTP relay
 
**Additional Notes:**
I wanted to experiment with sending emails via Django. There are many different ways to achieve this, though one hurdle was that Django’s built-in email processes default to a single “from” email address. Instead, I imported and implemented SendGrid, and used their SMTP relay (modified my app’s SMTP configuration). 
I then had to disable this, as SendGrid is not secure with free email accounts (such as gmail).

I also wanted to implement a form, since I hadn’t gotten to practice much with them during the Python stack. I used the form to gather the data for constructing clothing swap emails

Less successfully: I experimented with map capabilities, and while I was able to render a map on my page and allow the user to locate themselves by including a targeting icon, I was not successfully able to include automated “pin-dropping” because it required conversion of addresses (that users could add to my database) into longitude and latitude, which I was not able to accomplish.
Additionally, my computer ended up having problems with caching old versions of CSS files, and only updating to the new version every few days. Collecting static and manually restarting my computer, VS Code, and my servers did not resolve the issue, making it very difficult to improve the aesthetic appeal of the web application.
