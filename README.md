# Ex.07 Design of Interactive Image Gallery
## Date:18/03/2026
## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
### index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Photo Showcase</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="container">
    <h2>Image Gallery</h2>

    <div class="gallery-box">
      <button id="leftBtn">&#10094;</button>

      <img id="photo" src="01.jpg" alt="gallery image">

      <button id="rightBtn">&#10095;</button>
    </div>
  </div>

  <script>
    const pics = ["01.jpg", "02.jpg", "03.jpg", "04.jpg", "05.jpg"];
    let current = 0;

    const photo = document.getElementById("photo");
    const leftBtn = document.getElementById("leftBtn");
    const rightBtn = document.getElementById("rightBtn");

    leftBtn.addEventListener("click", () => {
      current--;
      if (current < 0) {
        current = pics.length - 1;
      }
      photo.src = pics[current];
    });

    rightBtn.addEventListener("click", () => {
      current++;
      if (current >= pics.length) {
        current = 0;
      }
      photo.src = pics[current];
    });
  </script>

</body>
</html>
```
### style.css
``` css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: linear-gradient(135deg, #dff6ff, #fce1ff);
  height: 100vh;
  display: grid;
  place-items: center;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}

.container {
  text-align: center;
}

h2 {
  margin-bottom: 20px;
  color: #333;
}

.gallery-box {
  position: relative;
  width: 750px;
  max-width: 95%;
}

.gallery-box img {
  width: 100%;
  height: 500px;
  object-fit: cover;
  border-radius: 12px;
  border: 4px solid white;
  box-shadow: 0 10px 25px rgba(0,0,0,0.3);
  transition: 0.3s ease-in-out;
}

.gallery-box img:hover {
  transform: scale(1.02);
}

button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: #333;
  color: white;
  border: none;
  padding: 10px 14px;
  font-size: 22px;
  cursor: pointer;
  border-radius: 8px;
  opacity: 0.8;
}

button:hover {
  opacity: 1;
  background: #000;
}

#leftBtn {
  left: 10px;
}

#rightBtn {
  right: 10px;
}
```


## OUTPUT
![alt text](<Screenshot 2026-03-18 113853.png>)

![alt text](<Screenshot 2026-03-18 113904.png>)

![alt text](<Screenshot 2026-03-18 113913.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.

### Name:Ashok Kumar Preetham Kumar
### Roll no:212224040032