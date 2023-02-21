FROM python:3.10-slim-buster

#Inside the container
#make a new folder inside the container
WORKDIR /backend-flask

# Outside Container --> Inside Container
# this contains the libraries we want to install o run the app
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

#python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]