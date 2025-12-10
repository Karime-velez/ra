<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>RA con Hiro</title>
  <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
  <script src="https://jeromeetienne.github.io/AR.js/aframe/build/aframe-ar.js"></script>
</head>
<body style="margin: 0; overflow: hidden;">

  <a-scene embedded arjs="sourceType: webcam; debugUIEnabled: false;">

    <!-- Assets -->
    <a-assets>
      <a-asset-item id="escultura" src="escultura.glb"></a-asset-item>
    </a-assets>

    <!-- Marcador Hiro -->
    <a-marker preset="hiro">
      <!-- Modelo 3D -->
      <a-entity
        gltf-model="#escultura"
        position="0 0 0"
        rotation="0 100 0"
        scale="0.5 0.5 0.5">
      </a-entity>
    </a-marker>

    <!-- Cámara -->
    <a-entity camera></a-entity>

    <!-- Entorno opcional para iluminación -->
    <a-entity environment="preset: default; lighting: bright; skyType: none;"></a-entity>

  </a-scene>

</body>
</html>
