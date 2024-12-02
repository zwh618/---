<!DOCTYPE html>
<html lang="zh">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>照片收集网站</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f9f9f9;
      color: #333;
    }
    header {
      background-color: #4CAF50;
      color: white;
      padding: 10px 20px;
      text-align: center;
    }
    .upload-section {
      padding: 20px;
      text-align: center;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
      gap: 10px;
      padding: 20px;
    }
    .gallery img {
      width: 100%;
      height: auto;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
    }
  </style>
</head>
<body>
  <header>
    <h1>照片收集网站</h1>
    <p>上传并展示您的照片</p>
  </header>
  
  <div class="upload-section">
    <input type="file" id="fileInput" accept="image/*" multiple>
    <button onclick="uploadPhotos()">上传照片</button>
  </div>
  
  <div class="gallery" id="gallery">
    <!-- 照片展示区 -->
  </div>
  
  <script>
    function uploadPhotos() {
      const input = document.getElementById('fileInput');
      const gallery = document.getElementById('gallery');
      
      if (input.files.length === 0) {
        alert("请选择至少一张照片！");
        return;
      }
      
      for (let i = 0; i < input.files.length; i++) {
        const file = input.files[i];
        const reader = new FileReader();
        
        reader.onload = function(e) {
          const img = document.createElement('img');
          img.src = e.target.result;
          gallery.appendChild(img);
        };
        
        reader.readAsDataURL(file);
      }
    }
  </script>
</body>
</html>
