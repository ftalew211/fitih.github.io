
    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Personal Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background: #f9f9f9;
        }
        header, section {
            background: white;
            margin-bottom: 20px;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 6px #ccc;
        }
        nav {
            margin-bottom: 30px;
        }
        nav a {
            margin-right: 15px;
            text-decoration: none;
            color: #0073b1; /* LinkedIn blue */
            font-weight: bold;
        }
        nav a:hover {
            text-decoration: underline;
        }
        img.profile-pic {
            width: 150px;
            height: 150px;
            object-fit: cover;
            border-radius: 50%;
            border: 3px solid #0073b1;
        }
        .references-list {
            margin-top: 10px;
        }
        .reference-item {
            padding: 8px;
            border-bottom: 1px solid #ddd;
        }
        input, textarea {
            padding: 8px;
            margin: 6px 0 10px;
            width: 100%;
            box-sizing: border-box;
            font-size: 1em;
        }
        button {
            background-color: #0073b1;
            color: white;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
            font-size: 1em;
            border-radius: 4px;
        }
        button:hover {
            background-color: #005582;
        }
    </style>
</head>
<body>

<header>
    <img src="https://your-picture-url.com/photo.jpg" alt="Your Name" class="profile-pic" />
    <h1>Your Name</h1>
    <p><strong>Current Organization:</strong> Example Organization</p>
    <p><strong>Contact:</strong> phone@example.org | ‪+251-912-345-678‬</p>
    <p><a href="https://www.linkedin.com/in/yourlinkedin" target="_blank">LinkedIn Profile</a></p>
</header>

<nav>
    <a href="#cv">CV</a>
    <a href="#course">Generative AI Course</a>
    <a href="#references">References</a>
</nav>

<section id="cv">
    <h2>Curriculum Vitae</h2>
    <p><strong>Professional Background:</strong> Public Health Program Manager specializing in polio eradication and health systems strengthening.</p>
    <p><strong>Skills:</strong> Program management, M&E, data analysis, DHIS2, health innovation.</p>
    <p><strong>Experience:</strong> CDC Stop Polio Program, health sector in Ethiopia, digital health solutions.</p>
</section>

<section id="course">
    <h2>Generative AI Course Module</h2>
    <ul>
        <li>Lesson 1: Introduction to Generative AI</li>
        <li>Lesson 2: AI Coding Basics</li>
        <li>Lesson 3: Using AI in Web Development</li>
        <li>Lesson 4: Project - Build a Personal Website</li>
        <li>Progress: <strong>In Progress</strong></li>
    </ul>
</section>

<section id="references">
    <h2>References</h2>
    <form id="refForm">
        <label for="refName">Reference Name:</label>
        <input type="text" id="refName" required />
        <label for="refDetails">Reference Details:</label>
        <textarea id="refDetails" rows="3" required></textarea>
        <button type="submit">Add Reference</button>
    </form>
    <div class="references-list" id="refList"></div>
</section>

<script>
    const refListEl = document.getElementById('refList');
    const refForm = document.getElementById('refForm');

    function loadReferences() {
        const refs = JSON.parse(localStorage.getItem('references') || '[]');
        refListEl.innerHTML = '';
        refs.forEach((ref, index) => {
            const div = document.createElement('div');
            div.className = 'reference-item';
            div.innerHTML = <strong>${ref.name}</strong><p>${ref.details}</p>;
            refListEl.appendChild(div);
        });
    }

    refForm.addEventListener('submit', function(e) {
        e.preventDefault();
        const name = document.getElementById('refName').value.trim();
        const details = document.getElementById('refDetails').value.trim();
        if (name && details) {
            const refs = JSON.parse(localStorage.getItem('references') || '[]');
            refs.push({ name, details });
            localStorage.setItem('references', JSON.stringify(refs));
            loadReferences();
            refForm.reset();
        }
    });

    loadReferences();
</script>

</body>
</html>
