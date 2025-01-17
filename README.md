# project-2
image slider using html &amp; css
HTML code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Image Slider</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="slider-container">
        <div class="slider">
            <img src="images/image1.jpg" alt="Image 1" class="slide active">
            <img src="images/image2.jpg" alt="Image 2" class="slide">
            <img src="images/image3.jpg" alt="Image 3" class="slide">
        </div>
        <button class="nav prev">&#10094;</button>
        <button class="nav next">&#10095;</button>
        <div class="thumbnails">
            <img src="images/image1.jpg" alt="Thumbnail 1" class="thumbnail active">
            <img src="images/image2.jpg" alt="Thumbnail 2" class="thumbnail">
            <img src="images/image3.jpg" alt="Thumbnail 3" class="thumbnail">
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
CSS CODE
body {
    margin: 0;
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
}

.slider-container {
    position: relative;
    width: 80%;
    max-width: 800px;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.slider {
    display: flex;
    transition: transform 0.5s ease-in-out;
}

.slide {
    min-width: 100%;
    opacity: 0;
    transition: opacity 0.5s ease-in-out;
}

.slide.active {
    opacity: 1;
}

.nav {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    border-radius: 50%;
}

.nav.prev {
    left: 10px;
}

.nav.next {
    right: 10px;
}

.nav:hover {
    background-color: rgba(0, 0, 0, 0.8);
}

.thumbnails {
    display: flex;
    justify-content: center;
    margin-top: 10px;
}

.thumbnail {
    width: 60px;
    height: 40px;
    object-fit: cover;
    margin: 0 5px;
    cursor: pointer;
    opacity: 0.6;
    border: 2px solid transparent;
    border-radius: 5px;
}

.thumbnail.active {
    opacity: 1;
    border-color: #333;
}
