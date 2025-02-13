
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
            text-align: center;
            background-color: #f5f5f5;
            padding: 20px;
        }

        /* Navigation Bar */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #333;
            padding: 15px 20px;
            color: white;
        }

        .nav-title {
            font-size: 20px;
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

        /* Banner */
        .banner_1 img {
            width: 100%;
            max-width: 800px;
            border-radius: 10px;
            margin-top: 20px;
        }

        /* Content Styling */
        p {
            font-size: 18px;
            max-width: 800px;
            margin: 10px auto;
            line-height: 1.5;
        }

        h2 {
            margin-top: 30px;
        }

        ul {
            list-style: none;
            padding: 0;
        }

        ul.publications li {
            background: white;
            padding: 15px;
            margin: 10px auto;
            max-width: 800px;
            border-radius: 10px;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
            text-align: left;
        }

        /* Slideshow */
        .slideshow-container {
            position: relative;
            max-width: 800px;
            margin: 30px auto;
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
            padding: 5px 10px;
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
            font-size: 18px;
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
            margin-top: 10px;
        }

        .dot {
            cursor: pointer;
            height: 10px;
            width: 10px;
            margin: 0 5px;
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
            margin-top: 40px;
            padding: 20px;
            background: #333;
            color: white;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <!-- Navigation Bar -->
    <nav class="navbar">
        <a href="index.html" class="nav-title">Ishan Jha</a>
        <div class="nav-links">
            <a href="projects.html">Projects</a>
            <a href="example.com" target="_blank">Google Scholar</a>
            <a href="example.com" target="_blank">GitHub</a>
        </div>
    </nav>

    <!-- Banner -->
    <div class="banner_1">
        <img src="image.jpg" alt="Banner">
    </div>

    <!-- Introduction -->
    <p>Greetings, I am a ninth grader at Troy High School in Fullerton, California.</p>
    <p>My passions are theoretical mathematics, artificial intelligence, and its applications. Within mathematics, my interests include topology and differential geometry. I also enjoy studying the applications of these ideas in machine learning and industry.</p>
    <p>Another passion of mine is conducting academic research, helping students with math at the UCI Math Circle, and presenting at conferences in AI.</p>

        <!-- Publications Section -->
        <h2>Publications</h2>
        <ul class="publications">
            <li>
                <div><span style="font-weight: 600;">AI-Powered VR Simulations for Semiconductor Industry Training and Education</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">I. Jha</span>, G. Codina, A. Dong, A. Rodriguez, F. Chen, J. Zhu, K. Hong 
</div>
                <div><i>Journal of Advanced Technological Education</i></div>
                <div><span style="color:#005A92;">Accepted November 27, 2024</span></div>
                <div>
                    <a href="https://github.com/Ishanyjha/ishanyjha.github.io/blob/cc91b88b509d26d686f32ebf886e378f5ed2b855/Final%20AI-Powered%20VR%20Simulations%20for%20Semiconductor%20Industry%20Training%20and%20Education_JP%20edited_12-3-24.docx%20(1).pdf" target="_blank" class="arrow-link">paper</a>
                    <a href="https://youtu.be/Ri-jqU0WzQM" target="_blank" class="arrow-link">video demo (short)</a>
                </div>
        </ul>

        <!-- Preprints Section -->
        <h2>Preprints and Reports</h2>
        <h6>*denotes equal contribution</h6>
        <ul class="publications">
            <li>
                <div><span style="font-weight: 600;">Example</span></div>
                <div>Example, <span style="color: #ff1423; font-weight:bold;">Example*</span></div>
                <div>Example</div>
                <div><span style="color:#005A92;">Example N, Example</span></div>
                <div>
                    <a href="https://github.com/sdkyuanpanda/SSP-CUB-2024/blob/b5678afb9f23b7d1544910b107fa32d53cd66db2/ssp_team08_final_report-1.pdf" target="_blank" class="arrow-link">paper</a>
                    <a href="https://github.com/sdkyuanpanda/SSP-CUB-2024/blob/b5678afb9f23b7d1544910b107fa32d53cd66db2/od/ssp_team08_orbital_integration_project_slides.pdf" target="_blank" class="arrow-link">slides</a>
                    <a href="https://github.com/sdkyuanpanda/SSP-CUB-2024" target="_blank" class="arrow-link">code</a>
                </div>
            </li>
        </ul>

  <!-- presenting Section -->
        <h2>Presentations</h2>
        <h6>*denotes equal contribution</h6>
        <ul class="presentations">
            <li>
                <div><span style="font-weight: 600;">AI For Education and Training</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">Ishan Jha</span></div>
                <div><i>Orange County Dept. of Education Future Leaders AI Conference</i></div>
                <div><span style="color: #ff1423;">Presentation, J.W Marriot Anaheim</span></div>
                <div><span style="color:#005A92;">MM DD, YYYY</span></div>
                <div>
                    <a href="https://www.nature.com/articles/s41598-024-61040-3" target="_blank" class="arrow-link">slides</a>
                </div>
            </li>
            <li>
                <div><span style="font-weight: 600;">Student Centered Undergraduate Research Experiences in Creating Virtual Digital Twin Cleanroom.”</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>, Kristal Hong, Gabriel Codina, Alice Dong</div>
                <div><i>TechConnect 2024 World Innovation Conference</i></div>
                <div><span style="color: #ff1423;">Poster and Panel Presentations, Gaylord National Hotel and Center</span></div>
                <div><span style="color:#005A92;">MM DD, YYYY</span></div>
                <div>
                    <a href="https://github.com/Ishanyjha/ishanyjha.github.io/blob/cc91b88b509d26d686f32ebf886e378f5ed2b855/UCI%20START%20Academic%20Poster%20(1).pdf" target="_blank" class="arrow-link">poster</a>
                </div>
            </li>
            <li>
                <div><span style="font-weight: 600;">Digital Twins for Semiconductor Fabrication Education.”</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>, Felicia Chen, Gabriel Codina, Alice Dong, Alexis Rodriguez</div>
                <div><i>California Institute of Technology</i></div>
                <div><span style="color: #ff1423;">Invited Presentation, Moore Courtyard, Electrical Engineering Dept.</span></div>
                <div><span style="color:#005A92;">MM DD, YYYY</span></div>
                <div>
                    <a href="https://github.com/Ishanyjha/ishanyjha.github.io/blob/cc91b88b509d26d686f32ebf886e378f5ed2b855/UCI%20START%20Academic%20Poster%20(1).pdf" target="_blank" class="arrow-link">poster</a>
                </div>
            </li>
            <li>
                <div><span style="font-weight: 600;">Empowering Students Through AI Clubs.”</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">Ishan Jha</span></div>
                <div><i>Orange County Dept. of Education, Student AI Summit</i></div>
                <div><span style="color: #ff1423;">Presentation, J.W Marriot Anaheim.</span></div>
                <div><span style="color:#005A92;">MM DD, YYYY</span></div>
                <div>
                    <a href="https://www.nature.com/articles/s41598-024-61040-3" target="_blank" class="arrow-link">poster</a>
                    <a href="https://www.youtube.com/watch?v=NugQOMaJuuw" target="_blank" class="arrow-link">video</a>
                </div>
            </li>
        </ul>

    <!-- Slideshow -->
    <div class="slideshow-container">
        <div class="mySlides fade">
            <div class="numbertext">1 / 5</div>
            <img src="IMG_5966.jpeg" alt="TechConnect">
            <div class="text">At TechConnect in D.C</div>
        </div>
        <div class="mySlides fade">
            <div class="numbertext">2 / 5</div>
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

    <!-- Footer -->
    <footer>
        Copyright &copy; Free to Use.
    </footer>

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
