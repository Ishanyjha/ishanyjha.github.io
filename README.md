<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Research Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f9f9f9;
        }
        .container {
            max-width: 900px;
            margin: auto;
        }
        h1, h2 {
            text-align: center;
            color: #333;
        }
        .section {
            margin-bottom: 40px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        .box {
            background: white;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
            cursor: pointer;
        }
        .box:hover {
            transform: scale(1.05);
        }
        .publication, .presentation {
            display: flex;
            align-items: center;
            background: white;
            padding: 10px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
            cursor: pointer;
        }
        .publication:hover, .presentation:hover {
            transform: scale(1.03);
        }
        .thumbnail {
            width: 80px;
            height: 80px;
            border-radius: 10px;
            margin-right: 15px;
        }
        .presentation .thumbnail {
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Research Website</h1>
        
        <div class="section">
            <h2>Research Projects</h2>
            <div class="grid">
                <div class="box" onclick="location.href='project1.html'">Project 1</div>
                <div class="box" onclick="location.href='project2.html'">Project 2</div>
                <div class="box" onclick="location.href='project3.html'">Project 3</div>
            </div>
        </div>

        <div class="section">
            <h2>Recent Publications</h2>
            <div class="publication" onmouseover="this.style.transform='scale(1.03)';" onmouseout="this.style.transform='scale(1)';">
                <img class="thumbnail" src="paper-thumbnail.jpg" alt="Paper">
                <p><strong>Title of Paper</strong><br>Journal Name, Year</p>
            </div>
        </div>

        <div class="section">
            <h2>Presentations</h2>
            <div class="presentation" onclick="window.open('https://youtube.com/watch?v=example', '_blank');">
                <img class="thumbnail" src="presentation-thumbnail.jpg" alt="Presentation">
                <p><strong>Title of Presentation</strong><br>Conference Name, Year</p>
            </div>
        </div>
    </div>
</body>
</html>
