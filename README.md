# Guess-number-game
<html>
    <head>
        <title>Number guess game</title>
        <style>
            body,html{
                margin: 0;
                padding: 0;
                height: 100vh;
            }
            .container{
                height: 100vh;
                background-color: rgb(50, 105, 207);
                display: flex;
                justify-content: center;
                align-items: center;
            }
            .box{
                text-align: center;
                background-color: rgb(162, 194, 254);
                color: rgb(8, 108, 111);
                padding: 50px 100px;
                border-radius: 20px 50px;
                border: 5px solid rgb(10, 68, 176);
            }
            h2{
                font-size: 40px;
            }
            #num1{
                border-radius: 5px;
                border: 3px solid rgb(11, 123, 203);
                background-color: rgb(97, 184, 205);
                height: 35px;
                width: 250px;
            }
            button{
                background-color: rgb(31, 123, 123);
                color: aliceblue;
                border-radius: 7px;
                height: 25px;
                width: 80px;
            }
            button:hover{
                background-color: rgb(211, 249, 249);
                color: black;
            }
            p{
                color: rgb(6, 107, 107);
                font-size: 30px;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <div class="box">
                <h2>Guess the number</h2>
                <input id="num1" type="number" placeholder="Enter number">
                <button onclick="guess()">submit</button>
                <p id="won"></p>
            </div>
        </div>
        <script>
            const a = Math.floor(Math.random()*10);
            function guess(){
                let b = parseInt(document.getElementById("num1").value);
                if(a == b){
                    document.getElementById("won").innerHTML = "You won the game";
                }
                else if(a < b){
                    alert("guess lower number");
                }
                else{
                    alert("guess higher number");
                }
            }
        </script>
    </body>
</html>
