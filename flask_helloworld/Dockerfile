# This is our base image, someone has done the work to put python in an image
FROM python

# Add our requirements file
ADD requirements.txt /
# Install that file with a shell command
RUN pip install -r requirements.txt

# Add our code 
# Fun note. Always where you can add code after requirements.txt. If we change code but not requirments
# We can reuse the former built up layer and do not need to fetch packages from pip. 
ADD app.py /src/

# Move our container directory to our source directory.
WORKDIR /src

# Run some python, this here is our declaration of PID 1
ENTRYPOINT ["python"]
CMD ["app.py"]
