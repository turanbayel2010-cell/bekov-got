<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>Вопрос</title>

<style>
    body {
        background: #111;
        color: white;
        font-family: Arial, sans-serif;
        text-align: center;
        margin-top: 100px;
    }

    h1 {
        font-size: 40px;
        text-shadow: 0 0 10px #00aaff;
    }

    button {
        padding: 15px 30px;
        font-size: 20px;
        border: none;
        border-radius: 10px;
        cursor: pointer;
        margin: 20px;
        transition: 0.2s;
    }

    #yes {
        background: #00ff55;
    }

    #no {
        background: #ff4444;
        position: absolute;
    }

    #result {
        margin-top: 40px;
        font-size: 35px;
        color: #00ccff;
        text-shadow: 0 0 15px #00ccff;
        display: none;
    }
</style>
</head>

<body>

<h1>Беков гей?</h1>

<button id="yes">Да</button>
<button id="no">Нет</button>

<h2 id="result">Я так и знал! 😎🔥</h2>

<script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const result = document.getElementById("result");

    // Кнопка "Нет" убегает
    noBtn.addEventListener("mouseover", () => {
        const x = Math.random() * (window.innerWidth - 150);
        const y = Math.random() * (window.innerHeight - 100);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    });

    // Нажали "Да"
    yesBtn.addEventListener("click", () => {
        result.style.display = "block";
    });
</script>

</body>
</html>
