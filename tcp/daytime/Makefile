# tools setting
RM = /bin/rm -f
MKDIR = /bin/mkdir -p
CP = /bin/cp -rf

# compiling setting
CC = gcc
CFLAGS = -W -Wall -ansi -pedantic -std=gnu99
LDFLAGS =
INCLUDES = -I./include/network/

# objects setting 
SERVER_OBJS = tcpserver.o socket.o 
CLIENT_OBJS = tcpclient.o socket.o

# target source 
SERVER_SRCS = $(SERVER_OBJS:.o=.c)
CLIENT_SRCS = $(CLIENT_OBJS:.o=.c)

# target we want
SERVER_NAME = server
CLIENT_NAME = client

# compiling rules and dependances
.PHONY : clean
all : $(SERVER_NAME) $(CLIENT_NAME)

$(SERVER_NAME) : $(SERVER_OBJS)
	$(CC) $(SERVER_OBJS) $(INCLUDES) $(LDFLAGS) -o $(SERVER_NAME)

$(CLIENT_NAME) : $(CLIENT_OBJS)
	$(CC) $(CLIENT_OBJS) $(INCLUDES) $(LDFLAGS) -o $(CLIENT_NAME)

clean:
	$(RM) *.o *~ $(SERVER_NAME) $(CLIENT_NAME)
