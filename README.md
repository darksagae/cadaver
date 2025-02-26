# cadaver
Cadaver is a command-line WebDAV client that allows users to interact with WebDAV servers, enabling file management over the web. It is useful for tasks like uploading, downloading, and managing files on remote servers.

### Installation
On Kali Linux, you can install Cadaver using the following command:

```bash
sudo apt-get install cadaver
```

### Basic Usage
Once installed, you can start using Cadaver by connecting to a WebDAV server:

```bash
cadaver http://example.com/webdav
```

### Common Commands
Here are some common commands you might use within Cadaver:

- **ls**: List files and directories in the current directory on the server.
  
  ```bash
  ls
  ```

- **cd**: Change the directory on the server.
  
  ```bash
  cd folder_name
  ```

- **get**: Download a file from the server.
  
  ```bash
  get filename.txt
  ```

- **put**: Upload a file to the server.
  
  ```bash
  put localfile.txt
  ```

- **delete**: Remove a file from the server.
  
  ```bash
  delete filename.txt
  ```

- **mkdir**: Create a new directory on the server.
  
  ```bash
  mkdir new_directory
  ```

- **exit**: Exit the Cadaver session.

### Example Usage
1. **Connect to the Server**
   ```bash
   cadaver http://example.com/webdav
   ```

2. **List Files**
   ```bash
   cadaver> ls
   ```

3. **Upload a File**
   ```bash
   cadaver> put myfile.txt
   ```

4. **Download a File**
   ```bash
   cadaver> get serverfile.txt
   ```

5. **Delete a File**
   ```bash
   cadaver> delete oldfile.txt
   ```

6. **Create a Directory**
   ```bash
   cadaver> mkdir new_folder
   ```

### Example Output
When you run `ls`, you might see output like:

```
  File:   document.txt
  File:   image.png
  Directory:   new_folder
```

When you upload a file, the output might confirm success:

```
Uploading myfile.txt to '/myfile.txt': 100% (4096 bytes) 0.04s
```

### Conclusion
Cadaver is a powerful tool for managing files over WebDAV, providing a command-line interface that is efficient for various file operations.




                                ALTERNATIVE
Cadaver is a Kali Linux tool used for web distributed authoring and versioning (WebDAV) attacks. WebDAV is a protocol that extends the HTTP protocol, allowing users to collaboratively edit and manage files on remote web servers.

Here's how you can use the Cadaver tool:

1. **Installation**: Cadaver is pre-installed in Kali Linux. If you're using another Linux distribution, you can install it using your package manager, e.g., `sudo apt-get install cadaver` on Ubuntu/Debian-based systems.

2. **Connecting to a WebDAV server**: To connect to a WebDAV server, use the following command:

   ```
   cadaver http://example.com/webdav/
   ```

   Replace `http://example.com/webdav/` with the actual URL of the WebDAV server you want to access.

3. **Listing directory contents**: Once connected, you can list the contents of the current directory on the WebDAV server using the `ls` command.

4. **Uploading files**: To upload a file to the WebDAV server, use the `put` command:

   ```
   put local_file.txt remote_file.txt
   ```

   This will upload the local file `local_file.txt` to the remote file `remote_file.txt` on the WebDAV server.

5. **Downloading files**: To download a file from the WebDAV server, use the `get` command:

   ```
   get remote_file.txt local_file.txt
   ```

   This will download the remote file `remote_file.txt` to the local file `local_file.txt`.

6. **Creating directories**: You can create a new directory on the WebDAV server using the `mkdir` command:

   ```
   mkdir new_directory
   ```

7. **Deleting files and directories**: To delete a file, use the `delete` command:

   ```
   delete remote_file.txt
   ```

   To delete a directory, use the `rmdir` command:

   ```
   rmdir remote_directory
   ```

8. **Exiting Cadaver**: To exit the Cadaver tool, use the `exit` command.

Example output:

```
dav://example.com/webdav/> ls
Listing collection `/webdav/': succeeded.
     Name                           Size  Last modified
----------------------------------------------------------
     file1.txt                        12  Feb 26 2025 12:34
     file2.txt                        20  Feb 25 2025 15:22
     directory/                       -  Feb 24 2025 09:45

dav://example.com/webdav/> put local_file.txt remote_file.txt
Uploading local_file.txt to remote_file.txt: succeeded.

dav://example.com/webdav/> get remote_file.txt local_file.txt
Downloading remote_file.txt to local_file.txt: succeeded.

dav://example.com/webdav/> mkdir new_directory
Creating new directory `/webdav/new_directory': succeeded.

dav://example.com/webdav/> delete remote_file.txt
Deleting `/webdav/remote_file.txt': succeeded.

dav://example.com/webdav/> rmdir directory
Removing `/webdav/directory': succeeded.

dav://example.com/webdav/> exit
```

