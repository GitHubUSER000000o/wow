<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Moderne Website</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        .navbar {
            display: flex;
            justify-content: space-around;
            background-color: #4CAF50;
            padding: 15px;
        }
        .navbar a {
            color: white;
            text-decoration: none;
            padding: 14px 20px;
            transition: background-color 0.3s;
        }
        .navbar a:hover {
            background-color: #45a049;
        }
        .content {
            padding: 20px;
            display: none;
        }
        .content.active {
            display: block;
        }
    </style>
</head>
<body>

<div class="navbar">
    <a href="#home">Home</a>
    <a href="#infos">Infos</a>
    <a href="#ueber-mich">Über mich</a>
    <a href="#schule">Schule</a>
</div>

<div class="content active" id="home">
    <h1>Willkommen auf meiner Website</h1>
    <p>Hier finden Sie Informationen über mich und meine Schule.</p>
</div>

<div class="content" id="infos">
    <h1>Infos</h1>
    <p>Hier sind einige Informationen.</p>
</div>

<div class="content" id="ueber-mich">
    <h1>Über mich</h1>
    <p>Hier erfahren Sie mehr über mich.</p>
</div>

<div class="content" id="schule">
    <h1>Schule</h1>
    <p>Informationen über meine Schule.</p>
</div>

<script>
    const links = document.querySelectorAll('.navbar a');
    const contents = document.querySelectorAll('.content');

    links.forEach(link => {
        link.addEventListener('click', function() {
            contents.forEach(content => content.classList.remove('active'));
            document.getElementById(this.getAttribute('href').substring(1)).classList.add('active');
        });
    });
</script>

</body>
</html>
