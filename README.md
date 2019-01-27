# blockchain-Sharing-Module
A simple implemntation of how a blockchain can be used for files Sharing over IPFS  


## Environment Setup:

1. Install Go , you can find the steps from here [https://golang.org/doc/install]
2. Install IPFS from here and follow the instructions for setting up the environment [https://docs.ipfs.io/introduction/install/]



## Building:
First, setup the GOPATH environment variables to our project.
Then install the dependencies for the project by running.

`go get github.com/davecgh/go-spew/spew`

`go get github.com/joho/godotenv`

Then we will open a terminal window on which we will run IPFS daemon on it using `$ ipfs daemon`.
This will intialize the connection with the ipfs nodes so we can later upload and download files from the network.
Note, that we will need to keep this terminal window running 

For uploading any file or directory to the IPFS network, open a terminal window and run this command
over the file you wish to upload `ipfs add filesname.format` .
this will upload our file to the network and gives us a hash which any other client can use it to download the file.

Then we will start our blockchain by running `go run main.go`
This will start our node , which then anyone can connect to it for sharing the files they uploaded to ipfs 

for example using our local machine we can start a new terminal window and connect to the blockchain by running 
`nc localhost 9000`.
This we will prompt us to enter our ipfs hash for the files we wish to share on the network .

Later we can download the files uploaded to the ipfs nodes by running this command with the file hash.
for example : `ipfs get QmUmcZDgPso7gcpa2iewYzJfXoGyjsvkVKeS3RM3hpjzQq`
