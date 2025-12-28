# Ex.08 Design of Interactive Image Gallery
## Date:25.12.2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Interactive Photo Gallery</title>

<style>
  body{
    font-family: Arial, sans-serif;
    background: #f7f7f7;
    padding: 20px;
  }

  h1{ margin-bottom: 20px; }

  .gallery img{
    width: 200px;
    margin: 10px;
    cursor: pointer;
    transition: transform .3s;
    border-radius: 10px;
    box-shadow: 0 3px 6px rgba(0,0,0,.3);
  }

  .gallery img:hover{
    transform: scale(1.1);
  }

  #lightbox{
    position: fixed;
    top:0; left:0; right:0; bottom:0;
    background: rgba(0,0,0,.85);
    display: none;
    justify-content:center;
    align-items:center;
    z-index: 1000;
  }

  #lightbox img{
    max-width: 90%;
    max-height: 90%;
    border-radius: 12px;
    box-shadow: 0 0 20px white;
  }
</style>
</head>
<body>

<h1>Interactive Photo Gallery</h1>

<!-- Replace images here -->
<div class="gallery">
  <img src="photo1.jpg" onclick="openLightbox(this.src)">
  <img src="photo2.jpg" onclick="openLightbox(this.src)">
  <img src="photo3.jpg" onclick="openLightbox(this.src)">
  <img src="photo4.jpg" onclick="openLightbox(this.src)">
  <img src="photo5.jpg" onclick="openLightbox(this.src)">
</div>

<!-- Lightbox -->
<div id="lightbox" onclick="closeLightbox()">
  <img id="lightbox-img">
</div>

<script>
  function openLightbox(src){
    document.getElementById("lightbox-img").src = src;
    document.getElementById("lightbox").style.display = "flex";
  }
  function closeLightbox(){
    document.getElementById("lightbox").style.display = "none";
  }
</script>

</body>
</html>


## OUTPUT:
<img width="1039" height="559" alt="Screenshot 2025-12-28 192454" src="https://github.com/user-attachments/assets/011018b9-9e3f-499a-9c8a-4644c200cbc1" />

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
