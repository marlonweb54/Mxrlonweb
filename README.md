<head>
    <title>Reproductor de video</title>
    <link rel="stylesheet" href="Noticias.css">
</head>
<body>
    <h1>mi reproductor de video</h1>
    <video width="320" height="240" id="video1">
        <source src="Imagenes/video0101.mp4" type="video/mp4">
        <source src="Imagenes/video0101.mp4" type="video/webm">       
    </video>
    <div>
        <button onclick="PlayPause()">&#9658;/||</button>
        <button onclick="stop()">&#9726;</button>
        <button onclick="skip(-10)">&lt;&lt;</button>
        <button onclick="skip (10)">&gt;&gt;</button>
    </div>
    <script>
        var mivideo =document.getElementById("video1");
        function PlayPause(){
            if (mivideo.paused)
                mivideo.play();
            else
            mivideo.pause();
        }
        function stop(){
            mivideo.pause();
            mivideo.currenTime = 0;
        }
        function skip(value){
            mivideo.currentTime += value;
        
        }
    </script>
</body>
