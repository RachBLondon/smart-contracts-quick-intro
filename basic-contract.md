# Basic Inbox Contract


Ok lets start writing our first basic contract:

Go to https://remix.ethereum.org/. Delete the exisiting code in the contract and type out the following:

```
pragma solidity ^0.4.17;

contract Inbox {
    string public message;
    
    function Inbox(string initialMessage) public {
        message = initialMessage;
    }
    
    function setMessage(string newMessage) public {
        message = newMessage;
    }
    
    function getMessage() public view returns (string){
        return message;
    }
}

````
