# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<TUDDAO>" />
  <meta name="revised" content="<27/03/2026>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
      
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.
-  The sidebar box moves diagonally downwards instead of being against the corner of the webpage in the original. The spacing at the top and left of the box increases or decreases depending on the value you give for the px.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?
- The footer behaves differently becase we used position fixed instead of relative, which makes the element stays in the same spot and follows the user scrolls.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?
- Position: absolute will make the element stay in the exact same spot and not move when the user scrolls. On the other hand, when we use position: fixed, it would stay in the users view regardless of where the user scrolls.

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```
- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?
- The notice appears on top of the content because we edited the z-index value to 1. Swapping the value of the z-index controls whether the element is in front of behind other elements.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    - I simply adjusted the px values of the top and left in the .notice box until it aligned to the top right corner of the .content box.
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    - The .content box moved from the upper portion of the page to the lower portion of the page.
    * What do you observe on about the effect of z-index on .notice and .content boxes?
    - The z-index controls which elements are on top or behind each element.

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 
    - Static position is the default positioning which follows the flow of the document. Relative positioning also follows the flow of the document but you can adjust its position (top, right, left, bottom). Absolute positioning allows you to place an element anywhere on the webpage without following the natural flow of the document. Lastly, fixed positioning will allow you to place an element anywhere but it will follow the behavior of the viewport/browser window.
    b. How does absolute positioning depend on its parent element?
    - Absolute positioning is relative to its nearest ancestor that has a position value.

    c. How do you differentiate sticky from fixed (you can research on sticky)?
     - Fixed positioning will follow the behaviour of the viewport window but stay in the same spot, while sticky will follow the viewport window but it will get pushed around depending on how the user scrolls up and down.
    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.
     - I would use specific positioning to make sure that the elements I want to show will be displayed properly for users. An example could be using fixed for navigation bars which is important so the user can easily access it when they need to visit other webpages. Another could be using the absolute positioning so that the information/element will be fixed and formatted properly in the right spots which would allow users to read through the website with ease.