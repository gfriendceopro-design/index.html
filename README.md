<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Clases asistidas - Matemáticas</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', Arial, sans-serif;
      background-color: #f2f4f8;
      color: #333;
    }

    header {
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      color: white;
      padding: 30px 20px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 28px;
    }

    header p {
      margin-top: 10px;
      font-size: 16px;
      opacity: 0.9;
    }

    nav {
      background-color: #ffffff;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      padding: 10px;
      text-align: center;
    }

    nav a {
      margin: 0 15px;
      text-decoration: none;
      color: #2a5298;
      font-weight: 600;
    }

    nav a:hover {
      text-decoration: underline;
    }

    .container {
      max-width: 1000px;
      margin: auto;
      padding: 20px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
    }

    .card {
      background: white;
      border-radius: 10px;
      padding: 25px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      transition: transform 0.2s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card h2 {
      margin-top: 0;
      color: #1e3c72;
    }

    .card p {
      line-height: 1.5;
    }

    .btn {
      display: inline-block;
      margin-top: 15px;
      padding: 12px 20px;
      background-color: #2a5298;
      color: white;
      text-decoration: none;
      border-radius: 6px;
      font-weight: bold;
      text-align: center;
    }

    .btn:hover {
      background-color: #1e3c72;
    }

    footer {
      background-color: #1e3c72;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 30px;
      font-size: 14px;
    }
    .header-content {
  max-width: 1000px;
  margin: auto;
    }
  </style>
  <script>
  function accesoProfesor() {
    const clave = prompt("Ingrese la contraseña del profesor:");

    if (clave === "profesor2026") {
      document.getElementById("profesor").style.display = "block";
      location.hash = "#profesor";
    } else {
      alert("Acceso denegado");
    }
  }
</script>
</head>

<body>

  <header>
  <div class="container header-content">
    <h1>Clases asistidas - Matemáticas</h1>
    <p>Plataforma educativa para la gestión y envío de tareas</p>
  </div>
</header>
  <nav>
  <a href="#inicio">Inicio</a>
  <a href="#" onclick="accesoProfesor()">Acceso Profesor</a>
  <a href="#estudiante">Estudiante</a>
</nav>

  <div class="container" id="inicio">
    <div class="cards">

      <div class="card" id="profesor" style="display:none;">
        <h2>👨‍🏫 Área del Profesor</h2>
        <p>
          En esta sección el docente podrá publicar tareas,
          guías de estudio y actividades para los estudiantes
          de los cursos A y B.
        </p>
        <a href="#" class="btn" onclick="accesoProfesor()">Acceder como profesor</a>
      </div>

      <div class="card" id="estudiante">
        <h2>👩‍🎓 Área del Estudiante</h2>
        <p>
          Aquí los estudiantes podrán enviar sus tareas,
          trabajos y actividades asignadas por el profesor
          de manera organizada.
        </p>
        <a href="#" class="btn">Enviar tareas</a>
      </div>

    </div>
  </div>

  <footer>
    © 2026 · Clases asistidas – Matemáticas | Plataforma educativa
  </footer>

</body>
</html>
