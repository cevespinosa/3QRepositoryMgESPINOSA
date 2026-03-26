<!DOCTYPE html>
<html>
<head>
<meta name="author" content="ESPINOSA, Cassandra Ellinoir V." />
<meta name="revised" content="March 26, 2026" />
<style>
body { font-family: Arial, sans-serif; margin: 0; padding: 0; }


.header {
background: lightblue;
padding: 10px;
}


.sidebar {
background: lightgreen;
width: 150px;
height: 200px;
position: relative;
top: 20px;
left: 20px;
}


.content {
background: lightyellow;
width: 300px;
height: 200px;
position: absolute;
top: 66px;
left: 200px;
z-index: 1;
padding: 10px;
}


.notice {
position: absolute;
top: 0;
right: 0;
background: orange;
padding: 10px;
z-index: 2;
}


.footer {
background: lightblue;
padding: 10px;
position: fixed;
bottom: 0;
width: 100%;
opacity: 0.5;
}
</style>
</head>
<body>

<div class="header">Header</div>

<div class="sidebar">Sidebar</div>


<div class="content">
Main Content
<div class="notice">Notice!</div>
</div>

<div class="footer">Footer</div>

</body>
</html>

```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.

ANSWER: The sidebar moved 20px down and 20px right from its normal position, but other elements stayed in place. Changing top, left, bottom, or right shifts it relative to where it would normally be
.
### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?

ANSWER: The footer stays visible at the bottom of the screen when scrolling because fixed elements are removed from normal flow and positioned relative to the viewport, unlike relative elements.


### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?

ANSWER: The content moves to exact coordinates and doesn’t affect other elements; unlike fixed, it scrolls with the page unless its parent is fixed.

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

ANSWER: The notice appears on top of the content because its z-index is higher; swapping z-index values would make the content cover the notice.


- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).

    To position the notice at the top-right of content, make 
    .content { 
    position: relative; } 
    
    AND

    .notice { position: 
    absolute; 
    top: 0; 
    right: 0;
    }.


    * Try to change the position of .content to relative then to fixed. What do you observed each time? 
    
    ANSWER: Changing .content to relative keeps it in flow; fixed moves it with the viewport.


    * What do you observe on about the effect of z-index on .notice and .content boxes?

    ANSWER: Higher z-index always places an element on top of lower z-index elements when they overlap.

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    b. How does absolute positioning depend on its parent element?

    c. How do you differentiate sticky from fixed (you can research on sticky)?

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.