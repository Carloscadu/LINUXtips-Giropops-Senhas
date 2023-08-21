FROM python:3.11-slim
#RUN apt-get update && apt-get install -y pip
WORKDIR /root/giropops-senhas
COPY giropops-senhas/requirements.txt /root/giropops-senhas/
COPY giropops-senhas/app.py .
COPY giropops-senhas/templates templates/
COPY giropops-senhas/static static/
RUN apt-get update && apt-get install -y pip && pip install --no-cache-dir -r requirements.txt
EXPOSE 5000
CMD ["flask", "run", "--host=0.0.0.0"]
