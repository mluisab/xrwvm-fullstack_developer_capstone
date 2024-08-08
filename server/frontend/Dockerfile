^O
FROM python:3.12.0-slim-bookworm

# Set environment variables
ENV PYTHONUNBUFFERED=1
ENV PYTHONWRITEBYTECODE=1
ENV APP=/app

# Change the working directory
WORKDIR $APP

# Add the requirements.txt file and install the dependencies
COPY requirements.txt $APP/
RUN pip install --upgrade pip && pip install -r requirements.txt

# Copy the rest of the application code
COPY . $APP/

# Expose port 8000
EXPOSE 8000

# Ensure the entrypoint script is executable
RUN chmod +x /app/entrypoint.sh

# Set the entrypoint script and the command to start the application
ENTRYPOINT ["/bin/bash", "/app/entrypoint.sh"]
CMD ["gunicorn", "--bind", ":8000", "--workers", "3", "djangoproj.wsgi"]

^T

^R

^X

x

X

