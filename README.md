<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Model 3D Showcase</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer@latest"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-image: url('bkgd.jpg');
            background-size: cover;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
        model-viewer {
            width: 50%; /* Ajustează după preferințe */
            height: 60%; /* Ajustează după preferințe */
        }
    </style>
</head>
<body>
    <model-viewer src="room.glb" ios-src="room.usdz" 
                  alt="A 3D model of a room" 
                  auto-rotate camera-controls 
                  background-color="#455A64"></model-viewer>
</body>
</html>
