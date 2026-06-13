<!DOCTYPE html>
<html>
    <head>
        <title>Moving Ball Animation</title>
        <style>

            #ball{
                width: 50px;
                height: 50px;
                background-color: red;
                border-radius: 50%;
                position: absolute;
                left: 10px;
                top: 80px;
            }

            button{
                margin-top: 70px;
            }
        </style>
    </head>
    <body>

        <h1>Moving Ball Animation</h1>

        <!--Ball-->
        <div id="ball"></div>

        <button onclick="startMoving()">Start Animation</button>

        <script>

            var position = 10;
            var timer;

            function startMoving(){
                timer = setInterval(moveBall, 50);
            }
            function moveBall() {
    position = position + 5;
    document.getElementById("ball").style.left = position + "px";

    if (position >= 500){
        //Stop
        clearInterval(timer);
    }
}
        </script>
    </body>
</html>
