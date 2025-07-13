
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <style>
        /* General Styling */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        .publications li {
            background: #fafafa;
            padding: 25px;
            margin: 20px auto;
            border-radius: 10px;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
            max-width: 1200px;
        }

        /* Slideshow */
        .slideshow-container {
            position: relative;
            max-width: 100%;
            margin: 40px auto;
        }

        .mySlides {
            display: none;
            position: relative;
        }

        .mySlides img {
            width: 100%;
            max-height: 600px;
            object-fit: cover;
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
            top: 10px;
            left: 20px;
        }

        .text {
            bottom: 15px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 20px;
        }

        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            padding: 12px;
            font-size: 24px;
            color: white;
            background-color: rgba(0, 0, 0, 0.5);
            border-radius: 5px;
            user-select: none;
            transform: translateY(-50%);
        }

        .prev { left: 20px; }
        .next { right: 20px; }

        .prev:hover, .next:hover {
            background-color: rgba(0, 0, 0, 0.8);
        }

        .dots-container {
            text-align: center;
            margin-top: 25px;
        }

        .dot {
            cursor: pointer;
            height: 14px;
            width: 14px;
            margin: 0 8px;
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
            margin-top: 60px;
            padding: 25px;
            background: #333;
            color: white;
            font-weight: bold;
            border-radius: 10px;
            text-align: center;
        }
    </style>
</head>
<body>

        <!-- Navigation Bar -->
        <nav class="navbar">
            <div class="navbar-content">
                <a href="index.html" class="nav-title" style="text-decoration: none;">Ishan Jha</a>
                <div class="nav-links">
                    <a href="projects.html" class="nav-link">Projects</a>
                    <!-- <a href="assets/Main_e5905a25-9683-46d6-865c-aaed7ef06243_720x.png" target="_blank" class="nav-link">CV</a> -->
                    <a href="https://scholar.google.com/citations?user=KJxBoMAAAAAJ&hl=en&" target="_blank" class="nav-link">Google Scholar</a>
                    <a href="https://github.com/ishanyjha" target="_blank" class="nav-link">GitHub</a>
                </div>
            </div>
        </nav>

        <!-- Introduction -->
        <section>
            <h1><center>Welcome!</center></h1>
            <p>Greetings, I am a ninth grader at Troy High School in Fullerton, California.</p>
            <p>My passions are theoretical mathematics, artificial intelligence, and its applications. Within artificial intelligence, my interests include geometric deep learning and physics-informed neural networks (PINNS, PINOs, PFNOs, SB/PI-NNs) which I am exploring through literature and projects. I also enjoy studying the applications of these ideas in machine learning and industry.</p>
            <p>Another passion of mine is conducting academic research, helping students with math at the UCI Math Circle, and presenting at conferences in AI. I love connecting with like minded people who are interested in AI, math, and research!</p>
        </section>

        <!-- Publications Section -->
        <section>
            <h2><center>Publications</center></h2>
            <ul class="publications">
                <li>
                <div><span style="font-weight: 600;">AI-Powered VR Simulations for Semiconductor Industry Training and Education</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">I. Jha</span>, G. Codina, A. Dong, K. Hong, A. Rodriguez, F. Chen, J. Zhu, G.P Li</div>
                <div><i>Journal of Advanced Technological Education</i></div>
                <div><span style="color:#005A92;">Accepted November 27, 2024</span></div>
                <div>
                    <a href="https://zenodo.org/records/14933891" target="_blank" class="arrow-link">paper</a>
                    <a href="https://www.youtube.com/watch?v=Ri-jqU0WzQM&t=5s" class="arrow-link">video demo</a>
                    <a href="https://www.nsf.gov/news/sparking-curiosity-future-semiconductor-workforce" class="arrow-link">NSF feature</a>
                </div>
                </li>
            </ul>
        </section>
        <section>
            <h2><center>Presentations</center></h2>
            <ul class="publications">
                <li>
                <div><span style="font-weight: 600;">AI For Education and Training</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>, Others</div>
                <div>Orange County Department of Education</div>
                <div><i>Future Leaders AI Conference</i></div>                
                <div>Presentation, J.W Marriot</div>
                <div><span style="color:#005A92;">November 20, 2024</span></div>
                <div>
                    <a href="https://docs.google.com/presentation/d/1trymELfKDnHdj340TnMqMLKF8STPKpN9xWVmITHn03Y/edit?usp=sharing" target="_blank" class="arrow-link">paper</a>      
                </div>
                </li>
                <li>
                <div><span style="font-weight: 600;">Student Centered Undergraduate Research Experiences in Creating Virtual Digital Twin Cleanroom.</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>, Gabriel Codina, Alice Dong, Kristal Hong</div>
                <div>TechConnect World Innovation Conference</div>
                <div><i>XRAI for Training Symposium</i></div>                
                <div>Poster presentation and panel, The Gaylord National Hotel</div>
                <div><span style="color:#005A92;">June 16-17, 2024</span></div>
                <div>
                    <a href="https://github.com/Ishanyjha/ishanyjha.github.io/blob/2c21d5897545eb75615c337f28bb3d09b966de41/UCI%20START%20Academic%20Poster%20(1).pdf" target="_blank" class="arrow-link">poster</a>               
                </div>
                </li>
                <li>
                <div><span style="font-weight: 600;">Digital Twins for Semiconductor Fabrication Education.</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">Ishan Jha</span>, Gabriel Codina, Alice Dong, Kristal Hong, Felicia Chen</div>
                <div>California Institue of Technology</div>
                <div><i>Kavli Nanoscience Institute</i></div>                
                <div>Poster and presentation, Moore Courtyard and EECS Bldg.</div>
                <div><span style="color:#005A92;">May 24, 2024</span></div>
                <div>
                    <a href="https://github.com/Ishanyjha/ishanyjha.github.io/blob/2c21d5897545eb75615c337f28bb3d09b966de41/UCI%20START%20Academic%20Poster%20(1).pdf" target="_blank" class="arrow-link">poster</a>                
                </div>
                </li>  
                <li>
                <div><span style="font-weight: 600;">Empowering Students Through AI Clubs</span></div>
                <div><span style="color: #ff1423; font-weight:bold;">Ishan Jha</span></div>
                <div>Orange County Department of Education</div>
                <div><i>Student AI Convening</i></div>                
                <div>Presentation, J.W Marriot</div>
                <div><span style="color:#005A92;">May 4, 2024</span></div>
                <div>
                    <a href="https://docs.google.com/presentation/d/1hj7_zbnqVg7TAxt5kjAVCEwvPyUrD_DBp5Ijl_JvQo8/edit?usp=sharing" target="_blank" class="arrow-link">paper</a>
                    <a href="https://www.youtube.com/watch?v=NugQOMaJuuw" class="arrow-link">video demo</a>                
                </div>
                </li>            
            </ul>
        </section>

        <!-- Slideshow -->
        <section>
            <h2><center>Gallery</center></h2>
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
        <footer>
            <p class="footer_bold">Copyright &copy; 2025 Ishan Jha</p>
        </footer></body>
</html>
