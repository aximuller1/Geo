<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Geolocation Test</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 90vh;
            background-color: #f0f0f0;
        }

        #location {
            text-align: center;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }

        #location button {
            background-color: #007bff;
            color: #fff;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
        }

        #location button:hover {
            background-color: #0056b3;
        }

        #message {
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <div id="location">
        <h1>Geolocation Test</h1>
        <p>Click the button below to get your current location.</p>
        <button onclick="getLocation()">Get Location</button>
        <p id="message"></p>
    </div>

    <script>
        function getLocation() {
            const message = document.getElementById('message');

            // Check if Geolocation is supported
            if (navigator.geolocation) {
                message.textContent = "Fetching location...";
                navigator.geolocation.getCurrentPosition(showPosition, showError);
            } else {
                message.textContent = "Geolocation is not supported by this browser.";
            }
        }

        // Show the position on success
        function showPosition(position) {
            const latitude = position.coords.latitude;
            const longitude = position.coords.longitude;
            document.getElementById('message').textContent = `Latitude: ${latitude}°, Longitude: ${longitude}°`;
        }

        // Show error messages
        function showError(error) {
            switch (error.code) {
                case error.PERMISSION_DENIED:
                    document.getElementById('message').textContent = "User denied the request for Geolocation.";
                    break;
                case error.POSITION_UNAVAILABLE:
                    document.getElementById('message').textContent = "Location information is unavailable.";
                    break;
                case error.TIMEOUT:
                    document.getElementById('message').textContent = "The request to get user location timed out.";
                    break;
                case error.UNKNOWN_ERROR:
                    document.getElementById('message').textContent = "An unknown error occurred.";
                    break;
            }
        }
    </script>

</body>
</html>
