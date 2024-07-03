FROM python:3.11
EXPOSE 8083
WORKDIR /app
COPY requirement.txt ./
RUN pip install -r requirement.txtdocker build -t pdf-reader-admin .
COPY . ./
ENTRYPOINT [ "streamlit", "run", "admin.py", "--server.port=8083", "--server.address=0.0.0.0" ]