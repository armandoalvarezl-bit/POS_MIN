<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Formulario de Registro</title>
  <!-- Bootstrap 5 CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body { background:#f7f9fc; }
    .required::after { content: " *"; color: #d00; }
  </style>
</head>
<body>
  <div class="container py-5">
    <div class="row justify-content-center">
      <div class="col-lg-8">
        <div class="card shadow-sm">
          <div class="card-body">
            <h3 class="card-title mb-4">Formulario de Registro</h3>

            <form id="registroForm" novalidate>
              <div class="row g-3">
                <div class="col-md-6">
                  <label for="nombre" class="form-label required">Nombre</label>
                  <input type="text" class="form-control" id="nombre" name="nombre" required>
                  <div class="invalid-feedback">Por favor ingresa el nombre.</div>
                </div>

                <div class="col-md-6">
                  <label for="apellido" class="form-label required">Apellido</label>
                  <input type="text" class="form-control" id="apellido" name="apellido" required>
                  <div class="invalid-feedback">Por favor ingresa el apellido.</div>
                </div>

                <div class="col-md-6">
                  <label for="cedula" class="form-label required">Cédula</label>
                  <input type="text" class="form-control" id="cedula" name="cedula" pattern="\d{6,15}" required>
                  <div class="form-text">Sólo números (6–15 dígitos).</div>
                  <div class="invalid-feedback">Cédula inválida. Solo números (6–15 dígitos).</div>
                </div>

                <div class="col-md-6">
                  <label for="telefono" class="form-label required">Teléfono</label>
                  <input type="tel" class="form-control" id="telefono" name="telefono" pattern="[0-9+()\-\s]{7,20}" required>
                  <div class="form-text">Ej: +57 300 1234567</div>
                  <div class="invalid-feedback">Teléfono inválido.</div>
                </div>

                <div class="col-md-6">
                  <label for="correo" class="form-label required">Correo electrónico</label>
                  <input type="email" class="form-control" id="correo" name="correo" required>
                  <div class="invalid-feedback">Correo inválido.</div>
                </div>

                <div class="col-md-6">
                  <label for="grado" class="form-label required">Grado de estudio</label>
                  <select id="grado" name="grado" class="form-select" required>
                    <option value="">-- Selecciona --</option>
                    <option>Primaria</option>
                    <option>Bachillerato</option>
                    <option>Técnico / Tecnólogo</option>
                    <option>Profesional</option>
                    <option>Especialización</option>
                    <option>Maestría</option>
                    <option>Doctorado</option>
                  </select>
                  <div class="invalid-feedback">Selecciona el grado de estudio.</div>
                </div>

                <div class="col-12">
                  <label for="direccion" class="form-label required">Dirección</label>
                  <input type="text" class="form-control" id="direccion" name="direccion" required>
                  <div class="invalid-feedback">Por favor ingresa la dirección.</div>
                </div>

                <div class="col-md-6">
                  <label for="sector" class="form-label">Sector (barrio/vereda)</label>
                  <input type="text" class="form-control" id="sector" name="sector">
                </div>

                <div class="col-md-6">
                  <label class="form-label required">Zona</label>
                  <div>
                    <div class="form-check form-check-inline">
                      <input class="form-check-input" type="radio" name="zona" id="urbano" value="Urbano" required>
                      <label class="form-check-label" for="urbano">Urbano</label>
                    </div>
                    <div class="form-check form-check-inline">
                      <input class="form-check-input" type="radio" name="zona" id="rural" value="Rural" required>
                      <label class="form-check-label" for="rural">Rural</label>
                    </div>
                  </div>
                  <div class="invalid-feedback d-block" id="zonaFeedback">Selecciona Urbano o Rural.</div>
                </div>

                <div class="col-12">
                  <label for="observaciones" class="form-label">Observaciones (opcional)</label>
                  <textarea class="form-control" id="observaciones" name="observaciones" rows="3"></textarea>
                </div>

              </div>

              <div class="mt-4 d-flex gap-2">
                <button type="submit" class="btn btn-primary" id="btnEnviar">Enviar</button>
                <button type="button" class="btn btn-outline-secondary" id="btnLimpiar">Limpiar</button>
                <button type="button" class="btn btn-outline-success ms-auto" id="btnDescargarJSON">Descargar JSON</button>
              </div>
            </form>

            <!-- Resultado -->
            <div class="mt-4" id="resultadoContainer" style="display:none;">
              <h5>Datos capturados</h5>
              <pre id="resultado" class="p-3 bg-light rounded" style="white-space:pre-wrap; max-height:300px; overflow:auto;"></pre>
            </div>

          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

  <script>
    // Helper: obtener datos del formulario
    function obtenerDatos() {
      const form = document.getElementById('registroForm');
      const fd = new FormData(form);
      const obj = {};
      for (const [key, value] of fd.entries()) {
        obj[key] = value;
      }
      return obj;
    }

    // Validación personalizada y envío
    (function(){
      const form = document.getElementById('registroForm');
      const resultadoContainer = document.getElementById('resultadoContainer');
      const resultadoPre = document.getElementById('resultado');
      const btnDescargarJSON = document.getElementById('btnDescargarJSON');
      const btnLimpiar = document.getElementById('btnLimpiar');
      const zonaFeedback = document.getElementById('zonaFeedback');

      // Previene envío por defecto, valida y muestra datos
      form.addEventListener('submit', function(e){
        e.preventDefault();
        e.stopPropagation();

        // HTML5 validity
        if (!form.checkValidity()) {
          form.classList.add('was-validated');
          // show zone feedback if missing
          const zonas = form.querySelectorAll('input[name="zona"]');
          let zonaSeleccionada = false;
          zonas.forEach(z => { if (z.checked) zonaSeleccionada = true; });
          zonaFeedback.style.display = zonaSeleccionada ? 'none' : 'block';
          return;
        }

        // Zona extra check
        const zonas = form.querySelectorAll('input[name="zona"]');
        let zonaSeleccionada = false;
        zonas.forEach(z => { if (z.checked) zonaSeleccionada = true; });
        zonaFeedback.style.display = zonaSeleccionada ? 'none' : 'block';
        if (!zonaSeleccionada) return;

        // Si pasa validación, obtener datos
        const datos = obtenerDatos();
        resultadoPre.textContent = JSON.stringify(datos, null, 2);
        resultadoContainer.style.display = 'block';

        // Aquí podrías hacer fetch() a tu servidor para guardar en DB
        // fetch('/guardar', {method:'POST', body: JSON.stringify(datos), headers:{'Content-Type':'application/json'}})

        // Feedback visual
        const btn = document.getElementById('btnEnviar');
        btn.disabled = true;
        btn.textContent = 'Enviando...';
        setTimeout(()=>{ btn.disabled = false; btn.textContent = 'Enviar'; }, 800);
      });

      // Limpiar formulario
      btnLimpiar.addEventListener('click', ()=>{
        form.reset();
        form.classList.remove('was-validated');
        resultadoContainer.style.display = 'none';
      });

      // Descargar JSON
      btnDescargarJSON.addEventListener('click', ()=>{
        const datos = obtenerDatos();
        const dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(datos, null, 2));
        const dlAnchor = document.createElement('a');
        dlAnchor.setAttribute('href', dataStr);
        const ced = datos.cedula || 'registro';
        dlAnchor.setAttribute('download', `registro-${ced}.json`);
        dlAnchor.click();
      });

    })();
  </script>
</body>
</html>
