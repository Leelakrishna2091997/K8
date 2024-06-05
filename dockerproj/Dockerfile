# Use Alpine Linux rootfs tarball to base our image on
FROM alpine:3.9 

# Set the working directory to be '/home'
WORKDIR '/home'

# Setup our application on container's file system
RUN wget http://www.cs.cmu.edu/afs/cs/academic/class/15213-s00/www/class28/tiny.c \
  && apk add build-base \
  && gcc tiny.c -o tiny \
  && echo 'Hello World' >> index.html

# Start the web server. This is container's entry point
CMD ["./tiny", "8083"]

# Expose port 8082
EXPOSE 8083
EXPOSE 8084