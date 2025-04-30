FROM python:3.11

# Set the working directory in the container
WORKDIR /app

# Copy requirements and install dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copy the entire project into the container
COPY . .

# Run database migrations
RUN python manage.py migrate

# Expose the application port
EXPOSE 8000

# Run the App
CMD ["python","manage.py","runserver","0.0.0.0:8000"]


