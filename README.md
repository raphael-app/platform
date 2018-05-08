# RAPHAEL - RESTAURANT LISTING APP - PLATFORM

#### What is that ? 

Raphael is a simple Django backed React-ish Restaurant Listing App was designed and developed by Muhammet Arslan. On that project, there are 3 repositories to be required for Raphall App.
- Raphael, is a Django powered backed application. Providing the main APIs via Rest + Oauth.
- RLA, is a React-ish frontend application. Consuming APIs and serving the content to the end-user
- Platform, is a Docker-based project. Contains Localbox, Dockerfiles and Kubernet-ish (in future!) manifestos.

#### Locally ? 

You want to run RAPHAEL application on your Local ? Nothing could be easier than that. Just paste the following commands and done!

Create a base directory to be sure, we are working clean!
```
mkdir /raphael/ && cd /raphael/ (or whenever you want to hold the project)
```
Clone the repos
``````
git clone https://github.com/raphael-app/platform.git
git clone https://github.com/raphael-app/raphael.git
git clone https://github.com/raphael-app/rla.git
``````
Run the localbox
```
docker-compose -p 'Raphael' up -d --build
```

Okay, now our localbox is ready! But we need to run our migrations for first time use.

Ssh to  docker container.
```
docker exec -it raphael-local-app bash
```
Prepare/Migrate the models
```
python3 manage.py makemigrations
python3 manage.py migrate
``` 
Create the first super user (Don't forget to fill the prompts)
```
python3 manage.py createsuperuser
```

Okay, now you are ready to use Raphael on your local. Browse to "http://localhost:8000" and bam!

For deep informations, please browse to application READMEs!


