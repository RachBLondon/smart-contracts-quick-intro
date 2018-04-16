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

1. After this has been selected you can deploy your contract by clicking create ![Create](https://github.com/RachBLondon/smart-contracts-quick-intro/blob/master/images/create.png?raw=true) 

2. Below create you shoould now see an box with three buttons (`setMessage`, `getMessage` and `message`). First lets try `getMessage`, this should return the string message. If you get `0: string:` then that is because when you deployed your contract you did not add an initalMessage (done in the box next to the create button). If you did this, redeploy your contract by clicking create and adding a string in the input box to the left *hint - strings (words and characters) need to be surrounded with "".

3. Change your `message` again using the `setMessage` function. Again pay attention to the "".

4. Looking at `message` and `getMessage` we can see that they really do the same thing. That is because `message` is a public string so it is viewable outside of the contract. 

## Extension

5. Let's extend our contract to be able to also take a string which contains the senders email or name (no need for validation). Add another variable called `sender` in to the contract, this time we won't make it public.

6. Now adapt `setMessage` to take a second string as an argument to assign to the var `sender` just as we did for `message`.

7. Write a function `getSender` which returns the sender string.





