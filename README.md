#  TASK1 : Robot Control Panel🤖

This project is a web-based control panel for a robot. It allows users to control the robot's movements using a joystick interface and stop the robot with a dedicated button. The commands are sent to a backend server and stored in a database for further processing.

## 📑 Table of Contents
- [📃 Project Description](#-project-description)
- [🛠️ Technologies Used](#️-technologies-used)
- [💻 Code Explanation](#-code-explanation)
  - [📄 HTML (index.html)](#-html-indexhtml)
  - [🎨 CSS (styles.css)](#-css-stylescss)
  - [📝 JavaScript (script.js)](#-javascript-scriptjs)
  - [🗄️ PHP (store_command.php)](#-php-store_commandphp)
- [⚙️ Installation](#-installation)
- [🚀 Usage](#-usage)
- [📁 File Structure](#-file-structure)
- [✨ Features](#-features)

## 📃 Project Description

The Robot Control Panel project provides a simple and intuitive web interface for controlling a robot. The interface includes a joystick that users can manipulate to send directional commands (Forward, Backward, Left, Right) to the robot. Additionally, a Stop button allows users to halt the robot's movement instantly.

Commands are processed in real-time and sent to a backend server using AJAX requests. These commands are then stored in a MySQL database for logging and further actions.

## 🛠️ Technologies Used

- **HTML**: To structure the web pages.
- **CSS**: To style the control panel and provide a user-friendly interface.
- **JavaScript**: To handle the joystick movements and send commands to the server.
- **PHP**: To handle server-side operations and interact with the MySQL database.
- **MySQL**: To store and retrieve the commands sent by the user.

## 💻 Code Explanation

### 📄 HTML (index.html)

This file defines the structure of the control panel web page. It includes the joystick and stop button elements which the user interacts with. It links to the external CSS for styling and JavaScript for functionality.

### 🎨 CSS (styles.css)

This file styles the control panel to make it visually appealing and user-friendly. It defines the appearance of the joystick, stick, and stop button.

### 📝 JavaScript (script.js)

This file handles the joystick interactions and sends the commands to the server. It listens for user actions (like dragging the joystick) and sends corresponding commands using AJAX.

### 🗄️ PHP (store_command.php)

This file processes the commands sent from the front end. It receives the commands via POST requests and stores them in a MySQL database.

## ⚙️ Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/robot-control-panel.git
    cd robot-control-panel
    ```

2. **Set up the database**:
    - Create a MySQL database named `robot_control`.
    - Create a table named `commands` with the following structure:
        ```sql
        CREATE TABLE commands (
            id INT AUTO_INCREMENT PRIMARY KEY,
            command VARCHAR(255) NOT NULL
        );
        ```

3. **Configure database connection**:
    - Update the database connection parameters in `store_command.php`:
        ```php
        $servername = "localhost";
        $username = "root";
        $password = "";
        $dbname = "robot_control";
        ```

4. **Run the project**:
    - Ensure you have a local server setup (e.g., XAMPP, WAMP).
    - Place the project folder in the `htdocs` directory (for XAMPP) or the appropriate directory for your server setup.
    - Start the server and navigate to `http://localhost/robot-control-panel` in your web browser.

## 🚀 Usage

1. **Control Panel**:
    - Navigate to the Control Panel page.
    - Click and drag the joystick to send movement commands (Forward, Backward, Left, Right) to the robot.
    - Click the Stop button to send a Stop command to the robot.

## 📁 File Structure

```
robot-control-panel/
│
├── index.html
├── styles.css
├── script.js
├── store_command.php
├── README.md
```

- `index.html`: The main HTML file that contains the structure of the control panel.
- `styles.css`: The CSS file for styling the control panel.
- `script.js`: The JavaScript file for handling the joystick interactions and sending commands.
- `store_command.php`: The PHP file for storing commands in the database.
- `README.md`: This file, containing information about the project.

## ✨ Features

- **Joystick Control**: Interact with the joystick to send movement commands to the robot.
- **Stop Button**: Easily stop the robot with a single click.
- **Command Storage**: Store commands in a MySQL database for further processing or analysis.

made with love by "she codes team "🤍😄 raghad Alshammari - sadeem alresaini - razan alothaim.
