#This file creates a docker image that contains all the dependencies that requires golang
#CLIENT

#Build image with latest golang version
FROM golang:latest

#Create directory
RUN mkdir app

#Add all the files in the current directory into the app directory created
ADD . /app

#Move to the directory
WORKDIR /app

#Get directory reuired to compile main.go
RUN go get github.com/chzyer/readline

#Compile and create main executable
RUN go build -o main .

ENTRYPOINT [ "/app/main", "conn 192.168.99.100:80"]

#CMD [ "/app/main" ] 

#Set the default command
#CMD ["conn", "192.168.99.100:80"]