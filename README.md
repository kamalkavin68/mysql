<h1>Install MySQL server 8.0.23 using a noinstall Exe Zip archive</h1>

<h4>The steps to install MySQL is as the following:</h4>

<h4><li>Download and extract the files</li></h4>
<p>
    First, let us download the Zip archive of MySQL 8.0 from the download page. On the <a href="https://dev.mysql.com/downloads/mysql/">download</a> page, choose Microsoft Windows from the Select operating System drop-down page. Select Windows (x86, 64-bit) ZIP archive.
</p>

<img src="https://github.com/kamalkavin68/mysql/blob/main/mysql-download-page.png" alt="" srcset="">

<p>
    Once the zip archives are downloaded, copy the files to your desired location and extract the files.
</p>

<img src="https://github.com/kamalkavin68/mysql/blob/main/extract-the-files.png" alt="">

<p>
    have created a directory named MySQL_Home on the C:\ drive of my workstation. We are using it as a home directory of MySQL. I have copied the extracted files to the C:\MySQL_Home directory.
</p>



<h4><li>Create MySQL configuration file</li></h4>

<p>
    The configuration file is used to initiate the MySQL database server. The file contains the following information.
</p>

<p>
    1. <b>Base directory:</b> The base directory to the installation. In our case, the <b>C:\MySQL_Home</b> is the base directory
</p>

<p>
    2. <b>Data directory:</b> The location of the data directory. In our case, <b>C:\MySQL_Data_Directory</b> is the data directory
</p>

<p>
    Create a new text file and enter the following parameters in it. We can use a plain text editor (notepad or notepad++) to create the configuration file.
    <a href="https://github.com/kamalkavin68/mysql/blob/main/config.ini">File like this</a>
</p>

<img src="https://github.com/kamalkavin68/mysql/blob/main/configuration-file.PNG" alt="" srcset="">

<p>
    Save the file as my.ini in the <b>C:\MySQL_Home directory</b> and close the editor.
</p>

<h4><li>Initialize the data directories and system databases</li></h4>

<p>
    The ZIP archive of MySQL does not include the data directory; therefore, we must initialize it manually. When we initialize it, MySQL creates the MySQL system database files and system tables in the location specified in the options file.

To initialize MySQL and create MySQL system databases, we must run the mysqld command with the –initialize or –initialize-insecure option. The details of both options are the following:

1. The –initialization option is considered secure by default. When we use this option, MySQL generates a random root password. Once installation completes, the root password will be expired, and you must create a new root password
2. When we use the –initialize-insecure option, we do not need to specify the root password. It is considered that the user will create the root password before moving on to production. In simple words, we must create a root password before putting this server for production usage
Before starting the service, we can determine the MySQL Server type. We can configure two types of MySQL Server on Windows.

Mysqld: These are optimized binary files and have named-pipe support
Mysqld-debug: These are optimized binary and compiled with full debugging. It has automatic memory allocation checking
In this demo, we will use the mysqld binaries. I am installing MySQL on my workstation to initialize the MySQL data directories; I am using the –initialize-insecure option.

Open the command prompt as an administrator user. First, navigate to the MySQL_Home\bin directory using the cd command.:
</p>
