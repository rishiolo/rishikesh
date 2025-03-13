<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Loading Page</title>
</head>
<body>
    <div id="loader-wrapper">
        <div class="loader-section section-left"></div>
        <div class="loader-section section-right"></div>
        <div id="loader"></div>
    </div>
    <div id="content">
        <h1>This is our page title</h1>
        <p>Lorem ipsum dolor sit amet.</p>
    </div>
    <script src="main.js"></script>
</body>
</html>




* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
}

#loader-wrapper {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1000;
    background-color: #222;
}

.loader-section {
    position: fixed;
    top: 0;
    width: 50%;
    height: 100%;
    background: #222;
}

.section-left {
    left: 0;
}

.section-right {
    right: 0;
}

#loader {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 60px;
    height: 60px;
    border: 8px solid #fff;
    border-top: 8px solid #3498db;
    border-radius: 50%;
    animation: spin 1s linear infinite;
    transform: translate(-50%, -50%);
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

.loaded #loader-wrapper {
    opacity: 0;
    visibility: hidden;
    transition: opacity 0.3s ease-out;
}





$(document).ready(function() {
    setTimeout(function() {
        $('body').addClass('loaded');
    }, 3000); // Adjust the time as needed
});
