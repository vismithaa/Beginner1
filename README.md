# Beginner

This is the first project of solidity where I have created my token and added two functions to it.

## Description

In this project, I have created my token on solidity language which is used to write smart contracts. My token name is "Vismitha" and token abbreviation is "VMP". I have also pre-minted 1 token to the total supply. The functionalities associated with this token is mint and burn where mint allows the user to add tokens to the address input and total supply , burn function does the opposite where it deducts the tokens .

## Getting Started

### Downloading/Installing the code

You can download the file or deploy the smart contract on remix IDE

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., first.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenname="Vismitha";
    string public tokenabbrv="VMP";
    uint public totalsupply=1;
    // mapping variable here
    mapping(address => uint)public balance;
    // mint function
    function mint(address mnttoaddr, uint  mntvalue)public {
      totalsupply += mntvalue;
      balance[mnttoaddr] += mntvalue;
   }
    // burn function
   function burn(address brntoaddr, uint brnvalue)public {
      if(balance[brntoaddr]>= brnvalue){
        totalsupply -= brnvalue;
        balance[brntoaddr] -= brnvalue;
      }
     }
  }

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile first.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by clicking on mint and burn by entering the respectives inputs- address and value.
## Authors

Vismitha P

@vismithaaap@gmail.com

## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
