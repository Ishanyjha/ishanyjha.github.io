<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dr. Jane Doe - Academic Research</title>
    <style>
        /* Reset and base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f5f5f5;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header styles */
        header {
            background-color: #fff;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            padding: 1rem 0;
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        nav ul {
            list-style: none;
            display: flex;
        }
        nav ul li {
            margin-left: 1.5rem;
        }
        nav a {
            text-decoration: none;
            color: #333;
        }
        nav a:hover {
            color: #0066cc;
        }

        /* Section styles */
        section {
            padding: 4rem 0;
        }
        h1, h2 {
            text-align: center;
            margin-bottom: 2rem;
        }
        h1 {
            font-size: 2.5rem;
        }
        h2 {
            font-size: 2rem;
        }

        /* Hero section */
        #hero {
            text-align: center;
            background-color: #fff;
            padding: 4rem 0;
        }
        #hero p {
            max-width: 600px;
            margin: 0 auto 2rem;
        }
        .btn {
            display: inline-block;
            background-color: #0066cc;
            color: #fff;
            padding: 0.5rem 1rem;
            text-decoration: none;
            border-radius: 4px;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: #0052a3;
        }

        /* Projects section */
        #projects .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        .project-card {
            background-color: #fff;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        .project-card:hover {
            transform: translateY(-5px);
        }
        .project-card h3 {
            margin-bottom: 1rem;
        }
        .project-card .read-more {
            display: inline-block;
            margin-top: 1rem;
            color: #0066cc;
            cursor: pointer;
        }
        .project-card .full-description {
            display: none;
            margin-top: 1rem;
        }

        /* Publications and Presentations sections */
        .item-list {
            list-style: none;
        }
        .item-list li {
            background-color: #fff;
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            display: flex;
            align-items: center;
        }
        .item-list img {
            width: 80px;
            height: 80px;
            object-fit: cover;
            border-radius: 8px;
            margin-right: 1rem;
        }
        .item-list .content {
            flex: 1;
        }
        .item-list h3 {
            margin-bottom: 0.5rem;
        }
        .item-list p {
            color: #666;
            font-size: 0.9rem;
        }

        /* Contact section */
        #contact form {
            max-width: 500px;
            margin: 0 auto;
        }
        #contact .form-group {
            margin-bottom: 1rem;
        }
        #contact label {
            display: block;
            margin-bottom: 0.5rem;
        }
        #contact input,
        #contact textarea {
            width: 100%;
            padding: 0.5rem;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        #contact button {
            display: block;
            width: 100%;
            padding: 0.75rem;
            background-color: #0066cc;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        #contact button:hover {
            background-color: #0052a3;
        }

        /* Footer styles */
        footer {
            background-color: #f0f0f0;
            color: #666;
            text-align: center;
            padding: 2rem 0;
            margin-top: 4rem;
        }

        /* Responsive design */
        @media (max-width: 768px) {
            nav {
                flex-direction: column;
            }
            nav ul {
                margin-top: 1rem;
            }
            nav ul li {
                margin-left: 0;
                margin-right: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <a href="#" class="logo">Dr. Jane Doe</a>
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#publications">Publications</a></li>
                <li><a href="#presentations">Presentations</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="hero">
            <div class="container">
                <h1>Dr. Jane Doe</h1>
                <h2>Computer Science Researcher</h2>
                <p>Exploring the frontiers of artificial intelligence and machine learning to solve complex real-world problems.</p>
                <a href="#contact" class="btn">Get in Touch</a>
            </div>
        </section>

        <section id="projects">
            <div class="container">
                <h2>Research Projects</h2>
                <div class="grid">
                    <div class="project-card">
                        <h3>AI-Driven Climate Modeling</h3>
                        <p>Developing machine learning models to improve climate change predictions and mitigation strategies.</p>
                        <span class="read-more">Read more</span>
                        <p class="full-description">This project focuses on leveraging artificial intelligence and machine learning techniques to enhance climate modeling accuracy. By incorporating vast amounts of historical climate data and real-time sensor information, we aim to create more precise and adaptable climate models.</p>
                    </div>
                    <div class="project-card">
                        <h3>Quantum Computing Algorithms</h3>
                        <p>Researching novel quantum algorithms for optimization problems in logistics and supply chain management.</p>
                        <span class="read-more">Read more</span>
                        <p class="full-description">Our quantum computing research is centered on developing innovative algorithms to solve complex optimization problems in logistics and supply chain management. By harnessing the power of quantum superposition and entanglement, we aim to tackle NP-hard problems that are intractable for classical computers.</p>
                    </div>
                    <div class="project-card">
                        <h3>Ethical AI Framework</h3>
                        <p>Creating a comprehensive framework for ethical considerations in AI development and deployment.</p>
                        <span class="read-more">Read more</span>
                        <p class="full-description">The Ethical AI Framework project is dedicated to addressing the growing concerns surrounding the ethical implications of artificial intelligence. We are developing a comprehensive set of guidelines, best practices, and evaluation metrics to ensure that AI systems are designed and deployed with strong ethical considerations.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="publications">
            <div class="container">
                <h2>Recent Publications</h2>
                <ul class="item-list">
                    <li>
                        <img src="https://via.placeholder.com/80" alt="Publication thumbnail">
                        <div class="content">
                            <h3>Machine Learning Approaches to Climate Model Uncertainty Reduction</h3>
                            <p>Journal of Climate Informatics, 2023</p>
                        </div>
                    </li>
                    <li>
                        <img src="https://via.placeholder.com/80" alt="Publication thumbnail">
                        <div class="content">
                            <h3>Quantum-Inspired Algorithms for NP-Hard Problems in Supply Chain Optimization</h3>
                            <p>Quantum Computing and Logistics, 2022</p>
                        </div>
                    </li>
                    <li>
                        <img src="https://via.placeholder.com/80" alt="Publication thumbnail">
                        <div class="content">
                            <h3>Ethical Considerations in Automated Decision-Making Systems</h3>
                            <p>AI Ethics Journal, 2021</p>
                        </div>
                    </li>
                </ul>
            </div>
        </section>

        <section id="presentations">
            <div class="container">
                <h2>Presentations</h2>
                <ul class="item-list">
                    <li>
                        <img src="https://img.youtube.com/vi/dQw4w9WgXcQ/0.jpg" alt="Presentation thumbnail">
                        <div class="content">
                            <h3>The Future of AI in Climate Science</h3>
                            <p>Global Climate Conference, May 15, 2023</p>
                            <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" rel="noopener noreferrer">Watch Video</a>
                        </div>
                    </li>
                    <li>
                        <img src="https://img.youtube.com/vi/dQw4w9WgXcQ/0.jpg" alt="Presentation thumbnail">
                        <div class="content">
                            <h3>Quantum Computing: A New Era in Optimization</h3>
                            <p>International Quantum Symposium, November 3, 2022</p>
                            <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" rel="noopener noreferrer">Watch Video</a>
                        </div>
                    </li>
                    <li>
                        <img src="https://img.youtube.com/vi/dQw4w9WgXcQ/0.jpg" alt="Presentation thumbnail">
                        <div class="content">
                            <h3>Ethics in AI: Challenges and Solutions</h3>
                            <p>AI Ethics Forum, September 22, 2022</p>
                            <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" rel="noopener noreferrer">Watch Video</a>
                        </div>
                    </li>
                </ul>
            </div>
        </section>

        <section id="contact">
            <div class="container">
                <h2>Contact Me</h2>
                <form>
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" rows="4" required></textarea>
                    </div>
                    <button type="submit">Send Message</button>
                </form>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2023 Dr. Jane Doe. All rights reserved.</p>
            <p>Department of Computer Science, University of Example</p>
        </div>
    </footer>

    <script>
        // Simple JavaScript to toggle project descriptions
        document.querySelectorAll('.read-more').forEach(button => {
            button.addEventListener('click', () => {
                const description = button.nextElementSibling;
                description.style.display = description.style.display === 'none' ? 'block' : 'none';
                button.textContent = button.textContent === 'Read more' ? 'Read less' : 'Read more';
            });
        });
    </script>
</body>
</html>

