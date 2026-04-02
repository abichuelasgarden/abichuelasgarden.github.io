---
layout: null
title: Mi Álbum de Postales
---
<!-- <!-- <!DOCTYPE html> --> -->
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Galería | Abichuela's Garden</title>
    <style>
        body {
            background-color: #FDFCF5; /* Tu crema cálido */
            font-family: 'Georgia', serif;
            margin: 0;
            padding: 40px 20px;
            color: #2E3A31;
        }

        h1 {
            text-align: center;
            color: #3A5F44;
            font-size: 2.5rem;
            margin-bottom: 50px;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        /* --- CONTENEDOR DEL ÁLBUM --- */
        .album-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 40px;
            max-width: 1100px;
            margin: 0 auto;
        }

        /* --- ESTILO DE LA POSTAL --- */
        .postal-card {
            background: white;
            padding: 15px 15px 40px 15px; /* Espacio extra abajo para el texto */
            box-shadow: 5px 5px 15px rgba(0,0,0,0.08);
            border: 1px solid #eee;
            text-decoration: none;
            color: inherit;
            transition: all 0.3s ease;
            
            /* Rotación aleatoria sutil para que parezcan "tiradas" */
            transform: rotate(-1.5deg);
        }

        /* Variamos la rotación en algunas para que se vea orgánico */
        .postal-card:nth-child(even) { transform: rotate(2deg); }
        .postal-card:nth-child(3n) { transform: rotate(-1deg); }

        .postal-card:hover {
            transform: rotate(0deg) scale(1.05);
            box-shadow: 10px 10px 25px rgba(0,0,0,0.15);
            z-index: 10;
        }

        /* IMAGEN DE LA POSTAL */
        .postal-card img {
            width: 100%;
            height: 200px;
            object-fit: cover; /* Para que todas las fotos midan lo mismo sin deformarse */
            display: block;
            border-bottom: 1px solid #f9f9f9;
        }

        /* TEXTO DE LA POSTAL */
        .postal-info {
            margin-top: 15px;
            text-align: left;
        }

        .postal-info h3 {
            margin: 0;
            font-size: 1.1rem;
            color: #333;
            font-family: 'Handlee', cursive, 'Georgia'; /* Si puedes, usa una fuente manuscrita */
        }

        .postal-meta {
            font-size: 0.8rem;
            color: #C87459; /* Tu terracota */
            margin-top: 5px;
            display: block;
        }

        .stamp-mark {
            float: right;
            width: 35px;
            height: 45px;
            border: 1px dashed #D6CDBA;
            margin-top: -30px;
            opacity: 0.5;
        }
        
        .back-link {
            display: block;
            text-align: center;
            margin-bottom: 40px;
            color: #3A5F44;
            text-decoration: none;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <a href="index.html" class="back-link">← Volver al Jardín</a>
    <h1>Galería de Recuerdos</h1>

    <div class="album-grid">
        {% for foto in site.galeria %}
        <a href="{{ foto.url }}" class="postal-card">
            <img src="{{ foto.imagen }}" alt="{{ foto.title }}">
            <div class="postal-info">
                <h3>{{ foto.title }}</h3>
                <span class="postal-meta">📍 {{ foto.lugar }} | {{ foto.date | date: "%d/%m/%Y" }}</span>
                <div class="stamp-mark"></div>
            </div>
        </a>
        {% endfor %}
    </div>

</body>
</html>