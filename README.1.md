
Check if s3 created with name: 
	clo835-bg-zahrah

 upload image called background.jpg 
export IMAGE_URL=s3://clo835-bg-zahrah/background.jpg
python3 app.py
Build images
docker build -t my_db -f Dockerfile_mysql . 
docker build -t my_app -f Dockerfile . 
docker run -d -e MYSQL_ROOT_PASSWORD=pw  my_db
docker inspect <container_id>
export DBHOST=172.17.0.2
export DBPORT=3306
export DBUSER=root
export DATABASE=employees
export DBPWD=pw
export APP_COLOR=blue
docker run -p 8080:8080 -e APP_COLOR=$APP_COLOR -e DBHOST=$DBHOST -e DBPORT=$DBPORT -e DBUSER=$DBUSER -e DBPWD=$DBPWD  my_app
