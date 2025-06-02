---
layout: home
title: Portfolio v1
---

# Introduction

Intro: Throughout the course of our studies at Full Sail University in the Computer Science Masters of Science with a focus on AI, we have been challenged to learn and perform a pace we often did not believe would be possible. This was a true real world educaction in the sense that it forced us to perform at a level we did not realize was possible. The courswork demanded our attention on a daily basis and to be successful we often worked up until the last moment of the deadline to submit our work on time. This was a challenge that brought us to gain a deep understanding of concepts like machine-learning, computer vision, statistical modeling, feature engineering, and more. This required a new level of discipline and many sacrifices to accomplish. It seemed life was hitting harder and harder until finally one day, it all paid off. We finnally made it to the Capstone Project and our presentation was accepted for development! We are excited to share the progress of our work and the challenges we faced along the way. 

## Recent Presentation

<div class="slideshow-container">
  <div class="slides">
    <img src="assets/slides/Slide1.jpg" alt="Slide 1" class="slide active">
    <img src="assets/slides/Slide2.jpg" alt="Slide 2" class="slide">
    <img src="assets/slides/Slide4.jpg" alt="Slide 3" class="slide">
    <img src="assets/slides/Slide5.jpg" alt="Slide 4" class="slide">
    <img src="assets/slides/Slide6.jpg" alt="Slide 5" class="slide">
    <img src="assets/slides/Slide7.jpg" alt="Slide 6" class="slide">
    <img src="assets/slides/Slide8.jpg" alt="Slide 7" class="slide">
    <img src="assets/slides/Slide9.jpg" alt="Slide 8" class="slide">
    <img src="assets/slides/Slide10.jpg" alt="Slide 9" class="slide">
    <img src="assets/slides/Slide11.jpg" alt="Slide 10" class="slide">
    <img src="assets/slides/Slide12.jpg" alt="Slide 11" class="slide">
    <img src="assets/slides/Slide13.jpg" alt="Slide 12" class="slide">
    <img src="assets/slides/Slide14.jpg" alt="Slide 13" class="slide">
    <img src="assets/slides/Slide15.jpg" alt="Slide 14" class="slide">
    <img src="assets/slides/Slide16.jpg" alt="Slide 15" class="slide">
    <img src="assets/slides/Slide17.jpg" alt="Slide 16" class="slide">
  </div>
  
  <button class="prev" onclick="changeSlide(-1)">❮</button>
  <button class="next" onclick="changeSlide(1)">❯</button>
  
  <div class="slide-counter">
    <span id="current-slide">1</span> / <span id="total-slides">16</span>
  </div>
</div>

<style>
.slideshow-container {
  position: relative;
  max-width: 800px;
  margin: auto;
  background: #f1f1f1;
  border-radius: 10px;
  overflow: hidden;
}

.slide {
  display: none;
  width: 100%;
  height: auto;
}

.slide.active {
  display: block;
}

.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  margin-top: -22px;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  background: rgba(0,0,0,0.5);
  border: none;
  transition: 0.3s ease;
  user-select: none;
}

.next {
  right: 0;
}

.prev:hover, .next:hover {
  background: rgba(0,0,0,0.8);
}

.slide-counter {
  text-align: center;
  padding: 20px;
  background: #333;
  color: white;
}
</style>

<script>
let currentSlide = 1;
const totalSlides = document.querySelectorAll('.slide').length;
document.getElementById('total-slides').textContent = totalSlides;

function changeSlide(direction) {
  const slides = document.querySelectorAll('.slide');
  slides[currentSlide - 1].classList.remove('active');
  
  currentSlide += direction;
  
  if (currentSlide > totalSlides) {
    currentSlide = 1;
  } else if (currentSlide < 1) {
    currentSlide = totalSlides;
  }
  
  slides[currentSlide - 1].classList.add('active');
  document.getElementById('current-slide').textContent = currentSlide;
}
</script>

## Monthly Development Blog

Below you'll find my development updates, featuring new features and retrospectives.
