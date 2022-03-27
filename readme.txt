Requirements
Have Python3
Have Postman (A http request sender (this is how we interact with the blockchain))





To run the Leaf Blockchain prototype
Open your Command prompt
Change the directory to the one where the file for example
-->cd   C:\Users\Mrinal\PycharmProjects\pythonProject
-->python leafBlockchain.py

It will initiate the nodes 

To interact
 go to postman
send a get request
http://localhost:5000/mine
this will mine a block and show on the command promt

Then you could add a transation using a post request
tick the raw option

http://localhost:5000/transactions/new

{
    "sender": "(write the hash of the previous mined block)",
    "recipient": "someone-other-address",
    "amount": 5  
}


to print chain send a get request
http://localhost:5000/chain


to run 
node running transaction resolution
post
http://localhost:5000/nodes/register

{
    "nodes" : ["http://127.0.0.1:5001"]

}

To resolve Nodes
send a get request 
http://localhost:5000/nodes/resolve