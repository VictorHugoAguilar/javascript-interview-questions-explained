# tabla-ordenable

````html
<!DOCTYPE HTML>
<html>

<head>
  <meta charset="utf-8">
  <style>
    table {
       border-collapse: collapse;
     }
     th, td {
       border: 1px solid black;
       padding: 4px;
     }
     th {
       cursor: pointer;
     }
     th:hover {
       background: yellow;
     }
  </style>
</head>

<body>

  <table id="grid">
    <thead>
      <tr>
        <th data-type="number">Age</th>
        <th data-type="string">Name</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>5</td>
        <td>John</td>
      </tr>
      <tr>
        <td>2</td>
        <td>Pete</td>
      </tr>
      <tr>
        <td>12</td>
        <td>Ann</td>
      </tr>
      <tr>
        <td>9</td>
        <td>Eugene</td>
      </tr>
      <tr>
        <td>1</td>
        <td>Ilya</td>
      </tr>
    </tbody>
  </table>

  <script>

    grid.onclick = function(e) {
      if (e.target.tagName != 'TH') return;

      let th = e.target;
      // si TH, entonces ordena
      // cellIndex es el número de th:
      //   0 para la primera columna
      //   1 para la segunda columna, etc.
      sortGrid(th.cellIndex, th.dataset.type);
    };

    function sortGrid(colNum, type) {
      let tbody = grid.querySelector('tbody');

      let rowsArray = Array.from(tbody.rows);

      // compare(a, b) compara dos filas, necesario para ordenar
      let compare;

      switch (type) {
        case 'number':
          compare = function(rowA, rowB) {
            return rowA.cells[colNum].innerHTML - rowB.cells[colNum].innerHTML;
          };
          break;
        case 'string':
          compare = function(rowA, rowB) {
            return rowA.cells[colNum].innerHTML > rowB.cells[colNum].innerHTML ? 1 : -1;
          };
          break;
      }

      // sort
      rowsArray.sort(compare);

      tbody.append(...rowsArray);
    }
  </script>

</body>
</html>
````



---
[⬅️ volver](https://github.com/VictorHugoAguilar/javascript-interview-questions-explained/tree/main/theory-event/event-delegation#readme#tabla-ordenable)
