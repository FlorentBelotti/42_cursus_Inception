<div align="left">

### 42_cursus_Inception![---------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div align="left">
    
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Shell](https://img.shields.io/badge/shell-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)

<nav>
    
### Summary![---------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<ul>
    <li><a href="#Introduction">Introduction</a></li>
    <li><a href="#Setup">Setup</a></li>
    <li><a href="#Mandatory-part">Mandatory Part</a></li>
    <li><a href="#Conclusion">Conclusion</a></li>
    <li><a href="#Thanks">Thanks</a></li>
</ul>
</nav>

### Introduction![---------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
<section id="Introduction">

<div align="justify">

The **Inception** project is part of the System Administration curriculum at 42. Its primary goal is to deepen students' understanding of Docker by requiring them to virtualize multiple services within a personal virtual machine. Each service is implemented in a dedicated Docker container, adhering to best practices and modern configurations such as `TLSv1.2/TLSv1.3` and environment variable management.

The project aims to provide hands-on experience with Docker, enhancing students' knowledge in containerization, system networking, and application deployment.

</div>

### Setup![---------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
<section id="Setup">

<div align="justify">

To get started:

1. Clone this repository and navigate to the root directory.
2. Ensure Docker and Docker Compose are installed on your machine.
3. Configure your `.env` file to include required variables such as domain name, MySQL credentials, etc.
4. Run the project setup using: "make all".
5. Clean containers using: "make clean".

### Mandatory_Part![---------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
<section id="Mandatory-part">

<div align="justify">

The **Mandatory Part** of the Inception project requires the creation of a mini-infrastructure using Docker containers. Each service must be isolated in its dedicated container, configured following best practices, and interconnected via a custom Docker network.

Here are the specific requirements:

- **NGINX container:**
  - Acts as the entry point for the infrastructure.
  - Configured to use **TLSv1.2** or **TLSv1.3** exclusively.
  - Listens on **port 443** only.

- **WordPress container:**
  - Configured with **php-fpm** but without NGINX integration.
  - Stores its data in a dedicated volume.

- **MariaDB container:**
  - Serves as the database for WordPress.
  - Requires secure credentials, managed using `.env` variables and/or Docker secrets.

- **Persistent Volumes:**
  - One for the WordPress database.
  - One for WordPress files.

- **Docker Network:**
  - Links all the containers securely.
  - The `network_mode: host` and deprecated features like `--link` are prohibited.

- **Local Domain Setup:**
  - Configured as `login.42.fr` (replace "login" with your username).
  - Points to your machine's local IP.

Additional Constraints:
- Avoid infinite loops (`while true`, `sleep infinity`, etc.) in entrypoints or scripts.
- Do not expose sensitive information like passwords in Dockerfiles.
- Use environment variables and, optionally, Docker secrets for security.
- All containers must restart automatically in case of failure.

</div>

### Conclusion![---------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
<section id="Conclusion">

The **Inception** project goes far beyond simply learning how to use Docker and Docker Compose. It offers an opportunity to delve into configuration files, scripts, and the inner workings of containers. By understanding these components, students gain a comprehensive view of what happens when a container is launched and how to customize it at a low level.

In this sense, Inception proves invaluable as it bridges the gap between theoretical knowledge and practical application. The project not only teaches containerization but also fosters a deeper understanding of system operations and infrastructure design.

</div>

### Thanks![---------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
<section id="Thanks">

<p>
To <a href="https://github.com/Beorlor">Beorlor </a>: who introduced me to the stakes of the subject.
</p>
<p>
To <a href="https://github.com/ThomasRibalta">Thomas Ribalta </a>: who provided guidance on the project's structure.
</p>

