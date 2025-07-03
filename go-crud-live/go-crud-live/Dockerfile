# user official golang image
FROM golang:1.24.4

# set the Current Working Directory inside the container
WORKDIR /app

# copy go mod and sum files
COPY go.mod go.sum ./

# download all dependencies. Dependencies will be cached if the go.mod and go.sum files are not changed
ENV GOPROXY=direct
RUN go mod download

# copy the source code into the container
COPY . .

# build the Go app
RUN go build -o main .

# Expose port 8080 to the outside world
EXPOSE 8080 

# command to run the executable
CMD ["./main"]  

# Use the official Golang image as a base
# FROM golang:1.21