<html lang="ro">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Modele AR Optimizate</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background-color: #f5f5f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .model-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }

    .model-section {
      text-align: center;
      margin-bottom: 50px;
    }

    model-viewer {
      width: 400px;
      height: 470px;
      margin: 0 auto;
      border-radius: 20px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    .ar-button {
      padding: 5px 10px;
      font-size: 0.8rem;
      margin-top: 10px;
      background-color: #007BFF;
      border: none;
      border-radius: 20px;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s, box-shadow 0.3s;
    }

    .ar-button:hover {
      background-color: #0056b3;
    }

    .back-link {
      display: block;
      margin-top: 50px;
      text-decoration: none;
      color: white;
      background-color: #007BFF;
      padding: 10px 15px;
      border-radius: 20px;
      font-size: 0.9rem;
      transition: background-color 0.3s;
    }

    .back-link:hover {
      background-color: #0056b3;
    }

    p {
      color: #333333;
      font-size: 1.2em;
    }

    @media (max-width: 768px) {
      .model-container {
        width: 90%;
      }

      model-viewer {
        width: 300px;
      }
    }
  </style>
  <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
</head>
<body>
  <div class="model-container">
    <div class="model-section">
      <p>Model 3D optimizat pentru realitate augmentată</p>
      <model-viewer
        src="room.glb"
        ios-src="room.usdz"
        ar
        ar-modes="webxr scene-viewer quick-look"
        camera-controls
        auto-rotate
        environment-image="neutral"
        shadow-intensity="1"
        loading="lazy"
        alt="Model 3D cameră"
        min-camera-orbit="auto 0deg 0deg"
        max-camera-orbit="auto 80deg auto">
        <button slot="ar-button" class="ar-button">Activează modul AR</button>
      </model-viewer>
    </div>
    <a href="https://augmentedrealityweb.github.io/toate-produsele/" class="back-link">Înapoi la meniul principal</a>
  </div>
</body>
</html>
