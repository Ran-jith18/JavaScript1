<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <style>
        .gallery {
            display: flex;
            flex-wrap: wrap;
        }
        .gallery img {
            width: 200px;
            margin: 10px;
            transition: transform 0.3s ease, filter 0.3s ease;
        }
        .highlight {
            transform: scale(1.1); /* Slight zoom effect */
            filter: brightness(1.2); /* Slight brightness boost */
        }
    </style>
</head>
<body>
    <h1>Interactive Photo Gallery</h1>
    <div class="gallery">
        <img src="image1.jpg" alt="Image 1" class="gallery-item">
        <img src="image2.jpg" alt="Image 2" class="gallery-item">
        <img src="image3.jpg" alt="Image 3" class="gallery-item">
        <img src="image4.jpg" alt="Image 4" class="gallery-item">
    </div>

    <script>
        // Function to handle mouse over event
        function handleMouseOver(event) {
            event.target.classList.add('highlight'); // Add the 'highlight' class to the image
        }

        // Function to handle mouse out event
        function handleMouseOut(event) {
            event.target.classList.remove('highlight'); // Remove the 'highlight' class from the image
        }

        // Select all gallery items
        const galleryImages = document.querySelectorAll('.gallery-item');

        // Add event listeners for mouse over and mouse out
        galleryImages.forEach(image => {
            image.addEventListener('mouseover', handleMouseOver); // Trigger on mouseover
            image.addEventListener('mouseout', handleMouseOut);   // Trigger on mouseout
        });
    </script>
</body>
</html>
