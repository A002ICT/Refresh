<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced Programming Guide</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-bg: #ecf0f1;
            --dark-text: #2c3e50;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            line-height: 1.6;
            color: var(--dark-text);
        }

        .header {
            background: var(--primary-color);
            color: white;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .nav {
            background: var(--secondary-color);
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav a {
            color: white;
            text-decoration: none;
            margin: 0 1.5rem;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            transition: background 0.3s;
        }

        .nav a:hover {
            background: rgba(255, 255, 255, 0.1);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .language-section {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            margin: 2rem 0;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .language-section:hover {
            transform: translateY(-5px);
        }

        .code-block {
            background: #f8f9fa;
            padding: 1.5rem;
            border-radius: 6px;
            margin: 1rem 0;
            overflow-x: auto;
        }

        .tip-box {
            background: var(--light-bg);
            border-left: 4px solid var(--secondary-color);
            padding: 1rem;
            margin: 1rem 0;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }

        .badge {
            display: inline-block;
            padding: 0.25rem 0.75rem;
            border-radius: 20px;
            font-size: 0.8rem;
            margin: 0.5rem 0;
        }

        .html-badge {
            background: #e34c26;
            color: white;
        }

        .c-badge {
            background: #004482;
            color: white;
        }

        .cs-badge {
            background: #682876;
            color: white;
        }

        .cpp-badge {
            background: #004482;
            color: white;
        }

        .python-badge {
            background: #3572A5;
            color: white;
        }

        .java-badge {
            background: #b07219;
            color: white;
        }

        @media (max-width: 768px) {
            .nav {
                text-align: center;
            }

            .nav a {
                display: block;
                margin: 0.5rem 0;
            }
        }
    </style>
</head>

<body>
    <header class="header">
        <h1>Advanced Programming Guide</h1>
        <p>Comprehensive Reference for Modern Developers</p>
    </header>

    <nav class="nav">
        <a href="#html">HTML5</a>
        <a href="#c">C</a>
        <a href="#csharp">C#</a>
        <a href="#cpp">C++</a>
        <a href="#python">Python</a>
        <a href="#java">Java</a>
    </nav>

    <div class="container">
        <!-- HTML Section -->
        <section id="html" class="language-section">
            <span class="badge html-badge">HTML5</span>
            <h2>Modern HTML5 Features</h2>
            <div class="tip-box">
                <strong>Pro Tip:</strong> Use semantic HTML elements for better accessibility and SEO
            </div>

            <h3>Key Features:</h3>
            <ul>
                <li>Semantic Elements (article, section, nav)</li>
                <li>Form Validation Attributes</li>
                <li>Audio/Video Support</li>
                <li>Canvas API</li>
            </ul>

            <div class="code-block">
                <pre><code>&lt;!-- Semantic HTML Example --&gt;
&lt;article&gt;
    &lt;header&gt;
        &lt;h1&gt;Article Title&lt;/h1&gt;
    &lt;/header&gt;
    &lt;section&gt;
        &lt;p&gt;Article content...&lt;/p&gt;
        &lt;figure&gt;
            &lt;img src="image.jpg" alt="Description"&gt;
            &lt;figcaption&gt;Image caption&lt;/figcaption&gt;
        &lt;/figure&gt;
    &lt;/section&gt;
    &lt;footer&gt;
        &lt;p&gt;Article footer&lt;/p&gt;
    &lt;/footer&gt;
&lt;/article&gt;</code></pre>
            </div>
        </section>

        <!-- C Section -->
        <section id="c" class="language-section">
            <span class="badge c-badge">C</span>
            <h2>C Programming Essentials</h2>
            <div class="tip-box">
                <strong>Pro Tip:</strong> Always initialize pointers to NULL and check for null before dereferencing
            </div>

            <div class="grid-container">
                <div>
                    <h3>Memory Management</h3>
                    <p>Use malloc and free carefully to prevent memory leaks</p>
                    <div class="code-block">
                        <pre><code>int *arr = (int*)malloc(10 * sizeof(int));
if(arr == NULL) {
    // Handle allocation error
}
// Use array
free(arr);</code></pre>
                    </div>
                </div>

                <div>
                    <h3>Pointers</h3>
                    <p>Understanding pointer arithmetic is crucial</p>
                    <div class="code-block">
                        <pre><code>int nums[] = {1,2,3};
int *ptr = nums;
printf("%d", *(ptr+1)); // Output: 2</code></pre>
                    </div>
                </div>
            </div>
        </section>

        <!-- Add similar sections for other languages -->

        <!-- Python Section -->
        <section id="python" class="language-section">
            <span class="badge python-badge">Python</span>
            <h2>Python Best Practices</h2>
            <div class="tip-box">
                <strong>Pro Tip:</strong> Use list comprehensions for concise iterations
            </div>

            <div class="code-block">
                <pre><code># Traditional approach
squares = []
for x in range(10):
    squares.append(x**2)

# Pythonic way
squares = [x**2 for x in range(10)]</code></pre>
            </div>

            <h3>Context Managers</h3>
            <div class="code-block">
                <pre><code># Proper file handling
with open('file.txt', 'r') as f:
    content = f.read()
# File automatically closed</code></pre>
            </div>
        </section>

        <!-- Java Section -->
        <section id="java" class="language-section">
            <span class="badge java-badge">Java</span>
            <h2>Java OOP Concepts</h2>
            <div class="tip-box">
                <strong>Pro Tip:</strong> Follow SOLID principles for maintainable code
            </div>

            <div class="code-block">
                <pre><code>// Interface example
interface Shape {
    double area();
}

class Circle implements Shape {
    private double radius;
    
    public Circle(double radius) {
        this.radius = radius;
    }
    
    @Override
    public double area() {
        return Math.PI * radius * radius;
    }
}</code></pre>
            </div>
        </section>
    </div>
</body>

</html>
