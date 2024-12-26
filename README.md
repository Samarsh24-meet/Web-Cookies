# Web-Cookies :)
## Objective:
  Create a simple one-page website designed by you, that saves user prefrences using cookies!
  - Use HTML, CSS & JavaScript for the website
  - User preferences: Username, selected background color for the page, etc...

<img src="https://media4.giphy.com/media/xT0xeMA62E1XIlup68/giphy.gif?cid=6c09b952b2fjpt8lb3z9cq443qg2mxo6e3p4aj8fqwl1tr4l&ep=v1_gifs_search&rid=giphy.gif&ct=g" >

### Step 1:
> BEFORE YOU START, We need to run our code using Terminal/Command Prompt, if you still haven't done this part please aproach the TAs!
- Create an HTML, CSS & JavaScript file to code on
- Copy the code written below in your JS file
  ```javascript
  function setCookie(cname,cvalue,exdays) {
    const d = new Date();
    d.setTime(d.getTime() + (exdays*24*60*60*1000));
    let expires = "expires=" + d.toUTCString();
    document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
  }
  
  function getCookie(cname) {
    let name = cname + "=";
    let decodedCookie = decodeURIComponent(document.cookie);
    let ca = decodedCookie.split(';');
    for(let i = 0; i < ca.length; i++) {
      let c = ca[i];
      while (c.charAt(0) == ' ') {
        c = c.substring(1);
      }
      if (c.indexOf(name) == 0) {
        return c.substring(name.length, c.length);
      }
    }
    return "";
  }
  
  function checkCookie() {
    let user = getCookie("username");
    if (user != "") {
      alert("Welcome again " + user);
    } else {
       user = prompt("Please enter your name:","");
       if (user != "" && user != null) {
         setCookie("username", user, 30);
       }
    }
  }
### Step 2:
- Start building your own website through HTML.
- Make sure you connect your HTML and JavScript files using `<script>` tags.
- Try activating the `checkCookie` function automatically once the website loads.
> Hint: try googling onload()

### Step 3: Customize the checkCookie function!
We want cookies to store more data about the user, go over the function `checkCookie` and see how it works and how it saves user names, after that, your goal is to enhance the function so it can:
1. Ask the user about their favorite color
2. Save it in a cookie
3. Set it as the background color for future visits

### Step 4: Design,Customize,Decorate,Personalize...!
- Make your website Fancy!

#### Great job!
##### Call an Instructor/TA to check your completed tasks

## Bonuses!!
### Bonus 1: Add more Cookies!
- Try asking for more personalized information that you can store & show in your website

### Bonus 2: Personalize!
- Try having a "Welcome, `Username`!" text which takes the username stored in cookies and displays it

### Bonus 3: Make it more realistic!
- Have an actual pop up asking if the user accepts cookies
