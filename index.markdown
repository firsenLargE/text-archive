---

layout: none
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>{{ site.title }}</title>
  <link rel="stylesheet" href="/assets/css/cards.css">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
</head>
<body>
  <div class="main-content">
    <h1 style="text-align:center; margin-bottom:2rem;">{{ site.title }}</h1>
    <div class="blog-cards">
      {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
      {% for post in sorted_posts %}
        <div class="blog-card">
          <div class="date">{{ post.date | date: "%b %d, %Y %H:%M" }}</div>
          <h2>{{ post.title }}</h2>
          <div>{{ post.content | markdownify }}</div>
        </div>
      {% endfor %}
    </div>
  </div>
</body>
</html>
