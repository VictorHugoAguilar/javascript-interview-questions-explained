# comportamiento-tooltip

````html
<!DOCTYPE HTML>
<html>

<head>
  <meta charset="utf-8">
  <style>
    body {
      height: 2000px;
      /* hacer body desplazable, el tooltip debe funcionar después del desplazamiento */
    }

    .tooltip {
      /* estilos del tooltip, puedes usar uno tuyo en su lugar*/
      position: fixed;
      padding: 10px 20px;
      border: 1px solid #b3c9ce;
      border-radius: 4px;
      text-align: center;
      font: italic 14px/1.3 sans-serif;
      color: #333;
      background: #fff;
      box-shadow: 3px 3px 3px rgba(0, 0, 0, .3);
    }
  </style>
</head>

<body>

  <p>LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa</p>
  <p>LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa LaLaLa</p>

  <button data-tooltip="the tooltip is longer than the element">Botón corto</button>
  <button data-tooltip="HTML<br>tooltip">Un botón más</button>

  <p>Desplaza la página para que los botones aparezcan arriba de todo, verifica que los tooltips se muestren correctamente.</p>


  <script>
    // ... tu código...
  </script>

</body>
</html>
````


---
[⬅️ volver](https://github.com/VictorHugoAguilar/javascript-interview-questions-explained/blob/main/theory-event/event-delegation/readme.md#comportamiento-tooltip)
