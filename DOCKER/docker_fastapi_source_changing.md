

```bash
# Dockerfile
FROM python:3.7
ENV HOME /root 
CMD [“/sbin/my_init”]
COPY . /app
WORKDIR /app
ENV PYTHONPATH /app
COPY pip.conf /root/.pip/pip.conf
RUN pip install -r requirements.pip
EXPOSE 5000
ENTRYPOINT [“python”]
CMD [“main.py”]
```





```bash
/app/main.py
APP = FastAPI(debug=True)

@APP.get("/hello-world")
async def hello():
    return {"Hello": "World"}

if __name__ == "__main__":
    uvicorn.run(app, host="0.0.0.0", port=8000)
```

## docker run command 

docker run -d —rm -p 80:80 -v $(pwd):/app myfastapi /start-reload.sh

verification 

http://localhost/hello-world







@uvicorn: @settings

https://www.uvicorn.org/settings/

