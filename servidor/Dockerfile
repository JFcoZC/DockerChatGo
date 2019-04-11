#This file creates a docker image that contains all the dependencies that requires golang
#SERVER

#Build image with latest golang version
FROM golang:latest

#Create directory
RUN mkdir app

#Add all the files in the current directory into the app directory created
ADD . /app

#Move to the directory
WORKDIR /app

#Epose port 80
EXPOSE 80

RUN go build -o main .

#Set the default comand for the container to execute main
CMD ["/app/main"]