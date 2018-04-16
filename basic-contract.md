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

### Compile Contract
For this workshop we are are not going to deploy to either the ethereum testnet or main net. We will instead use the javascript virtal network inbuilt in to remix, this will let us start working with our contracts more quickly.

![Select JavaScript VM](https://github.com/RachBLondon/smart-contracts-quick-intro/blob/master/images/javascript-vm.png?raw=true)

After this has been selected you can deploy your contract by clicking create ![Create](https://github.com/RachBLondon/smart-contracts-quick-intro/blob/master/images/create.png?raw=true) 


### Adding a message

