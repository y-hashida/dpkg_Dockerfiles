FROM ubuntu:focal

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y --no-install-recommends build-essential debhelper devscripts debmake equivs && \
    apt-get install -y --no-install-recommends lsb-release git bash && \
    echo "Acquire::http::Proxy \"http://10.0.0.79:3142/\";" > /etc/apt/apt.conf.d/02proxy
