FROM python:3.8.0-alpine3.10

# Copy the src
WORKDIR /app
COPY src/ /app/src/
COPY ./requirements.txt /app

# Install python dependencies
RUN pip3 install --upgrade pip
RUN pip3 install --no-cache-dir -r /app/requirements.txt


# EXPOSE 80
EXPOSE 80
CMD ["python3", "/app/src/app.py"]
#CMD  python3 /app/src/app.py
