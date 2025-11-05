# Getting Started with the Vision Starter Kit

## Step 1: Connection
1. Connect the Inspector with the network cable and power supply.  
2. Connect the network cable to the USB network adapter.  
3. Plug the power supply into a power strip.  
4. Connect the USB network adapter to the PC.  


## Step 2: Nova Tutorial Series

This function/module is part of the Nova tutorial series. For a detailed explanation and step-by-step guidance, please refer to the Nova tutorial videos (1-7) available on YouTube.

### Nova Tutorial Videos
![type:video](https://www.youtube.com/embed/9dk3b6dBXlw?si=_dvCgyK8Z7HEmYnc)

## Step 3: Start Coding
Open your IDE (Visual Studio Code) and run the following demo.

```python
import socket

# Function to initialize and connect the client socket
def run_client():
    global client
    # Create a socket object using IPv4 and TCP
    client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    
    # Define the server's IP address and port number
    server_ip = "192.168.0.1"
    server_port = 34170
    
    # Connect to the server
    client.connect((server_ip, server_port))

# Function to continuously receive data from the server
def get_requests_continuously():
    global client
    try:
        while True:
            # Receive data from the server (buffer size: 1024 bytes)
            request = client.recv(1024)
            # Decode the received bytes to a string
            request = request.decode("utf-8")
            print("Received:", request)
    except KeyboardInterrupt:
        print("Stopping client...")
    finally:
        client.close()

# Initialize and run the client
run_client()
get_requests_continuously()
```


