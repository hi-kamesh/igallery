# Ex.08 Design of Interactive Image Gallery
## Date: 22-04-2025

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
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Modern Responsive Gallery</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Arial', sans-serif;
      background-color: #121212; /* Dark Background */
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      color: #EAEAEA; /* Light text color for readability */
    }

    h1 {
      background-color: #8A2BE2; /* Electric Purple */
      color: white;
      padding: 20px;
      text-align: center;
      width: 100%;
      font-size: 2.5em;
      margin-bottom: 20px;
      border-radius: 8px;
      animation: slideIn 0.5s ease-out;
    }

    h2 {
      font-size: 1.2em;
      margin-bottom: 40px;
      color: #EAEAEA;
      animation: fadeIn 1s ease-in;
    }

    @keyframes slideIn {
      0% { transform: translateY(-30px); opacity: 0; }
      100% { transform: translateY(0); opacity: 1; }
    }

    @keyframes fadeIn {
      0% { opacity: 0; }
      100% { opacity: 1; }
    }

    .gallery-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      justify-content: center;
      width: 90%;
      margin-top: 20px;
    }

    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease-in-out, box-shadow 0.3s ease;
      height: 250px;
      background-color: #1C1C1C; /* Dark gray background for items */
      animation: fadeInUp 0.6s ease-out;
    }

    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(30px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease-in-out;
      border-radius: 12px;
    }

    .gallery-item:hover img {
      transform: scale(1.1);
    }

    .gallery-item:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.5); /* Larger shadow on hover */
    }

    .gallery-item a {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background-color: rgba(0, 0, 0, 0.4); /* Dark overlay */
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transition: opacity 0.4s ease-in-out;
      border-radius: 12px;
    }

    .gallery-item:hover a {
      opacity: 1;
    }

    .view-button {
      color: white;
      font-size: 1.2em;
      background-color: #00C6FF; /* Vibrant Cyan for hover button */
      padding: 10px 20px;
      border-radius: 6px;
      text-decoration: none;
      opacity: 0.9;
      transition: opacity 0.4s ease, transform 0.3s ease;
    }

    .view-button:hover {
      opacity: 1;
      transform: translateY(-5px); /* Slight upward movement on hover */
    }

    @media only screen and (max-width: 768px) {
      .gallery-container {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media only screen and (max-width: 480px) {
      .gallery-container {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <h1>Vintage and Retro Cars Responsive Image Gallery</h1>
  <h2>BALA SARAVANAN K - 24900611</h2>

  <div class="gallery-container">
    <div class="gallery-item">
      <img src="1.jpeg" alt="Cinque Terre">
      <a href="1.jpeg" target="_blank">
        <span class="view-button">View Full Image</span>
      </a>
    </div>
    <div class="gallery-item">
      <img src="2.jpeg" alt="Forest">
      <a href="2.jpeg" target="_blank">
        <span class="view-button">View Full Image</span>
      </a>
    </div>
    <div class="gallery-item">
      <img src="3.jpeg" alt="Northern Lights">
      <a href="3.jpeg" target="_blank">
        <span class="view-button">View Full Image</span>
      </a>
    </div>
    <div class="gallery-item">
      <img src="4.jpeg" alt="Mountains">
      <a href="4.jpeg" target="_blank">
        <span class="view-button">View Full Image</span>
      </a>
    </div>
    <div class="gallery-item">
      <img src="5.jpeg" alt="Mountains">
      <a href="5.jpeg" target="_blank">
        <span class="view-button">View Full Image</span>
      </a>
    </div>
    <div class="gallery-item">
      <img src="6.jpeg" alt="Mountains">
      <a href="6.jpeg" target="_blank">
        <span class="view-button">View Full Image</span>
      </a>
    </div>
  </div>

  <script>
    const galleryItems = document.querySelectorAll('.gallery-item');
    galleryItems.forEach(item => {
      item.addEventListener('mouseenter', () => {
        item.querySelector('a').style.opacity = '1';
      });
      item.addEventListener('mouseleave', () => {
        item.querySelector('a').style.opacity = '0';
      });
    });
  </script>

</body>
</html>

```

## OUTPUT:
![Screenshot 2025-04-22 214040](https://github.com/user-attachments/assets/91d2210c-fe10-46d8-ae8c-b39ad6e89b9a)
![Screenshot 2025-04-22 214044](https://github.com/user-attachments/assets/4d101066-f6e1-4867-8d08-554225411ad3)
![Screenshot 2025-04-22 214048](https://github.com/user-attachments/assets/384cc7f7-c202-4cb0-8101-ea02a5019d0a)
![Screenshot 2025-04-22 214052](https://github.com/user-attachments/assets/5b567509-500a-4b74-aa17-08d1ad205e08)
![Screenshot 2025-04-22 214107](https://github.com/user-attachments/assets/0a785895-d784-48c0-9bc7-ee45a431ed0c)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
