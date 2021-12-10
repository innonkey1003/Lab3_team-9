FROM python:3                           
WORKDIR /app

## Install packages 
COPY requirements.txt ./                
RUN pip install -r requirements.txt     

## Copy all src files 
COPY . .                                

## Run the application on the port 4000
EXPOSE 4000

#CMD ["python", "./setup.py", "runserver", "--host=0.0.0.0", "-p 4000"] 
CMD ["gunicorn", "--bind", "0.0.0.0:3000", "build.wsgi:application"] 
