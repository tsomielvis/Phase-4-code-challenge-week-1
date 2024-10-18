Skip to content
Navigation Menu
Marcos-tech003
/
SuperHeroes-codechallenge

Type / to search
Code
Issues
Pull requests
Actions
Projects
Security
Insights
Owner avatar
SuperHeroes-codechallenge
Public
Marcos-tech003/SuperHeroes-codechallenge
Go to file
t
Add file
Folders and files
Name		
Latest commit
Marcos-tech003
Marcos-tech003
Update README.md
3ba1bac
 · 
2 days ago
History
instance
updated corection
2 days ago
migrations
updated corection
2 days ago
models
updated corection
2 days ago
Pipfile
updated corection
2 days ago
Pipfile.lock
updated corection
2 days ago
README.md
Update README.md
2 days ago
app.py
updated corection
2 days ago
config.py
code intergration
last week
routes.py
updated corection
2 days ago
seed.py
updated corection
2 days ago
Repository files navigation
README
SuperHeroes Code Challenge
This project is a RESTful API built with Flask and Flask-SQLAlchemy. It tracks superheroes and their unique superpowers, following a one-to-many relationship. The project is structured to follow best practices in Python and API development.

Features
Superhero Management: Add, update, and delete superheroes.
Power Management: Add, update, and delete superpowers.
HeroPower Assignment: Assign powers to superheroes with additional attributes such as the hero's rating for a given power.
Models
Hero

Attributes: id, name, super_name
Relationships: A hero can have many powers through the HeroPower model.
Power

Attributes: id, name, description
Relationships: Powers can be linked to multiple heroes through the HeroPower model.
HeroPower

Attributes: id, strength (values: Weak, Average, Strong), hero_id, power_id
Relationships: A join table to connect heroes and powers, with an additional attribute for the power's strength in the hero.
Installation
Prerequisites
Python 3.8.x
Flask
Flask-SQLAlchemy
Flask-Migrate
pytest (for testing)
Setup
Clone the repository:

git clone https://github.com/Marcos-tech003/SuperHeroes-codechallenge.git
cd SuperHeroes-codechallenge
##Create and activate a virtual environment

python3 -m venv venv source venv/bin/activate # For Linux/macOS or venv\Scripts\activate # For Windows

##Install dependencies pip install -r requirements.txt

Set up the database
flask db init flask db migrate flask db upgrade

##Seed the database python seed.py

##Run the application flask run

The API will be available at http://127.0.0.1:5555.

API Endpoints
GET /heroes: Retrieve a list of all superheroes.

GET /heroes/ : Retrieve details for a specific hero.

POST /heroes: Create a new superhero.

PATCH /heroes/ : Update a specific hero's details.

DELETE /heroes/ : Remove a superhero from the database.

GET /powers: Retrieve a list of all superpowers.

GET /powers/ : Retrieve details for a specific power.

PATCH /powers/ : Update a specific power's details.

POST /heropowers: Assign a power to a superhero with a specific strength.

About
No description, website, or topics provided.
Resources
 Readme
 Activity
Stars
 0 stars
Watchers
 2 watching
Forks
 0 forks
Report repository
Releases
No releases published
Packages
No packages published
Languages
Python
96.3%
 
Mako
3.7%
Footer
© 2024 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact
Manage cookies
Do not share my personal information
Copied!
