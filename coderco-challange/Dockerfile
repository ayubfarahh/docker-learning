FROM python:3.8-slim

wORKDIR /app

COPY . . 

RUN pip install flask redis

EXPOSE 5001

CMD ["python", "count.py"]

