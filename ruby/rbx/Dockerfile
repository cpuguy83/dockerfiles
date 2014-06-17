FROM cpuguy83/ruby-mri
ENV SHELL /bin/bash
RUN apt-get update && apt-get install -y ruby1.9.1-dev && ruby-install rbx 2.2.9 && apt-get clean
ENV PATH /opt/rubies/rbx-2.2.9/bin:$PATH
