<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Radar Dev</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body {
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
      color: white;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 40px;
    }

    h1 {
      margin-bottom: 20px;
      color: #fff;
      font-size: 2rem;
    }

    canvas {
      max-width: 500px;
      background: rgba(255, 255, 255, 0.05);
      padding: 20px;
      border-radius: 16px;
      box-shadow: 0 0 20px rgba(0,0,0,0.5);
    }

    p {
      margin-top: 40px;
      font-size: 1.1rem;
      color: #ccc;
      max-width: 600px;
      text-align: center;
    }
  </style>
</head>
<body>

  <h1>🚀 Radar do Dev Noturno</h1>
  <canvas id="devRadar"></canvas>

  <p>Programo com frequência, nas madrugadas escuras, ouvindo música 🎧 e tomando café ☕.<br>
  JavaScript, React e SQL são meus aliados de batalha.</p>

  <script>
    const ctx = document.getElementById('devRadar').getContext('2d');
    new Chart(ctx, {
      type: 'radar',
      data: {
        labels: ['JavaScript', 'React', 'SQL', 'Cafeína ☕', 'Música 🎧', 'Madrugada 🌙'],
        datasets: [{
          label: 'Meu Nível',
          data: [7, 6, 6, 10, 9, 10],
          backgroundColor: 'rgba(255, 255, 255, 0.2)',
          borderColor: '#00FFFF',
          pointBackgroundColor: '#00FFFF',
          borderWidth: 2
        }]
      },
      options: {
        scales: {
          r: {
            angleLines: { color: '#aaa' },
            grid: { color: '#444' },
            pointLabels: {
              color: '#fff',
              font: {
                size: 14
              }
            },
            ticks: {
              backdropColor: 'transparent',
              color: '#eee',
              stepSize: 2
            }
          }
        },
        plugins: {
          legend: {
            labels: {
              color: '#fff'
            }
          }
        }
      }
    });
  </script>

</body>
</html>

