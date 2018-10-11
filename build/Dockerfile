# Base image
FROM python:3.7

# Change shell
SHELL ["/bin/bash", "-c"]

# Setup working directory
WORKDIR /app

# Share host current directory with container's working directory
#ADD . /app

# Setup port
EXPOSE 80

# Setup apt-get
RUN apt-get clean \
&& apt-get update \
&& apt-get install nano

# Setup git
RUN cd ~/ \
&& git clone https://github.com/odkey/bash_env.git \
&& cp bash_env/bashrc .bashrc \
&& source .bashrc

# Install python libraries
RUN pip install --upgrade setuptools pip
RUN pip install requests lxml scrapy twython django numpy pandas matplotlib scipy jupyter

CMD ["bash"]