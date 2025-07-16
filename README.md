
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ishan Jha</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        body {
            background: white;
            color: #333;
            line-height: 1.6;
        }

        /* Navigation */
        .navbar {
            background: white;
            border-bottom: 1px solid #e5e5e5;
            padding: 1rem 1.5rem;
        }

        .navbar-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-title {
            font-size: 1.25rem;
            font-weight: bold;
            color: #111;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 1.5rem;
        }

        .nav-link {
            color: #555;
            text-decoration: none;
        }

        .nav-link:hover {
            color: #111;
        }

        /* Main content */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem 1.5rem;
        }

        /* Introduction */
        .intro {
            margin-bottom: 3rem;
        }

        .intro h1 {
            font-size: 2rem;
            font-weight: bold;
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .intro-content {
            max-width: 800px;
            margin: 0 auto;
            color: #444;
        }

        .intro-content p {
            margin-bottom: 1rem;
        }

        /* Sections */
        .section {
            margin-bottom: 3rem;
        }

        .section h2 {
            font-size: 1.5rem;
            font-weight: bold;
            text-align: center;
            margin-bottom: 2rem;
        }

        /* Publication items */
        .publication-item {
            max-width: 800px;
            margin: 0 auto 2rem auto;
        }

        .publication-title {
            font-size: 1.125rem;
            font-weight: 600;
            color: #111;
            margin-bottom: 0.5rem;
            line-height: 1.4;
        }

        .publication-authors {
            font-size: 1rem;
            color: #111;
            margin-bottom: 0.5rem;
        }

        .author-highlight {
            color: #ff1423;
            font-weight: bold;
        }

        .publication-venue {
            font-size: 1rem;
            font-style: italic;
            color: #111;
            margin-bottom: 0.5rem;
        }

        .publication-institution {
            font-size: 1rem;
            font-style: italic;
            color: #111;
            margin-bottom: 0.5rem;
        }

        .publication-details {
            font-size: 1rem;
            color: #111;
            margin-bottom: 0.5rem;
        }

        .publication-date {
            font-size: 1rem;
            color: #005A92;
            margin-bottom: 1rem;
        }

        /* Abstract dropdown */
        .abstract-container {
            margin: 1rem 0;
        }

        .abstract-button {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            background: none;
            border: none;
            font-size: 1rem;
            font-weight: 500;
            color: #111;
            cursor: pointer;
            padding: 0;
        }

        .abstract-button:hover {
            color: #555;
        }

        .chevron {
            width: 16px;
            height: 16px;
            transition: transform 0.2s;
        }

        .chevron.rotated {
            transform: rotate(180deg);
        }

        .abstract-content {
            max-height: 0;
            opacity: 0;
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .abstract-content.open {
            max-height: 400px;
            opacity: 1;
            margin-top: 1rem;
        }

        .abstract-text {
            font-size: 1rem;
            color: #444;
            line-height: 1.6;
        }

        /* Links */
        .publication-links {
            display: flex;
            gap: 0.25rem;
            font-size: 1rem;
            flex-wrap: wrap;
        }

        .link-bracket {
            color: #111;
        }

        .publication-link {
            color: #2563eb;
            text-decoration: underline;
        }

        .publication-link:hover {
            color: #1d4ed8;
        }

        /* Footer */
        .footer {
            margin-top: 4rem;
            padding: 1.5rem;
            background: #333;
            color: white;
            text-align: center;
            border-radius: 10px;
            margin-left: 1.5rem;
            margin-right: 1.5rem;
        }

        .footer p {
            font-weight: bold;
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="navbar">
        <div class="navbar-content">
            <div class="nav-links">
                <center>
                <a href="projects.html" class="nav-link">Projects</a>
                <a href="https://scholar.google.com/citations?user=KJxBoMAAAAAJ&hl=en&" target="_blank" class="nav-link">Google Scholar</a>
                <a href="https://github.com/ishanyjha" target="_blank" class="nav-link">GitHub</a>
                </center>
            </div>
        </div>
    </nav>

    <div class="container">
        <!-- Introduction -->
        <section class="intro">
            <h1>Welcome!</h1>
            <div class="intro-content">
                <p>Greetings, I am a ninth grader at Troy High School in Fullerton, California.</p>
                <p>My passions are theoretical mathematics, artificial intelligence, and its applications. Within artificial intelligence, I am currently exploring computer vision and physics-informed neural networks through literature and projects. I also enjoy studying the applications of these ideas in machine learning and industry.</p>
                <p>Another passion of mine is conducting academic research, helping students with math at the UCI Math Circle, and presenting at conferences in AI. I love connecting with like minded people who are interested in AI, math, and research!</p>
            </div>
        </section>

        <!-- Publications Section -->
        <section class="section">
            <h2>Publications</h2>
            
            <div class="publication-item">
                <div class="publication-title">AI-Powered VR Simulations for Semiconductor Industry Training and Education</div>
                <div class="publication-authors"><span class="author-highlight">I. Jha</span>, G. Codina, A. Dong, K. Hong, A. Rodriguez, F. Chen, J. Zhu, G.P Li</div>
                <div class="publication-venue">Journal of Advanced Technological Education</div>
                <div class="publication-date">Accepted November 27, 2024</div>
                
                <div class="abstract-container">
                    <button class="abstract-button" onclick="toggleAbstract('pub-1')">
                        <span>abstract</span>
                        <svg class="chevron" id="chevron-pub-1" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <polyline points="6,9 12,15 18,9"></polyline>
                        </svg>
                    </button>
                    <div class="abstract-content" id="abstract-pub-1">
                        <div class="abstract-text">
                            VR simulations hold great potential for training, and AI capabilities can scaffold the learning process through large language model (LLM) powered tutors that provide personalized responses to students. However, such training typically requires multidisciplinary teams of programmers, 3D artists, and instructional designers, and complex software such as game engines. If such advanced training could be created by less skilled users using simpler software, then a vast amount of quality training would become available to help address the workforce challenges. Here, we investigate whether it is feasible for community college and K-12 students to create such VR simulations. We describe how the students in the author group designed and created an AI-powered VR simulation for a common semiconductor fabrication process and pilot-tested it to evaluate its effectiveness. Pilot test results show that students reported high levels of engagement, ease of use, and increased interest in and knowledge of semiconductor manufacturing. Linear regression analysis of the data revealed that engagement, ease of use, knowledge increase, and interest increase are significant predictors of the desire to use VR training in the future. These findings show that given well-designed software tools and expert mentoring, a team of community college and K-12 students can successfully produce engaging and effective VR training simulations. Our work suggests a nationally scalable approach to addressing the semiconductor workforce challenge while also training the next generation of VR simulation developers. To our knowledge, this is the first time K-12 and community college students have developed and evaluated VR simulations with high efficiency and engagement.
                        </div>
                    </div>
                </div>

                <div class="publication-links">
                    <span class="link-bracket">[</span>
                    <a href="https://zenodo.org/records/14933891" target="_blank" class="publication-link">paper</a>
                    <span class="link-bracket">] [</span>
                    <a href="https://www.youtube.com/watch?v=Ri-jqU0WzQM&t=5s" target="_blank" class="publication-link">video demo</a>
                    <span class="link-bracket">] [</span>
                    <a href="https://www.nsf.gov/news/sparking-curiosity-future-semiconductor-workforce" target="_blank" class="publication-link">NSF feature</a>
                    <span class="link-bracket">]</span>
                </div>
            </div>
        </section>

        <!-- Presentations Section -->
        <section class="section">
            <h2>Presentations</h2>
            
            <div class="publication-item">
                <div class="publication-title">AI For Education and Training</div>
                <div class="publication-authors"><span class="author-highlight">Ishan Jha, </span>K. Hong, N. Vatanshenas, A. Ashcroft, A. Ahmadi, R. Almache, R. Dhar, H. Mandadi, R.D. Melara, J.J. Mosquera, P.K. Stout, B. Harrop</div>
                <div class="publication-venue">TechConnect Word Conference</div>
                <div class="publication-institution">University of California, Irvine ; Princeton University</div>
                <div class="publication-details">Poster and Invited Talk, J.W Marriot Austin</div>
                <div class="publication-date">June 9-11, 2025</div>
                

                <div class="publication-links">
                    <span class="link-bracket">[</span>
                    <a href="https://princeton.edu" target="_blank" class="publication-link">poster</a>
                    <span class="link-bracket">]</span>
                </div>
            </div>

            <div class="publication-item">
                <div class="publication-title">Agentic AI-embedded Digital Twins for Semiconductor Manufacturing Education</div>
                <div class="publication-authors"><span class="author-highlight">Ishan Jha,</span> Kristal Hong, Nick Vatanshenas, Adam Ashcroft</div>
                <div class="publication-venue">California Institute of Technology</div>
                <div class="publication-institution">Kavli Nanoscience Institute</div>
                <div class="publication-details">Poster Presentation, Moore Courtyard</div>
                <div class="publication-date">May 30, 2025</div>
                
    

                <div class="publication-links">
                    <span class="link-bracket">[</span>
                    <a href="https://github.com/Ishanyjha/ishanyjha.github.io/blob/b8a08e5515cd70a42ba76ed5155820049a36e841/Poster%20for%20Caltech%202025.pdf" target="_blank" class="publication-link">poster</a>
                    <span class="link-bracket">]</span>
                </div>
            </div>

            <div class="publication-item">
                <div class="publication-title">AI For Education and Training</div>
                <div class="publication-authors"><span class="author-highlight">Ishan Jha</span>, Others</div>
                <div class="publication-venue">Orange County Department of Education</div>
                <div class="publication-institution">Future Leaders AI Conference</div>
                <div class="publication-details">Presentation, J.W Marriot</div>
                <div class="publication-date">November 20, 2024</div>
                
                <div class="publication-links">
                    <span class="link-bracket">[</span>
                    <a href="https://docs.google.com/presentation/d/1trymELfKDnHdj340TnMqMLKF8STPKpN9xWVmITHn03Y/edit?usp=sharing" target="_blank" class="publication-link">slides</a>
                    <span class="link-bracket">]</span>
                </div>
            </div>

            <div class="publication-item">
                <div class="publication-title">Student Centered Undergraduate Research Experiences in Creating Virtual Digital Twin Cleanroom.</div>
                <div class="publication-authors"><span class="author-highlight">Ishan Jha</span>, Gabriel Codina, Alice Dong, Kristal Hong</div>
                <div class="publication-venue">TechConnect World Innovation Conference</div>
                <div class="publication-institution">XRAI for Training Symposium</div>
                <div class="publication-details">Poster presentation and panel, The Gaylord National Hotel</div>
                <div class="publication-date">June 16-17, 2024</div>
                
                <div class="publication-links">
                    <span class="link-bracket">[</span>
                    <a href="https://github.com/Ishanyjha/ishanyjha.github.io/blob/2c21d5897545eb75615c337f28bb3d09b966de41/UCI%20START%20Academic%20Poster%20(1).pdf" target="_blank" class="publication-link">poster</a>
                    <span class="link-bracket">]</span>
                </div>
            </div>

            <div class="publication-item">
                <div class="publication-title">Digital Twins for Semiconductor Fabrication Education.</div>
                <div class="publication-authors"><span class="author-highlight">Ishan Jha</span>, Gabriel Codina, Alice Dong, Kristal Hong, Felicia Chen</div>
                <div class="publication-venue">California Institute of Technology</div>
                <div class="publication-institution">Kavli Nanoscience Institute</div>
                <div class="publication-details">Poster and presentation, Moore Courtyard and EECS Bldg.</div>
                <div class="publication-date">May 24, 2024</div>
                
                <div class="publication-links">
                    <span class="link-bracket">[</span>
                    <a href="https://github.com/Ishanyjha/ishanyjha.github.io/blob/2c21d5897545eb75615c337f28bb3d09b966de41/UCI%20START%20Academic%20Poster%20(1).pdf" target="_blank" class="publication-link">poster</a>
                    <span class="link-bracket">]</span>
                </div>
            </div>

            <div class="publication-item">
                <div class="publication-title">Empowering Students Through AI Clubs</div>
                <div class="publication-authors"><span class="author-highlight">Ishan Jha</span></div>
                <div class="publication-venue">Orange County Department of Education</div>
                <div class="publication-institution">Student AI Convening</div>
                <div class="publication-details">Presentation, J.W Marriot</div>
                <div class="publication-date">May 4, 2024</div>
                
                <div class="publication-links">
                    <span class="link-bracket">[</span>
                    <a href="https://docs.google.com/presentation/d/1hj7_zbnqVg7TAxt5kjAVCEwvPyUrD_DBp5Ijl_JvQo8/edit?usp=sharing" target="_blank" class="publication-link">slides</a>
                    <span class="link-bracket">] [</span>
                    <a href="https://www.youtube.com/watch?v=NugQOMaJuuw" target="_blank" class="publication-link">video</a>
                    <span class="link-bracket">]</span>
                </div>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer class="footer">
        <p>Copyright &copy; 2025 Ishan Jha</p>
    </footer>

    <script>
        function toggleAbstract(id) {
            const abstractContent = document.getElementById('abstract-' + id);
            const chevron = document.getElementById('chevron-' + id);
            
            if (abstractContent.classList.contains('open')) {
                abstractContent.classList.remove('open');
                chevron.classList.remove('rotated');
            } else {
                abstractContent.classList.add('open');
                chevron.classList.add('rotated');
            }
        }
    </script>
</body>
</html>
