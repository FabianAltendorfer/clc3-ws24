# Pull in the layer of the base image
FROM golang:1.23.3-alpine

# Set author label
LABEL author="<YOUR-EMAIL>"

# Set working directory
WORKDIR /opt

# Copy local files to the working directory
COPY go.mod main.go ./

# List items in working directory and show main.go content
RUN ls -lsa && cat main.go

# Build the app and show /usr directory
RUN CGO_ENABLED=0 go build -o /usr/myapp && \
    ls -lsa /usr

# Expose port 8888
EXPOSE 8888

# Set the entrypoint to run the app
ENTRYPOINT ["/usr/myapp"]
