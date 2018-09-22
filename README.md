# Making your own ICO

Change Line 4 to the title of your crowdsale.
You will just change Line 6 after you deploy the contract on the Blockchain.
Change Line 7’s Symbol to your respective coin name (Keep it short)
Change Line 8 to the name of your token

Go to Line 102 and change “bitfwd” to “(YourCrowdsaleName). DON’T USE SPACE OR IT WON’T WORK.
Do the same for Line 118
Go to Line 119 and change the symbol name, the same as the ones you did in the comment section
Do the same for Line 120
Leave Decimals at 18.
On line 122 you will have to define you first ICO parameter, when does the bonus ends?
And on line 123, you will define when does the Crowdsale ends.

Alright, we are almost done editing the contract code.

Now, go to line 212. On that comment, write what is the amount of your tokens you will be giving away for ETH.
On line 218, define how much people will get within the BONUS.
On line 220, define how much people will get without the BONUS (the same ratio that you put on line 212).
The “msg.value” is the amount of ETH that someone sent. So taking my contract as example, for every 1 ETH, i would give 1000 FWD in return.

Boom! The contract is done. Yes, it was that easy right? Now we are going to do some fun stuff, so bare with me until the end!

Go to http://remix.ethereum.org/
In the browser/ballot.sol, paste the code you just edited! If something red comes up, there is something wrong in the code. If there are any yellow warnings it’s alright, let’s hope for the best.

Now Under Compile→Choose the Token you are creating →Details
On ByteCode press the 📋 button to copy the ByteCode to your clipboard.
Now, you will paste it into code editor. DON’T FREAK OUT. There will be a lot of stuff there. The one and only thing we want is the BYTECODE (a huge chunk of numbers and letters) from the object. What you will see will be like: “object”: “BYTECODE”, .
Add 0x to the beginning of the BYTECODE, like: “object”: “0xBYTECODE”,. And copy it to another file on the text editor.

Now, go to MEW where we will start to deploy the contract. REMEMBER we want to be on the Ropsten Test Network so make sure the top right hand corner says that.
Navigate to the Contracts tab → Press Deploy Contract
Paste your ByteCode into the ByteCode box. Your gas limit should automatically update
Access your wallet by going into the Private Key → Enter your private key →Unlock your wallet
Now press Sign Transaction → Deploy Contract

register this contract. To do that:

In the Overview Tab → Click on the Contract Address
Go to the Contract Code Tab → Click Verify and Publish

Now you have 5 things to do on this page.

Be sure that the contract address field corresponds to the contract address that you have just deployed. Remember contract address is different to the MEW address you created so make sure not to get them confused
The contract name has to match the one in the code, in my case is this: bitfwdToken. This was on Line 102 in your code
To check which version of the complier, go back to the remix page where you got the BYTECODE from and look at the URL, the complier version will be there. In most cases it should be: v0.4.19+commit.c4cbbb05.js
On Optimisation, choose No (We haven’t enable it before).
On ENTER THE SOLIDITY CONTRACT CODE BELOW, copy the whole code from Remix, and paste in that area. NOT THE BYTECODE, but the code itself. Can also be copied from your text editor.
*Remember to add on line 6 the contract address that has been generated!

Now, leave the other fields in blank and click on Verify and Publish.

https://medium.com/bitfwd/how-to-do-an-ico-on-ethereum-in-less-than-20-minutes-a0062219374
