---
layout: null
title: Nubetrosfera
---
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Nubetrosfera | Divulgación Atmosférica</title>
    <style>
        body { background-color: #fdfdfd; font-family: 'Lora', serif; margin: 0; padding: 0; color: #1a1a1a; }
        .header-nube { background: #3A5F44; color: white; padding: 60px 20px; text-align: center; }
        .container { max-width: 900px; margin: 0 auto; padding: 40px 20px; }
        
        /* Navegación de Secciones */
        .nube-nav { display: flex; justify-content: center; gap: 40px; margin-bottom: 50px; border-bottom: 2px solid #f0f0f0; padding-bottom: 20px; }
        .nube-nav a { text-decoration: none; color: #3A5F44; font-weight: bold; text-transform: uppercase; font-size: 0.9rem; letter-spacing: 2px; transition: 0.3s; }
        .nube-nav a:hover { color: #C87459; }

        /* Bienvenida */
        .welcome-grid { display: grid; grid-template-columns: 1fr 1.5fr; gap: 40px; align-items: center; margin-bottom: 60px; }
        .welcome-img { width: 100%; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.1); }
        .welcome-text { font-size: 1.2rem; line-height: 1.6; color: #444; }

        /* Lista de Entradas */
        .section-title { border-bottom: 1px solid #eee; padding-bottom: 10px; margin-top: 60px; color: #333; text-transform: uppercase; font-size: 1rem; letter-spacing: 1px; }
        .post-item { display: flex; justify-content: space-between; align-items: baseline; padding: 15px 0; border-bottom: 1px solid #f9f9f9; text-decoration: none; color: inherit; transition: 0.2s; }
        .post-item:hover { background: #fcfcfc; padding-left: 10px; }
        .post-title { font-weight: bold; color: #3A5F44; font-size: 1.1rem; }
        .post-date { font-size: 0.85rem; color: #999; font-family: monospace; }
        .category-tag { font-size: 0.7rem; background: #eef2ff; color: #514E94; padding: 3px 8px; border-radius: 4px; text-transform: uppercase; margin-left: 10px; }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
</head>
<body>

    <header class="header-nube">
        <h1 style="margin:0; font-size: 3.5rem; letter-spacing: -2px;">NUBETROSFERA</h1>
        <p style="opacity: 0.9; font-style: italic;">Ciencia atmosférica con rigor y calidez</p>
    </header>

    <div class="container">
        <nav class="nube-nav">
            <a href="#gaceta">Gaceta</a>
            <a href="#blog">Blog</a>
            <a href="#recursos">Recursos</a>
            <a href="index.html">← Salir al Jardín</a>
        </nav>

        <div class="welcome-grid">
            <img src="{{ site.baseurl }}/assets/images/DSCN0282.JPG" class="welcome-img" alt="Bienvenida">
            <div class="welcome-text">
                <p>Bienvenidx a la sección más dedicada de mi jardín. Aquí la pasión por la meteorología y la divulgación se unen para crear un espacio de aprendizaje compartido.</p>
                <p>Explora mis artículos detallados, notas personales o descarga recursos útiles para tus propios proyectos.</p>
            </div>
        </div>

        <h2 class="section-title">Últimas publicaciones</h2>
        <div class="post-list">
            {% for post in site.nubetrosfera limit:10 %}
            <a href="{{ post.url }}" class="post-item">
                <div>
                    <span class="post-title">{{ post.title }}</span>
                    <span class="category-tag">{{ post.category }}</span>
                </div>
                <span class="post-date">{{ post.date | date: "%d %b %Y" }}</span>
            </a>
            {% endfor %}
        </div>
    </div>

</body>
</html>