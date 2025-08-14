<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>موقع تحميل فيديوهات سموقي🦅👑</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #4b6cb7, #182848);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      color: #fff;
      overflow: hidden;
    }
    h1 {
      font-size: 40px;
      margin-bottom: 20px;
      text-shadow: 2px 2px 10px rgba(0,0,0,0.7);
    }
    input {
      width: 60%;
      padding: 10px;
      font-size: 16px;
      margin-bottom: 20px;
      border-radius: 5px;
      border: none;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      border-radius: 5px;
      border: none;
      cursor: pointer;
      background-color: #ff9800;
      color: #fff;
    }
    .bg-name {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 100px;
      color: rgba(255,255,255,0.1);
      pointer-events: none;
      user-select: none;
      z-index: 0;
    }
    .content {
      z-index: 1;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="bg-name">سموقي🦅👑</div>
  <div class="content">
    <h1>تحميل فيديوهات</h1>
    <input type="text" id="videoUrl" placeholder="ضع رابط الفيديو المباشر هنا">
    <br>
    <button onclick="downloadVideo()">تحميل الفيديو</button>
  </div>

  <script>
    function downloadVideo() {
      const url = document.getElementById('videoUrl').value;
      if(!url) {
        alert('ضع رابط الفيديو أولاً');
        return;
      }
      const a = document.createElement('a');
      a.href = url;
      a.download = 'video.mp4';
      document.body.appendChild(a);
      a.click();
      document.body.removeChild(a);
    }
  </script>
</body>
</html>
