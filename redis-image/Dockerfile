# Use an existing docker image as a base
FROM alpine 

#  Download and install dependencies
RUN apk add --update redis
RUN apk add --update gcc

# Tell image what to do when the container starts
CMD ["redis-server"]