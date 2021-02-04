FROM fastai/jekyll:2020-12-30

WORKDIR /fastpages
COPY . .
RUN apt-get update && apt-get install -y r-base
RUN chmod u+x action_entrypoint.sh
RUN chmod u+x word2post.sh
RUN dos2unix /fastpages/*.sh

CMD [ "/fastpages/action_entrypoint.sh" ]
