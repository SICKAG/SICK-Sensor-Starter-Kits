# SICK Sensor Starter Kits

Welcome to the GitHub for the SICK Sensor Starter Kits!

The Kits provide a comprehensive set of sensors, accessories and examples to help you quickly get started with SICK sensors. These kits include everything you need to explore, prototype, and integrate sensor solutions into your projects.

<!-- Slideshow Container -->
<div class="slideshow-container" style="text-align:center;">
  <img id="slideshow" src="images/bild1.jpg" style="width:400px; height:auto; border-radius:8px;">
  <br>
  <!-- Navigation Buttons -->
  <button onclick="prevImage()" style="margin:10px; padding:8px;">⬅️ Zurück</button>
  <button onclick="nextImage()" style="margin:10px; padding:8px;">➡️ Weiter</button>
</div>

<script>
  // Liste der Bilder
  const images = [
    "C:\Users\meinefl\OneDrive - SICK AG\Desktop\SICK-Sensor-Starter-Kits\SICK-Sensor-Starter-Kits\docs\images/A7406000.jpg",
    "C:\Users\meinefl\OneDrive - SICK AG\Desktop\SICK-Sensor-Starter-Kits\SICK-Sensor-Starter-Kits\docs\images/A7405998.jpg",
    "images/A7405946.jpg",
    "images/A7405872.jpg",
    "images/A7405854.jpg"
  ];

  let index = 0;
  const imgElement = document.getElementById("slideshow");

  // Automatischer Wechsel alle 2 Sekunden
  setInterval(() => {
    index = (index + 1) % images.length;
    imgElement.src = images[index];
  }, 2000);

  // Manuelles Weiterklicken
  function nextImage() {
    index = (index + 1) % images.length;
    imgElement.src = images[index];
  }

  function prevImage() {
    index = (index - 1 + images.length) % images.length;
    imgElement.src = images[index];
  }
</script>

Don’t have a Starter Kit yet? Purchase yours here!

Link sick.com

Please note that the starter kits are intended for educational purposes only and must not be used in production environments.

Got your Starter Kit(s)? Start exploring now!

- [LIDAR Starter Kit](lidar/lidar_overview.md)
- [Vision Starter Kit](vision/vision_overview.md)
- [IO Link Starter Kit](iolink/iolink_overview.md)
