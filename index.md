---
layout: null
title: Abichuela's Garden 🌱
---
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abichuela's Garden</title>
    <style>
        /* --- ESTILOS GENERALES --- */
        body {
            background-color: #F3EBE1; /* Fondo beige cálido como la imagen */
            margin: 0;
            padding: 0;
            font-family: 'Georgia', serif; /* Fuente serif clásica y elegante */
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center; /* Centra todo horizontalmente */
            min-height: 100vh; /* Asegura que el fondo cubra toda la altura */
        }

        /* --- IMAGEN DE ENREDADERAS --- */
        .vines-header {
            width: 100%;
            max-width: 1000px; /* Limita el ancho en pantallas grandes */
            height: auto;
            display: block;
            margin-top: -10px; /* Ajuste sutil para que suba un poco */
        }

        /* --- TÍTULO PRINCIPAL CON SOMBRA --- */
        h1 {
            font-size: 3rem; /* Tamaño grande y llamativo */
            font-weight: bold;
            text-transform: uppercase; /* Todo en mayúsculas */
            letter-spacing: 2px; /* Espaciado entre letras */
            margin-top: 20px;
            margin-bottom: 5px;
            color: #000; /* Texto negro */
            /* Efecto de sombra sutil como en la imagen */
            text-shadow: 2px 2px 0px rgba(0,0,0,0.1); 
        }

        /* --- SUBTÍTULO --- */
        .subtitle {
            font-size: 1.2rem;
            color: #555;
            margin-bottom: 50px; /* Espacio antes de los botones */
            font-weight: normal;
        }

        /* --- CONTENEDOR DE BOTONES (Horizontal) --- */
        .garden-nav {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex; /* Magia de Flexbox: pone los elementos en línea */
            flex-direction: row; /* Horizontal */
            gap: 20px; /* Espacio entre los botones */
            justify-content: center; /* Centra el grupo de botones */
            width: 90%;
            max-width: 800px;
        }

        /* --- ESTILO DE CADA BOTÓN (Redondeado y Pequeño) --- */
        .garden-nav li a {
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            
            /* Botones más pequeños y compactos */
            padding: 10px 30px; 
            border-radius: 50px; /* Bordes totalmente redondeados (píldora) */
            
            transition: transform 0.2s, box-shadow 0.2s;
            min-width: 120px; /* Ancho mínimo para que se vean uniformes */
            text-align: center;
        }

        /* --- COLORES ESPECÍFICOS DE CADA BOTÓN (Inspirados en tu imagen) --- */
        
        /* Botón 1: Verde Oliva Suave */
        .nav-galeria {
            background-color: #B9C481;
            color: #3B441D;
        }

        /* Botón 2: Beige/Tierra Suave */
        .nav-radiocumulus {
            background-color: #D6CDBA;
            color: #5C5441;
        }

        /* Botón 3: Morado Cumulonimbus (Más oscuro) */
        .nav-nubetrosfera {
            background-color: #514E94;
            color: white;
        }

        /* --- EFECTO HOVER --- */
        .garden-nav li a:hover {
            transform: translateY(-3px); /* Pequeño salto hacia arriba */
            box-shadow: 0 5px 15px rgba(0,0,0,0.1); /* Sombra suave */
        }
    </style>
</head>
<body>

    <img src="https://png.pngtree.com/png-vector/20241030/ourmid/pngtree-hanging-green-vines-with-heart-shaped-leaves-png-image_14168939.png" alt="Enredaderas colgantes" class="vines-header">

    <h1>Abichuela's Garden</h1>
    
    <p class="subtitle">El jardín digital de un pony de varios trucos</p>

    <ul class="garden-nav">
        <li><a href="galeria.html" class="nav-galeria">Galeria</a></li>
        <li><a href="radiocumulus.html" class="nav-radiocumulus">Radiocumulus</a></li>
        <li><a href="nubetrosfera.html" class="nav-nubetrosfera">Nubetrosfera</a></li>
    </ul>

</body>
</html>