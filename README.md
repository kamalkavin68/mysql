<h1>Install MySQL server 8.0.23 using a noinstall Exe Zip archive</h1>

<h4>The steps to install MySQL is as the following:</h4>

<li><h4>Download and extract the files</h4></li>
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



<li><h4>Create MySQL configuration file</h4></li>

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
</p>

<a href="https://github.com/kamalkavin68/mysql/blob/main/config.ini">File like this</a>

