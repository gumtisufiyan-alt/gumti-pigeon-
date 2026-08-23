<!DOCTYPE html>
<html lang="ur">
<head>
    <meta charset="UTF-8">
    <title>گمٹی پیجن فلائنگ ٹورنامنٹ</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; direction: rtl; background-color: #f8f9fa; }
        .container { width: 98%; margin: 10px auto; }
        table { width: 100%; margin-top: 20px; border-collapse: collapse; background: white; font-size: 13px; }
        th, td { border: 1px solid #ddd; padding: 6px 3px; text-align: center; }
        th { background-color: #004085; color: white; }
        .input-box { background: white; padding: 15px; border-radius: 8px; box-shadow: 0 0 10px rgba(0,0,0,0.1); display: inline-block; margin-top: 10px; }
        input { padding: 8px; margin: 5px; width: 280px; }
        button { padding: 8px 15px; background-color: #004085; color: white; border: none; border-radius: 4px; cursor: pointer; font-weight: bold; }
    </style>
</head>
<body>

<div class="container">
    <h2>گمٹی پیجن فلائنگ ٹورنامنٹ 🏆</h2>

    <div class="input-box">
        <h3>نئی اینٹری / وقت اپڈیٹ کریں 📝</h3>
        <input type="text" id="ownerName" placeholder="مالک کا نام (مثلاً Ali)"><br>
        <input type="text" id="pigeonTimes" placeholder="اوقات (مثلاً 12:30, 12:50, 13:10...)"><br>
        <button onclick="addOrUpdateData()">جدول میں شامل کریں 💾</button>
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
                <th>Pigeon 8</th>
                <th>Pigeon 9</th>
                <th>Pigeon 10</th>
                <th>Pigeon 11</th>
            </tr>
        </thead>
        <tbody id="tableBody">
            <!-- یہاں ہر بندے کا ڈیٹا سامنے شو ہوگا -->
        </tbody>
    </table>
</div>

<script>
    function addOrUpdateData() {
        let nameInput = document.getElementById('ownerName').value.trim();
        let timeInput = document.getElementById('pigeonTimes').value.trim();

        if (!nameInput) {
            alert("براہ کرم مالک کا نام درج کریں!");
            return;
        }

        // کاما، ڈاٹ یا سپیس سے ٹائم کو الگ کریں
        let timesArray = timeInput.split(/[,.\s]+/).filter(t => t !== "");

        let tableBody = document.getElementById('tableBody');
        let rows = tableBody.getElementsByTagName('tr');
        let existingRow = null;

        // چیک کریں کہ کیا اس نام کی رو پہلے سے موجود ہے؟
        for (let i = 0; i < rows.length; i++) {
            let nameCell = rows[i].getElementsByTagName('td')[1];
            if (nameCell && nameCell.textContent.toLowerCase() === nameInput.toLowerCase()) {
                existingRow = rows[i];
                break;
            }
        }

        if (existingRow) {
            // اگر نام پہلے سے ہے، تو اسی کے سامنے 11 خانوں میں ٹائم اپڈیٹ کریں
            let cells = existingRow.getElementsByTagName('td');
            for (let i = 0; i < 11; i++) {
                if (timesArray[i]) {
                    cells[i + 2].textContent = timesArray[i];
                }
            }
        } else {
            // اگر نیا نام ہے (مثلاً Ahmed)، تو نئی رو بنائیں اور تمام 11 کبوتروں کے خانوں میں ٹائم ڈالیں
            let newRow = tableBody.insertRow();
            let rowCount = rows.length;

            newRow.insertCell(0).textContent = rowCount; // #
            newRow.insertCell(1).textContent = nameInput; // Name

            // 11 کبوتروں (Pigeon 1 to 11) کے لیے خانے بنائیں
            for (let i = 0; i < 11; i++) {
                let cell = newRow.insertCell(i + 2);
                cell.textContent = timesArray[i] ? timesArray[i] : "-";
            }
        }

        // ان پٹ صاف کریں
        document.getElementById('ownerName').value = '';
        document.getElementById('pigeonTimes').value = '';
    }
</script>

</body>
</html>
