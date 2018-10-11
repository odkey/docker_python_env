# Base image
FROM python:3.7

# Setup working directory
WORKDIR /app

# Share host current directory with container's working directory
ADD . /app

# Setup port
EXPOSE 80

# Install python libraries
RUN pip install --upgrade setuptools pip
RUN pip install requests lxml scrapy twython django numpy pandas matplotlib scipy jupyter

RUN apt-get clean
RUN apt-get update
RUN apt-get install nano
RUN apt-get git
