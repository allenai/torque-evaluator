FROM library/python:3.8

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

RUN pip3.8 install sklearn

COPY . .

RUN mkdir /results

CMD ["/bin/bash"]
