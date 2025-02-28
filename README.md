<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lista de Proveedores</title>
    <style>
    /* Estilos generales */
body {
    font-family: Arial, sans-serif;
    background: linear-gradient(120deg, #f6d365, #fda085);
    text-align: center;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
}
.menu {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-bottom: 20px;
    flex-wrap: wrap;
}

.menu a {
    text-decoration: none;
    padding: 12px 25px;
    background: #007BFF;
    color: white;
    border-radius: 5px;
    font-weight: bold;
    transition: background 0.3s, transform 0.2s, box-shadow 0.3s;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
    display: inline-block;
    text-align: center;
    font-size: 18px;
}

.menu a:hover {
    background: #0056b3;
    transform: scale(1.05);
    box-shadow: 3px 3px 8px rgba(0, 0, 0, 0.4);
}

/* Efecto cuando un botón está activo */
.menu a.active {
    background: red !important;
    color: white;
    box-shadow: 0px 0px 15px rgba(255, 0, 0, 0.7);
}

/* 📱 Diseño responsivo para teléfonos - Botones más pequeños */
@media (max-width: 768px) {
    .menu {
        flex-direction: column;
        align-items: center;
        gap: 8px;
    }

    .menu a {
        width: 50%; /* Reducido un 30% */
        padding: 10px; /* Menos padding */
        font-size: 14px; /* Letra más pequeña */
    }
}



/* Animación de entrada */
@keyframes fadeIn {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes slideUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}

/* Contenedor principal */
.container {
    width: 90%;
    max-width: 1200px;
    margin: 20px auto;
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    transition: all 0.3s ease-in-out;
    animation: fadeIn 1s ease-in-out;
}

.container:hover {
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
}

/* Título */
h1 {
    color: #333;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
}

/* Barra de búsqueda */
.search-bar {
    margin-bottom: 20px;
}

.search-bar input {
    padding: 10px;
    width: 80%;
    max-width: 400px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 16px;
}

/* Contenedor de tarjetas */
.card-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 15px;
    padding: 10px;
    animation: slideUp 0.8s ease-in-out;
}

/* Estilos de tarjetas con colores dinámicos */
.card {
    background: white;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    padding: 15px;
    text-align: center;
    transition: transform 0.3s, background 0.5s ease-in-out;
}

/* Cambio de color en tarjetas con hover */
.card:hover {
    transform: scale(1.05);
}

