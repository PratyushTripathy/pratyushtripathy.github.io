---
layout: post
title: "A Book-Style Blog Post"
date: 2025-03-12
categories: blog
---

<!-- Navigation Links for Sections -->
<div class="section-navigation">
  <a href="#section1" class="nav-link">Introduction</a>
  <a href="#section2" class="nav-link">Chapter 1</a>
  <a href="#section3" class="nav-link">Chapter 2</a>
  <a href="#section4" class="nav-link">Conclusion</a>
</div>

<!-- Section 1: Introduction -->
<div id="section1" class="book-section">
  <h2>Introduction</h2>
  <p>
    Welcome to this blog post presented as a book. In this post, you’ll find a detailed exploration of my latest research, complete with code demos and in-depth explanations.
  </p>
</div>

<!-- Section 2: Chapter 1 -->
<div id="section2" class="book-section">
  <h2>Chapter 1: Research Background</h2>
  <p>
    [Your content here...]
  </p>
</div>

<!-- Section 3: Chapter 2 -->
<div id="section3" class="book-section">
  <h2>Chapter 2: Methods and Code Demo</h2>
  <p>
    Below is an example of the code I used in my analysis.
  </p>
  <div class="code-demo">
    <pre><code class="language-python"># Sample Python Code
def greet(name):
    return f"Hello, {name}!"

print(greet("World"))</code></pre>
    <button class="copy-btn">Copy Code</button>
  </div>
</div>

<!-- Section 4: Conclusion -->
<div id="section4" class="book-section">
  <h2>Conclusion</h2>
  <p>
    Thank you for reading. I hope this book-style post gives you a deeper insight into the work. Feel free to leave comments or reach out!
  </p>
</div>

<!-- Navigation Arrows -->
<div class="section-arrows">
  <button id="prev-section">← Previous</button>
  <button id="next-section">Next →</button>
</div>

<!-- Inline JavaScript for Copy & Section Navigation -->
<script>
document.addEventListener("DOMContentLoaded", function() {
  // Copy code functionality
  document.querySelectorAll('.copy-btn').forEach(function(button) {
    button.addEventListener('click', function() {
      const codeBlock = button.previousElementSibling.innerText;
      navigator.clipboard.writeText(codeBlock).then(function() {
        button.innerText = "Copied!";
        setTimeout(() => { button.innerText = "Copy Code"; }, 2000);
      });
    });
  });

  // Section navigation functionality
  const sections = document.querySelectorAll('.book-section');
  let currentSection = 0;
  function showSection(index) {
    sections.forEach((section, i) => {
      section.style.display = (i === index) ? "block" : "none";
    });
  }
  showSection(currentSection);

  document.getElementById('prev-section').addEventListener('click', function() {
    if (currentSection > 0) { currentSection--; showSection(currentSection); }
  });
  document.getElementById('next-section').addEventListener('click', function() {
    if (currentSection < sections.length - 1) { currentSection++; showSection(currentSection); }
  });
});
</script>

<!-- Inline CSS Styles -->
<style>
.book-section {
  display: none;
  padding: 20px;
  border: 1px solid #ddd;
  margin-bottom: 20px;
}
.code-demo {
  position: relative;
  background: #f5f5f5;
  padding: 10px;
  border: 1px solid #ccc;
  overflow: auto;
}
.copy-btn {
  position: absolute;
  top: 10px;
  right: 10px;
  background: #007acc;
  color: #fff;
  border: none;
  padding: 5px 10px;
  cursor: pointer;
}
.section-arrows {
  text-align: center;
  margin-top: 20px;
}
.section-arrows button {
  margin: 0 10px;
  padding: 5px 15px;
}
.section-navigation {
  text-align: center;
  margin-bottom: 20px;
}
.section-navigation .nav-link {
  margin: 0 10px;
  text-decoration: none;
  color: #007acc;
}
</style>
