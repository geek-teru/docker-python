FROM amazonlinux:latest

RUN yum install -y git tar unzip findutils
RUN yum install -y gcc make patch zlib-devel bzip2 bzip2-devel readline-devel \
    sqlite sqlite-devel openssl-devel tk-devel libffi-devel xz-devel
RUN cd /opt && git clone https://github.com/yyuu/pyenv.git
RUN ln -s /opt/pyenv/bin/pyenv /usr/local/bin/pyenv

RUN touch /root/.bash_profile
RUN echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
RUN echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
RUN echo 'eval "$(pyenv init -)"' >> ~/.bash_profile

RUN pyenv install 3.11.7
RUN pyenv global 3.11.7
