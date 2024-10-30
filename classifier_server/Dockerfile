FROM python:3.14-rc-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

RUN pip install torch --index-url https://download.pytorch.org/whl/cpu

# COPY model /app/model

COPY . .

EXPOSE 5000

CMD [ "python", "classifier_api.py" ]