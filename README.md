<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>python-telegram-bot Rifas</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
          integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@jaames/iro@5"></script>
</head>

<script type="text/javascript">
    const nombre_web = document.getElementById('nombre')
    const tarjeta_web = document.getElementById('tarjeta')
    const telefono_web = document.getElementById('telefono')
    Telegram.WebApp.ready();
    Telegram.WebApp.MainButton.setText('Guardar').show().onClick(function () {
        const data = JSON.stringify({nombre: nombre_web, tarjeta: tarjeta_web, telefono: telefono_web});
        Telegram.WebApp.sendData(data);
        Telegram.WebApp.close();
    });
</script>

<body style="background-color: #ffffff">
<div class="container">
    <div class="d-flex align-items-center justify-content-center">
        <div class="card shadow-lg p-3">
            <label class="form-label">Nombre</label>
            <input class="form-control mb-2" type="text" id="nombre"/>
            <label class="form-label">Tarjeta</label>
            <input class="form-control mb-2" type="text" id="tarjeta"/>
            <label class="form-label">Telefono</label>
            <input class="form-control mb-2" type="text" id="telefono"/>
        </div>
    </div>
</div>
</body>
<script type="text/javascript">
    Telegram.WebApp.expand();
</script>

</html>
