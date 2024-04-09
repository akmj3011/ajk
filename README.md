



<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Image Slider</title>
<style>


  .slider-container {


    position: relative;
    width: 100%;
    max-width: 600px;
    margin: 0 auto;
    overflow: hidden;
  }
  .slides {
    display: flex;
    transition: transform 0.5s ease;
  }
  .slide {
    min-width: 100%;
    overflow: hidden;
  }
  .slide img {
    width: 100%;
    height: auto;
  }
  .arrow {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    cursor: pointer;
    padding: 10px;
    background-color: rgba(255, 255, 255, 0.5);
    border: none;
    outline: none;
  }
  .prev {
    left: 0;
  }
  .next {
    right: 0;
  }
</style>
</head>
<body>

<div class="slider-container">
  <div class="slides">
    <div class="slide">
      <img src="image1.jpg" alt= [image](https://github.com/akmj3011/ajk/assets/128561949/77ce47fd-f894-4d99-95cb-ac563af05c7c)">
    </div>
    <div class="slide">
      <img src="image2.jpg" alt=[image](https://github.com/akmj3011/ajk/assets/128561949/64251316-1b82-4376-8ed7-143b810821a7">
    </div>
    <div class="slide">
      <img src="image3.jpg" alt="![image](https://github.com/akmj3011/ajk/assets/128561949/5a355117-97bc-47da-8a37-fac85bac0c5c):>

    </div>
    <!-- Add more slides as needed -->
  </div>
  
  <button class="arrow prev" onclick="prevSlide()">&#10094;</button>
  <button class="arrow next" onclick="nextSlide()">&#10095;</button>
</div>

<script>
  let slideIndex = 0;
  const slides = document.querySelectorAll('.slide');
  
  function showSlides() {
    slides.forEach(slide => slide.style.display = 'none');
    slideIndex++;
    if (slideIndex > slides.length) {slideIndex = 1}
    slides[slideIndex - 1].style.display = 'block';
    setTimeout(showSlides, 2000); // Change image every 2 seconds
  }
  
  function nextSlide() {
    slideIndex++;
    if (slideIndex > slides.length) {slideIndex = 1}
    showSlides();
  }
  
  function prevSlide() {
    slideIndex--;
    if (slideIndex < 1) {slideIndex = slides.length}
    showSlides();
  }
  
  showSlides();
</script>


</body>
</html>
