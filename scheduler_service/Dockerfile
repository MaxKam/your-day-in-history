# Command to build Docker image must be run from top level project folder,
# otherwise the contents of the protos folder will not be copied to the image.
# Example: docker build -f ./scheduler_service/Dockerfile -t history_scheduler .

FROM python:3.8-alpine
WORKDIR /app/
COPY ./scheduler_service/ /app/
COPY ./protos/ /app/rpc_classes
RUN pip install --trusted-host pypi.python.org -r /app/requirements.txt
CMD ["python","/app/scheduler.py"]
