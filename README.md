# IPComs

Communicate between two local IP adresses.

## Server

Configure your **IP** and **PORT** in the `./server/config.cfg` file

```
[HOST]
IP = <YOUR LOCAL IP> (i.e. 127.0.0.1)
PORT = <FOUR NUMBER PORT> (i.e. 5555)
```

You should always navigate to the `./server/` directory first
```bash
$ cd ./server/
```
Then run the `server.py` script
```bash
$ py server.py
```

## Client

In order to use the client, `server.py` must be running on a device connected to your local network

Also navigate to the `./client` directory first
```bash
$ cd ./client/
```
Then run the `client.py` script
```bash
$ py client.py
```

You will be asked to fill out several inputs

```
Server IP Address: <SERVER LOCAL IP> (i.e. 127.0.0.1)
Server Port: <SERVER PORT> (i.e. 5555)
Username: <USERNAME> (i.e. kubgus)
```

Now you can write messages for other clients to see

```
kubgus > Hello everyone!
```

Press **ENTER** to send messages and refresh chat

## Troubleshooting

### ERROR: The requested address is not valid in its context
This error appears when you enter an invalid IP address  
Try to change the address in `./server/config.cfg` to `127.0.0.1` to test it

### ERROR: No section: 'HOST'
This error appears when you run the python script from another working directory  
  
**This is what you should NOT do:**
```bash
$ py ./server/server.py
```
```bash
$ py ./client/client.py
```
**This is the correct way:**
```bash
$ cd ./server/
$ py server.py
```
```bash
$ cd ./client/
$ py client.py
```
This happens because of how the `./server/config.cfg` file works
