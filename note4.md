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
