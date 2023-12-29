<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <h1>Rutu's GitHub Profile</h1>
     <img src="https://i.pinimg.com/originals/e7/26/c7/e726c74ac081eed50feee1433d12c998.gif" alt="Animated GIF" style="max-width: 100%;">
    <!-- Updated Font Awesome link -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" integrity="sha512-wr5eWCOmF2uLD5fW0MXtvsJ+ZwFMA8iVVHri5YBBj5U0DqEgTICJLjm2X2lE1aMsmUJWWs90eefwsDapJXsq/A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
</head>
<body style="font-family: 'Arial', sans-serif; line-height: 1.6; color: #333; background-color: #f8f8f8; padding: 20px;">

# Hello, I'm Rutu Teggi 👋

I'm passionate about software engineering. I love to code.

## 🔧 Technologies & Tools

<span style="display: inline-block; padding: 5px 10px; margin: 0 5px; border-radius: 3px; font-size: 14px; background-color: #e44d26; color: #fff;">HTML</span>
<span style="display: inline-block; padding: 5px 10px; margin: 0 5px; border-radius: 3px; font-size: 14px; background-color: #264de4; color: #fff;">CSS</span>
<span style="display: inline-block; padding: 5px 10px; margin: 0 5px; border-radius: 3px; font-size: 14px; background-color: #563d7c; color: #fff;">Bootstrap</span>
<span style="display: inline-block; padding: 5px 10px; margin: 0 5px; border-radius: 3px; font-size: 14px; background-color: #f0db4f; color: #333;">JavaScript</span>
<!-- Add more badges for technologies/tools you use -->

## 🚀 Projects

- **Project Management Tool**
  - Developed and maintained responsive web applications using HTML, CSS, and JavaScript.
  - Collaborated with cross-functional teams to implement new features and improve user experience.
  - Conducted code reviews to ensure code quality and adherence to best practices.

- **Video Conferencing Website**
  - Worked on the front-end development of a customer-facing e-commerce platform using HTML, CSS, and JavaScript.
  - Integrated CSS animations to enhance user interactions and create visually appealing transitions, contributing to an enriched user experience.
  - Designed and implemented interactive web forms using HTML and JavaScript, enhancing user engagement and data collection efficiency.

- **Content Management Tool**
  - Implemented responsive image handling techniques, utilizing HTML and CSS to ensure optimal image display across various device resolutions and screen sizes.
  - Managed browser storage efficiently using JavaScript, optimizing data storage and retrieval for improved application performance.
  - Utilized CSS preprocessors like SASS to streamline stylesheet development, resulting in cleaner and more maintainable stylesheets for complex web applications.
<!-- Add more projects with their descriptions -->

## 🌱 I’m currently learning

- Codeigniter framework
- Advanced JavaScript
<!-- Add more learning resources -->

## 📫 Connect with me
[<img src="https://cdn-icons-png.flaticon.com/256/174/174857.png" alt="LinkedIn Logo" height="30" width="30"> ](https://www.linkedin.com/in/rutu-teggi-7162a41a2/)

## ⚡ Fun fact

I enjoy coding.

    <canvas id="snakeCanvas" width="400" height="400"></canvas>
    <script>
        const canvas = document.getElementById('snakeCanvas');
        const ctx = canvas.getContext('2d');

        const boxSize = 20;

        let snake = [{ x: 0, y: 0 }];
        let food = { x: 0, y: 0 };

        function draw() {
            // Clear the canvas
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // Draw the snake
            for (let i = 0; i < snake.length; i++) {
                ctx.fillStyle = i === 0 ? 'green' : 'white';
                ctx.fillRect(snake[i].x, snake[i].y, boxSize, boxSize);
            }

            // Draw the food
            ctx.fillStyle = 'red';
            ctx.fillRect(food.x, food.y, boxSize, boxSize);
        }

        function update() {
            // Move the snake
            const head = { x: snake[0].x + boxSize, y: snake[0].y };
            snake.unshift(head);

            // Check for collisions
            if (head.x === food.x && head.y === food.y) {
                // If the snake eats the food, generate a new food position
                food = {
                    x: Math.floor(Math.random() * (canvas.width / boxSize)) * boxSize,
                    y: Math.floor(Math.random() * (canvas.height / boxSize)) * boxSize
                };
            } else {
                // If the snake doesn't eat the food, remove the last segment
                snake.pop();
            }
        }

        function gameLoop() {
            update();
            draw();
        }

        // Generate initial food position
        food = {
            x: Math.floor(Math.random() * (canvas.width / boxSize)) * boxSize,
            y: Math.floor(Math.random() * (canvas.height / boxSize)) * boxSize
        };

        setInterval(gameLoop, 100); // Run the game loop every 100 milliseconds
    </script>
</body>
</html>
