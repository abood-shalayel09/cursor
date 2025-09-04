<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>لعبة المتاهة</title>
  <style>
    #maze {
      width: 300px;
      height: 300px;
      background-color: #eee;
      position: relative;
      border: 2px solid #333;
    }
    #player {
      width: 20px;
      height: 20px;
      background-color: red;
      position: absolute;
      top: 0;
      left: 0;
    }
  </style>
</head>
<body>
  <h1>لعبة المتاهة 🎮</h1>
  <div id="maze">
    <div id="player"></div>
  </div>

  <script>
    const player = document.getElementById("player");
    let x = 0, y = 0;

    document.addEventListener("keydown", function(e) {
      if (e.key === "ArrowRight") x += 10;
      if (e.key === "ArrowLeft") x -= 10;
      if (e.key === "ArrowDown") y += 10;
      if (e.key === "ArrowUp") y -= 10;

      // حدود المتاهة
      x = Math.max(0, Math.min(x, 280));
      y = Math.max(0, Math.min(y, 280));

      player.style.left = x + "px";
      player.style.top = y + "px";
    });
  </script>
</body>
</html>

