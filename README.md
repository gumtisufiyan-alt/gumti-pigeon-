<script>
function addOrUpdateData() {
    let nameInput = document.getElementById('ownerName').value.trim();
    let timeInput = document.getElementById('pigeonTimes').value.trim();

    if (!nameInput) {
        alert("براہ کرم مالک کا نام درج کریں!");
        return;
    }

    // صرف کاما (,) یا اسپیس کی بنیاد پر وقت الگ ہوگا (ڈاٹ . سے وقت نہیں ٹوٹے گا)
    let timesArray = timeInput.split(/[\s,]+/).filter(t => t !== "");

    let tableBody = document.getElementById('tableBody');
    let rows = tableBody.getElementsByTagName('tr');
    let existingRow = null;

    for (let i = 0; i < rows.length; i++) {
        let nameCell = rows[i].getElementsByTagName('td')[1];
        if (nameCell && nameCell.textContent.toLowerCase() === nameInput.toLowerCase()) {
            existingRow = rows[i];
            break;
        }
    }

    if (existingRow) {
        let cells = existingRow.getElementsByTagName('td');
        for (let i = 0; i < 11; i++) {
            if (timesArray[i]) {
                cells[i + 2].textContent = timesArray[i];
            }
        }
    } else {
        let newRow = tableBody.insertRow();
        let rowCount = rows.length + 1;

        newRow.insertCell(0).textContent = rowCount;
        newRow.insertCell(1).textContent = nameInput;

        for (let i = 0; i < 11; i++) {
            let cell = newRow.insertCell(i + 2);
            cell.textContent = timesArray[i] ? timesArray[i] : "-";
        }
    }

    document.getElementById('ownerName').value = '';
    document.getElementById('pigeonTimes').value = '';
}
</script>
