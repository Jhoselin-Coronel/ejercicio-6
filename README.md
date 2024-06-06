<!DOCTYPE html>
<html>
<head>
  <title>Demostración del límite</title>
</head>
<body>
  <h1>Demostración del límite</h1>
  <p>Valor de e: <span id="exp-value"></span></p>
  <p>Valores calculados:</p>
  <ul id="calculated-values"></ul>

  <script>
    // Crear el vector n
    const n = [1, 10, 100, 500, 1000, 2000, 4000, 8000];

    // Calcular el vector y
    const y = n.map(x => Math.pow(1 + 1/x, x));

    // Mostrar los resultados
    const expValue = Math.E;
    document.getElementById('exp-value').textContent = expValue.toFixed(10);

    const calculatedValuesList = document.getElementById('calculated-values');
    y.forEach(value => {
      const listItem = document.createElement('li');
      listItem.textContent = value.toFixed(10);
      calculatedValuesList.appendChild(listItem);
    });
  </script>
</body>
</html>
