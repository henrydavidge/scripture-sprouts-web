---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Home
---

<div class="home-container">
  <!-- Logo Section - Prominent and Centered -->
  <div class="logo-container">
    <img src="{{ site.baseurl }}/img/logo.png" alt="Scripture Sprouts Logo" class="logo">
  </div>

  <!-- App Description -->
  <div class="app-description">
    <h2>Grow in faith with Bible study</h2>
    <p>Grow closer to God through conversational Bible study tailored to you. Scripture Sprouts helps you bring the Bible into your life by building study plans for any topic on your spiritual journey. Focus on your study without distracting interfaces and unnecessary graphics.</p>
    <!-- Add app store badges here when available -->
  </div>

  <!-- Feature List Section -->
  <div class="features-section">
    <h3>Why choose Scripture Sprouts?</h3>
    <ul class="features-list">
      <li>
        <span class="feature-icon">✓</span>
        <span class="feature-text">Create custom study plans about any topic, for whatever schedule and daily reading time works for you. Just say what you want to learn, and we'll choose relevant readings.</span>
      </li>
      <li>
        <span class="feature-icon">✓</span>
        <span class="feature-text">Converse with a scripture expert powered by advanced AI that respects your denomination and study goals.</span>
      </li>
      <li>
        <span class="feature-icon">✓</span>
        <span class="feature-text">Learn about the Bible at your own pace and track your progress.</span>
      </li>
      <li>
        <span class="feature-icon">✓</span>
        <span class="feature-text">Ask any question about the Bible and get the answer immediately, with references to key passages.</span>
      </li>
      <li>
        <span class="feature-icon">✓</span>
        <span class="feature-text">An easy-to-use interface free of any ads or distractions.</span>
      </li>
      <li>
        <span class="feature-icon">✓</span>
        <span class="feature-text">Dictation and text-to-speech support to learn in a conversational way.</span>
      </li>
      <li>
        <span class="feature-icon">✓</span>
        <span class="feature-text">Read the Bible wherever you go.</span>
      </li>
    </ul>
  </div>

  <!-- Carousel Section - Now Larger -->
  <div class="carousel-container">
    <div class="carousel">
      <div class="carousel-inner">
        <!-- Using the actual image file names we found in the directory -->
        <div class="carousel-item active">
          <img src="{{ site.baseurl }}/img/IMG_6769.PNG" alt="Scripture Sprouts App Screenshot 1" class="carousel-image">
        </div>
        <div class="carousel-item">
          <img src="{{ site.baseurl }}/img/IMG_6770.PNG" alt="Scripture Sprouts App Screenshot 2" class="carousel-image">
        </div>
        <div class="carousel-item">
          <img src="{{ site.baseurl }}/img/IMG_6771.PNG" alt="Scripture Sprouts App Screenshot 3" class="carousel-image">
        </div>
        <div class="carousel-item">
          <img src="{{ site.baseurl }}/img/IMG_6772.PNG" alt="Scripture Sprouts App Screenshot 4" class="carousel-image">
        </div>
        <div class="carousel-item">
          <img src="{{ site.baseurl }}/img/IMG_6773.PNG" alt="Scripture Sprouts App Screenshot 5" class="carousel-image">
        </div>
        <div class="carousel-item">
          <img src="{{ site.baseurl }}/img/IMG_6777.PNG" alt="Scripture Sprouts App Screenshot 6" class="carousel-image">
        </div>
      </div>
      <button class="carousel-control carousel-control-prev" id="prev-button">&#10094;</button>
      <button class="carousel-control carousel-control-next" id="next-button">&#10095;</button>
    </div>
  </div>

  <!-- Contact Info Section -->
  <div class="contact-section">
    <h3>Contact Us</h3>
    <div class="contact-info">
      <div class="contact-item">
        <span class="contact-label">Feedback:</span>
        <a href="mailto:feedback@scripturesprouts.app">feedback@scripturesprouts.app</a>
      </div>
      <div class="contact-item">
        <span class="contact-label">Support:</span>
        <a href="mailto:support@scripturesprouts.app">support@scripturesprouts.app</a>
      </div>
      <div class="contact-item">
        <span class="contact-label">General Info:</span>
        <a href="mailto:info@scripturesprouts.app">info@scripturesprouts.app</a>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="site-footer">
    <div class="footer-links">
      <a href="{{ site.baseurl }}/privacy-policy">Privacy Policy</a>
      <span class="footer-separator">|</span>
      <a href="{{ site.baseurl }}/terms-of-use">Terms of Use</a>
    </div>
    <div class="footer-copyright">
      &copy; {{ site.time | date: '%Y' }} Scripture Sprouts. All rights reserved.
    </div>
  </footer>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    // Carousel functionality
    const carouselItems = document.querySelectorAll('.carousel-item');
    const prevButton = document.getElementById('prev-button');
    const nextButton = document.getElementById('next-button');
    let currentIndex = 0;

    function showSlide(index) {
      // Hide all slides
      carouselItems.forEach(item => {
        item.classList.remove('active');
      });
      
      // Show the current slide
      carouselItems[index].classList.add('active');
    }

    // Previous button click
    prevButton.addEventListener('click', function() {
      currentIndex = (currentIndex - 1 + carouselItems.length) % carouselItems.length;
      showSlide(currentIndex);
    });

    // Next button click
    nextButton.addEventListener('click', function() {
      currentIndex = (currentIndex + 1) % carouselItems.length;
      showSlide(currentIndex);
    });

    // Auto advance slides every 5 seconds
    setInterval(function() {
      currentIndex = (currentIndex + 1) % carouselItems.length;
      showSlide(currentIndex);
    }, 5000);
  });
</script>
