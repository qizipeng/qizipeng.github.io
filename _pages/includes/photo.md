# 🐱 My Cat

Here’s a little photo viewer of my lovely cat, 麻团 😄.

<div class="carousel-container">
  <img id="cat-image" src="images/matuan1.jpg" class="carousel-image" alt="My cat photo">

  <div class="carousel-dots">
    <span class="dot active" onclick="showSlide(0)"></span>
    <span class="dot" onclick="showSlide(1)"></span>
    <span class="dot" onclick="showSlide(2)"></span>
    <span class="dot" onclick="showSlide(3)"></span>
  </div>
</div>

<style>
.carousel-container {
  text-align: center;
  margin-top: 10px;
}
.carousel-image {
  width: 300px;
  height: 200px;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.2);

  object-fit: contain;       /* 保持图片比例，完整显示 */
  background-color: #ffffff; /* 背景色，防止空白看起来突兀 */
}
.carousel-dots {
  margin-top: 10px;
}
.dot {
  height: 12px;
  width: 12px;
  margin: 0 5px;
  background-color: #ccc;
  border-radius: 50%;
  display: inline-block;
  cursor: pointer;
}
.dot.active {
  background-color: #333;
}
</style>

<script>
const photos = [
  "images/matuan1.jpg",
  "images/matuan2.jpg",
  "images/matuan3.jpg",
  "images/matuan4.jpg"
];

function showSlide(index) {
  const image = document.getElementById("cat-image");
  image.src = photos[index];

  const dots = document.querySelectorAll(".dot");
  dots.forEach(dot => dot.classList.remove("active"));
  dots[index].classList.add("active");
}
</script>
