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
  <p>This month we developed a system to create and train action recognition models using MediaPipe, PyTorch, SciKitLearn and data augmentation techniques to produce accurate models with less than 50 samples. Google provides a demo library for Mediapipe which allows us to create the required tracking landmarks we need to record action data. Source : https://github.com/google-ai-edge/mediapipe. We were able to introduce the model we trained along with our new action recognition pipeline into the main application that performs object detection called "EyeSpy+".</p>
  
  <div style="text-align: center; margin: 20px 0;">
    <img src="assets/images/demoMs1.png" alt="Action Recognition Trainer" style="border: 2px solid #00ff41; border-radius: 10px; max-width: 100%;">
    <p style="font-style: italic; color: #a0a0a0; margin-top: 10px;">Action Recognition Trainer with skeleton wireframe</p>
  </div>

  <h4>Retrospective</h4>
  
  <h5>What went right this month?</h5>
  <p>This month we were fortunate to have a lot of time available to dedicate to our project due to our work schedule opening up time for us to work on our studies. Knowing how challenging it is to annotate images for model training from a previous project, we decided to make this the focus of the effort. Our efforts began by examining other action recognition projects and looking for trends in the model composition and sample types. Thanks to "Python Feature Engineering Cookbook" by Soledad Galli which was recommended further reading material from our Machine Learning course, we were able to find ways to augment the sample data (JSON format) by adding versions of each sample at different time scales, rotating the position of the base, introducing noise, and flipping the images through into our action recognition model training algorithm.</p>

  <div style="text-align: center; margin: 20px 0;">
    <img src="assets/images/Eyespy_capture_20250530_194008.png" alt="Active detection in main app" style="border: 2px solid #00ff41; border-radius: 10px; max-width: 100%;">
    <p style="font-style: italic; color: #a0a0a0; margin-top: 10px;">Active detection in main app</p>
  </div>
  
  <h5>What went wrong this month?</h5>
  <p>Initially, we were not successful with the model training algorithm. Our approach was to train only a single action thinking this would be the most efficient way to produce a lightweight model. However, because we did not train the model on what an action is NOT - it was performing poorly by classifying each action as the same event, simply because there was motion. We then had issues with where our position was before we began the action we were training on. In moving to the starting position there was data being recorded that had nothing to do with the gesture we wanted to record. We solved this by creating a countdown timer to allow us to get into place and position before beginning the action. Finally, after adding 5 more actions to train on we reduced our false positive rate to an acceptable level and the model began performing with high confidence scores in the training and validation process.</p>
  
  <p>When we attempted to integrate the action recognition feature into our main application we had to do quite a bit of troubleshooting to understand what variables were affecting each model's performance. The size of the video frame in the main application did not match the size of the training application. I assumed this was just a display setting, not something the models would consider when performing inference. Once I matched the main application size and frame rate to the action recognition model's training data we were able to get successful detections of both the action and object detection models.</p>
  
  <p>Also, our Version 3 prototype performed great with just CPU processing. For this version we have had to leverage CUDA for performance enhancements since the action recognition and object detection concurrent inference tasks are not running optimally.</p>
  
  <h5>How can you improve moving forward?</h5>
  <p>Going forward I will need to give a full effort to the development process. Right now the prototype works, but it seems to be very heavy on resource consumption. Additionally, we may want to use this method for object detection "https://developers.googleblog.com/en/object-detection-and-tracking-using-mediapipe/" rather than our existing YOLO pipeline in order to lighten the processing load.</p>

  <div style="text-align: center; margin: 20px 0;">
    <img src="assets/images/bear.gif" alt="Google GIF" style="border: 2px solid #00ff41; border-radius: 10px; max-width: 100%;">
    <p style="font-style: italic; color: #a0a0a0; margin-top: 10px;">Bear object detection demonstration</p>
  </div>
</div>

