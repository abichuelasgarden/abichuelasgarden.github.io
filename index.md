---
layout: null
title: Abichuela's Garden
---
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Abichuela's Garden</title>
    <style>
        /* Tu paleta botánica directamente aquí */
        body {
            background-color: #FDFCF5; /* Crema cálido */
            color: #2E3A31; /* Verde oscuro */
            font-family: 'Georgia', serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 20px;
            line-height: 1.6;
        }

        h1 {
            color: #3A5F44; /* Verde invernadero */
            text-align: center;
            border-bottom: 2px solid #3A5F44;
            padding-bottom: 20px;
        }

        .garden-nav {
            list-style: none;
            padding: 0;
            margin-top: 50px;
        }

        .garden-nav li {
            margin-bottom: 20px;
        }

        .garden-nav a {
            display: block;
            text-decoration: none;
            color: #3A5F44;
            border: 2px solid #3A5F44;
            padding: 20px;
            border-radius: 12px;
            transition: all 0.3s ease;
            background: white;
        }

        .garden-nav a:hover {
            background-color: #3A5F44;
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(58, 95, 68, 0.2);
        }

        .description {
            font-style: italic;
            display: block;
            font-size: 0.9em;
            color: #C87459; /* Terracota */
            margin-top: 5px;
        }
    </style>
</head>
<body>

    <h1>Abichuela's Garden 🌱</h1>

    <p style="text-align: center;">El jardín digital de un pony de varios trucos.</p>

    <ul class="garden-nav">
        <li>
            <a href="galeria.html">
                <strong>Galería</strong>
                <span class="description">Mi hobbie favorito: la fotografía.</span>
            </a>
        </li>
        <li>
            <a href="radiocumulus.html">
                <strong>Radiocumulus</strong>
                <span class="description">Mi programa de radio en YouTube.</span>
            </a>
        </li>
        <li>
            <a href="nubetrosfera.html">
                <strong>Nubetrosfera</strong>
                <span class="description">Divulgación meteorológica y mi portafolio profesional.</span>
            </a>
        </li>
    </ul>

</body>
</html>