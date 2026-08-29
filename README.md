<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML and JavaScript Activity</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            line-height: 1.6;
        }

        header {
            background-color: #2563eb;
            color: white;
            padding: 20px;
            text-align: center;
        }

        nav {
            background-color: #1e293b;
            padding: 10px;
            text-align: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
        }

        main {
            padding: 20px;
        }

        /* Responsive two-column Flexbox */
        .container {
            display: flex;
            gap: 20px;
        }

        .column {
            flex: 1;
            padding: 20px;
            background-color: #f1f5f9;
            border-radius: 10px;
        }

        img {
            width: 100%;
            max-width: 250px;
            height: 150px;
            object-fit: cover;
            margin: 10px;
            border-radius: 8px;
        }

        iframe {
            width: 100%;
            height: 300px;
            border: 0;
            margin-top: 10px;
        }

        button {
            background-color: #2563eb;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #1d4ed8;
        }

        footer {
            background-color: #1e293b;
            color: white;
            text-align: center;
            padding: 15px;
            margin-top: 20px;
        }

        /* Responsive design */
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }

            nav a {
                display: block;
                margin: 8px;
            }
        }
    </style>
</head>

<body>

    <!-- Semantic HTML: header -->
    <header>
        <h1>My Webpage</h1>
        <p>HTML, CSS and JavaScript Activity</p>
    </header>

    <!-- Semantic HTML: navigation -->
    <nav>
        <a href="#home">Home</a>
        <a href="#images">Images</a>
        <a href="#video">Video</a>
        <a href="#map">Map</a>
        <a href="#code">Code</a>
    </nav>

    <!-- Semantic HTML: main content -->
    <main id="home">

        <h2>Welcome</h2>

        <p id="message">
            This paragraph will change when you click the button.
        </p>

        <!-- JavaScript button -->
        <button onclick="changeText()">
            Change Paragraph Text
        </button>

        <hr>
        <!-- Responsive two-column Flexbox -->
        <div class="container">

            <section class="column">
                <h2>Column 1</h2>
                <p>
                    This is the first column. The two columns use
                    CSS Flexbox and will become one column on smaller screens.
                </p>

                <h3>Three Image File Paths</h3>

                <!-- 1. Same folder -->
                <img src="image1.jpg" alt="Image from same folder">

                <!-- 2. Subfolder -->
                <img src="images/image2.jpg" alt="Image from subfolder">

                <!-- 3. Parent folder -->
                <img src="../image3.jpg" alt="Image from parent folder"> 
            </section>

            <section class="column">
                <h2>Column 2</h2>
                <p>
                    This is the second column. It contains an embedded
                    YouTube video and Google Map.
                </p>

                <h3 id="video">YouTube Video</h3>

                <!-- YouTube iframe -->
                <iframe
                    src="https://www.youtube.com/embed/dQw4w9WgXcQ"
                    title="YouTube Video"
                    allowfullscreen>
                </iframe>

                <h3 id="map">Google Map</h3>

                <!-- Google Map iframe -->
                <iframe
                    src="https://www.google.com/maps?q=Manila,Philippines&output=embed"
                    title="Google Map"
                    allowfullscreen
                    loading="lazy">
                </iframe>
            </section>

        </div>

        <hr>

        <!-- Code snippet -->
        <section id="code">
            <h2>JavaScript Code Example</h2>

            <pre><code>
function changeText() {
    document.getElementById("message").innerHTML =
        "The paragraph has been changed!";
}
            </code></pre>
        </section>

        <hr>

        <!-- Example of semantic HTML conversion -->
        <section>
            <h2>Semantic HTML Structure</h2>

            <p>
                Instead of using many generic div elements, this webpage
                uses semantic elements such as:
            </p>

            <ul>
                <li>&lt;header&gt; - page header</li>
                <li>&lt;nav&gt; - navigation links</li>
                <li>&lt;main&gt; - main content</li>
                <li>&lt;section&gt; - grouped content</li>
                <li>&lt;footer&gt; - page footer</li>
            </ul>
        </section>

    </main>

    <!-- Semantic HTML: footer -->
    <footer>
        <p>&copy; 2026 My Webpage</p>
    </footer>

    <!-- JavaScript -->
    <script>
        function changeText() {
            document.getElementById("message").innerHTML =
                "The paragraph has been changed successfully!";
        }
    </script>

</body>
</html>
