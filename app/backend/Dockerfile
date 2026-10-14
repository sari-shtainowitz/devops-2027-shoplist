FROM python:3.11-slim

# --- NetFree + ESET: מלמדים את ה-container להכיר את התעודות שבודקות את חיבורי ה-HTTPS ---
COPY extra-ca.crt /usr/local/share/ca-certificates/extra-ca.crt
RUN cat /usr/local/share/ca-certificates/extra-ca.crt >> /etc/ssl/certs/ca-certificates.crt
ENV PIP_CERT=/etc/ssl/certs/ca-certificates.crt
ENV REQUESTS_CA_BUNDLE=/etc/ssl/certs/ca-certificates.crt
ENV SSL_CERT_FILE=/etc/ssl/certs/ca-certificates.crt
# --- סוף NetFree + ESET ---

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

EXPOSE 5000

CMD ["python", "app.py"]