Remember, the use of Cadaver should be limited to authorized and legal activities only. Ethical and responsible use of this tool is essential.




                                ALTLERNATIVE
**Cadaver** is a command-line tool for WebDAV (Web Distributed Authoring and Versioning) that allows users to interact with web servers that support the WebDAV protocol. Although Cadaver itself is not specifically a Kali tool, it can be used in penetration testing scenarios to explore web servers that implement WebDAV.

### Installing Cadaver

If you haven't installed Cadaver yet, you can do so on Kali Linux with the following command:

```bash
sudo apt-get install cadaver
```

### Basic Usage

Once installed, you can use Cadaver to connect to a WebDAV server. The basic syntax is:

```bash
cadaver <URL>
```

### Examples

#### 1. Connecting to a WebDAV Server

```bash
cadaver http://example.com/webdav/
```

This command connects to the specified WebDAV URL. You'll be prompted for authentication if required.

#### 2. Listing Files and Directories

After connecting, you can list files and directories using the `ls` command:

```bash
dav:/> ls
```

#### 3. Uploading a File

To upload a file to the server, use the `put` command:

```bash
dav:/> put localfile.txt remotefile.txt
```

This uploads `localfile.txt` from your local machine to the server as `remotefile.txt`.

#### 4. Downloading a File

To download a file from the server, use the `get` command:

```bash
dav:/> get remotefile.txt localfile.txt
```

This downloads `remotefile.txt` from the server to your local machine as `localfile.txt`.

#### 5. Creating a Directory

You can create a new directory on the server with the `mkdir` command:

```bash
dav:/> mkdir new_directory
```

#### 6. Deleting a File

To delete a file from the server, use the `delete` command:

```bash
dav:/> delete remotefile.txt
```

### Example Output

When you list files with the `ls` command, you might see output like this:

```
Listing collection at /webdav/:
drwxr-xr-x   2 user group     4096 Jan 01 00:00 new_directory
-rw-r--r--   1 user group      123 Jan 01 00:00 remotefile.txt
```

### Important Notes

- **Authentication**: Many WebDAV servers require authentication. You may need to provide credentials when prompted.
- **Security**: Be cautious when interacting with WebDAV servers, especially those that you do not own or manage, as unauthorized access may be illegal.

### Conclusion

Cadaver is a powerful tool for interacting with WebDAV servers. Familiarizing yourself with its commands can enhance your capabilities in web-based file management and penetration testing. Always ensure you have permission to access and modify the resources you are working with.



                         ALTERNATIVE
Cadaver is a command-line WebDAV client for Unix, and it is included in Kali Linux. It allows you to manipulate files and directories on a WebDAV server, similar to how you would use the `ftp` command to interact with an FTP server.

Here's a basic usage guide for Cadaver:

**Syntax:**
```
cadaver [options] <url>
```
**Options:**

* `-h` or `--help`: Display help and exit
* `-v` or `--verbose`: Increase verbosity
* `-q` or `--quiet`: Decrease verbosity
* `-d` or `--debug`: Enable debug mode
* `-u` or `--username`: Specify the username for authentication
* `-p` or `--password`: Specify the password for authentication

**Examples:**

1. **Connect to a WebDAV server:**
```
cadaver https://example.com/webdav
```
This will prompt you for a username and password, and then you'll be connected to the WebDAV server.

2. **List files and directories:**
```
cadaver> ls
```
This will display a list of files and directories on the WebDAV server.

3. **Create a new directory:**
```
cadaver> mkdir mynewdir
```
This will create a new directory named "mynewdir" on the WebDAV server.

4. **Upload a file:**
```
cadaver> put localfile.txt /remote/path/
```
This will upload a file named "localfile.txt" from your local machine to the specified remote path on the WebDAV server.

5. **Download a file:**
```
cadaver> get /remote/path/remotefile.txt
```
This will download a file named "remotefile.txt" from the specified remote path on the WebDAV server to your local machine.

6. **Delete a file:**
```
cadaver> delete /remote/path/remotefile.txt
```
This will delete a file named "remotefile.txt" from the specified remote path on the WebDAV server.

**Output:**

The output of Cadaver will vary depending on the command you execute. Here are some examples:

* **ls** command:
```
 cadaver> ls
drwxr-xr-x  1 user group  0 Jan  1  2022  dir1
-rw-r--r--  1 user group 123 Jan  1  2022  file1.txt
drwxr-xr-x  1 user group  0 Jan  1  2022  dir2
```
This output shows a list of files and directories on the WebDAV server, along with their permissions and timestamps.

* **put** command:
```
cadaver> put localfile.txt /remote/path/
Uploading localfile.txt to /remote/path/
Transfer complete.
```
This output indicates that the file "localfile.txt" was successfully uploaded to the specified remote path on the WebDAV server.

