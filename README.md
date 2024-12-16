# Secure File Transfer Protocol (SFTP) Using FileZilla Server

## Project Overview
This project demonstrates how to **implement a Secure File Transfer Protocol (SFTP) server** using FileZilla Server on a Windows system. The setup ensures **secure file transmission** between systems with features like:

- **User Authentication** for controlled access.
- **Data Encryption** in transit using FTP over TLS.
- **Secure file upload and download testing.**

---

## Project Requirements
To successfully implement this SFTP server, you need:
- **Windows Operating System** (Windows 10/11 recommended).
- **FileZilla Server** (For creating the SFTP server).
- **FileZilla Client** (For testing secure file transfers).
- Basic networking knowledge (IP Address, Port).

---

## Tools Used
1. **FileZilla Server**: Software to set up the SFTP server.
2. **FileZilla Client**: Tool to connect to the server and test file transfer.
3. **TLS Certificate**: Ensures encrypted data transmission.

---

## Steps to Set Up SFTP Server

### Step 1: Download and Install FileZilla Server
1. Go to the [FileZilla Server Download Page](https://filezilla-project.org/download.php?type=server).
2. Download the latest version of FileZilla Server.
3. Run the installer and complete the installation process.
4. Launch the **FileZilla Server Interface**.

---

### Step 2: Configure FileZilla Server

#### 2.1 Create a User Account
1. Open FileZilla Server Interface.
2. Go to **Edit > Users**.
3. Click **Add** to create a new user:
   - Enter a **username** (e.g., "testuser").
   - Set a **password** for the user.
4. Assign a folder for file sharing:
   - Go to **Shared Folders**.
   - Click **Add** to select the directory.
   - Set folder permissions (**Read/Write**).

#### 2.2 Enable FTP over TLS Encryption
1. Go to **Edit > Settings > FTP over TLS settings**.
2. Check **Enable FTP over TLS support**.
3. Generate a new TLS certificate:
   - Fill in certificate details (Country, Organization, etc.).
   - Save the certificate file securely.
4. Click **OK** to apply the settings.

---

### Step 3: Test the SFTP Server Locally

#### 3.1 Install FileZilla Client
1. Download FileZilla Client from the [official site](https://filezilla-project.org/download.php?type=client).
2. Install and launch the FileZilla Client.

#### 3.2 Connect to the Server
1. Open FileZilla Client.
2. Go to **File > Site Manager**.
3. Add a new site with the following details:
   - **Host**: `127.0.0.1` (for local testing).
   - **Port**: `22` (SFTP default port).
   - **Protocol**: SFTP - SSH File Transfer Protocol.
   - **Logon Type**: Normal.
   - **User**: Your created username (e.g., "testuser").
   - **Password**: Your set password.
4. Click **Connect**.

#### 3.3 Upload and Download Files
1. Drag and drop a test file (e.g., `testfile.txt`) from your local system to the remote server directory.
2. Verify that the file transfer completes successfully.
3. Download the file back to your local system to ensure bidirectional transfer.

---

### Step 4: Configure Firewall and Port Forwarding (Optional for Remote Access)
1. Open **Windows Defender Firewall**:
   - Allow inbound traffic on **Port 22**.
2. For remote access:
   - Log into your router and forward **Port 22** to your system's IP address.

---

## Testing the File Transfer
1. **File Upload**: Verify file upload from client to server.
2. **File Download**: Verify file download from server to client.
3. **Secure Connection**: Confirm that the transfer is encrypted (check the lock icon in FileZilla Client).

---

## Security Measures
- **FTP over TLS** ensures encryption of data in transit.
- Use strong passwords for user authentication.
- Restrict folder access to specific users.
- Update TLS certificates regularly for enhanced security.

---

## Screenshots

### 1. FileZilla Server User Configuration
![user config](https://github.com/user-attachments/assets/a2659c68-65b1-426c-a245-ad73cf055d88)


### 2. FTP over TLS Settings
![TLS config](https://github.com/user-attachments/assets/57b99be2-ffed-41be-ba55-5424e57229b0)


---

## Conclusion
This project successfully demonstrates the implementation of an **SFTP server** using FileZilla Server. By enabling FTP over TLS, it ensures:
- Secure transmission of files.
- Controlled access through user authentication.
- Encrypted communication to prevent data interception.

You can now securely transfer files between systems using SFTP.

---

## License
This project is licensed under the MIT License.

---

## Acknowledgments
- [FileZilla Project](https://filezilla-project.org/) for providing free FTP and SFTP solutions.

---
