
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coin2Cash Exchange</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f8ff; /* Light blue background */
            color: #333; /* Dark text for contrast */
        }
        header {
            background-color: #228B22; /* Green header */
            color: #fff; /* White text */
            padding: 20px 0;
            text-align: center;
        }
        nav {
            margin: 0;
            padding: 10px;
            background-color: #20B2AA; /* Light blue-green for navigation */
            text-align: center;
        }
        nav a {
            color: #fff; /* White text */
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .container {
            width: 80%;
            margin: 20px auto;
            background-color: #fff; /* White container background */
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        footer {
            background-color: #228B22; /* Green footer */
            color: #fff; /* White text */
            text-align: center;
            padding: 10px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: #228B22; /* Green labels */
        }
        .form-group input {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
            border: 1px solid #20B2AA; /* Light blue border */
            border-radius: 4px;
        }
        .btn {
            background-color: #228B22; /* Green button */
            color: #fff; /* White text */
            padding: 10px 15px;
            border: none;
            cursor: pointer;
            border-radius: 4px;
            font-weight: bold;
        }
        .btn:hover {
            background-color: #20B2AA; /* Light blue on hover */
        }
        h2 {
            color: #228B22; /* Green headings */
        }
        h3 {
            color: #20B2AA; /* Light blue subheadings */
        }
        .welcome-message {
            text-align: center;
            margin: 20px 0;
            font-size: 1.5em;
            color: #228B22; /* Green text */
        }
    </style>
</head>
<body>

    <header>
        <h1>Coin2Cash Exchange</h1>
    </header>

    <nav>
        <a href="#home">Home</a>
        <a href="#login">Login</a>
        <a href="#register">Register</a>
        <a href="#plans">Investment Plans</a>
    </nav>

    <div class="container">
        <!-- Welcome Message -->
        <div class="welcome-message">
            Welcome to Coin2Cash Exchange! Sign up or log in to get started.
        </div>

        <!-- Login Form -->
        <section id="login">
            <h2>Login</h2>
            <form id="loginForm">
                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" required>
                </div>
                <div class="form-group">
                    <label for="password">Password:</label>
                    <input type="password" id="password" required>
                </div>
                <button type="submit" class="btn">Login</button>
            </form>
        </section>

        <!-- Registration Form -->
        <section id="register">
            <h2>Register</h2>
            <form id="registerForm">
                <div class="form-group">
                    <label for="regEmail">Email:</label>
                    <input type="email" id="regEmail" required>
                </div>
                <div class="form-group">
                    <label for="regPassword">Password:</label>
                    <input type="password" id="regPassword" required>
                </div>
                <button type="submit" class="btn">Register</button>
            </form>
        </section>

        <!-- Investment Plans -->
        <section id="plans">
            <h2>Investment Plans</h2>
            <div>
                <h3>Plan 1: 1 Month</h3>
                <p>Minimum Investment: $50,000</p>
                <form id="investForm">
                    <div class="form-group">
                        <label for="amount">Investment Amount:</label>
                        <input type="number" id="amount" min="50000" required>
                    </div>
                    <div class="form-group">
                        <label for="duration">Duration (Months):</label>
                        <input type="number" id="duration" min="1" required>
                    </div>
                    <button type="submit" class="btn">Invest Now</button>
                </form>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2025 Coin2Cash Exchange. All rights reserved.</p>
    </footer>

    <script>
        // Frontend Validation and Interaction
        document.getElementById('investForm').addEventListener('submit', function (e) {
            e.preventDefault();
            const amount = parseFloat(document.getElementById('amount').value);
            const duration = parseInt(document.getElementById('duration').value);

            if (amount < 50000) {
                alert('Minimum investment is $50,000.');
                return;
            }
            if (duration < 1) {
                alert('Minimum duration is 1 month.');
                return;
            }

            alert(`Investment of $${amount} for ${duration} month(s) submitted!`);
            // Here you would send the data to the backend for processing
        });
    </script>
</body>
</html>
<!--
  <<< Author notes: Course header >>>
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses MIT license.
-->

# GitHub Pages

_Create a site or blog from your GitHub repositories with GitHub Pages._

</header>

<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

## Step 1: Enable GitHub Pages

_Welcome to GitHub Pages and Jekyll :tada:!_

The first step is to enable GitHub Pages on this [repository](https://docs.github.com/en/get-started/quickstart/github-glossary#repository). When you enable GitHub Pages on a repository, GitHub takes the content that's on the main branch and publishes a website based on its contents.

### :keyboard: Activity: Enable GitHub Pages

1. Open a new browser tab, and work on the steps in your second tab while you read the instructions in this tab.
1. Under your repository name, click **Settings**.
1. Click **Pages** in the **Code and automation** section.
1. Ensure "Deploy from a branch" is selected from the **Source** drop-down menu, and then select `main` from the **Branch** drop-down menu.
1. Click the **Save** button.
1. Wait about _one minute_ then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/en/actions) will automatically update to the next step.
   > Turning on GitHub Pages creates a deployment of your repository. GitHub Actions may take up to a minute to respond while waiting for the deployment. Future steps will be about 20 seconds; this step is slower.
   > **Note**: In the **Pages** of **Settings**, the **Visit site** button will appear at the top. Click the button to see your GitHub Pages site.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/github-pages) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
