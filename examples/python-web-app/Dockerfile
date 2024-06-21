FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app
# I have added   --break-system-packages to pip install command as I was getting an error as   error: externally-managed-environment
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install -r requirements.txt --break-system-packages && \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




