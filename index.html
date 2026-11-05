<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Friocosta SAS — Autorizaciones</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@2.44.0/tabler-icons.min.css" />
  
  <script src="https://unpkg.com/pdf-lib@1.17.1/dist/pdf-lib.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/mammoth/1.6.0/mammoth.browser.min.js"></script>

  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      background: #e8edf5;
      min-height: 100vh;
      padding: 2rem 1rem;
      color: #1a1a1a;
    }

    .container { max-width: 900px; margin: 0 auto; }

    /* ── HEADER ── */
    .header {
      background: linear-gradient(135deg, #1433b8 0%, #1a3ec7 60%, #2752d4 100%);
      border-radius: 16px;
      padding: 1rem 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 1.5rem;
      box-shadow: 0 6px 24px rgba(20,51,184,0.35);
    }

    .header-logo {
      background: white;
      padding: 4px 12px;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .header-logo img {
      height: 48px;
      display: block;
    }

    .header-info { text-align: right; }
    .header-info .titulo { color: white; font-size: 20px; font-weight: 700; letter-spacing: 0.5px; text-shadow: 0 1px 3px rgba(0,0,0,0.3); }
    .header-info .subtitulo { color: rgba(255,255,255,0.75); font-size: 12px; margin-top: 2px; }

    /* ── ACCIONES ── */
    .acciones { display: flex; gap: 10px; margin-bottom: 0.75rem; }

    .btn-agregar {
      flex: 1; padding: 11px 16px; background: white;
      border: 2px solid #1a3ec7; color: #1a3ec7;
      border-radius: 10px; font-size: 14px; font-weight: 500;
      cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 7px;
      transition: all 0.15s; box-shadow: 0 2px 8px rgba(26,62,199,0.1);
    }
    .btn-agregar:hover { background: #1a3ec7; color: white; box-shadow: 0 4px 14px rgba(26,62,199,0.3); }
    .btn-agregar:disabled { border-color: #ccc; color: #aaa; cursor: not-allowed; background: white; box-shadow: none; }

    .btn-eliminar-todo {
      flex: 1; padding: 11px 16px; background: white;
      border: 2px solid #e24b4a; color: #e24b4a;
      border-radius: 10px; font-size: 14px; font-weight: 500;
      cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 7px;
      transition: all 0.15s; box-shadow: 0 2px 8px rgba(226,75,74,0.1);
    }
    .btn-eliminar-todo:hover { background: #e24b4a; color: white; box-shadow: 0 4px 14px rgba(226,75,74,0.3); }

    /* ── CONFIRM BAR ── */
    .confirm-bar {
      background: #fff0f0; border: 1.5px solid #f09595;
      border-radius: 10px; padding: 12px 16px;
      display: none; align-items: center; justify-content: space-between;
      margin-bottom: 1rem; gap: 10px; flex-wrap: wrap;
    }
    .confirm-bar span { font-size: 13px; color: #a32d2d; font-weight: 500; }
    .confirm-btns { display: flex; gap: 8px; }
    .btn-si { background: #e24b4a; color: white; border: none; padding: 7px 18px; border-radius: 8px; font-size: 13px; cursor: pointer; font-weight: 500; }
    .btn-si:hover { background: #a32d2d; }
    .btn-no { background: white; color: #555; border: 1px solid #ccc; padding: 7px 18px; border-radius: 8px; font-size: 13px; cursor: pointer; }
    .btn-no:hover { background: #f0f0f0; }

    /* ── CONTADOR ── */
    .contador { font-size: 12px; color: #5566aa; text-align: center; margin-bottom: 14px; font-weight: 500; letter-spacing: 0.3px; }

    /* ── CARDS ── */
    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
      margin-bottom: 1.5rem;
    }
    @media (max-width: 768px) { .cards { grid-template-columns: repeat(2, 1fr); } }
    @media (max-width: 480px) { .cards { grid-template-columns: 1fr; } }

    .card {
      background: white; border: 1.5px solid #dde5f5; border-radius: 14px;
      padding: 1rem; display: flex; flex-direction: column; gap: 10px;
      box-shadow: 0 2px 10px rgba(26,62,199,0.07); transition: transform 0.15s, box-shadow 0.2s;
      position: relative;
    }
    .card:hover { box-shadow: 0 4px 18px rgba(26,62,199,0.14); }
    
    .card.dragging {
      opacity: 0.5;
      transform: scale(0.98);
      border-color: #1a3ec7;
      background: #f4f7fe;
    }
    .card.drag-over {
      border: 2px dashed #1a3ec7;
      box-shadow: 0 0 12px rgba(26,62,199,0.2);
    }
    
    .card-label {
      font-size: 12px; font-weight: 700; color: #1a3ec7;
      text-transform: uppercase; letter-spacing: 0.8px;
      display: flex; align-items: center; justify-content: flex-start; gap: 8px;
      cursor: grab;
      user-select: none;
    }
    .card-label:active { cursor: grabbing; }
    .card-label i.ti-arrows-move { color: #8fa8e0; font-size: 14px; }

    .card-header-right {
      margin-left: auto;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .badge-ok {
      background: #e6f4d7; color: #3b6d11; font-size: 11px;
      padding: 2px 9px; border-radius: 20px;
      display: flex; align-items: center; gap: 3px; font-weight: 600;
    }

    .btn-eliminar-card {
      background: none; border: none; color: #f09595; cursor: pointer;
      padding: 2px; display: flex; align-items: center; justify-content: center;
      border-radius: 4px; transition: all 0.15s;
    }
    .btn-eliminar-card:hover { color: #e24b4a; background: #fff0f0; }

    .upload-wrap { position: relative; }

    .upload-box {
      border: 2px dashed #b0bfe8; border-radius: 10px;
      min-height: 140px; display: flex; align-items: center; justify-content: center;
      cursor: pointer; position: relative; overflow: hidden;
      background: #f4f7fe; transition: all 0.2s;
    }
    .upload-box:hover { border-color: #1a3ec7; background: #eaf0ff; }
    .upload-box input[type=file] { position: absolute; inset: 0; opacity: 0; cursor: pointer; width: 100%; height: 100%; z-index: 5; }
    
    /* Cursor de lupa sobre las vistas previas cargadas */
    .upload-box img { max-width: 100%; max-height: 140px; display: block; border-radius: 6px; object-fit: contain; cursor: zoom-in; }
    .upload-box .pdf-clickable-cover { position: absolute; inset: 0; z-index: 6; cursor: zoom-in; background: transparent; }
    .upload-box iframe { width: 100%; height: 140px; border: none; border-radius: 6px; pointer-events: none; }

    .file-box { background: #f4f7fe; }
    .file-preview {
      display: flex; flex-direction: column; align-items: center; gap: 8px;
      padding: 16px 10px; pointer-events: none; width: 100%;
    }
    .file-name {
      font-size: 11px; color: #444; font-weight: 500;
      text-align: center; word-break: break-all;
      max-width: 100%; line-height: 1.3;
    }

    .placeholder { display: flex; flex-direction: column; align-items: center; gap: 7px; pointer-events: none; }
    .placeholder i { font-size: 28px; color: #8fa8e0; }
    .placeholder span { font-size: 12px; color: #8fa8e0; font-weight: 500; }

    .btn-x {
      position: absolute; top: 6px; right: 6px;
      width: 26px; height: 26px; border-radius: 50%;
      background: #e24b4a; border: none; color: white; font-size: 13px; cursor: pointer;
      display: flex; align-items: center; justify-content: center;
      z-index: 10; transition: background 0.15s; box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }
    .btn-x:hover { background: #a32d2d; }

    .nombre-inp {
      border: 1.5px solid #dde5f5; border-radius: 8px;
      padding: 8px 11px; font-size: 13px;
      background: #f4f7fe; color: #1a1a1a;
      outline: none; width: 100%; font-family: inherit;
    }
    .nombre-inp:focus { border-color: #1a3ec7; background: white; box-shadow: 0 0 0 3px rgba(26,62,199,0.12); }

    .comentario-inp {
      border: 1.5px solid #dde5f5; border-radius: 8px;
      padding: 8px 11px; font-size: 12px;
      background: #f4f7fe; color: #1a1a1a;
      outline: none; width: 100%; font-family: inherit;
      resize: vertical; min-height: 56px;
    }
    .comentario-inp:focus { border-color: #1a3ec7; background: white; box-shadow: 0 0 0 3px rgba(26,62,199,0.12); }
    .campo-lbl { font-size: 11px; font-weight: 600; color: #5566aa; letter-spacing: 0.4px; margin-bottom: 3px; display: block; }

    /* ── SECCIONES DE CONFIGURACIÓN GENERAL ── */
    .ubicacion-wrap {
      background: white; border: 1.5px solid #dde5f5; border-radius: 14px;
      padding: 1rem 1.25rem; margin-bottom: 1rem;
      box-shadow: 0 2px 10px rgba(26,62,199,0.07);
    }
    .ubicacion-wrap label {
      display: flex; align-items: center; gap: 7px;
      font-size: 13px; font-weight: 600; color: #1a3ec7;
      text-transform: uppercase; letter-spacing: 0.6px; margin-bottom: 8px;
    }
    .ubicacion-wrap input {
      width: 100%; border: 1.5px solid #b0bfe8; border-radius: 8px;
      padding: 10px 13px; font-size: 14px;
      background: #f4f7fe; color: #1a1a1a; outline: none; font-family: inherit;
    }
    .ubicacion-wrap input:focus { border-color: #1a3ec7; background: white; box-shadow: 0 0 0 3px rgba(26,62,199,0.1); }

    .nombre-archivo-wrap {
      background: white; border: 1.5px solid #dde5f5; border-radius: 14px;
      padding: 1rem 1.25rem; margin-bottom: 1rem;
      box-shadow: 0 2px 10px rgba(26,62,199,0.07);
    }
    .nombre-archivo-wrap label {
      display: flex;
      align-items: center; gap: 7px;
      font-size: 13px; font-weight: 600; color: #1a3ec7;
      text-transform: uppercase; letter-spacing: 0.6px; margin-bottom: 8px;
    }
    .nombre-archivo-row { display: flex; align-items: center; gap: 0; }
    .nombre-archivo-row input {
      flex: 1; border: 1.5px solid #b0bfe8; border-right: none;
      border-radius: 8px 0 0 8px; padding: 10px 13px; font-size: 14px;
      background: #f4f7fe; color: #1a1a1a; outline: none; font-family: inherit;
    }
    .nombre-archivo-row input:focus { border-color: #1a3ec7; background: white; box-shadow: 0 0 0 3px rgba(26,62,199,0.1); }
    .nombre-archivo-row .ext {
      background: #1a3ec7; color: white; padding: 10px 14px; font-size: 14px;
      font-weight: 600; border-radius: 0 8px 8px 0; border: 1.5px solid #1a3ec7; user-select: none;
    }

    /* ── BOTÓN PDF ── */
    .btn-pdf {
      width: 100%; padding: 15px;
      background: linear-gradient(135deg, #1433b8, #2752d4);
      color: white; border: none; border-radius: 12px;
      font-size: 16px; font-weight: 600; cursor: pointer;
      display: flex; align-items: center; justify-content: center; gap: 9px;
      transition: all 0.2s; box-shadow: 0 4px 16px rgba(26,62,199,0.35);
      letter-spacing: 0.3px;
    }
    .btn-pdf:hover { background: linear-gradient(135deg, #0f27a0, #1a3ec7); box-shadow: 0 6px 22px rgba(26,62,199,0.45); transform: translateY(-1px); }
    .btn-pdf:disabled { background: #ccc; color: #999; cursor: not-allowed; box-shadow: none; transform: none; }

    .msg { font-size: 13px; color: #888; text-align: center; margin-top: 12px; font-weight: 500; }
    .msg.ok { color: #3b6d11; }
    .msg.error { color: #a32d2d; }

    /* ── MODAL DE PREVISUALIZACIÓN EN GRANDE (LIGHTBOX) ── */
    .preview-modal {
      position: fixed; inset: 0; background: rgba(10, 18, 50, 0.85);
      z-index: 9999; display: none; align-items: center; justify-content: center;
      padding: 20px; backdrop-filter: blur(5px); animation: fadeIn 0.2s ease-out;
    }
    .preview-content-wrapper {
      position: relative; max-width: 90%; max-height: 90vh;
      display: flex; flex-direction: column; align-items: center; gap: 10px;
    }
    .preview-modal img {
      max-width: 100%; max-height: 80vh; border-radius: 8px;
      box-shadow: 0 12px 40px rgba(0,0,0,0.5); object-fit: contain;
    }
    .preview-modal iframe {
      width: 80vw; height: 80vh; background: white; border-radius: 8px;
      box-shadow: 0 12px 40px rgba(0,0,0,0.5); border: none;
    }
    .btn-close-modal {
      position: absolute; top: -45px; right: 0; background: #e24b4a;
      color: white; border: none; border-radius: 50%; width: 36px; height: 36px;
      font-size: 18px; cursor: pointer; display: flex; align-items: center; justify-content: center;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3); transition: background 0.15s;
    }
    .btn-close-modal:hover { background: #a32d2d; }
    .modal-caption { color: white; font-size: 14px; font-weight: 500; text-shadow: 0 2px 4px rgba(0,0,0,0.5); }
    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
  </style>
</head>
<body>
  <div class="container">

    <div class="header">
      <div class="header-logo">
        <img src="img/FRIOCOSTA LOGO.png"/>
      </div>
      <div class="header-info">
        <div class="titulo">Autorizaciones</div>
        <div class="subtitulo">Departamento TIC</div>
      </div>
    </div>

    <div class="acciones">
      <button class="btn-agregar" id="btn-add" onclick="agregar()">
        <i class="ti ti-plus"></i> Agregar autorizado
      </button>
      <button class="btn-eliminar-todo" onclick="pedirConfirmacion()">
        <i class="ti ti-trash"></i> Eliminar todo
      </button>
    </div>

    <div class="confirm-bar" id="confirm-bar">
      <span><i class="ti ti-alert-triangle"></i> ¿Eliminar todas las autorizaciones?</span>
      <div class="confirm-btns">
        <button class="btn-no" onclick="cancelar()">Cancelar</button>
        <button class="btn-si" onclick="eliminarTodo()">Sí, eliminar</button>
      </div>
    </div>

    <div class="contador" id="contador">2 de 40 autorizados</div>
    <div class="cards" id="cards"></div>

    <div class="ubicacion-wrap">
      <label for="ubicacion">
        <i class="ti ti-map-pin" style="font-size:16px;"></i> Ubicación
      </label>
      <input type="text" id="ubicacion" placeholder="Ej: Sede principal, Montería — Piso 2" />
    </div>

    <div class="nombre-archivo-wrap">
      <label for="nombre-archivo">
        <i class="ti ti-file-text" style="font-size:16px;"></i> Nombre del archivo PDF
      </label>
      <div class="nombre-archivo-row">
        <input type="text" id="nombre-archivo" placeholder="Ej: autorizacion_computador_juan" value="autorizaciones_friocosta" />
        <span class="ext">.pdf</span>
      </div>
    </div>

    <div class="ubicacion-wrap">
      <label for="observacion">
        <i class="ti ti-message-dots" style="font-size:16px;"></i> Observación general
      </label>
      <textarea id="observacion" rows="3" placeholder="Escribe aquí cualquier observación general para el documento..." style="width:100%; border:1.5px solid #b0bfe8; border-radius:8px; padding:10px 13px; font-size:14px; background:#f4f7fe; color:#1a1a1a; outline:none; font-family:inherit; resize:vertical;"></textarea>
    </div>

    <button class="btn-pdf" id="btn-gen" onclick="generarPDF()">
      <i class="ti ti-file-download"></i> Generar PDF
    </button>
    <div class="msg" id="msg"></div>

  </div>

  <div class="preview-modal" id="preview-modal" onclick="cerrarPrevisualizacion()">
    <div class="preview-content-wrapper" onclick="event.stopPropagation()">
      <button class="btn-close-modal" onclick="cerrarPrevisualizacion()"><i class="ti ti-x"></i></button>
      <div id="modal-media-container"></div>
      <div class="modal-caption" id="modal-caption"></div>
    </div>
  </div>

  <script>
    const LOGO_DATA_URL = "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/4gHYSUNDX1BST0ZJTEUAAQEAAAHIAAAAAAQwAABtbnRyUkdCIFhZWiAH4AABAAEAAAAAAABhY3NwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQAA9tYAAQAAAADTLQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAlkZXNjAAAA8AAAACRyWFlaAAABFAAAABRnWFlaAAABKAAAABRiWFlaAAABPAAAABR3dHB0AAABUAAAABRyVFJDAAABZAAAAChnVFJDAAABZAAAAChjcHJ0AAABjAAAADxtbHVjAAAAAAAAAAEAAAAMZW5VUwAAAAgAAAAcAHMAUgBHAEJYWVogAAAAAAAAb6IAADj1AAADkFhZWiAAAAAAAABimQAAt4UAABjaWFlaIAAAAAAAACSgAAAPhAAAts9YWVogAAAAAAAA9tYAAQAAAADTLXBhcmEAAAAAAAQAAAACZmYAAPKnAAANWQAAE9AAAApbAAAAAAAAAABtbHVjAAAAAAAAAAEAAAAMZW5VUwAAACAAAAAcAEcAbwBvAGcAbABlACAASQBuAGMALgAgADIAMAAxADb/2wBDAAgGBgcGBQgHBwcJCQgKDBQNDAsLDBkSEw8UHRofHh0aHBwgJC4nICIsIxwcKDcpLDAxNDQ0Hyc5PTgyPC4zNDL/2wBDAQkJCQwLDBgNDRgyIRwhMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjL/wAARCAGQAZADASIAAhEBAxEB/8QAHQABAAICAwEBAAAAAAAAAAAAAAQGBQgBAwcJAv/EAEYQAAEDAgMCDAQEAwYEBwAAAAABAgMEBQYHERLSCBMUFyExQVFVVpKkImGBoUJScZEWMnIJIySCscEnlKLRMzRDU2Kywv/EABsBAQACAwEBAAAAAAAAAAAAAAABBQIDBAYH/QANREAAgECAwcCBAUEAwEAAAAAAAECAxEEFJEFEiExUVJTE0EyYXHwIoGhsdEGM8HhFRYjQv/aAAwPLOAD0FeYwF6yYy3uuZGJ226k2qegh0fW1at1SJncne5exCl0FLPXVsFHTRuknnkbHGxqaq5yroiH0OyXwNR4AwLR2eFjVq3NSWtlROmSVU6enuTqQqNr7QydK0fifL+TrwWG9afHkjLYFwhYcF2KKz2GiZTwRp8TtNXyO7XOXtVTPgrWOsdYWwTQ8rxFdYaRFTVkWu1JJ/S1OlTwtqlafu29T0H4YR6JHlvDBx9fcIYctVuw/WyUFTc5X8ZURLpI2NiJqjV7FVXJ0p3GqvOJj3znf/8An5P+5dOEtmjbMy7za3WelqoKS3RytR06IiyK9W9KInUmje0qGX1dgKlWWPGlmutcj3pxctFUNZxbe3VFTpPb7Owiw+EW/TvL34K/P+ChxNZ1az3ZcDq5xMe+cr//AM/J/By8ZHZrY6pMyrHQ1V+uN1obhWxUlRTVUzpkVsjkbtJta6Kmuuqd3ceo5eZZZBY7g2rBW3GSdqavppKrYlb/lVp6lgXJTAGDbwy8Wq1yS10WvEzVMqyLEqppq1OhEX56anHjNp4NQlTlSd7cmkjdRwldyUlLh9SjcI/IyjxLRVGKMKUsdNfImrJPTsTZZWInX0dj+5e3qXsVNN5Y5IpXxSscyRjla5rk0Vqp1oqH1HNOeGPl5FYsQw4vtcCMo7m7ZqmtToZN3/5v9TTsLacnLL1H9P4/gz2hhVb1Y/ma+AHB6wqDkHAAOQcAA5AOUa5UVURV069EAOAcHIAAcitXRyKn6gAA52XbO1ouz36dBwAActa5y6NRVX5IcdQAAAAAAAAAJAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAPXuCNh1l+zho6idiPgtcL61yKnRtJo1n/U5F+hvWancA2Bjr1impVE22U8DEX5Oc9V/+qG2J4Tb9Rzxji/ZJf5/yX+zopUU+pQc8sxaTLnB0lycjZbjUKsVDAv436da/JOtTQjFOILvia8z3e91stXVzOVXOeuunyROxPkeo8L3E017zYqLakirS2mNKdjNehH9b1/dSrZE5fyZjY9gs0kj4bdCxaivlZ/M2JFRNlv/CnKqIndqq9Omhe7Kw1LBYX16nNq7fy6Ffi6s69b048uRQzukpKuOljqpKWdlPIqpHK6NUY9U69F6lLfnpRWq2Zr3212SkipLfRSsp4Yo+puxGxrv1VXIqqq7KdJ0e8w=";

    document.addEventListener("DOMContentLoaded", () => {
      const logoEl = document.getElementById("img-logo-institucional");
      if (logoEl) logoEl.src = LOGO_DATA_URL;
    });

    let data = [
      { id: 1, img: null, nombre: '', comentario: '', fileData: null, fileType: null, fileName: null, rawBuffer: null },
      { id: 2, img: null, nombre: '', comentario: '', fileData: null, fileType: null, fileName: null, rawBuffer: null }
    ];
    let nextId = 3;
    let draggedIndex = null;

    function agregar() {
      if (data.length >= 40) return;
      data.push({ id: nextId++, img: null, nombre: '', comentario: '', fileData: null, fileType: null, fileName: null, rawBuffer: null });
      render();
    }

    function eliminarIndividual(index) {
      data.splice(index, 1);
      render();
    }

    function pedirConfirmacion() {
      document.getElementById('confirm-bar').style.display = 'flex';
    }

    function cancelar() {
      document.getElementById('confirm-bar').style.display = 'none';
    }

    function eliminarTodo() {
      data = [
        { id: 1, img: null, nombre: '', comentario: '', fileData: null, fileType: null, fileName: null, rawBuffer: null },
        { id: 2, img: null, nombre: '', comentario: '', fileData: null, fileType: null, fileName: null, rawBuffer: null }
      ];
      nextId = 3;
      document.getElementById('confirm-bar').style.display = 'none';
      setMsg('', '');
      render();
    }

    // ── FUNCIONES DRAG & DROP ──
    function handleDragStart(index) {
      draggedIndex = index;
      document.querySelectorAll('.card')[index].classList.add('dragging');
    }

    function handleDragOver(e, index) {
      e.preventDefault();
      if (draggedIndex === index) return;
      document.querySelectorAll('.card')[index].classList.add('drag-over');
    }

    function handleDragLeave(index) {
      document.querySelectorAll('.card')[index].classList.remove('drag-over');
    }

    function handleDrop(index) {
      document.querySelectorAll('.card')[index].classList.remove('drag-over');
      if (draggedIndex !== null && draggedIndex !== index) {
        const [movedItem] = data.splice(draggedIndex, 1);
        data.splice(index, 0, movedItem);
        render();
      }
    }

    function handleDragEnd() {
      draggedIndex = null;
      document.querySelectorAll('.card').forEach(c => {
        c.classList.remove('dragging');
        c.classList.remove('drag-over');
      });
    }

    // ── NUEVAS FUNCIONES PARA PREVISUALIZAR EN GRANDE ──
    function abrirPrevisualizacion(index) {
      const item = data[index];
      if (!item.img && !item.fileData) return;

      const modal = document.getElementById('preview-modal');
      const mediaContainer = document.getElementById('modal-media-container');
      const caption = document.getElementById('modal-caption');

      mediaContainer.innerHTML = ''; // Limpiar previsualización anterior
      caption.textContent = item.nombre ? `Autorización: ${item.nombre}` : `Autorizado #${index + 1}`;

      if (item.img) {
        // Si es una imagen (PC o móvil), inyectamos la etiqueta img limpia
        const imgEl = document.createElement('img');
        imgEl.src = item.img;
        mediaContainer.appendChild(imgEl);
      } else if (item.fileType === 'pdf') {
        // Si es un PDF, embebemos el iframe a pantalla completa
        const iframeEl = document.createElement('iframe');
        iframeEl.src = item.fileData;
        mediaContainer.appendChild(iframeEl);
      } else if (item.fileType === 'word') {
        setMsg('Los archivos Word procesan su texto directo en el comentario.', 'ok');
        return;
      }

      modal.style.display = 'flex';
    }

    function cerrarPrevisualizacion() {
      document.getElementById('preview-modal').style.display = 'none';
    }

    function render() {
      const cont = document.getElementById('cards');
      cont.innerHTML = '';
      data.forEach((d, i) => {
        const card = document.createElement('div');
        card.className = 'card';
        
        card.draggable = true;
        card.setAttribute('ondragstart', `handleDragStart(${i})`);
        card.setAttribute('ondragover', `handleDragOver(event, ${i})`);
        card.setAttribute('ondragleave', `handleDragLeave(${i})`);
        card.setAttribute('ondrop', `handleDrop(${i})`);
        card.setAttribute('ondragend', `handleDragEnd()`);

        card.innerHTML = `
          <div class="card-label">
            <i class="ti ti-arrows-move"></i> Autorizado #${i + 1}
            <div class="card-header-right">
              ${(d.img || d.fileData) ? '<span class="badge-ok"><i class="ti ti-check" style="font-size:11px"></i> Cargado</span>' : ''}
              <button class="btn-eliminar-card" onclick="eliminarIndividual(${i})" title="Eliminar este autorizado" onmousedown="event.stopPropagation()">
                <i class="ti ti-trash" style="font-size:16px;"></i>
              </button>
            </div>
          </div>
          <div class="upload-wrap" onmousedown="event.stopPropagation()">
            <div class="upload-box${d.fileType && d.fileType !== 'image' ? ' file-box' : ''}">
              ${!d.fileData && !d.img ? `<input type="file" accept="image/*,.pdf,.doc,.docx,application/pdf" onchange="cargar(event, ${i})" />` : ''}
              ${d.img
                ? `<img src="${d.img}" alt="Autorización ${i + 1}" onclick="abrirPrevisualizacion(${i})" title="Clic para ver en grande" />`
                : d.fileType === 'pdf'
                  ? `<div class="pdf-clickable-cover" onclick="abrirPrevisualizacion(${i})" title="Clic para ver en grande"></div><iframe src="${d.fileData}#toolbar=0&navpanes=0&scrollbar=0"></iframe>`
                  : d.fileType === 'word'
                    ? `<div class="file-preview"><i class="ti ti-file-type-doc" style="font-size:48px;color:#1a3ec7;"></i><span class="file-name">${d.fileName || 'archivo.docx'}</span><span style="font-size:10px; color: #5566aa;">(Texto extraído para el informe)</span></div>`
                    : `<div class="placeholder"><i class="ti ti-upload"></i><span>Imagen, PDF o Word</span></div>`
              }
            </div>
            ${(d.img || d.fileData) ? `<button class="btn-x" onclick="limpiar(${i})" title="Quitar archivo"><i class="ti ti-x" style="font-size:13px"></i></button>` : ''}
          </div>
          <span class="campo-lbl">Nombre del autorizador</span>
          <input class="nombre-inp" type="text" placeholder="Nombre (opcional)"
            value="${d.nombre || ''}" oninput="data[${i}].nombre = this.value" onmousedown="event.stopPropagation()" />
          <span class="campo-lbl">Comentario</span>
          <textarea class="comentario-inp" placeholder="Observación o comentario (opcional)"
            oninput="data[${i}].comentario = this.value" onmousedown="event.stopPropagation()">${d.comentario || ''}</textarea>
        `;
        cont.appendChild(card);
      });
      document.getElementById('contador').textContent = `${data.length} de 40 autorizados`;
      document.getElementById('btn-add').disabled = data.length >= 40;
    }

    function cargar(e, idx) {
      const file = e.target.files[0];
      if (!file) return;

      const isPDF = file.type === 'application/pdf' || file.name.toLowerCase().endsWith('.pdf');
      const isWord = file.type === 'application/msword' ||
                     file.type === 'application/vnd.openxmlformats-officedocument.wordprocessingml.document' ||
                     file.name.toLowerCase().endsWith('.doc') ||
                     file.name.toLowerCase().endsWith('.docx');

      const readerDataURL = new FileReader();
      const readerBuffer = new FileReader();

      readerBuffer.onload = evBuffer => {
        data[idx].rawBuffer = evBuffer.target.result;
      };
      readerBuffer.readAsArrayBuffer(file);

      readerDataURL.onload = evDataURL => {
        if (isPDF) {
          data[idx].img = null;
          data[idx].fileData = evDataURL.target.result;
          data[idx].fileType = 'pdf';
          data[idx].fileName = file.name;
        } else if (isWord) {
          data[idx].img = null;
          data[idx].fileData = evDataURL.target.result;
          data[idx].fileType = 'word';
          data[idx].fileName = file.name;
          
          mammoth.extractRawText({ arrayBuffer: data[idx].rawBuffer })
            .then(res => { if(res.value && !data[idx].comentario) data[idx].comentario = res.value.trim(); render(); })
            .catch(() => {});
        } else {
          data[idx].img = evDataURL.target.result;
          data[idx].fileData = null;
          data[idx].fileType = 'image';
          data[idx].fileName = file.name;
        }
        render();
      };
      readerDataURL.readAsDataURL(file);
    }

    function limpiar(idx) {
      data[idx].img = null;
      data[idx].fileData = null;
      data[idx].fileType = null;
      data[idx].fileName = null;
      data[idx].rawBuffer = null;
      render();
    }

    function setMsg(texto, tipo) {
      const el = document.getElementById('msg');
      el.textContent = texto;
      el.className = 'msg ' + tipo;
    }

    function obtenerDimensionesImagen(src) {
      return new Promise((resolve) => {
        const img = new Image();
        img.onload = () => {
          resolve({ anchoReal: img.naturalWidth, altoReal: img.naturalHeight });
        };
        img.onerror = () => resolve({ anchoReal: 0, altoReal: 0 });
        img.src = src;
      });
    }

    async function generarPDF() {
      const cargados = data.filter(d => d.img || d.fileData);
      
      if (cargados.length < 2) {
        setMsg('Falta información: Se requiere un mínimo de 2 autorizados con archivos cargados para exportar el documento.', 'error');
        return;
      }

      const nombreRaw = document.getElementById('nombre-archivo').value.trim();
      const nombreArchivo = (nombreRaw || 'autorizaciones_friocosta')
        .replace(/[^a-zA-Z0-9_\-áéíóúÁÉÍÓÚñÑ ]/g, '')
        .replace(/\s+/g, '_') + '.pdf';

      const ubicacion = document.getElementById('ubicacion').value.trim();
      const observacion = document.getElementById('observacion') ? document.getElementById('observacion').value.trim() : '';

      const btn = document.getElementById('btn-gen');
      btn.disabled = true;
      btn.innerHTML = '<i class="ti ti-loader"></i> Generando...';
      setMsg('', '');
      await new Promise(r => setTimeout(r, 40));

      try {
        const pdfMaestro = await PDFLib.PDFDocument.create();

        let embeddingLogo = null;
        try {
          const base64PureText = LOGO_DATA_URL.split(',')[1];
          const binaryStr = atob(base64PureText);
          const logoBytes = new Uint8Array(binaryStr.length);
          for (let k = 0; k < binaryStr.length; k++) {
            logoBytes[k] = binaryStr.charCodeAt(k);
          }
          embeddingLogo = await pdfMaestro.embedJpg(logoBytes);
        } catch(logoErr) {
          console.warn("Aviso: Logotipo omitido.", logoErr);
        }

        const fuenteNormal = await pdfMaestro.embedFont(PDFLib.StandardFonts.Helvetica);
        const fuenteNegrita = await pdfMaestro.embedFont(PDFLib.StandardFonts.HelveticaBold);
        const fuenteItalica = await pdfMaestro.embedFont(PDFLib.StandardFonts.HelveticaOblique);

        for (let i = 0; i < cargados.length; i++) {
          const item = cargados[i];

          if (item.fileType === 'pdf' && item.rawBuffer) {
            const pdfExterno = await PDFLib.PDFDocument.load(item.rawBuffer);
            const paginasExternas = await pdfMaestro.copyPages(pdfExterno, pdfExterno.getPageIndices());
            paginasExternas.forEach((pag) => pdfMaestro.addPage(pag));
          } else {
            const nuevaPagina = pdfMaestro.addPage([595.276, 841.89]); 
            const { width, height } = nuevaPagina.getSize();

            // Encabezado
            nuevaPagina.drawRectangle({
              x: 0, y: height - 85, width: width, height: 85,
              color: PDFLib.rgb(0.078, 0.207, 0.721),
            });
            nuevaPagina.drawRectangle({
              x: 0, y: height - 85, width: width, height: 28,
              color: PDFLib.rgb(0.101, 0.243, 0.78),
            });
            nuevaPagina.drawRectangle({
              x: 40, y: height - 68, width: 140, height: 52,
              color: PDFLib.rgb(1, 1, 1),
            });

            if (embeddingLogo) {
              nuevaPagina.drawImage(embeddingLogo, { x: 45, y: height - 64, width: 130, height: 44 });
            }

            nuevaPagina.drawText('AUTORIZACIÓN DE COMPRA', {
              x: width - 40, y: height - 42, size: 14, font: fuenteNegrita, color: PDFLib.rgb(1, 1, 1), alignment: 'right',
            });
            nuevaPagina.drawText('Departamento TIC — 26/5/2026', {
              x: width - 40, y: height - 64, size: 9, font: fuenteNormal, color: PDFLib.rgb(0.784, 0.843, 1), alignment: 'right',
            });

            // Contenedor dinámico (520pt)
            nuevaPagina.drawRectangle({
              x: 40, y: 40, width: width - 80, height: height - 135,
              color: PDFLib.rgb(0.929, 0.949, 0.988),
            });
            nuevaPagina.drawRectangle({
              x: 40, y: 40, width: 8, height: height - 135,
              color: PDFLib.rgb(0.078, 0.207, 0.721),
            });

            nuevaPagina.drawText(`AUTORIZADO #${i + 1}`, {
              x: width / 2 - 45, y: height - 112, size: 12, font: fuenteNegrita, color: PDFLib.rgb(0.078, 0.207, 0.721),
            });

            const detallesFila = [item.nombre, ubicacion].filter(Boolean).join('   |   ');
            if (detallesFila) {
              nuevaPagina.drawText(detallesFila.substring(0, 75), {
                x: 65, y: height - 126, size: 8.5, font: fuenteNormal, color: PDFLib.rgb(0.313, 0.313, 0.313),
              });
            }

            const maxAncho = width - 116; 
            const maxAlto = 520; 
            const centroX = 58 + (maxAncho / 2);
            const centroY = 82 + (maxAlto / 2);

            if (item.fileType === 'word') {
              nuevaPagina.drawRectangle({
                x: 58, y: 82, width: maxAncho, height: maxAlto, color: PDFLib.rgb(1, 1, 1),
              });
              const palabrasWord = item.comentario || '(Documento Word procesado sin texto)';
              nuevaPagina.drawText(palabrasWord.substring(0, 900), {
                x: 70, y: 580, size: 9, font: fuenteNormal, color: PDFLib.rgb(0.2, 0.2, 0.2), lineHeight: 13,
              });
            } else if (item.img) {
              try {
                const cleanBase64 = item.img.split(',')[1];
                const imgBinaryStr = atob(cleanBase64);
                const imgBytes = new Uint8Array(imgBinaryStr.length);
                for (let s = 0; s < imgBinaryStr.length; s++) {
                  imgBytes[s] = imgBinaryStr.charCodeAt(s);
                }

                let embeddedCardImg;
                if (item.img.includes('image/png') || item.fileName.toLowerCase().endsWith('.png')) {
                  embeddedCardImg = await pdfMaestro.embedPng(imgBytes);
                } else {
                  embeddedCardImg = await pdfMaestro.embedJpg(imgBytes);
                }

                const { anchoReal, altoReal } = await obtenerDimensionesImagen(item.img);
                
                let renderAncho = maxAncho;
                let renderAlto = maxAlto;

                if (anchoReal > 0 && altoReal > 0) {
                  const escalaX = maxAncho / anchoReal;
                  const escalaY = maxAlto / altoReal;
                  const escalaFinal = Math.min(escalaX, escalaY);

                  renderAncho = anchoReal * escalaFinal;
                  renderAlto = altoReal * escalaFinal;
                }

                const posX = centroX - (renderAncho / 2);
                const posY = centroY - (renderAlto / 2);

                nuevaPagina.drawRectangle({
                  x: posX - 4, y: posY - 4, width: renderAncho + 8, height: renderAlto + 8, color: PDFLib.rgb(1, 1, 1),
                });

                nuevaPagina.drawImage(embeddedCardImg, {
                  x: posX,
                  y: posY,
                  width: renderAncho,
                  height: renderAlto,
                });
              } catch(errImg) {
                console.error("Error al incrustar la imagen:", errImg);
              }
            }

            if (item.comentario && item.fileType !== 'word') {
              nuevaPagina.drawText('Comentario:', {
                x: 60, y: 70, size: 8.5, font: fuenteNegrita, color: PDFLib.rgb(0.235, 0.313, 0.549),
              });
              nuevaPagina.drawText(item.comentario.substring(0, 100), {
                x: 60, y: 56, size: 8.5, font: fuenteItalica, color: PDFLib.rgb(0.196, 0.196, 0.313),
              });
            }

            // Pie de página
            nuevaPagina.drawRectangle({
              x: 0, y: 0, width: width, height: 28, color: PDFLib.rgb(0.078, 0.207, 0.721),
            });
            nuevaPagina.drawText('FRIOCOSTA SAS — Documento generado digitalmente', {
              x: 40, y: 10, size: 8, font: fuenteNormal, color: PDFLib.rgb(1, 1, 1),
            });
          }
        }

        if (observacion) {
          const paginaCierre = pdfMaestro.addPage([595.276, 841.89]);
          const { width, height } = paginaCierre.getSize();

          paginaCierre.drawRectangle({
            x: 0, y: height - 85, width: width, height: 85, color: PDFLib.rgb(0.078, 0.207, 0.721),
          });
          paginaCierre.drawText('NOTAS DE AUTORIZACIÓN', {
            x: 40, y: height - 50, size: 14, font: fuenteNegrita, color: PDFLib.rgb(1, 1, 1),
          });
          paginaCierre.drawRectangle({
            x: 40, y: height - 210, width: width - 80, height: 80, color: PDFLib.rgb(1, 0.972, 0.862),
          });
          paginaCierre.drawText('OBSERVACIÓN GENERAL:', {
            x: 55, y: height - 160, size: 9, font: fuenteNegrita, color: PDFLib.rgb(0.47, 0.313, 0),
          });
          paginaCierre.drawText(observacion.substring(0, 300), {
            x: 55, y: height - 190, size: 9, font: fuenteNormal, color: PDFLib.rgb(0.235, 0.156, 0),
          });
          paginaCierre.drawRectangle({
            x: 0, y: 0, width: width, height: 28, color: PDFLib.rgb(0.078, 0.207, 0.721),
          });
          paginaCierre.drawText('FRIOCOSTA SAS — Anexo general', {
            x: 40, y: 10, size: 8, font: fuenteNormal, color: PDFLib.rgb(1, 1, 1),
          });
        }

        const pdfFinalBytes = await pdfMaestro.save({ useObjectStreams: false });
        
        const blob = new Blob([pdfFinalBytes], { type: 'application/pdf' });
        const link = document.createElement('a');
        link.href = URL.createObjectURL(blob);
        link.download = nombreArchivo;
        link.click();

        setMsg(`✓ PDF "${nombreArchivo}" generado correctamente.`, 'ok');
      } catch (err) {
        setMsg('Error al compilar documento: ' + err.message, 'error');
        console.error(err);
      }

      btn.disabled = false;
      btn.innerHTML = '<i class="ti ti-file-download"></i> Generar PDF';
    }

    render();
  </script>
</body>
</html>
