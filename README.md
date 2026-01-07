<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Dr. Francisco Arizaga Luque</title>
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

/* ===== HEADER ===== */
.main-header {
  background: linear-gradient(135deg, #1e3c72, #2a5298);
  width: 100%;
}

.header-inner {
  max-width: 1000px;
  margin: 0 auto;
  padding: 90px 20px;
  text-align: center;
  color: white;
}

.header-inner h1 {
  margin: 0;
  font-size: 38px;
}

.header-inner p {
  margin-top: 15px;
  font-size: 18px;
  opacity: 0.95;
}

/* ===== NAV ===== */
nav {
  background-color: #ffffff;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  padding: 12px;
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

/* ===== CONTENIDO ===== */
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
}

.btn:hover {
  background-color: #1e3c72;
}

/* ===== FOOTER ===== */
footer {
  background-color: #1e3c72;
  color: white;
  text-align: center;
  padding: 15px;
  margin-top: 30px;
  font-size: 14px;
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

  <header class="main-header">
  <div class="header-inner">
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
        <a href="https://forms.gle/6Ecq7oBXtpY7nQwr7" 
   class="btn" 
   target="_blank">
   Enviar tarea
</a>
      </div>

    </div>
  </div>

  <footer>
    © 2026 · Clases asistidas – Matemáticas | Plataforma educativa
  </footer>

</body>
</html>
