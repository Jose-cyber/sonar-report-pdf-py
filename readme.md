GENERATE REPORT PDF FOR SONARQUBE

Env var:
component->project_key
sonar_edpoint->sonar_address
user->sonar_user
password->sonar_password

Docker Build:
docker build -t sonar-report . -f .docker/Dockerfile

Docker Run:
docker run --rm -e component=project_name -e sonar_edpoint=https://sonar.example.com -e user=admin -e password=admin -v $PWD:/app/result sonar-report
