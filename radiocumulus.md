---
layout: null
title: Radiocumulus
---
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Radiocumulus | Abichuela's Garden</title>
    <style>
        body { background-color: #FDFCF5; font-family: 'Georgia', serif; padding: 40px 20px; color: #2E3A31; }
        .container { max-width: 800px; margin: 0 auto; }
        h1 { text-align: center; color: #3A5F44; border-bottom: 2px solid #3A5F44; padding-bottom: 10px; }
        
        /* Estilo Bookmark tipo Notion */
        .bookmark-list { display: flex; flex-direction: column; gap: 20px; margin-top: 40px; }
        .bookmark {
            display: flex;
            text-decoration: none;
            border: 1px solid #D6CDBA;
            border-radius: 10px;
            overflow: hidden;
            background: white;
            transition: transform 0.2s, box-shadow 0.2s;
            height: 120px;
        }
        .bookmark:hover { transform: translateY(-3px); box-shadow: 0 5px 15px rgba(0,0,0,0.1); }
        .bookmark-thumb { width: 200px; background-size: cover; background-position: center; }
        .bookmark-content { padding: 15px; flex: 1; display: flex; flex-direction: column; justify-content: center; }
        .bookmark-content h3 { margin: 0; font-size: 1.1rem; color: #3A5F44; }
        .bookmark-content p { margin: 5px 0 0; font-size: 0.9rem; color: #666; line-height: 1.3; }
        .bookmark-meta { font-size: 0.75rem; color: #C87459; margin-top: 8px; font-weight: bold; }
    </style>
</head>
<body>
    <div class="container">
        <a href="index.html" style="color: #3A5F44; text-decoration: none;">← Volver al Jardín</a>
        <h1>Radiocumulus 🎙️</h1>
        <p style="text-align: center; font-style: italic;">Bitácora de guiones y nubes sonoras.</p>

        <div class="bookmark-list">
            {% for video in site.radiocumulus %}
            <a href="{{ video.url }}" class="bookmark">
                <div class="bookmark-thumb" style="background-image: url('{{ video.thumbnail }}');"></div>
                <div class="bookmark-content">
                    <h3>{{ video.title }}</h3>
                    <p>{{ video.description | truncate: 100 }}</p>
                    <span class="bookmark-meta">📅 {{ video.date | date: "%d/%m/%Y" }}</span>
                </div>
            </a>
            {% endfor %}
        </div>
    </div>
</body>
</html>