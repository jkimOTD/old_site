
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Iframe</title>
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
            width: 70%;
            height: 70%;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
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
    </style>
</head>
<body>
    <div class="responsive-iframe-container">
        <iframe loading="lazy" class="responsive-iframe" src="https://www.canva.com/design/DAGGYfTVDFU/2okhskRT1PITlyavT1AAOA/view?embed" allowfullscreen="allowfullscreen" allow="fullscreen"></iframe>
    </div>
</body>
</html>

</div>

[Click here to take the pre-module knowledge check](https://forms.gle/i1GvF7vxFe7C3FySA)

[Click here to take the post-module knowledge check](https://forms.gle/msZcdK3EDeMQ2P1DA)

