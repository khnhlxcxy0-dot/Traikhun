<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>BMI Calculator</title>
</head>
<body>
    <h1>คำนวณ BMI</h1>

    <input id="weight" type="number" placeholder="น้ำหนัก (กก.)">
    <input id="height" type="number" placeholder="ส่วนสูง (เมตร)">
    <br><br>
    <button onclick="calcBMI()">คำนวณ</button>

    <p id="result"></p>

    <script>
        function calcBMI() {
            let w = document.getElementById("weight").value;
            let h = document.getElementById("height").value;
            let bmi = w / (h * h);

            let text = "BMI: " + bmi.toFixed(2);

            if (bmi < 18.5) {
                text += " → น้ำหนักต่ำกว่าเกณฑ์";
            } else if (bmi < 23) {
                text += " → ปกติ";
            } else if (bmi < 25) {
                text += " → เริ่มสูงกว่าเกณฑ์";
            } else {
                text += " → สูงกว่าเกณฑ์มาก";
            }

            document.getElementById("result").innerText = text;
        }
    </script>
</body>
</html>

