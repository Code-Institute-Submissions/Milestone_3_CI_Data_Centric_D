<h1>MILESTONE 3 - CODE INSTITUTE</h1>
<h2>Overview</h2>
A web application created in Python and Flask. 
View website on <a href="https://milestone3-data-centric.herokuapp.com/" target="_blank">Heroku</a>
A recipe database where viewers can search and view recipes. 
Users can also add, edit or delete their own recipes.
<h2>UX</h2>
This website was created with the intention to store and share recipes with other users, in a simple uncluttered layout, to make it easy to navigate. The user can choose a specific recipe from the list where more details about the recipe will be displayed, such as: category (appetizers, entrees and desserts), ingredients, cooking method, servings, preparation time and difficulty level. This page also allows the user to delete or edit the recipe. Within the navbar the user has access to all recipes. There's also a link that brings to a form to add a new recipe.
<h3>User Stories</h3>
<ul>
<li>As a user I would like to search and view recipes by keywords or categories.</li>
<li>I would like to add my own recipes into the database.</li>
<li>I would like to able to edit and delete recipes.</li>
</ul>
<h2>Features</h2>
<ul>
<li><strong>C</strong>reate new recipes - recipe name, category, level of difficulty, servings, preparation time, method, ingredients.</li>
<li><strong>R</strong>ead recipes</li>
<li><strong>U</strong>pdate recipes</li>
<li><strong>D</strong>elete recipes</li>
</ul>
<h2>Features left to implement</h2>
<h4>User authentication</h4>
As it is any user can update and delete recipes, which could lead to the recipe information being amended/deleted maliciously. In order to amend this I would like to have implemented a user authentication system that would mean only the original author of the recipe has the power to edit or remove it.
<h4>Pagination</h4>
To handle that the number of recipe results doesn't become too long, as the database grows.
<h2>Technologies used</h2>
<ul>
<li><a href ="https://getbootstrap.com/" target="_blank">Bootstrap</a></li>
Bootstrap is the most popular CSS Framework for developing responsive and mobile-first websites.
<li><a href="https://www.python.org/" target="_blank">Python</a></li>
<p> An interpreted, high-level, general-purpose programming language.
<li><a href="https://flask.palletsprojects.com/en/1.1.x/" target="_blank">Flask</a></li>
Flask is a micro web framework written in Python. It is classified as a microframework because it does not require particular tools or libraries.
<li><a href="https://www.mongodb.com/" target="_blank">MongoDB</a></li>
A general purpose, document-based, distributed database built for modern application developers and for the cloud era.
<li><a href="https://flask-pymongo.readthedocs.io/en/latest/>" target="_blank">Flask-Pymongo</a></li>
Flask-PyMongo bridges Flask and PyMongo and provides some convenience helpers.
<li><a href="https://materializecss.com/" target="_blank">Materialize</a></li>
A modern responsive front-end framework based on Material Design.
</ul>
<h2>Testing</h2>
All the CRUD actions were tested and are working as it should.   
The responsiveness was tested on every page. 
Every link was tested and works properly. 
All forms handle empty input fields.
<h2>Deployment</h2>
Deployment and source control was carried out via GitHub and Heroku. The following steps were taken to deploy the website:
<ul>
<li>Database was created in MongoDB Atlas</li>
<li>Project workspace was created in GitPod. In this workspace: Flask was installed - pip3 install flask</li>
<li>Setup app.py file and imported flask and os - from flask import Flask. import os</li>
<li>Created an instance of flask - app = flask(__name__)</li>
<li>Inside the app run() function set the host, ip and debug=true</li>
<li>Create a new Heroku App - unique name and EU Server</li>
<li>In GitPod login to Heroku through CLI to confirm existance of app. CLI: heroku login</li> 
<li>gitpod /workspace/M3-CI-DCD $ heroku login -i</li>
<li>heroku: Enter your login credentials</li>
<li>Email: roxana.hefferon@gmail.com</li>
<li>Password: **********</li>
<li>CLI: heroku apps</li>
<li>Create a git repository in GitPod. CLI: git init. CLI: git add . CLI: git commit -m "Initial Commit"</li>
<li>Connect GitPod to Heroku. Use code found on Heroku. CLI - $heroku git remote -a</li>
<li>Create requirements.txt file - CLI: pip3 freeze --local > requirements.txt</li>
<li>Create Procfile - echo web:python app.py>Procfile</li>
<li>Add and Commit to Git Repository</li>
<li>Push to Heroku using code supplied by Heroku.</li>
<li>CLI - heroku ps:scale web=1 Command to tell Heroku to run the app</li>
<li>Log in to Heroku to add config variables including IP, Port, Mongo_DB and Mongo_URI</li> 
<ul><li>Set Config Vars adding IP and PORT on Heroku app settings</li>
<li>IP 0.0.0.0 - PORT 5000</li></ul>
<h5>Install the Heroku CLI</h5>
<p>Download and install the Heroku CLI</p>
<p>If you haven't already, log in to your Heroku account and follow the prompts to create a new SSH public key</p>
<p>$ heroku login</p>
<h5>Create a new git repository</h5>
<p>Initialize a git repository in a new or existing directory</p>
<p>$ cd my-project/</p>
<p>$ git init</p>
<p>$ heroku git:remote -a data-centric-m3-ci</p>
<h5>Deploy your application</h5>
<p>Commit your code to the repository and deploy it to Heroku using Git</p>
<p>$ git add .</p>
<p>$ git commit -am "make it better"</p>
<p>$ git push heroku master</p>
<h5>Existing Git repository<h5>
<p>For existing repositories, simply add the heroku remote</p>
<p>$ heroku git:remote -a data-centric-m3-ci</p>
<h3>Running the code locally</h3>
<ul>
<li>Under the repository name on GitHub, click Clone or download</li>
<li>In the Clone with HTTPs section, click the icon beside the URL to copy the clone URL for the repository</li>
<li>Change the current working directory to the location where you want the cloned directory to be made</li>
<li>Type git clone, and then paste the URL you copied for the repository</li>
<li>Press Enter. Your local clone will be created</li>
<li>Set up a virtual environment</li>
<li>Install the packages in requirements.txt by typing pip3 install -r requirements.txt in the CLI</li>
<li>Set the IP address to 127.0.0.1 and the PORT to 5000</li>
</ul>
<h2>MongoDB Structure</h2>
<p>recipe_manager.recipe</p>
<p>{"_id":{"$oid":"5eb53ab9f5a3f431259becc4"},</p>
<p>"category_name":"",</p>
<p>"recipe_name":"",</p>
<p>"recipe_description":"",</p>
<p>"is_vegetarian":"",</p>
<p>"ingredientes":"",</p>
<p>"method":"",</p>
<p>"servings":"",</p>
<p>"difficulty":"",</p>
<p>"cook_time":""}"}</p>
<br>
<p>recipe_manager.categories</p>
<p>{"_id":{"$oid":"5eb5d6014faee9a32d0ebe3e"},</p>
<p>"category_name":""}"}</p>
<br>
<p>recipe_manager.difficulty</p>
{"_id":{"$oid":"5eb5da874faee9a32d0ebe41"},</p>
"difficulty_level":""}"}</p>
<br>
<p>recipe_manager.users</p>
<p>{"_id":{"$oid":"5eb5d7624fahe9a90d0ele7e"},</p>
<p>"username":"",</p>
<p>"password":""}"}</p>
<h2>Validation</h2> 
<h3>CSS</h3>
<a href="https://jigsaw.w3.org/css-validator/" target="_blank">Jigsaw</a> was used for validation of css code and did not generate significant errors.
<h3>HTML</h3>
<a href="https://validator.w3.org/" target="_blank">HTML validator</a> was used for validation of HTML code. Errors were thrown on the raw HTML code by the use of Jinja2 templating language which was not recognised by the validator.
<h3>jQuery</h3>
<a href="https://codebeautify.org/jsvalidate" target="_blank">Code Beautify</a> and <a href="https://jshint.com/">JShint</a> target="_blank"> were used for validation of jQuery code. No significant erros were generated.
<h3>Python</h3>
<a href="http://pep8online.com/" target="_blank">PEP8</a> was used to validate Python code and did not generate any errors
<h3>HTML Beautifier</h3>
<a href="http://minifycode.com/html-beautifier/" target="_blank">Minify Code</a> was used to beautify HTML code.
<h2>Credits</h2>
<p>The recipes used to start the database were taken from <a href="https://www.jamieoliver.com/" target="_blank">Jamie Oliver's Website</a></p>
<p>Logo created in <a href="https://www.canva.com/">Canva</a></p>
<p>Favicon created in <a href="https://www.favicon-generator.org/">Favicon</a></p>
<a href="https://images.unsplash.com/photo-1517953720815-3ad3488a67f1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1525&q=80" target="_blank">Image</a> from <a href="www.unsplash.com">Unsplash</a>
<h2>Acknowledgements</h2>
<ul>
<li>The Code Institute Slack community, where I have found many answers to many questions and learned a huge amount by reading through the posts.</li>
<li>W3SCHOOLS.</li>
<li>Stack Overflow.</li>
</ul>
<h2>Disclaimer</h2>
For educational purposes only.



