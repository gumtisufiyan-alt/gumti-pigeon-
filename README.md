<!DOCTYPE html>
<html lang="ur" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>گمٹی پیجن فلائنگ ٹورنامنٹ</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background-color: #f4f7f6;
    }
    h2 { text-align: center; }
    .card {
      background: white;
      padding: 15px;
      border-radius: 8px;
      max-width: 400px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      margin: 0 auto 20px auto;
    }
    .input-group {
      margin-bottom: 10px;
    }
    .input-group label {
      display: block;
      margin-bottom: 5px;
    }
    .input-group input {
      width: 100%;
      padding: 8px;
      box-sizing: border-box;
    }
    button {
      background: #003366;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 4px;
      cursor: pointer;
      width: 100%;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      background: white;
    }
    th, td {
      border: 1px solid #ddd;
      padding: 10px;
      text-align: center;
    }
    th {
      background-color: #003366;
      color: white;
    }
    /* Circle Time Badge Formatting */
    .time-circle {
      display: inline-block;
      width: 45px;
      height: 45px;
      line-height: 45px;
      border-radius: 50%;
      background-color: #e6f0fa;
      color: #003366;
      border: 2px solid #003366;
      font-weight: bold;
      text-align: center;
      margin: 2px;
      font-size: 13px;
      direction: ltr; /* Time format (11.35) sahi dikhane ke liye */
    }
  </style>
</head>
<body>

  <h2>🏆 گمٹی پیجن فلائنگ ٹورنامنٹ</h2>

  <div class="card">
    <h3>📝 نئی اینٹری / وقت اپڈیٹ کریں</h3>
    <div class="input-group">
      <input type="text" id="ownerName" placeholder="مالک کا نام (مثلاً Ali)">
    </div>
    <div class="input-group">
      <input type="text" id="pigeonTimes" placeholder="اوقات کوما سے الگ کریں (مثلاً 11.35,12.50,13.10)">
    </div>
    <button onclick="addEntry()">جدول میں شامل کریں 💾</button>
  </div>

  <table>
    <thead>
      <tr>
        <th>#</th>
        <th>Name</th>
        <th>Pigeon 1</th>
        <th>Pigeon 2</th>
        <th>Pigeon 3</th>
        <th>Pigeon 4</th>
        <th>Pigeon 5</th>
        <th>Pigeon 6</th>
        <th>Pigeon 7</th>
      </tr>
    </thead>
    <tbody id="tournamentTable">
    </tbody>
  </table>

  <script>
    let count = 1;

    function addEntry() {
      const name = document.getElementById('ownerName').value.trim();
      const timesInput = document.getElementById('pigeonTimes').value.trim();

      if (!name) {
        alert("لطفاً نام درج کریں۔");
        return;
      }

      // Comma se times ko alag karna
      const timesArray = timesInput ? timesInput.split(',').map(t => t.trim()) : [];
      
      const tbody = document.getElementById('tournamentTable');
      const row = document.createElement('tr');

      let rowHTML = `<td>${count++}</td><td><b>${name}</b></td>`;

      for (let i = 0; i < 7; i++) {
        if (timesArray[i]) {
          // Circle Badge me pura time (jaise 11.35) dikhana
          rowHTML += `<td><span class="time-circle">${timesArray[i]}</span></td>`;
        } else {
          rowHTML += `<td>-</td>`;
        }
      }

      row.innerHTML = rowHTML;
      tbody.appendChild(row);

      // Clear inputs
      document.getElementById('ownerName').value = '';
      document.getElementById('pigeonTimes').value = '';
    }
  </script>

</body>
</html>
