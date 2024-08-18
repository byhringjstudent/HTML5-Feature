"# HTML5-Feature" 
<!DOCTYPE html>
<html>

<head>
    <title>My Awesome Storybook</title>
    <!-- Basic CSS for styling -->
    <style>
        body {
            font-family: sans-serif;
            text-align: center;
        }
        
        #storyArea {
            width: 80%;
            margin: 20px auto;
            border: 2px dashed #ccc;
            padding: 20px;
            min-height: 200px;
        }
        
        .draggable {
            display: inline-block;
            padding: 10px;
            margin: 5px;
            border: 1px solid #ddd;
            cursor: pointer;
        }
        
        img {
            max-width: 100px;
            max-height: 100px;
        }
    </style>

    <!-- Include Sortable.js -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Sortable/1.14.0/Sortable.min.js"></script>
</head>

<body>

    <h1>The Adventures of Fluffy the Cat</h1>
    <img src="./images/fluffy.jpg" alt="Fluffy the Cat">
    <p>Once upon a time, there was a cat named Fluffy...</p>

    <div class="dropzone" id="storyArea">
        <!-- Items will be dropped here -->
    </div>

    <div id="wordBank">
        <div class="draggable" draggable="true" id="text1">Once upon a time</div>
        <div class="draggable" draggable="true" id="text2">there was a</div>
        <div class="draggable"><img src="./images/astronaut.jpg" alt="Astronaut"></div>
        <div class="draggable">who loved to</div>
        <div class="draggable"><img src="./images/eat-pizza.jpg" alt="Eating pizza"></div>
        <div class="draggable">on the</div>
        <div class="draggable"><img src="./images/moon.jpg" alt="Moon"></div>
        <div class="draggable">The end!</div>
    </div>

    <script>
        // Enable dragging between storyArea and wordBank
        new Sortable(storyArea, {
            group: 'shared', // Allow dragging between wordBank and storyArea
            animation: 300,
        });

        new Sortable(wordBank, {
            group: 'shared',
            animation: 300
        });
    </script>

</body>

</html>

</html>