<div class="blog-post">
  <h3 class="post-title"> Multi-Camera System Development + Mobile Alerts + Jetson Orin Nano AI Accelerator</h3>
  <div class="post-meta"> June 29, 2025 • By JCP</div>
  
  <h4>Features Developed This Month</h4>
  <p>This month we focused on enhancing the multi-camera system's capabilities including a video matrix interface with source selection menu, integrating mobile alerts via Telegram API, refactoring, and integrating a Jetson Orin Nano AI Accelerator for action recognition.</p>
  
  
  <h4>Retrospective</h4>
  
  <h5>What went right this month?</h5>
  <p>Successfully implemented a video matrix interface that allows users to select camera sources and view them in a grid layout. This feature enhances the user experience by providing a clear and organized way to monitor multiple camera feeds simultaneously. This month provided a valuable learning experience on how the action recognition models need to be tuned to perform on different video resolutions and frame rates and their limitations. Using the Telegram API it was possible to create mobile alerts, only requiring the user to have the Telegram application on their phone. The initial go at the Jetson device was partially successful. This is a compact and powerful device which can be used to augment certain inference tasks for Eyespy. At present, the Jetson is handling all action recognition processing tasks so the PC can take care of firearm detections. So far, only 2 camera feeds are being processed simultaneously for action recognition. The idea to use an edge processing device like this was inspired from the feedback provided by Dr. Oleg Kachirski. In seeking some insight from the faculty my advisor Dr. Andreas Marpaung suggested I get Dr. Oleg's input on the problems with the action recognition model not being "resolution aware", which was very helpful and provided us with a path forward to improve the novel training method used to create the AR model. To save on PC resources we reduced the display resolution and reduced object detection frequency. This significantly improved the issues related to video latency and processing errors.</p>

  <div style="text-align: center; margin: 20px 0;">
    <img src= "assets/images/Jetson_no_shell.png" alt="Active detection in main app" style="border: 2px solid #00ff41; border-radius: 10px; max-width: 100%;">
    <p style="font-style: italic; color: #a0a0a0; margin-top: 10px;">Jetson Orin Nano AI Accelerator out of the box</p>
  </div>

  <div style="text-align: center; margin: 20px 0;">
    <img src= "assets/images/Jetson_first_power_up.png" alt="Active detection in main app" style="border: 2px solid #00ff41; border-radius: 10px; max-width: 100%;">
    <p style="font-style: italic; color: #a0a0a0; margin-top: 10px;">First Power up</p>
  </div>

  <h5>What went wrong this month?</h5>
  <p> 1: Our action recognition model did not perform well due to inconsistencies in video source formats and resolutions. This lead to using only the firearm detection feature in the multi-camera version of Eyespy for the time being. </p>
  <p> 2: The integration of the Jetson Orin Nano AI Accelerator was more challenging than expected. The object detection model was not able to run concurrently with the action recognition model, which limited the functionality of the system. Efforts to off-load the inference processes to the Jetson were met with release limitations for Jetpack 6.2 Support request: https://forums.developer.nvidia.com/t/jetpack-6-2-pytorch-with-cuda-support-coming-any-time-soon/337290 </p>
  <p> 3: Went deep into the development rabbit hole spending long nights and working into exhaustion. This lead to a poor thesis draft submission due to working on the Development Milestones up until the hour of submission.</p>
  
  <div style="text-align: center; margin: 20px 0;">
    <img src= "assets/images/Jetson_Orin_Nano_In_Case.png" alt="Active detection in main app" style="border: 2px solid #00ff41; border-radius: 10px; max-width: 100%;">
    <p style="font-style: italic; color: #a0a0a0; margin-top: 10px;">Jetson Orin Nano AI Accelerator in case</p>
  </div>

  <h5>How can you improve moving forward?</h5>
  <p>To improve moving forward, we will focus on the following actions:</p>
  <p>1. Optimize the action recognition model's settings to better handle varying video qualities and frame rates.</p>
  <p>2. Continue exploring the capabilities of the Jetson Orin Nano AI Accelerator and its integration with our existing system. i.e. more action recognition capable feeds. </p>
  <p>3. Build diagnostic tools to better understand model performance and identify bottlenecks.</p>
  <p>4. Contiunue looking for ways to improve efficiency and resource conservation.</p>
</div>


<div class="blog-post">
  <h3 class="post-title"> Development Updates & Milestones </h3>
  <div class="post-meta"> July 21, 2025 • By JCP</div>
  
  <h4>Features Developed This Month</h4>
  <p> This month development efforts scaled the system & application architecture to suport distributed processing and additional hardware components. See System diagram figure 1.
    Jetson Orin Nano powered camera server with edge side action recognition processing. </p>
</div>

    
