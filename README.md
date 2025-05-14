# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive Flexbox Page</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">MySite</div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="container">
    <section class="main-content">
      <h1>Welcome to My Responsive Page</h1>
      <p>This content adjusts depending on screen size using media queries and Flexbox layout.</p>
    </section>

    <aside class="sidebar">
      <h2>Sidebar</h2>
      <p>Additional links or widgets can go here.</p>
    </aside>
  </main>

  <footer class="footer">
    <p>© 2025 MySite. All rights reserved.</p>
  </footer>
</body>
</html>

style.css
/* Base Reset and Global Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', sans-serif;
  background-color: #f9f9f9;
  color: #333;
  line-height: 1.6;
}

header {
  background-color: #0077cc;
  padding: 15px 20px;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
}

.navbar .logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 20px;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

.container {
  display: flex;
  gap: 20px;
  padding: 20px;
}

/* Layout sections */
.main-content {
  flex: 3;
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
}

.sidebar {
  flex: 1;
  background-color: #e4e4e4;
  padding: 20px;
  border-radius: 8px;
}

.footer {
  text-align: center;
  padding: 15px;
  background-color: #333;
  color: white;
  margin-top: 20px;
}

/* Media Queries */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }

  .nav-links {
    flex-direction: column;
    gap: 10px;
    margin-top: 10px;
  }

  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  .container {
    flex-direction: row;
    flex-wrap: wrap;
  }

  .main-content, .sidebar {
    flex: 1 1 100%;
  }

  .nav-links {
    gap: 15px;
  }
}

