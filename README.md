<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Affichage à Minuit</title>
    <style>
        #secretText {
            display: none;
            font-size: 24px;
            font-weight: bold;
            text-align: center;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div id="secretText">N 43°21.134 E 005°50.306</div>
    <script>
        function checkTime() {
            let now = new Date();
            let hours = now.getHours();
            let minutes = now.getMinutes();
            let secretText = document.getElementById("secretText");
            
            if (hours === 0 && minutes === 0) {
                secretText.style.display = "block";
            } else {
                secretText.style.display = "none";
            }
        }
        
        checkTime();
        setInterval(checkTime, 60000); // Vérifie chaque minute
    </script>
</body>
</html>

