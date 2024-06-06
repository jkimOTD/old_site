
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Password Protected Section</title>
    <style>
        .responsive-iframe-container {
            position: relative;
            width: 100%;
            height: 0;
            padding-top: 56.25%; /* Aspect ratio 16:9 */
            padding-bottom: 0;
            box-shadow: 0 2px 8px 0 rgba(63, 69, 81, 0.16);
            margin-top: 1.6em;
            margin-bottom: 0.9em;
            overflow: hidden;
            border-radius: 8px;
            will-change: transform;
        }
        .responsive-iframe {
            position: absolute;
            width: 80%; /* Default width for desktop and fullscreen mode */
            height: 80%; /* Default height for desktop and fullscreen mode */
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border: none;
            padding: 0;
            margin: 0;
        }
        @media only screen and (max-width: 600px) {
            .responsive-iframe {
                width: 90%; /* Adjust width for smaller screens */
                height: 90%; /* Adjust height for smaller screens */
            }
        }
        #locked-section {
            display: none;
        }
        #placeholder-section {
            display: none;
        }
    </style>
</head>
<body>
    <div id="placeholder-section">
        <div id="password-section">
            <p>Enter password: </p>
            <input type="password" id="password-input" placeholder="Enter password">
            <button onclick="checkPassword()">Submit</button>
        </div>
    </div>
    <div id="locked-section">
        <div class="responsive-iframe-container">
            <iframe loading="lazy" class="responsive-iframe" src="https://www.canva.com/design/DAGHY9Vhj7Y/IYCqGwZUwQnDW8zRzi-dxg/view?embed" allowfullscreen="allowfullscreen" allow="fullscreen"></iframe>
        </div>
        
        <a href="https://forms.gle/wxX3j2o6irCBaNoQ7">Click here to take the pre-module knowledge check</a><br> 
            
        <a href="https://forms.gle/h3mC45XLMKZFunuT9">Click here to take the post-module knowledge check</a>

    </div>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            // Set the time when the section should be unlocked
            const unlockTime = new Date("July 10, 2024 19:00:00").getTime();

            // Function to check the current time and unlock the section if the time has come
            function checkTime() {
                const currentTime = new Date().getTime();

                if (currentTime >= unlockTime) {
                    document.getElementById("locked-section").style.display = "block";
                } else {
                    document.getElementById("placeholder-section").style.display = "block";
                }
            }

            // Check the time immediately on load
            checkTime();
        });

        function checkPassword() {
            const enteredPassword = document.getElementById("password-input").value;
            const correctPassword = "flute"; // Set your password here

            if (enteredPassword === correctPassword) {
                document.getElementById("locked-section").style.display = "block";
                document.getElementById("placeholder-section").style.display = "none";
            } else {
                alert("Incorrect password. Please try again.");
            }
        }
    </script>
</body>
</html>