.card:nth-child(1):hover { background: #ff7eb3; }
.card:nth-child(2):hover { background: #6a85b6; }
.card:nth-child(3):hover { background: #ffcc5c; }
.card:nth-child(4):hover { background: #6ab04c; }
.card:nth-child(5):hover { background: #ff6b6b; }
.card:nth-child(6):hover { background: #00cec9; }
.card:nth-child(7):hover { background: #ff7eb3; }
.card:nth-child(8):hover { background: #6a85b6; }
.card:nth-child(9):hover { background: #ffcc5c; }
.card:nth-child(10):hover { background: #6ab04c; }
.card:nth-child(11):hover { background: #ff6b6b; }
.card:nth-child(12):hover { background: #00cec9; }
.card:nth-child(13):hover { background: #ff7eb3; }
.card:nth-child(14):hover { background: #6a85b6; }
.card:nth-child(15):hover { background: #ffcc5c; }
.card:nth-child(16):hover { background: #6ab04c; }
.card:nth-child(17):hover { background: #ff6b6b; }
.card:nth-child(18):hover { background: #00cec9; }
.card:nth-child(19):hover { background: #ff7eb3; }
.card:nth-child(20):hover { background: #6a85b6; }
.card:nth-child(21):hover { background: #ffcc5c; }
.card:nth-child(22):hover { background: #6ab04c; }
.card:nth-child(23):hover { background: #ff6b6b; }
.card:nth-child(24):hover { background: #00cec9; }
.card:nth-child(25):hover { background: #ff7eb3; }
.card:nth-child(26):hover { background: #6a85b6; }
.card:nth-child(27):hover { background: #ffcc5c; }
.card:nth-child(28):hover { background: #6ab04c; }
.card:nth-child(29):hover { background: #ff6b6b; }
.card:nth-child(30):hover { background: #00cec9; }
.card:nth-child(31):hover { background: #ff7eb3; }
.card:nth-child(32):hover { background: #6a85b6; }
.card:nth-child(33):hover { background: #ffcc5c; }
.card:nth-child(34):hover { background: #6ab04c; }
.card:nth-child(35):hover { background: #ff6b6b; }
.card:nth-child(36):hover { background: #00cec9; }
.card:nth-child(37):hover { background: #ff7eb3; }
.card:nth-child(38):hover { background: #6a85b6; }
.card:nth-child(39):hover { background: #ffcc5c; }
.card:nth-child(40):hover { background: #6ab04c; }
.card:nth-child(41):hover { background: #ff6b6b; }
.card:nth-child(42):hover { background: #00cec9; }
/* Logo dentro de las tarjetas */
.logo {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 10px;
}

/* Íconos de contacto */
.contact-icons {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 10px;
}

.contact-icons a {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: #f0f0f0;
    transition: transform 0.3s ease, background-color 0.3s ease;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
}

.contact-icons a:hover {
    transform: scale(1.2);
}

.whatsapp {
    background-color: #25d366;
}

.whatsapp:hover {
    background-color: #1ebe57;
}

.phone {
    background-color: #0d6efd;
}

.phone:hover {
    background-color: #0842a0;
}

.sms {
    background-color: #ff9900;
}

.sms:hover {
    background-color: #e67e00;
}

/* BOTONES FLOTANTES EN MÓVILES */
.contact-icons-mobile {
    position: fixed;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    gap: 15px;
    background: rgba(0, 0, 0, 0.8);
    padding: 10px 15px;
    border-radius: 30px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
    transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
    animation: fadeIn 1s ease-in-out;
}

/* Efecto de rebote al aparecer */
@keyframes bounce {
    0% { transform: scale(0.8); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

/* Íconos dentro de botones flotantes */
.contact-icons-mobile a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 55px;
    height: 55px;
    border-radius: 50%;
    transition: transform 0.3s ease, background-color 0.3s ease;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
    animation: bounce 0.6s ease-in-out 1;
}

.contact-icons-mobile svg {
    width: 30px;
    height: 30px;
    fill: #ffffff;
}

/* --- RESPONSIVE DESIGN --- */
/* En tablets (2 tarjetas en vez de 3) */
@media (max-width: 768px) {
    .card-container {
        grid-template-columns: repeat(2, 1fr);
    }

    .contact-icons-mobile {
        display: flex;
        opacity: 1;
    }
}

/* En teléfonos (solo 1 tarjeta por fila) */
@media (max-width: 480px) {
    .card-container {
        grid-template-columns: 1fr;
        gap: 20px;
    }

    .card {
        padding: 20px;
        font-size: 14px;
    }

    .menu {
        flex-direction: column;
    }

    .menu a {
        width: 100%;
        text-align: center;
    }

    .contact-icons-mobile {
        display: flex;
    }
}
.card:active {
    background: red !important;
    color: white;
    transition: background 0.3s ease-in-out, color 0.3s ease-in-out;
}
/* Ocultar botones flotantes en pantallas grandes */
@media (min-width: 769px) {
    .contact-icons-mobile {
        display: none;
    }
}

    </style>
</head>
<body>
    <div class="container">
        <h1>Lista de Proveedores</h1>
        <div class="menu">
            <a href="#" onclick="showList('lima')">Proveedores Lima</a>
            <a href="#" onclick="showList('chiclayo')">Proveedores Chiclayo</a>
        </div>
        <div class="search-bar">
            <input type="text" id="searchInput" onkeyup="searchList()" placeholder="Buscar por producto...">
        </div>
        <div class="card-container" id="proveedoresContainer">
            <!-- Se insertarán los proveedores dinámicamente -->
        </div>
    </div>
    <script>
        const proveedores = {
            "lima": [
        { nombre: "FADSEGUR GROUP", venta: "VENTA DE EPPS", celular: "922452824", logo: "logo1.png" },
        { nombre: "KARLY’S SOLUTIONS SAC", venta: "VENTA DE EPPS (ZAPATOS)", celular: "986098112", logo: "logo2.png" },
        { nombre: "AUTOMOTIV", venta: "VENTA DE FILTROS PARA GRUAS", celular: "998326376", logo: "logo3.png" },
        { nombre: "BRAMMERTS", venta: "BOMBAS HIDRAULICAS", celular: "943128577", logo: "logo4.png" },
        { nombre: "CONTINENTAL HIDRAULYC", venta: "VENTA DE BOMBAS , MOTORES , ETC", celular: "981206286", logo: "logo5.png" },
        { nombre: "CROMO INDUSTRIAL", venta: "FABRICACION Y CROMADOS DE EJES", celular: "962457904", logo: "logo6.png" },
        { nombre: "CORPORACION VROM - KARIN", venta: "EJE CROMADO", celular: "", logo: "logo7.png" },
        { nombre: "HARD CHROMIUM SERVICES", venta: "SERVICIO DE CROMADO DE EJES Y VENTA EJES", celular: "994017303", logo: "logo8.png" },
        { nombre: "HIDRAULIC CORPORACION", venta: "BARRAS CROMADAS, VALVULAS, MOTORES", celular: "902717347", logo: "logo9.png" },
        { nombre: "HM CROMO", venta: "SERVICIO DE CROMADO", celular: "946320541", logo: "logo10.png" },
        { nombre: "HPR GROUP", venta: "COMPONENTES HIDRAULICOS - BOBINA", celular: "984890623", logo: "logo11.png" },
        { nombre: "HPR GROUP", venta: "COMPONENTES HIDRAULICOS - BOBINA", celular: "956724233", logo: "logo12.png" },
        { nombre: "HYDRAULIC AND HIDROSTATIC", venta: "VENTA DE MOTORES Y BOMBAS", celular: "998332028", logo: "logo13.png" },
        { nombre: "JG HIDRAULIK", venta: "VALVULAS, FILTROS DE AIRE, VIZOR, ETC", celular: "946173510", logo: "logo14.png" },
        { nombre: "SEBASTIAN HFP - HRP", venta: "SERVICIO DE CROMADO DE EJES Y VENTA EJES", celular: "940321720", logo: "logo15.png" },
        { nombre: "OLEOHUDRAULICS SERVICES", venta: "VENTAS DE VALVULAS, BOBINES", celular: "981276880", logo: "logo16.png" },
        { nombre: "SERVICIO IMERPERU", venta: "EQUIPOS HIDRAULICOS", celular: "982562154/922414793", logo: "logo17.png" },
        { nombre: "ZAPLER", venta: "EJE PALANCA DE CAMBIOS, RESORTES, FILTROS PALFINGER", celular: "956594728", logo: "logo18.png" },
        { nombre: "REGRÚAS DEL PERU- CAJAMARCA", venta: "REPUESTOS PARA GRUAS EN GENERAL", celular: "962667933", logo: "logo19.png" },
        { nombre: "KARCHER", venta: "COMPONENTES DE HIDROLAVADO", celular: "993451639", logo: "logo20.png" },
        { nombre: "FILTROS LYS- MELANIE", venta: "FILTROS DE AIRE, ACEITE", celular: "902838423 / 944026031", logo: "logo21.png" },
        { nombre: "IHP (IMPORTACIONES HILDEMARO)", venta: "FILTROS DE AIRE, ACEITE", celular: "940039620", logo: "logo22.png" },
        { nombre: "PUROLATOR- GLADYS ANICAMA", venta: "FILTROS DE AIRE, ACEITE", celular: "981482860", logo: "logo23.png" },
        { nombre: "FETWELL PERU S.A.C.", venta: "FILTROS FLEETGUARD", celular: "987024757", logo: "logo24.png" },
        { nombre: "NEWMAQ PERU S.A.", venta: "VENTA DE FILTROS DONALSON", celular: "986237652", logo: "logo25.png" },
        { nombre: "PRONA FILTROS (ROCCO)", venta: "FABRICACION DE FILTROS", celular: "998499102", logo: "logo26.png" },
        { nombre: "ASIA REPUESTOS", venta: "REPUESTOS DE AUTOS CHINOS", celular: "951221730", logo: "logo27.png" },
        { nombre: "AUTOPARTES VICTOR HUGO", venta: "ACCESORIOS DE AUTOS", celular: "981299958", logo: "logo28.png" }
    ],
            "chiclayo": [
        { nombre: "CHAPOÑAN", venta: "FERRETERÍA", celular: "957607369", logo: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRk5uQarA_OGr8FL0wcxnzaZKf2HOi4vn5maA&s" },
        { nombre: "ELIZABETH COMPANY", venta: "FERRETERIA- LUIS GONZALES", celular: "999431101", logo: "https://lh4.googleusercontent.com/proxy/OvLzFyElNImV6nTU-ZenySJW45NE_9jxoEEN9YkKBD7JBxv3E6U4Q3uq7kvUbp8J4bZMv0w4UAUSeXVpSpRzHNxDmf2jxAWW6iHy" },
        { nombre: "EPPS FERRETEROS CHICLAYO EIRL", venta: "VENTA DE EPPS", celular: "974372943", logo: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8FGbGPrd7gUZAIIkdbYyCNXiOJl1SBIPRQw&s" },
        { nombre: "FERCOCENT", venta: "PINTURAS, VARILLAS, THINER. ETC", celular: "978947852", logo: "logo4.png" },
        { nombre: "FERRETERIA ARACELY", venta: "DISCOS DE CORTE, HERRAMIENTAS", celular: "940426720", logo: "logo5.png" },
        { nombre: "FERRETERIA UNIVERSAL", venta: "HERRAMIENTAS", celular: "986262832", logo: "logo6.png" },
        { nombre: "IMAN GROUP", venta: "FERRETERIA- LUIS GONZALES", celular: "933627332", logo: "logo7.png" },
        { nombre: "MAXI FERRETERIA LA VICTORIA", venta: "FERRETERIA- LOS INCAS", celular: "937283217", logo: "logo8.png" },
        { nombre: "LUBRICANTES EL REY", venta: "FILTROS, ACEITES", celular: "950892699", logo: "logo9.png" },
        { nombre: "SHEEL- JORGE BELLASMIL", venta: "ACEITE HIDRAULICOS, GRASAS", celular: "965778104", logo: "logo10.png" },
        { nombre: "SHEEL EDGARDO (SERCORISAC)", venta: "ACEITE HIDRAULICOS, DE MOTOR Y GRASAS", celular: "964291221", logo: "logo11.png" },
        { nombre: "TINCOR O LUBRIOFERTAS", venta: "FILTROS, ACEITES", celular: "969290341", logo: "logo12.png" },
        { nombre: "VALVOLINE", venta: "VENTA DE VALDE DE ACEITE HIDRAULICO", celular: "908883322", logo: "logo13.png" },
        { nombre: "VISTONI- VICTOR MURILLO", venta: "ACEITE HIDRAULICOS, GRASAS", celular: "946398648", logo: "logo14.png" },
        { nombre: "LUBRICANTES EL ANGEL", venta: "VENTA DE ACEITE", celular: "979238876", logo: "logo15.png" },
        { nombre: "CAMPOS", venta: "MANGUERAS, CONECTORES", celular: "978945599", logo: "logo16.png" },
        { nombre: "PRODUCTOS INDUSTRIALES", venta: "NIPLES, MANGUERAS HIDRAULICAS", celular: "979739422", logo: "logo17.png" },
        { nombre: "SEMPARCO", venta: "MANGUERAS HIDRAULICAS, NIPLES", celular: "961901678", logo: "logo18.png" },
        { nombre: "STROBBE (JESUS GUILLEN)", venta: "MANGUERAS HIDRAULICAS, NIPLES (POR MAYOR)", celular: "994132151", logo: "logo19.png" },
        { nombre: "AMSEQ DE LA VICTORIA CHOSICA", venta: "PLANCHAS DE FIERRO", celular: "987891674", logo: "logo20.png" },
        { nombre: "AMSEQ DE LEGUIA", venta: "TUBOS, FIERRO", celular: "947202162", logo: "logo21.png" },
        { nombre: "METALES RUIZ", venta: "SERVICIO DE DOBLEZ, METALES", celular: "943204835", logo: "logo22.png" },
        { nombre: "SR CURO", venta: "TORNO VECINO", celular: "994147737", logo: "logo23.png" },
        { nombre: "WILSNORTH", venta: "FIERRO, BRONCE, Y NAYLOM", celular: "994098230", logo: "logo24.png" },
        { nombre: "BRONCE AV CORNEJO", venta: "FIERRO, BRONCE, Y NAYLOM", celular: "979867313", logo: "logo25.png" },
        { nombre: "DAMIAN", venta: "SERVICIO DE DOBLEZ, METALES", celular: "968598883", logo: "logo26.png" },
        { nombre: "MAYLO", venta: "VENTA DE RODAJES Y RETENES", celular: "979609552", logo: "logo27.png" }
            ]
        };
        function showList(ciudad) {
            const container = document.getElementById("proveedoresContainer");
            container.innerHTML = "";
            proveedores[ciudad].forEach(proveedor => {
      const card = `<div class="card">
          <img src="${proveedor.logo}" class="logo" alt="Logo">
          <h3>${proveedor.nombre}</h3>
          <p>${proveedor.venta}</p>
          <div class="contact-icons">
              <!-- Ícono de llamada mejorado -->
              <a href="tel:${proveedor.celular}" class="phone" title="Llamar">
                  <svg viewBox="0 0 24 24">
                      <path d="M6.6 10.8C8.4 14.4 10.8 16.8 14.4 18.6L16.8 16.2C17.1 15.9 17.4 15.9 17.7 16.2L21 18C21.3 18.3 21.6 18.6 21.6 19.2V22.2C21.6 22.5 21.3 22.8 21 22.8C16.8 22.8 3 9 3 4.8C3 4.5 3.3 4.2 3.6 4.2H6.6C7.2 4.2 7.5 4.5 7.8 4.8L9.6 8.1C9.9 8.4 9.9 8.7 9.6 9L6.6 10.8Z"/>
                  </svg>
              </a>
              
              <!-- Ícono de SMS mejorado -->
              <a href="sms:${proveedor.celular}" class="sms" title="Mensaje">
                  <svg viewBox="0 0 24 24">
                      <path d="M3 4v12h4v4l4-4h10V4H3zm14 5h-8v-2h8v2zm0 4h-8v-2h8v2z"/>
                  </svg>
              </a>
              
              <!-- Ícono de WhatsApp mejorado -->
              <a href="https://wa.me/${proveedor.celular}" class="whatsapp" target="_blank" title="WhatsApp">
                  <svg viewBox="0 0 24 24">
                      <path d="M12 1C6.48 1 2 5.48 2 11c0 2.13.63 4.11 1.82 5.81L2 22l5.36-1.53C9 21.27 10.45 22 12 22c5.52 0 10-4.48 10-10S17.52 1 12 1zm0 18c-1.43 0-2.82-.39-4.02-1.12l-.29-.17-3.18.91 1.04-3.08-.18-.29C4.39 14.82 4 13.43 4 12c0-4.41 3.59-8 8-8s8 3.59 8 8-3.59 8-8 8zm3.79-5.37c-.22-.11-1.31-.65-1.52-.72-.2-.07-.34-.11-.48.11s-.55.72-.68.87c-.12.15-.25.17-.47.06-.22-.11-.93-.34-1.77-1.06-.66-.58-1.11-1.3-1.24-1.52s-.01-.34.1-.45c.1-.1.22-.26.34-.39.11-.13.15-.22.22-.37.07-.15.04-.28-.02-.39s-.48-1.15-.66-1.57c-.17-.41-.35-.35-.48-.36-.12 0-.26-.01-.4-.01s-.37.05-.56.28c-.18.22-.72.71-.72 1.74s.74 2.02.85 2.17c.11.15 1.46 2.3 3.54 3.23 1.31.58 1.82.63 2.47.54.4-.06 1.31-.54 1.5-1.06.19-.52.19-.96.14-1.06-.05-.1-.2-.15-.42-.26z"/>
                  </svg>
              </a>
          </div>
      </div>`;
      container.innerHTML += card;
  });
        }
        function searchList() {
            const input = document.getElementById("searchInput").value.toLowerCase();
            const cards = document.querySelectorAll(".card");
            cards.forEach(card => {
                const text = card.textContent.toLowerCase();
                card.style.display = text.includes(input) ? "block" : "none";
            });
        }
        
    </script>
</body>
</html>
