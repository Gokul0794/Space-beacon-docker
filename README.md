cat Dockerfile 
FROM python:3.9-slim-buster
WORKDIR /app
ADD . /app
RUN pip install --no-cache-dir -r requirements.txt
EXPOSE 80
ENV NAME World
CMD ["python", "app.py"]
cat app.py 
from flask import Flask
app = Flask(_name_)

@app.route('/')
def hello():
    return "Greetings from the DevOps Squadron!"

if _name_ == '_main_':
    app.run(host='0.0.0.0', port=80
