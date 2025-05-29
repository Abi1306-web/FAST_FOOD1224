<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FOOD EXPRESS</title>
    <link rel="stylesheet" href="STYLES.CSS">
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }

        header {
            background-color: #f71414a2;
            color: rgb(0, 0, 0);
            padding: 1em 1em;
            display: flex;
            flex-direction: column;   
            align-items: center;
            width: 100%;
        }

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            max-width: 900px;
            margin-bottom: 0.5em;
        }

        header h1 {
            margin: 0;
            font-size: 1.8em;
        }

        header img {
            max-height: 80px;
        }

        .carousel-container {
            width: 100%; /* Ocupar todo el ancho del contenedor padre */
            margin: 10px auto; /* Centrar horizontalmente si es necesario */
            overflow: hidden;
            border-radius: 5px;
            max-width: 900px; /* Limitar el ancho máximo del carrusel */
        }

        .carousel-slide {
            display: flex;
            width: calc(100% * 15); /* Ajusta el número según la cantidad de imágenes */
            transition: transform 0.8s ease-in-out;
            transform: translateX(0);
        }

        .carousel-slide img {
            max-height: 200px; /* Hacer las imágenes más grandes para la interacción */
            margin: 0 10px;
            cursor: pointer; /* Indicar que son clickeables */
        }

        section {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
        }

        section h2 {
            color: #1a9be6a2;
            border-bottom: 2px solid #ccc;
            padding-bottom: 0.5em;
            margin-bottom: 1em;
            text-align: center; /* Centrar el título de las secciones */
        }

        /* Ocultar las secciones que ya no están en la navegación principal */
        #nosotros, #contacto {
            display: none;
        }
        nav ul {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center; /* Centrar los enlaces de navegación */
            width: 100%; /* Ocupar todo el ancho del header */
            max-width: 400px; /* Limitar el ancho de la navegación si es necesario */
        }

        nav li {
            margin: 0 1em; /* Espacio entre los elementos de la lista */
        }

        nav li a {
            color: white;
            text-decoration: none;
            padding: 0.5em 1em;
            display: block;
        }

        nav li a:hover {
            background-color: #555;
        }

        .menu {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center; /* Centrar el contenido dentro del menú */
        }

        .menu h2 {
            text-align: center;
            margin-bottom: 20px;
            color: #333;
        }

        .paquete {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 20px; /* Espacio entre los paquetes y el botón */
        }

        .item {
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 15px;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out; /* Agregamos una transición suave */
        }

        .item:hover {
            transform: scale(1.05); /* Escala ligeramente al pasar el mouse */
        }

        .item h3 {
            margin-top: 0;
            color: #555;
        }

        .item p {
            margin-bottom: 5px;
            color: #777;
        }

        .precio {
            font-weight: bold;
            color: green;
            font-size: 1.1em;
        }

        .item-image {
            max-width: 100%;
            height: auto;
            margin-bottom: 10px;
            border-radius: 5px;
        }

        .boton-pedido {
            display: block; /* Cambiado a block para que ocupe todo el ancho */
            width: 200px; /* Ancho fijo del botón */
            margin: 20px auto; /* Centrar horizontalmente */
            padding: 10px 20px;
            background-color: #5cb85c; /* Un color verde llamativo */
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s ease;
            text-align: center; /* Centrar el texto dentro del botón */
        }

        .boton-pedido:hover {
            background-color: #4cae4c;
        }

        .pedido-qr {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .pedido-qr h2 {
            color: #333;
            margin-bottom: 15px;
        }

        .qr-container {
            margin-top: 20px;
        }

        .qr-image {
            max-width: 200px;
            height: auto;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

    </style>
</head>
<body>
    <header>
        <div class="header-top">
            <h1>FOOD EXPRESS </h1>
            <img src="images/image.png" alt="Logo Tosti Tosti">
        </div>
    </header>

    <div class="carousel-container">
        <div class="carousel-slide">
            <a href="#"><img src="https://cdn7.kiwilimon.com/recetaimagen/26245/960x640/38984.jpg.jpg" alt="Tostada 1 - Pedir"></a>
            <a href="#"><img src="https://tb-static.uber.com/prod/image-proc/processed_images/51ee045d91085dfa0f4c588fedd86472/9e31c708e4cf73b6e3ea1bd4a9b6e16b.jpeg" alt="Bebida 1 - Pedir"></a>
            <a href="#"><img src="https://img-global.cpcdn.com/recipes/2103946_4f1951f9a2b82f79/400x400cq70/photo.jpg" alt="Postre 1 - Pedir"></a>
            <a href="#"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbUH2Ts6LzfErBmbBKplF8n1CAw2ECSRPqIw&s" alt="Extra 1 - Pedir"></a>
            <a href="#"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRmpiQswtK4_V9QUbrNglGDCRz-cSG3S-BDAQ&s" alt="Tostada 2 - Pedir"></a>
            <a href="#"><img src="https://www.unileverfoodsolutions.com.mx/dam/global-ufs/mcos/NOLA/calcmenu/recipes/MX-recipes/torta-cubana/torta.jpg" alt="Taco 2 - Pedir"></a>
            <a href="#"><img src="https://peopleenespanol.com/thmb/I7zH_8mxTpJLulhHoqrOT1MLYBE=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/ensalada-de-codito-con-pollo-y-verduras-2000-30ee7afe632142809e238869d4cb5fd4.jpg" alt="Bebida 2 - Pedir"></a>
            <a href="#"><img src="https://recetasdecocina.elmundo.es/wp-content/uploads/2018/10/Consome-receta-1024x683.jpg" alt="Postre 2 - Pedir"></a>
            <a href="#"><img src="https://www.vvsupremo.com/wp-content/uploads/2017/09/Chilaquiles-with-Salsa-Verde-900x570-sRGB.jpg" alt="Tostada 3 - Pedir"></a>
            <a href="#"><img src="https://cdn.prod.website-files.com/64ee6d040da86184dbf962a0/650b64ca3784c1962e96986d_IMG_1073%20copy.webp" alt="Taco 3 - Pedir"></a>
            <a href="#"><img src="https://tb-static.uber.com/prod/image-proc/processed_images/51ee045d91085dfa0f4c588fedd86472/9e31c708e4cf73b6e3ea1bd4a9b6e16b.jpeg" alt="Bebida 3 - Pedir"></a>
            <a href="#"><img src="https://img-global.cpcdn.com/recipes/2103946_4f1951f9a2b82f79/400x400cq70/photo.jpg" alt="Postre 3 - Pedir"></a>
            <a href="#"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbUH2Ts6LzfErBmbBKplF8n1CAw2ECSRPqIw&s" alt="Extra 2 - Pedir"></a>
        </div>
    </div>

    <section class="menu">
        <h2>¡Nuestros Paquetes Ahorro y más!</h2>
        <div class="paquete">
            <div class="item">
                <h3>PKT #1</h3>
                <img src="https://upload.wikimedia.org/wikipedia/commons/a/a7/Tostada_Siberia.jpg" alt="PKT #1" class="item-image">
                <p>2 Tostadas grandes</p>
                <p>1 Taco grande</p>
                <p class="precio">$165 MXN</p>
            </div>
            <div class="item">
                <h3>PKT #2</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT5HNhm2EuNUcrflZd2XZfrLm-YQYHixtnSGg&s" alt="PKT #2" class="item-image">
                <p>3 Tacos grandes</p>
                <p class="precio">$135 MXN</p>
            </div>
            <div class="item">
                <h3>PKT #3</h3>
                <img src="https://upload.wikimedia.org/wikipedia/commons/a/a7/Tostada_Siberia.jpg" alt="PKT #3" class="item-image">
                <p>3 Tostadas grandes</p>
                <p class="precio">$180 MXN</p>
            </div>
            <div class="item">
                <h3>PKT #4</h3>
                <img src="https://cdn.prod.website-files.com/62a0d7bf983758ee827aca82/62f6af130a419212de31e1ef_A45.png" alt="PKT #4" class="item-image">
                <p>2 Tacos grandes</p>
                <p>1 Tostada Jr.</p>
                <p class="precio">$125 MXN</p>
            </div>
            <div class="item">
                <h3>PKT #5</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGcApkYiAUjn1ox3CxI2sup5cVYPMeIViNpg&s" alt="PKT #5" class="item-image">
                <p>2 Tostadas</p>
                <p>1/2 Consomé</p>
                <p class="precio">$155 MXN</p>
            </div>
            <div class="item">
                <h3>PKT #6</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGcApkYiAUjn1ox3CxI2sup5cVYPMeIViNpg&s" alt="PKT #6" class="item-image">
                <p>1 Tostada</p>
                <p>1 Taco</p>
                <p>1/2 Consomé</p>
                <p class="precio">$140 MXN</p>
            </div>
            <div class="item">
                <h3>PKT Individual</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGcApkYiAUjn1ox3CxI2sup5cVYPMeIViNpg&s" alt="PKT Individual" class="item-image">
                <p>1 Tostada</p>
                <p>1/2 Consomé</p>
                <p class="precio">$90 MXN</p>
            </div>
            <div class="item">
                <h3>PKT Familiar</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRxqxGmlMpDd1QPa1U5lWrnb5WM-ETK5qwjEQ&s" alt="PKT Familiar" class="item-image">
                <p>3 Tostadas</p>
                <p>2 Tacos</p>
                <p>1L Caldo</p>
                <p class="precio">$320 MXN</p>
            </div>
            <div class="item">
                <h3>Tostadas Jr.</h3>
                <img src="https://cdn.prod.website-files.com/64ee6d040da86184dbf962a0/650b64ca8445d16c6768d784_IMG_0630%20copy.webp" alt="Tostadas Jr." class="item-image">
                <p class="precio">$35 MXN</p>
            </div>
            <div class="item">
                <h3>Tostadas de la Siberia</h3>
                <img src="https://img-global.cpcdn.com/recipes/1f9744288b2390b0/680x482cq70/tostadas-y-tacos-tipo-siberia-100-caseras-foto-principal.jpg" alt="Tostadas de la Siberia" class="item-image">
                <p class="precio">$65 MXN</p>
            </div>
            <div class="item">
                <h3>Tacos de la Siberia Jr.</h3>
                <img src="https://upload.wikimedia.org/wikipedia/commons/a/a7/Tostada_Siberia.jpg" alt="Tacos de la Siberia Jr." class="item-image">
                <p class="precio">$25 MXN</p>
            </div>
            <div class="item">
                <h3>Tacos de la Siberia grandes</h3>
                <img src="https://img-global.cpcdn.com/recipes/1f9744288b2390b0/680x482cq70/tostadas-y-tacos-tipo-siberia-100-caseras-foto-principal.jpg" alt="Tacos de la Siberia grandes" class="item-image">
                <p class="precio">$50 MXN</p>
            </div>
            <div class="item">
                <h3>Enmoladas</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRt58PiJ0RWQGkZXmGHjl2NNyLAJU0JkJJCOw&s" alt="Enmoladas" class="item-image">
                <p class="precio">$75 MXN </p>
            </div>
            <div class="item">
                <h3>Flautas</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSnbe_CxGksacwxEd_RY5X70ipa7-Fmcy3PSdnduT60mrPTQEQXYBszcOopc21NstwPkas&usqp=CAU" alt="Flautas" class="item-image">
                <p class="precio">$75 MXN</p>
            </div>
            <div class="item">
                <h3>Tortas</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQenq1rC1vqQvjki4fElLNN4mmSIg5w_C69Fg&s" alt="Arroz" class="item-image">
                <p class="precio">$80 MXN </p>
            </div>
            <div class="item">
                <h3>Pepsi 1.5l</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRMH8MWimnnYMqDplKkLMoldbdS53cTmN7Xng&s" alt="Coca-Cola" class="item-image">
                <p class="precio">$30 MXN </p>
            </div>
            <div class="item">
                <h3>Caldo litro</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSZVnds2djufqSUQsPouzRa1dtTNiiLBh5aqw&s" alt="Coca-Cola" class="item-image">
                <p class="precio">$55 MXN </p>
            </div>
            <div class="item">
                <h3>Caldo 1/2L</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRrQkSlcrNcNHnh-OyMJFkYNW6lWyjPQYhn4g&s" alt="Coca-Cola" class="item-image">
                <p class="precio">$45 MXN </p>
            </div>
            <div class="item">
                <h3>Enchiladas</h3>
                <img src="https://familiakitchen.com/wp-content/uploads/2021/01/iStock-1178656148-enchiladas-low-res-v3.jpg" alt="Coca-Cola" class="item-image">
                <p class="precio">$75 MXN </p>
            </div>
            <div class="item">
                <h3>Chilaquiles</h3>
                <img src="https://www.vvsupremo.com/wp-content/uploads/2017/09/Chilaquiles-with-Salsa-Verde-900x570-sRGB.jpg" alt="Coca-Cola" class="item-image">
                <p class="precio">$75 MXN </p>
            </div>
            <div class="item">
                <h3>Ensalada de pollo</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTuiRayfI3SbnbfGR-RdXpIKhNjAPSn3MqHsQ&s" alt="Coca-Cola" class="item-image">
                <p class="precio">$70 MXN </p>
            </div>
            <div class="item">
                <h3>Ensalada de coditos</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRK5XzSz_-RqsjCK0Ns7ZkvHaj88gGD8ZZyuQ&s" alt="Coca-Cola" class="item-image">
                <p class="precio">$65 MXN </p>
            </div>
            <div class="item">
                <h3>Ensalada Mixta</h3>
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSSfWxGTcnC6LVhE1cpfYVaYDegDeqNggVNSw&s" alt="Coca-Cola" class="item-image">
                <p class="precio">$65 MXN </p>
            </div>
            <div class="item">
                <h3>Consomé litro</h3>
                <img src="https://tb-static.uber.com/prod/image-proc/processed_images/e73e81e3eecb1623691f14eef9148d15/f0d1762b91fd823a1aa9bd0dab5c648d.jpeg" alt="Coca-Cola" class="item-image">
                <p class="precio">$45 MXN </p>
            </div>
            <div class="item">
                <h3>Consomé 1/2L</h3>
                <img src="https://tb-static.uber.com/prod/image-proc/processed_images/e73e81e3eecb1623691f14eef9148d15/f0d1762b91fd823a1aa9bd0dab5c648d.jpeg" alt="Coca-Cola" class="item-image">
                <p class="precio">$35 MXN </p>
            </div>
        </div>
<a href="pedidos.html" class="boton-pedido">Realizar Pedido</a>
    </section>

    <section class="pedido-qr">
        <h2>¡Paga con QR!</h2>
        <p>Escanea el siguiente código QR para realizar tu pago de forma rápida y segura.</p>
        <div class="qr-container">
            <img src="images/qr_ejemplo.png" alt="Código QR para pago" class="qr-image">
            <p>Muestra este código al realizar tu pedido.</p>
        </div>
    </section>

    <script>
        const carouselContainer = document.querySelector('.carousel-container');
        const carouselSlide = document.querySelector('.carousel-slide');
        const images = document.querySelectorAll('.carousel-slide img');

        let counter = 0;
        let slideWidth = images[0].offsetWidth + 20;
        const slideSpeed = 3000;

        carouselSlide.style.width = `${images.length * slideWidth}px`;

        function nextSlide() {
            counter++;
            if (counter >= images.length) {
                counter = 0;
                carouselSlide.style.transition = 'transform 0s';
                carouselSlide.style.transform = `translateX(-${counter * slideWidth}px)`;
                carouselSlide.offsetWidth;
                carouselSlide.style.transition = 'transform 0.8s ease-in-out';
            } else {
                carouselSlide.style.transform = `translateX(-${counter * slideWidth}px)`;
            }
        }

        setInterval(nextSlide, slideSpeed);

        window.onload = () => {
            slideWidth = images[0].offsetWidth + 20;
            carouselSlide.style.width = `${images.length * slideWidth}px`;
        };

        window.addEventListener('resize', () => {
            slideWidth = images[0].offsetWidth + 20;
            carouselSlide.style.width = `${images.length * slideWidth}px`;
            carouselSlide.style.transition = 'transform 0s';
            carouselSlide.style.transform = `translateX(-${counter * slideWidth}px)`;
            carouselSlide.offsetWidth;
            carouselSlide.style.transition = 'transform 0.8s ease-in-out';
        });
    </script>
</body>
</html>
