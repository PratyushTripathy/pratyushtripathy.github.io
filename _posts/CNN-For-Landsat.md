---
layout: post
title: "CNN for Landsat Classification"
date: 2025-03-12
categories: blog
---

<!-- Navigation Links for Sections -->
<div class="section-navigation">
  <a href="#section1" class="nav-link">Introduction</a>
  <a href="#section2" class="nav-link">Code Demo</a>
  <a href="#section3" class="nav-link">Explanation</a>
</div>

<!-- Section 1: Introduction -->
<div id="section1" class="demo-section">
  <h2>Introduction</h2>
  <p>
    In this demo, we will showcase some sample code and explain how it works.
    Use the navigation buttons below to move between sections.
  </p>
</div>

<!-- Section 2: Code Demo -->
<div id="section2" class="demo-section">
  <h2>Code Demo</h2>
  <p>
    Below is an example of Python code. Click the “Copy Code” button to easily copy the snippet.
  </p>
  <div class="code-demo">
    <pre><code class="language-python"># Sample Python Code
def greet(name):
    return f"Hello, {name}!"

print(greet("World"))</code></pre>
    <button class="copy-btn">Copy Code</button>
  </div>
</div>

<!-- Section 3: Explanation -->
<div id="section3" class="demo-section">
  <h2>Explanation</h2>
  <p>
    The code above defines a simple function that returns a greeting. You can modify it to experiment with different inputs.
  </p>
</div>

<!-- Navigation Arrows -->
<div class="section-arrows">
  <button id="prev-section">← Previous</button>
  <button id="next-section">Next →</button>
</div>

<!-- JavaScript for Copy & Section Navigation -->
<script>
document.addEventListener("DOMContentLoaded", function() {
  // Copy button functionality
  document.querySelectorAll('.copy-btn').forEach(function(button) {
    button.addEventListener('click', function() {
      // Get the code text from the preceding <pre><code> block
      const codeBlock = button.previousElementSibling.innerText;
      navigator.clipboard.writeText(codeBlock).then(function() {
        button.innerText = "Copied!";
        setTimeout(() => {
          button.innerText = "Copy Code";
        }, 2000);
      });
    });
  });

  // Section navigation functionality
  const sections = document.querySelectorAll('.demo-section');
  let currentSection = 0;
  
  // Function to show the desired section
  function showSection(index) {
    sections.forEach((section, i) => {
      section.style.display = (i === index) ? "block" : "none";
    });
  }
  showSection(currentSection);

  // Navigation arrow handlers
  document.getElementById('prev-section').addEventListener('click', function() {
    if (currentSection > 0) {
      currentSection--;
      showSection(currentSection);
    }
  });
  document.getElementById('next-section').addEventListener('click', function() {
    if (currentSection < sections.length - 1) {
      currentSection++;
      showSection(currentSection);
    }
  });
});
</script>

<!-- CSS Styles for the Demo -->
<style>
/* Hide sections by default */
.demo-section {
  display: none;
  padding: 20px;
  border: 1px solid #ddd;
  margin-bottom: 20px;
}

/* Style for the code demo container */
.code-demo {
  position: relative;
  background: #f5f5f5;
  padding: 10px;
  border: 1px solid #ccc;
  overflow: auto;
}

/* Copy button styling */
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

/* Navigation arrows */
.section-arrows {
  text-align: center;
  margin-top: 20px;
}
.section-arrows button {
  margin: 0 10px;
  padding: 5px 15px;
}

/* Navigation links for quick jump */
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
