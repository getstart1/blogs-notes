August 29th, 2018 

Today I review the Openwords lesson builder website for several reasons. First, I think that this is a good opportunity for me to refresh my memory about JQuery and JavaScript. Second, I want to reorganize my thoughts about this project. 


August 30th, 2018
Today, I continue trying about connecting local server with XAMPP's database. 

What is XAMPP： it is a open source cross-platform web server solution stack package developed by Apache Friends. It consists Apache HTTP server, MySQL database...

In order to write a PHP file and run on the local server, we need to follow the following steps:
1) run XAMPP, start the local server and all the services(Mysql, proFTPD, Apache)  -- this is for opening the services
2) write a PHP file -- PHP file includes the code for connect to the database that associates with the server. 
3) Put the PHP into this folder belongs to XAMPP: ~/htdocs
	After entering this folder, I can create a new folder. Put php file into this new folder, easier to manage the file later. 
	
My failure was because I put the file into a different XAMPP folder, but not the one that associates with the server. For mac, it is under the Shared category, and there is an IP address. Click this IP address, then I will be able to find the target 'htdocs' folder. 


After figuring out how to open a php web page in a server, next step is to actually connect to the database. 

The code I used to connect to connect to the database is as the following: 
```PHP
$servername = "localhost";
$username= "root";
$password= "";
$conn= new mysqli($servername,$username,$password);

//check connection
if($conn -> connect_error){
    die("Connection failed: ". $conn->connect_error);
}
else{
    echo"Server connected successfully";
}
```

The code I used to create a new database is as the following:
```PHP
$sql= "CREATE DATABASE newDB1";
if ($conn-> query($sql) == TRUE){
    echo"Database created successfully";
}else {
    echo"Error creating database". $conn->error;
}
```

The tutorial I followed that works is: 
https://www.w3schools.com/php/php_mysql_create.asp


After creating a new database, then I created a new table inside the database 'newDB1' that just created by myself. The code is as the following:
```PHP
<?php
$servername = "localhost";
$username= "root";
$password= "";
$dbname="newDB1";
$conn= new mysqli($servername,$username,$password,$dbname);

//check connection
if($conn -> connect_error){
    die("Connection failed: ". $conn->connect_error);
}
else{
    echo"Server connected successfully";
}


$sql = "CREATE TABLE Manage_user(
    username VARCHAR(20) NOT NULL,
    password VARCHAR(30) NOT NULL,
    email VARCHAR(50) NOT NULL,
    reg_data TIMESTAMP
)";

if (mysqli_query($conn, $sql)){
    echo "Table Manage_user created successfully";
} else {
    echo "Error creating table". mysqli_error($conn);
}

?>
```

After creating a new table, I tried to insert value into this table.
The code is as the following:

``` PHP
<?php
$servername = "localhost";
$username= "root";
$password= "";
$dbname="newDB1";
$conn= new mysqli($servername,$username,$password,$dbname);

//check connection
if($conn -> connect_error){
    die("Connection failed: ". $conn->connect_error);
}
else{
    echo"Server connected successfully";
}


$sql = "INSERT INTO Manage_user(username,password,email)
VALUES ('qd1', '127ty', 'qdai0723@gmail.com')";

if($conn->query($sql) === TRUE){
    echo "New record created successfully";
}else{
    echo"Error:".$sql . "<br>". $conn->error;
}

?>

```

My next step is to create 3 textbox, then link these textbox with the table 'Manage_user'. Insert value to that table by entering value in these textboxes.
