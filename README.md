<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ishan Jha</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        /* General Styling */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        body {
            background-color: #f5f5f5;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 40px 20px;
        }

        /* Centered Container */
        .container {
            background: white;
            width: 85%;
            max-width: 1100px;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        /* Navigation Bar */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #333;
            padding: 15px 20px;
            border-radius: 10px;
            margin-bottom: 40px;
        }

        .nav-title {
            font-size: 22px;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-size: 16px;
        }

        .nav-links a:hover {
            text-decoration: underline;
        }

        /* Section Styling */
        section {
            margin-bottom: 50px;
        }

        h1, h2 {
            margin-bottom: 20px;
        }

        p {
            font-size: 18px;
            line-height: 1.7;
            margin-bottom: 20px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        ul {
            list-style: none;
            padding: 0;
        }

        .publications li {
            background: #fafafa;
            padding: 20px;
            margin: 20px auto;
            border-radius: 10px;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
            text-align: left;
            max-width: 900px;
        }

        /* Slideshow */
        .slideshow-container {
            position: relative;
            max-width: 900px;
            margin: 40px auto;
        }

        .mySlides {
            display: none;
            position: relative;
        }

        .mySlides img {
            width: 100%;
            border-radius: 10px;
        }

        .numbertext, .text {
            position: absolute;
            color: white;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 8px 12px;
            border-radius: 5px;
        }

        .numbertext {
            top: 8px;
            left: 16px;
        }

        .text {
            bottom: 8px;
            left: 50%;
            transform: translateX(-50%);
        }

        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            padding: 10px;
            font-size: 20px;
            color: white;
            background-color: rgba(0, 0, 0, 0.5);
            border-radius: 5px;
            user-select: none;
            transform: translateY(-50%);
        }

        .prev { left: 10px; }
        .next { right: 10px; }

        .prev:hover, .next:hover {
            background-color: rgba(0, 0, 0, 0.8);
        }

        .dots-container {
            text-align: center;
            margin-top: 20px;
        }

        .dot {
            cursor: pointer;
            height: 12px;
            width: 12px;
            margin: 0 6px;
            background-color: #bbb;
            border-radius: 50%;
            display: inline-block;
            transition: background-color 0.3s;
        }

        .active, .dot:hover {
            background-color: #717171;
        }

        /* Footer */
        footer {
            margin-top: 50px;
            padding: 20px;
            background: #333;
            color: white;
            font-weight: bold;
            border-radius: 10px;
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Navigation Bar -->
        <nav class="navbar">
            <a href="index.html" class="nav-title">Ishan Jha</a>
            <div class="nav-links">
                <a href="projects.html">Projects</a>
                <a href="example.com" target="_blank">Google Scholar</a>
                <a href="example.com" target="_blank">GitHub</a>
            </div>
        </nav>

        <!-- Introduction -->
        <section>
            <h1>Welcome!</h1>
            <p>Greetings, I am a ninth grader at Troy High School in Fullerton, California.</p>
            <p>My passions are theoretical mathematics, artificial intelligence, and its applications. Within mathematics, my interests include topology and differential geometry. I also enjoy studying the applications of these ideas in machine learning and industry.</p>
            <p>Another passion of mine is conducting academic research, helping students with math at the UCI Math Circle, and presenting at conferences in AI.</p>
        </section>

        <!-- Publications Section -->
        <section>
            <h2>Publications</h2>
            <ul class="publications">
                <li>
                    <strong>AI-Powered VR Simulations for Semiconductor Industry Training and Education</strong><br>
                    <span style="color: #ff1423;">I. Jha</span>, G. Codina, A. Dong, A. Rodriguez, F. Chen, J. Zhu, K. Hong<br>
                    <em>Journal of Advanced Technological Education</em><br>
                    Accepted November 27, 2024<br>
                    <a href="paper-link" target="_blank">Paper</a> | 
                    <a href="video-link" target="_blank">Video Demo</a>
                </li>
            </ul>
        </section>

        <!-- Slideshow -->
        <section>
            <h2>Gallery</h2>
            <div class="slideshow-container">
                <div class="mySlides fade">
                    <img src="IMG_5966.jpeg" alt="TechConnect">
                    <div class="text">At TechConnect in D.C</div>
                </div>
                <div class="mySlides fade">
                    <img src="IMG_5727.jpeg" alt="White House">
                    <div class="text">At the White House</div>
                </div>
                <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
                <a class="next" onclick="plusSlides(1)">&#10095;</a>
            </div>

            <div class="dots-container">
                <span class="dot" onclick="currentSlide(1)"></span>
                <span class="dot" onclick="currentSlide(2)"></span>
            </div>
        </section>

        <!-- Footer -->
        <footer>
            Copyright &copy; Free to Use.
        </footer>
    </div>

    <script>
        let slideIndex = 1;
        showSlides(slideIndex);

        function plusSlides(n) { showSlides(slideIndex += n); }
        function currentSlide(n) { showSlides(slideIndex = n); }
        function showSlides(n) {
            let slides = document.getElementsByClassName("mySlides");
            let dots = document.getElementsByClassName("dot");

            if (n > slides.length) { slideIndex = 1; }
            if (n < 1) { slideIndex = slides.length; }

            for (let slide of slides) { slide.style.display = "none"; }
            for (let dot of dots) { dot.className = dot.className.replace(" active", ""); }

            slides[slideIndex - 1].style.display = "block";
            dots[slideIndex - 1].className += " active";
        }
    </script>

</body>
</html>
