Lax Gemao — Personal Portfolio
A responsive personal portfolio landing page built with HTML, CSS, and JavaScript, served locally using the Bonezegei Scripting Language (BSL) HTTP server.

Repository: Fhugshore/BSL_HTTP_and_WebSocket
1. Project Description
I'm Lax Gemao, a Bachelor of Science in Information Technology student specializing in Network Systems. I created this portfolio to introduce myself, share my technical interests, showcase projects I've worked on, and document my continuing development in programming and networking.

The site is designed as a single-page portfolio with navigation links to the following sections:
- Home: Introduction and an animated, rotating role description.
- About: Background and interests in software and computer networks.
- Skills: Programming, web development, databases, networking, and developer tools.
- Projects: Kinetic — Emergency Notification System, MSU-IIT Campus Navigation, AWS Club Booth Game, and database management projects.
- Achievements: Academic project experience, continued learning, and DICT cybersecurity training.
- Contact: Contact details and links included in the portfolio.
Technology Stack
Technology	Purpose
HTML5	Structure and content of the portfolio
CSS3	Styling and responsive layout
JavaScript	Rotating typing effect and automatic footer year
Bonezegei Scripting Language (BSL)	Runs the local web server
BSL http library	Handles HTTP requests and serves HTML files
Visual Studio Code	Code editor and development environment
Git and GitHub	Version control and project repository


The portfolio's styles and JavaScript are embedded in public/index.html. The BSL application in app.bzg serves that page from the root URL. The reference server also includes WebSocket event handlers, although the portfolio page itself does not depend on WebSocket communication.
2. Repository Setup
Step 1 — Clone the repository
Open PowerShell, Command Prompt, or the terminal in Visual Studio Code and run:
git clone https://github.com/Fhugshore/BSL_HTTP_and_WebSocket.git
cd BSL_HTTP_and_WebSocket
If the project is already downloaded, open its folder directly in Visual Studio Code instead.
Step 2 — Install Bonezegei Scripting Language
Install Bonezegei Scripting Language (BSL) using its official installation instructions. Make sure the BSL command-line tools are accessible from your terminal.

To check that the interpreter is available, run:
bonezegei -v
If the command is not recognized, check the BSL installation and your system PATH, then reopen the terminal.
Step 3 — Open the project in Visual Studio Code
1. Start Visual Studio Code.
2. Choose File > Open Folder.
3. Select the BSL_HTTP_and_WebSocket directory.
4. Open Terminal > New Terminal.
5. Make sure your terminal's working directory contains app.bzg and package.json.
Step 4 — Install project dependencies
Run the BSL package manager from the repository root:
bzg install
The dependency declared in package.json is the BSL http library, which the server loads from lib/http.bzg.
Step 5 — Run the web server
Execute:
bzg run
This runs the configured BSL application (app.bzg). Its server configuration uses port 8000:
var server = http(8000);
Keep the terminal open while viewing the page.
Step 6 — Open the portfolio in a browser
Visit:

http://localhost:8000

The server's root route (/) displays public/index.html. For other paths, the application serves public/404.html as a fallback page.

To stop the server, return to the terminal and press Ctrl + C.
Step 7 — Save changes to GitHub
After editing and testing the page or README, commit and push your changes:
git add .
git commit -m "Document portfolio setup and execution"
git push origin main
3. Execution Verification
The following checks should be completed on the local computer before submitting the laboratory.
Check	Expected result	Status
bonezegei -v	Displays the installed interpreter version	To verify locally
bzg install	Installs or confirms the required HTTP dependency	To verify locally
bzg run	Starts the BSL server without errors	To verify locally
http://localhost:8000	Opens the personal portfolio landing page	To verify locally
Navigation links	Jump to their corresponding page sections	To verify locally
Responsive layout	Page adapts to smaller browser widths	To verify locally


Terminal Screenshot — bzg run
Capture the Visual Studio Code terminal showing the bzg run command and successful server output, without errors.

Save the image as docs/screenshots/terminal.png.

Browser Screenshot — Personal Portfolio
While the server is running, open http://localhost:8000 in a browser and capture the rendered landing page. Include the address bar in the screenshot when possible.

Save the image as docs/screenshots/browser.png.

Screenshot reminder: The two image links above will display after the actual PNG files have been added to docs/screenshots/ and committed to the repository. They are not generated screenshots.

4. Project Structure
BSL_HTTP_and_WebSocket/
├── app.bzg                  # BSL HTTP server and WebSocket handlers
├── package.json             # BSL project configuration and HTTP dependency
├── lib/                     # HTTP library and related dependency files
├── public/
│   ├── index.html           # Personal portfolio, embedded CSS, and JavaScript
│   └── 404.html             # Fallback page
├── docs/                    # Add for laboratory documentation
│   └── screenshots/         # Add your actual execution screenshots here
│       ├── terminal.png
│       └── browser.png
├── libwinpthread-1.dll      # Runtime-related library present in repository
├── .gitattributes
├── LICENSE                  # MIT license and original attribution
└── README.md                # Project documentation
Note: docs/screenshots/ and its two image files are intended additions for the laboratory and may not exist until screenshots are saved.
5. Troubleshooting
bzg or bonezegei is not recognized
Confirm that Bonezegei Scripting Language is installed and its command-line tools are available on the system PATH. Reopen VS Code or the terminal if necessary.

lib/http.bzg cannot be loaded
Run bzg install from the directory containing package.json, then check that the required library is present.

localhost:8000 does not load
Verify that bzg run is still running without errors and that the browser address is http://localhost:8000 (not https://).

Port 8000 is already in use
Stop an existing server using that port before starting the project again.

The old portfolio version is displayed
Save public/index.html, then refresh the browser with Ctrl + F5.

Images do not appear in the GitHub README
Make sure the screenshots are committed under docs/screenshots/ and that their filenames exactly match the Markdown image paths.
6. Conclusion
This project helped me practice front-end web development, local HTTP server setup, dependency installation, and documentation. It also demonstrates how BSL can serve a personal portfolio page through a local development server, while Git and GitHub provide a way to track and share the source code.
7. Attribution and License
The server code is based on the MSU-IIT BSL HTTP and WebSocket reference project. This repository includes an MIT License with copyright attribution to Mindanao State University – Iligan Institute of Technology. See LICENSE for the full terms.
