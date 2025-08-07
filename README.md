# Sweet-Bite
Sweet and Delicious
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mi Sitio Web con Menú</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    nav {
      background: #333;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 60px;
    }
    nav ul {
      list-style: none;
      padding: 0;
      margin: 0;
      display: flex;
    }
    nav ul li {
      margin: 0 15px;
    }
    nav ul li a {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.2s;
    }
    nav ul li a:hover {
      color: #f0c040;
    }
    @media (max-width: 600px) {
      nav ul {
        flex-direction: column;
        background: #333;
        position: absolute;
        top: 60px;
        left: 0;
        width: 100%;
        display: none;
      }
      nav ul.open {
        display: flex;
      }
      .menu-toggle {
        display: block;
        cursor: pointer;
        padding: 0 20px;
      }
    }
    .menu-toggle {
      display: none;
      color: #fff;
      font-size: 2em;
    }
  </style>
</head>
<body>
  <nav>
    <span class="menu-toggle">&#9776;</span>
    <ul>
      <li><a href="#inicio">Inicio</a></li>
      <li><a href="#acerca">Acerca de</a></li>
      <li><a href="#servicios">Servicios</a></li>
      <li><a href="#contacto">Contacto</a></li>
    </ul>
  </nav>

  <script>
    const toggle = document.querySelector('.menu-toggle');
    const menu = document.querySelector('nav ul');
    toggle.addEventListener('click', () => {
      menu.classList.toggle('open');
    });
  </script>
</body>
</html>
