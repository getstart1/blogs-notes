Sept 3, 2018

1. What is TypeScript:
	Basicially, it is a superset of JavaScript. The code written in TypeScript would compile into JavaScript file. The syntax is simpler than JavaScript. It can be used in the major text editors and visual studio.It can also be used in AngularJS, Protractor(a testing tool for AngularJS app), Jasmine for automation testing. 
	
resource: https://www.youtube.com/watch?v=bAPJ2W6Fr4Q

2. Why not able to update the npm version on my mac? 

After I navigate to the '/usr/local/lib/node_modules', I added 'qdai' as one of the administrator and chose the 'read and write' permission.
The step I cannot miss is that: Tap Operation pop-up menu , select "applies to an included."

Then I found out that some packages are missing in my folder. I decide to delete the current one and reinstall the npm package.

Somehow, reinstallation works, but the terminal still says that the update process failed without specify the error. 

Then I was able to install 'create-react-app' tool. 

3. Error "Failed to compile" appears

```
/Users/qdai/first_app/node_modules/@types/react/index.d.ts
(2305,19): Interface 'Element' cannot simultaneously extend types 'ReactElement<any>' and 'ReactElement<any>'.
  Named property 'type' of types 'ReactElement<any>' and 'ReactElement<any>' are not identical.
```

4. How to kill the application running on certain port? 
tried command that works: 
```lsof -P | grep ':PortNumber' | awk '{print $2}' | xargs kill -9```

When I delete an extra @Type folder, the React application can be compiled without error. 

5. It is easy to lose certain package if delete some package for wrong. I suspect that each time when the code is compiled and build app, a new @type folder would be generated...
It is important to generate @type folder in each module. Just follow the error message as the following: 

```
Could not find a declaration file for module 'react-bootstrap'. '/Users/qdai/node_modules/react-bootstrap/lib/index.js' implicitly has an 'any' type.
Try `npm install @types/react-bootstrap` if it exists or add a new declaration (.d.ts) file containing `declare module 'react-bootstrap';`
```
This problem can be resolved by using the following command: 
	```npm install -D @types/module-name```
	
	
Conclusion for the first part--build a basic React web application Framework:	
After I follow the basic instructions about how to run the react app provided by MSA, I understand:
1) React provides a framework for building web application or software application. By following the instruction provided, I can create a basic template for my web application. 
2) It is important to implement some libraries into react app. 
3) There is one important file in the React application, which is the 'router.tsx'. This is a file that takes care of the navigation between different pages. In order to make this file works, we need to install the React Router package. 
4) There is only one html file which is the 'index.html' file in the public folder, and it is linked with a 'index.tsx' file. These two files are linked through the following way:
https://stackoverflow.com/questions/41738421/how-react-js-index-js-file-contacting-index-html-for-id-references

Next step: Apply some details in the application. For instance:
1) How to add paragraphs (done!)
2) How to change the navigation. link to different pages.  
⋅⋅1. add a new tab(done!)
			⋅⋅*In order to deploy a new tab. add route path in the file 'router.tsx'
			⋅⋅*import component from its ancester file-- eg. import ThirdComponent from './components/ThirdComponent'
			⋅⋅*create the component file
			⋅⋅*update 'Header.tsx' file, add new navigation bar
⋅⋅2. hyperlink(done!) -- as normal (done!)
	```<a href= "">
	```
3) How to add images(done!)
		```
		import image1 from './images/tree.jpg';
		 <img src={image1} width= "100" height= "50"/>
		```
4) How to implement API

resource: https://blog.hellojs.org/fetching-api-data-with-react-js-460fe8bbf8f2



Now I search on some tags that I did not meet before in order to understand more basic code:
1) <noscript> : This is for showing the alternative content for users if the browser does not support the script. 
resource: https://www.w3schools.com/tags/tag_noscript.asp
2) I am confused by what is index.html 's role in this application, since the default page is not specified here? (Need more research) 







 