* **get** command:
```
cadaver> get /remote/path/remotefile.txt
Downloading /remote/path/remotefile.txt to remotefile.txt
Transfer complete.
```
This output indicates that the file "remotefile.txt" was successfully downloaded from the specified remote path on the WebDAV server to your local machine.





                        ALTERNATIVE
Cadaver is a command-line WebDAV (Web-based Distributed Authoring and Versioning) client for Unix-like operating systems, including Kali Linux. It allows users to interact with WebDAV servers, which enable collaborative editing and management of files on remote web servers. Cadaver supports file upload, download, on-screen display, in-place editing, namespace operations (move/copy), collection creation and deletion, property manipulation, and resource locking.

### How to install Cadaver on Kali Linux

```bash
sudo apt update
sudo apt install cadaver
```

### Basic Cadaver usage

1.  **Connecting to a WebDAV Server:**

    ```bash
    cadaver http://example.com/webdav/
    ```
2.  **Basic Commands:**

*   `ls`: Lists the contents of the current or specified WebDAV directory.
*   `cd <directory>`: Changes the current directory to the specified directory on the WebDAV server.
*   `pwd`: Displays the current directory path on the WebDAV server.
*   `get <remote_file> [local_file]`: Downloads a file from the WebDAV server to your local machine. If `local_file` is not specified, the file will be saved with the same name.
*   `put <local_file> [remote_file]`: Uploads a file from your local machine to the WebDAV server. If `remote_file` is not specified, the file will be uploaded with the same name.
*   `edit <file>`: Edits a file on the WebDAV server.
*   `mkcol <directory>`: Creates a new directory (collection) on the WebDAV server.
*   `delete <file>`: Deletes a file from the WebDAV server.
*   `rmcol <directory>`: Deletes a directory (collection) and




                               ALTERNATIVE
  Cadaver is a command-line WebDAV client available in Kali Linux, designed for managing files on remote web servers. It allows users to upload, download, edit, and manage files collaboratively using the WebDAV protocol. Here’s how to use Cadaver, along with some examples and expected outputs.

### Installation
To install Cadaver on Kali Linux, use the following command:
```bash
sudo apt install cadaver
```

### Basic Usage
To start using Cadaver, you need to connect to a WebDAV server by specifying its URL. The command format is:
```bash
cadaver [URL]
```
For example:
```bash
cadaver http://example.com/webdav/
```

### Common Commands
Once connected, you can use various commands. Here are some key commands along with examples:

1. **List Files**: To display files in the current directory, use:
   ```bash
   ls
   ```
   **Output**: This will show a list of files and directories in the current WebDAV location.

2. **Upload Files**: To upload a single file, use:
   ```bash
   put filename.txt
   ```
   To upload multiple files that share a common prefix, use:
   ```bash
   mput hr*
   ```
   **Output**: This will upload all files starting with "hr" to the server.

3. **Download Files**: To download a single file, use:
   ```bash
   get filename.txt
   ```
   To download multiple files, use:
   ```bash
   mget hr*
   ```
   **Output**: This will download all files starting with "hr" from the server to your local machine.

4. **Locking Files**: To lock a file while you work on it, use:
   ```bash
   lock filename.txt
   ```
   This prevents others from modifying the file until you unlock it.

5. **Unlocking Files**: Once you are done, unlock the file using:
   ```bash
   unlock filename.txt
   ```

6. **Help Command**: To see a list of available commands, type:
   ```bash
   help
   ```

### Example Session
Here’s a brief example of a Cadaver session:
```bash
$ cadaver http://example.com/webdav/
dav:/webdav/> ls
file1.txt
file2.txt
dav:/webdav/> put myfile.txt
Uploading myfile.txt to `/webdav/myfile.txt': 100% |**********|  1.00k  00:00 ETA
dav:/webdav/> get file1.txt
Downloading `file1.txt' to `file1.txt': 100% |**********|  1.00k  00:00 ETA
dav:/webdav/> lock file2.txt
dav:/webdav/> unlock file2.txt
dav:/webdav/> exit
```

In this session, the user connects to a WebDAV server, lists files, uploads a file, downloads another, locks a file, unlocks it, and then exits the session.

### Conclusion
Cadaver is a powerful tool for managing files on WebDAV servers, providing a range of commands for file operations. Its command-line interface is straightforward, making it accessible for users familiar with terminal commands.

---
Learn more:
1. [cadaver | Kali Linux Tools](https://www.kali.org/tools/cadaver/)
2. [18.7 Using Cadaver as a WebDAV Client](https://docs.oracle.com/cd/E21764_01/portal.1111/e10235/webdav007.htm)
3. [cadaver | Joe Orton](https://notroj.github.io/cadaver/)
                         
