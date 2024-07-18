# 720websitertmplive
code:
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>givemetocode 公司成立日 LIVE</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background-color: #f2f2f2;
    }

    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .video-container {
      position: relative;
      width: 800px;
      height: 450px;
      background-color: #000;
      overflow: hidden;
    }

    #live-stream {
      width: 100%;
      height: 100%;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: #fff;
      text-align: center;
    }

    .overlay h1 {
      font-size: 36px;
      margin-bottom: 20px;
    }

    .overlay p {
      font-size: 18px;
      margin-bottom: 40px;
    }

    .overlay button {
      background-color: #4CAF50;
      color: #fff;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="video-container">
      <video id="live-stream" controls autoplay>
        Your browser does not support the video tag.
      </video>
      <div class="overlay">
        <h1>givemetocode 公司成立日 LIVE</h1>
        <p>Click the button to Join</p>
        <button onclick="startStream()">Start Streaming</button>
      </div>
    </div>
  </div>

  <script>
    function startStream() {
      // Replace the following URL with your actual RTMP server URL
      const rtmpUrl = 'rtmp://your-rtmp-server-url/live/stream_name';

      const liveStream = document.getElementById('live-stream');
      liveStream.src = rtmpUrl;
      liveStream.play();

      // Hide the overlay
      document.querySelector('.overlay').style.display = 'none';
    }
  </script>
</body>
</html>
