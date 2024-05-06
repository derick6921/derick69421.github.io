<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Goku vs SpongeBob</title>
<style>
    canvas {
        border: 1px solid black;
    }
</style>
</head>
<body>
<canvas id="myCanvas" width="800" height="400"></canvas>
<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');

    let gokuX = 50;
    let spongeBobX = 600;

    function draw() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // Draw Goku
        ctx.fillStyle = 'orange';
        ctx.fillRect(gokuX, 150, 50, 50);

        // Draw SpongeBob
        ctx.fillStyle = 'yellow';
        ctx.fillRect(spongeBobX, 150, 50, 50);

        // Update positions
        gokuX += 2;
        spongeBobX -= 2;

        // Reset positions when they reach the end of canvas
        if (gokuX > canvas.width) {
            gokuX = -50;
        }
        if (spongeBobX < -50) {
            spongeBobX = canvas.width;
        }
    }

    setInterval(draw, 20);
</script>
</body>
</html>
