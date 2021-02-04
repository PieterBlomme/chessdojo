FROM python:3.7

RUN pip install fastapi uvicorn

COPY proteus_api/requirements.txt ./requirements.txt

RUN pip install -r requirements.txt

EXPOSE 80

COPY api/app /app

CMD ["sh","-c","pip install -r /packages/package_install.txt && uvicorn app.main:app --reload --host 0.0.0.0 --port 80"]