---
layout: default
title: Portfolio v1
---

<style>
body {
  background: #0a0a0a !important;
  color: #00ff41 !important;
  font-family: 'Courier New', monospace !important;
}

.site-header, header {
  background: #1a1a1a !important;
  border-bottom: 2px solid #00ff41 !important;
}

.site-title, .site-title:visited {
  color: #00ff41 !important;
  text-shadow: 0 0 15px #00ff41 !important;
}

h1, h2, h3, h4, h5, h6 {
  color: #00ff41 !important;
  text-shadow: 0 0 10px rgba(0, 255, 65, 0.5) !important;
}

.wrapper, .page-content, main, .container {
  background: rgba(26, 26, 26, 0.9) !important;
  border: 1px solid #00ff41 !important;
  border-radius: 10px !important;
  box-shadow: 0 0 30px rgba(0, 255, 65, 0.2) !important;
}

.slideshow-container {
  position: relative;
  max-width: 900px;
  margin: auto;
  background: rgba(26, 26, 26, 0.9);
  border: 2px solid #00ff41;
  border-radius: 10px;
  box-shadow: 0 0 30px rgba(0, 255, 65, 0.3);
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
  color: #00ff41;
  font-weight: bold;
  font-size: 18px;
  background: rgba(0, 0, 0, 0.8);
  border: 1px solid #00ff41;
  transition: 0.3s ease;
  user-select: none;
  border-radius: 3px;
}

.next {
  right: 0;
}

.prev:hover, .next:hover {
  background: rgba(0, 255, 65, 0.2);
  box-shadow: 0 0 15px rgba(0, 255, 65, 0.5);
  text-shadow: 0 0 10px #00ff41;
}

.slide-counter {
  text-align: center;
  padding: 15px;
  background: #1a1a1a;
  color: #00ff41;
  border-top: 1px solid #00ff41;
  font-family: 'Courier New', monospace;
}

.blog-post {
  background: rgba(0, 0, 0, 0.7);
  border: 1px solid #333;
  border-left: 4px solid #00ff41;
  margin: 2rem 0;
  padding: 1.5rem;
  border-radius: 5px;
}

.post-title {
  color: #00ff41 !important;
  font-size: 1.4rem;
  margin-bottom: 0.5rem;
}

.post-meta {
  color: #a0a0a0;
  font-style: italic;
  margin-bottom: 1rem;
  font-size: 0.9rem;
}
</style>
# Introduction

Intro: Throughout the course of our studies at Full Sail University in the Computer Science Masters of Science with a focus on AI, we have been challenged to learn and perform a pace we often did not believe would be possible. This was a true real world educaction in the sense that it forced us to perform at a level we did not realize was possible. The courswork demanded our attention on a daily basis and to be successful we often worked up until the last moment of the deadline to submit our work on time. This was a challenge that brought us to gain a deep understanding of concepts like machine-learning, computer vision, statistical modeling, feature engineering, and more. This required a new level of discipline and many sacrifices to accomplish. It seemed life was hitting harder and harder until finally one day, it all paid off. We finnally made it to the Capstone Project and our presentation was accepted for development! We are excited to share the progress of our work and the challenges we faced along the way. In the future we hope to create a more robust version of our software while also reducing the resources required for it to perform. As AI becomes more embedded into everyday life the amount of electricity and processing power required for this technology to work continues to grow. While this need fuels investment in infrastructure it should also be approached as a problem. We hope that through our research and development efforts we can improve the efficiency of our application by at least 1%. 

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

<div class="blog-post">
  <h3 class="post-title">Action Recognition Modeling and Integration</h3>
  <div class="post-meta">June 1, 2025 • By JCP</div>
  <h4>Features Developed This Month</h4>
  <p>This month we developed a system to create and train action recognition models using MediaPipe, PyTorch, SciKitLearn and data augmentation techniques to produce accurate models with less than 50 samples. We were able to introduce the model we trained into the main application that performs object detection to integration action recognition and object detection in our main application "EyeSpy+".</p>
  
![Action Recognition Trainer with skeleton wireframe](assets/images/demoMs1.png)

  <h4>Retrospective</h4>
  <h5>What went right this month?</h5>
  <p>This month we were fortunate to have a lot of time available to dedicate to our project due to our work schedule opening up time for us to work on our studies. Knowing how challenging it is to annotate images for model training from a previous project, we decided to make this the focus of the effort. Our efforts began by examining other action recognition projects and looking for trends in the model composition and sample types. Thanks to "Python Feature Engineering Cookbook" by Soledad Galli which was recommended further reading material from our Machine Learning course, we were able to find ways to augment the sample data (JSON format) by adding versions of each sample at different time scales, rotating the position of the base, introducing noise, and flipping the images through into our action recognition model training algorithm.</p>

![Active detection in main app](assets/images/Eyespy_capture_20250530_194008.png)  
  <h5>What went wrong this month?</h5>
  <p>Initially, we were not successful with the model training algorithm. Our approach was to train only a single action thinking this would be the most efficient way to produce a lightweight model. However, because we did not train the model on what an action is NOT - it was performing poorly by classifying each action as the same event, simply because there was motion. We then had issues with where our position was before we began the action we were training on. In moving to the starting position there was data being recorded that had nothing to do with the gesture we wanted to record. We solved this by creating a countdown timer to allow us to get into place and position before beginning the action. Finally, after adding 5 more actions to train on we reduced our false positive rate to an acceptable level and the model began performing with high confidence scores in the training and validation process.</p>
  <p>When we attempted to integrate the action recognition feature into our main application we had to do quite a bit of troubleshooting to understand what variables were affecting each model's performance. The size of the video frame in the main application did not match the size of the training application. I assumed this was just a display setting, not something the models would consider when performing inference. Once I matched the main application size and frame rate to the action recognition model's training data we were able to get successful detections of both the action and object detection models.</p>
  <p>Also, our Version 3 prototype performed great with just CPU processing. For this version we have had to leverage CUDA for performance enhancements since the action recognition and object detection concurrent inference tasks are not running optimally.</p>
  <h5>How can you improve moving forward?</h5>
  <p>Going forward I will need to give a full effort to the development process. Right now the prototype works, but it seems to be very heavy on resource consumption.</p>
</div>
