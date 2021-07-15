FROM python:2.7-stretch as api
MAINTAINER YoussoufouOusmanou(youssoufa.ousman@gmail.com)
RUN apt-get update
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0
ADD student_age.py /
VOLUME /data
EXPOSE 5000
ENTRYPOINT ["python", "./student_age.py"]

#docker run --name monapi -p 8080:5000 -d -v /root/Mini-Projet-Docker/simple_api/student_age.json:/data/student_age.json mon_api
#docker run --name monapi -p 8080:5000 -d -v /home/admin/Mini-Projet-Docker/simple_api/student_age.json:/data/student_age.json mon_api
