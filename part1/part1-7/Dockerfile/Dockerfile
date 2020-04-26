FROM ubuntu:16.04
WORKDIR /mydir
RUN apt-get update
RUN apt-get install -y curl
COPY curl_search.sh .
RUN chmod +x ./curl_search.sh
CMD ["./curl_search.sh"]
