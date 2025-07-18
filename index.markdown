---
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Imperfect Hosts Times</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Georgia:wght@400;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', 'Times New Roman', serif;
            line-height: 1.5;
            color: #121212;
            background-color: #fff;
            font-size: 16px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Section */
        .header {
            border-bottom: 4px double #000;
            padding: 20px 0;
            margin-bottom: 0;
        }

        .top-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 11px;
            color: #666;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e2e2e2;
        }

        .main-nav {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 15px 0;
            border-bottom: 1px solid #e2e2e2;
            margin-bottom: 20px;
        }

        .main-nav ul {
            display: flex;
            list-style: none;
            margin: 0;
            padding: 0;
            gap: 40px;
        }

        .main-nav li {
            position: relative;
        }

        .main-nav a {
            color: #121212;
            text-decoration: none;
            font-size: 14px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            padding: 8px 16px;
            border-radius: 3px;
            transition: all 0.2s ease;
            display: block;
        }

        .main-nav a:hover {
            background-color: #f8f8f8;
            color: #326891;
            text-decoration: underline;
        }

        .main-nav a:active {
            background-color: #326891;
            color: #fff;
        }

        .weather-date {
            font-size: 11px;
            color: #666;
        }

        .subscription-info {
            font-size: 11px;
            color: #326891;
            text-decoration: underline;
        }

        .masthead-container {
            text-align: center;
            margin: 20px 0;
        }

        .masthead {
            font-family: 'Playfair Display', serif;
            font-size: 62px;
            font-weight: 700;
            letter-spacing: 4px;
            color: #000;
            margin-bottom: 5px;
            text-shadow: none;
        }

        .publication-info {
            font-size: 11px;
            color: #666;
            margin-bottom: 8px;
            letter-spacing: 1px;
        }

        .tagline {
            font-size: 12px;
            font-weight: normal;
            color: #666;
            font-style: italic;
            margin-bottom: 15px;
        }

        .date-weather-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 11px;
            color: #666;
            padding: 10px 0;
            border-top: 1px solid #e2e2e2;
            border-bottom: 1px solid #e2e2e2;
            margin-bottom: 20px;
        }

        .date-info {
            font-weight: bold;
        }

        .price-info {
            font-size: 10px;
        }

        /* Main Content Layout */
        .main-content {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
            margin-bottom: 30px;
        }

        .left-column {
            display: flex;
            flex-direction: column;
        }

        .right-column {
            display: flex;
            flex-direction: column;
        }

        /* Lead Story */
        .lead-story {
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid #e2e2e2;
        }

        .lead-headline {
            font-family: 'Playfair Display', serif;
            font-size: 42px;
            font-weight: 700;
            line-height: 1.1;
            color: #000;
            margin-bottom: 15px;
            letter-spacing: -0.5px;
        }

        .lead-summary {
            font-size: 18px;
            line-height: 1.4;
            color: #333;
            margin-bottom: 15px;
            font-weight: 400;
        }

        .byline {
            font-size: 13px;
            color: #666;
            margin-bottom: 15px;
            font-style: italic;
        }

        .article-content {
            font-size: 16px;
            line-height: 1.6;
            color: #333;
            column-count: 2;
            column-gap: 20px;
            text-align: justify;
        }

        /* Secondary Stories */
        .secondary-stories {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 30px;
        }

        .story {
            padding-bottom: 20px;
            border-bottom: 1px solid #e2e2e2;
        }

        .story-headline {
            font-family: 'Playfair Display', serif;
            font-size: 22px;
            font-weight: 700;
            line-height: 1.2;
            color: #000;
            margin-bottom: 10px;
        }

        .story-summary {
            font-size: 14px;
            line-height: 1.5;
            color: #333;
            margin-bottom: 8px;
        }

        .story-text {
            font-size: 14px;
            line-height: 1.5;
            color: #666;
        }

        /* Sidebar */
        .sidebar {
            background-color: #f8f8f8;
            padding: 20px;
            border-left: 1px solid #e2e2e2;
        }

        .sidebar-headline {
            font-family: 'Playfair Display', serif;
            font-size: 20px;
            font-weight: 700;
            color: #000;
            margin-bottom: 15px;
            border-bottom: 2px solid #000;
            padding-bottom: 8px;
        }

        .sidebar-story {
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 1px solid #ddd;
        }

        .sidebar-story:last-child {
            border-bottom: none;
        }

        .sidebar-story-headline {
            font-size: 16px;
            font-weight: 700;
            color: #000;
            margin-bottom: 8px;
            line-height: 1.3;
        }

        .sidebar-story-text {
            font-size: 13px;
            line-height: 1.4;
            color: #666;
        }

        /* Bottom Section */
        .bottom-stories {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            border-top: 2px solid #000;
            padding-top: 20px;
        }

        .bottom-story {
            padding-bottom: 15px;
        }

        .bottom-headline {
            font-size: 16px;
            font-weight: 700;
            color: #000;
            margin-bottom: 8px;
            line-height: 1.3;
        }

        .bottom-text {
            font-size: 13px;
            line-height: 1.4;
            color: #666;
        }

        /* Quote styling */
        .quote {
            font-style: italic;
            color: #555;
            border-left: 3px solid #326891;
            padding-left: 15px;
            margin: 15px 0;
            font-size: 16px;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .masthead {
                font-size: 36px;
            }
            
            .main-content {
                grid-template-columns: 1fr;
            }
            
            .secondary-stories {
                grid-template-columns: 1fr;
            }
            
            .bottom-stories {
                grid-template-columns: 1fr;
            }
            
            .article-content {
                column-count: 1;
            }
            
            .lead-headline {
                font-size: 28px;
            }
            
            .main-nav ul {
                flex-direction: column;
                gap: 10px;
                align-items: center;
            }
            
            .main-nav a {
                font-size: 12px;
            }
        }

        /* Print-like styling */
        .section-label {
            font-size: 10px;
            color: #666;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 10px;
            font-weight: 700;
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <div class="top-nav">
                <div class="weather-date">Tuesday, July 15, 2025 | Today's Paper | Video | Most Popular</div>
                <div class="subscription-info">Subscribe for $0.000/week</div>
            </div>
            
            <div class="masthead-container">
                <h1 class="masthead">The Imperfect Hosts Times</h1>
                <div class="publication-info">VOL. I . . . No. 1 © Imhosts LLC 7/15/2025</div>
                <div class="tagline">News for working musicians Published almost weekly.</div>
            </div>
            
            <nav class="main-nav">
                <ul>
                    <li><a href="#band-info">Band Info</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#music">Music</a></li>
                    <li><a href="#dates">Dates</a></li>
                </ul>
            </nav>
            
            <div class="date-weather-bar">
                <div class="date-info">Tuesday, July 15, 2025</div>
                <div class="weather-info">Music City | 72°F</div>
                <div class="price-info">Late Edition | $0.000</div>
            </div>
        </header>

        <main class="main-content">
            <div class="left-column">
{% assign lead_posts = site.posts | where:"section","lead" %}
{% for post in lead_posts %}
                <article class="lead-story">
                    <h2 class="lead-headline">{{ post.title }}</h2>
                    <p class="lead-summary">{{ post.summary }}</p>
                    <p class="byline">{{ post.byline }}</p>
                    <div class="article-content">
                        {{ post.content }}
                    </div>
                </article>
{% endfor %}
                <section class="secondary-stories">
{% assign secondary_posts = site.posts | where:"section","secondary" %}
{% for post in secondary_posts %}
                    <article class="story">
                        <h3 class="story-headline">{{ post.title }}</h3>
                        <p class="story-summary">{{ post.summary }}</p>
                        <p class="story-text">{{ post.content }}</p>
                    </article>
{% endfor %}
                </section>
            </div>

            <aside class="right-column">
                <div class="sidebar">
                    <h3 class="sidebar-headline">Music Industry News</h3>
{% assign sidebar_posts = site.posts | where:"section","sidebar" %}
{% for post in sidebar_posts %}
                    <article class="sidebar-story">
                        <h4 class="sidebar-story-headline">{{ post.title }}</h4>
                        <p class="sidebar-story-text">{{ post.content }}</p>
                    </article>
{% endfor %}
                </div>
            </aside>
        </main>

        <section class="bottom-stories">
{% assign bottom_posts = site.posts | where:"section","bottom" %}
{% for post in bottom_posts %}
            <article class="bottom-story">
                <h3 class="bottom-headline">{{ post.title }}</h3>
                <p class="bottom-text">{{ post.content }}</p>
            </article>
{% endfor %}
        </section>
    </div>
</body>
</html>
