FROM python:3.12-bookworm
ENV PYTHONUNBUFFERED=1
RUN apt-get update && apt-get install python3-dev libgdal-dev graphviz -y --force-yes
WORKDIR /usr/src/app
RUN pip install --upgrade pip && pip install --upgrade setuptools
COPY requirements.txt ./
RUN pip --no-cache-dir install -r requirements.txt
EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]