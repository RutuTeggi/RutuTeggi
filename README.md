<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rutu's GitHub Profile</title>
    <!-- Updated Font Awesome link -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" integrity="sha512-wr5eWCOmF2uLD5fW0MXtvsJ+ZwFMA8iVVHri5YBBj5U0DqEgTICJLjm2X2lE1aMsmUJWWs90eefwsDapJXsq/A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <style>
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f8f8;
            padding: 20px;
        }

        h1 {
            color: #0366d6;
        }

        canvas {
            border: 1px solid #000;
            display: block;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <h1>Hello, I'm Rutu Teggi 👋</h1>

    <p>I'm passionate about software engineering. I love to code.</p>

    <!-- Technologies & Tools Badges -->
    <div>
        <span class="badge html-badge">HTML</span>
        <span class="badge css-badge">CSS</span>
        <span class="badge bootstrap-badge">Bootstrap</span>
        <span class="badge javascript-badge">JavaScript</span>
        <!-- Add more badges for technologies/tools you use -->
    </div>

    <!-- Projects -->
    <h2>🚀 Projects</h2>
    <ul>
        <li>
            <strong>Project Management Tool</strong>
            <ul>
                <li>Developed and maintained responsive web applications using HTML, CSS, and JavaScript.</li>
                <li>Collaborated with cross-functional teams to implement new features and improve user experience.</li>
                <li>Conducted code reviews to ensure code quality and adherence to best practices.</li>
            </ul>
        </li>
        <!-- Add more projects with their descriptions -->
    </ul>

    <!-- Learning -->
    <h2>🌱 I’m currently learning</h2>
    <ul>
        <li>Codeigniter framework</li>
        <li>Advanced JavaScript</li>
        <!-- Add more learning resources -->
    </ul>

    <!-- Connect with me -->
    <h2>📫 Connect with me</h2>
    <ul>
        <li>
            <a href="https://www.linkedin.com/in/rutu-teggi-7162a41a2/">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
        </li>
        <!-- Add more social media links -->
    </ul>

    <!-- Fun fact -->
    <h2>⚡ Fun fact</h2>
    <p>I enjoy coding.</p>

    <!-- Display the GIF at the beginning of the page -->
    <img src="https://i.pinimg.com/originals/e7/26/c7/e726c74ac081eed50feee1433d12c998.gif" alt="Animated GIF" style="max-width: 100%;">

    <h1>Rutu's GitHub Profile</h1>

    <!-- Snake Game -->
    <canvas id="snakeCanvas" width="400" height="400"></canvas>
    <script>
        const canvas = document.getElementById('snakeCanvas');
        const ctx = canvas.getContext('2d');

        const boxSize = 20;

        let snake = [{ x: 0, y: 0 }];
        let food = { x: 0, y: 0 };

        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            for (let i = 0; i < snake.length; i++) {
                ctx.fillStyle = i === 0 ? 'green' : 'white';
                ctx.fillRect(snake[i].x, snake[i].y, boxSize, boxSize);
            }

            ctx.fillStyle = 'red';
            ctx.fillRect(food.x, food.y, boxSize, boxSize);
        }

        function update() {
            const head = { x: snake[0].x + boxSize, y: snake[0].y };
            snake.unshift(head);

            if (head.x === food.x && head.y === food.y) {
                food = {
                    x: Math.floor(Math.random() * (canvas.width / boxSize)) * boxSize,
                    y: Math.floor(Math.random() * (canvas.height / boxSize)) * boxSize
                };
            } else {
                snake.pop();
            }
        }

        function gameLoop() {
            update();
            draw();
        }

        food = {
            x: Math.floor(Math.random() * (canvas.width / boxSize)) * boxSize,
            y: Math.floor(Math.random() * (canvas.height / boxSize)) * boxSize
        };

        setInterval(gameLoop, 100);
    </script>

</body>
</html>
