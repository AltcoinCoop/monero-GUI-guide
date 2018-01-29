// TODO: add suggestions about permissions    
// TODO: add binaries verification (sha256)     
// TODO: add warning for antivirus (it might mess everything)    

# I. Choose a language
![Language](/media/language.png)
After extracting the package click on `monero-wallet-gui.exe` you'll see a list of available languages, click on the one of your choice, then go to the next step.

# II. Create a Wallet
![welcome](/media/welcome.png)
On this page you can choose between three options:

1. **Create a new wallet:** Start the procedure to make a new [wallet](https://getmonero.org/resources/moneropedia/wallet.html) from scratch. Choose this option if it's the first time you are creating a wallet.
2. **Restore wallet from keys or mnemonic seed:** Click here if you want to recover a pre-existent wallet using the mnemonic seed or the keys (This is also the option for creating a 'watch-only wallet')
3. **Open a wallet from file:** Choosing this option you will have to select the file in the ".keys" format from a previus wallet
4. check *testnet* if you are going to make tests and not using the main net

## 1. Create new wallet
![new](/media/create_new.png)
Now give a name to your wallet (in this example is *testname*), write down your [mnemonic seed](https://getmonero.org/resources/moneropedia/mnemonicseed.html) and keep it safe. Your seed is the master key of your wallet, you can use it to recovery your funds.

### Add a password
![add password](/media/password.png)
Add a strong password to protect your wallet

### Summary
![summary](/media/summary.png)
Your wallet is created and almost ready to be used!
Check the summary to be sure everything went alright
&nbsp;

*Language* - The language you have chosen for your wallet    
*Wallet name* - The name of your wallet (and its file)    
*Backup Seed* - master key of your wallet, you can use it to recovery your funds. More info on the [Moneropedia](https://getmonero.org/resources/moneropedia/mnemonicseed.html)    
*Wallet path* - The path where your wallet is saved    
*Daemon address* - The address of the daemon. Default is `localhost:18081`. We will talk about this later.    
*testnet* - if *disabled* you are on the main net

### Run a full node
When the windows closes you will be prompted to the settings menu, but first, you will see a window like this popping up
![sync](/media/sync.png)
If you want to create a normal wallet using your personal full node, you don't need to do anything, let the countdown finish, then Wait untill your node is fully synced.

if you need some special settings like running a remote node, set up a view-only wallet or add manually the blockchain, go to section III: "Settings"


## 2. Restore Wallet from keys or mnemonic seed
![restore from key](/media/restore_key.png)

### Restoring from seed
![restore from seed](/media/restore_seed.png)
This is the easiest way to recover your wallet, you only need to put a name for it [1], paste your seed made of 25 words in the correct field [2] and select the destination folder of the wallet [3].

### Restoring from keys (or create a view only wallet)

## 3. Open a wallet from file

# III. Settings

![settings](/media/settings.png)
After creating/recovering your wallet, you will be prompted to the "settings page". From here you have the possibility tu personalize your configurations according to your personal use.

## Run a remote node
A remote node is the fastest way to start a wallet, but you won't have all the benefits of running a full local node. You also need to specify the address of the remote daemon

To run a remote node you need to use somebody else's daemon, this means you need to communicate with it. Add the remote daemon address and port (10) and click connect (e.g many use the remote nodes available at [moneroworld.com](https://moneroworld.com/#nodes). in this case the configuration would be `node.moneroworld.com` `18089`). Click on "connect" and your wallet will start syncing, this takes some minutes. To check the progresses click on "Show status"(7). 

## Create a view-only wallet
Click on (2) the following page will open
## Add manually the blockchain

## Other settings
Close Wallet: This closes your wallet.

### Show seed & keys

This shows your wallets mnemonic seed (explained earlier) as well as your secret view key, public view key, secret spend key and public spend key. These are outlined below.

### Public / Secret view key
These keys allow you and others to view your Monero wallet incoming transactions (not outgoing). Only give your public view key NOT your private view key to others. This is useful for auditing purposes. Your private view key is also used to ‘scan’ the blockchain to find funds sent to your address. Learn more.

### Public / Secret spend key
These keys allow you to participate in ring signatures. The private key is used to sign a key image which is generated when a transaction happens and the public spend key is used by the network to verify the signature of the key image you generated. This is what prevents double-spend as the network enforces the rule that a key image can be spent only once. Learn more.

### Re-scan wallet balance
This scans the Monero blockchain for any funds that belong to you.


# IV. Send some Moneroj
![send](https://cdn-images-1.medium.com/max/800/1*hB-YNycALp2uwLLZ6geoZw.png)
After clicking on *Send*, on the left menu, you need to specify

**Amount:** This is how much Monero you want to send.

**Transaction priority:** This is the priority your transaction will get to be put into the next Monero blockchain block by miners. The more you pay the more likely you get included in the next block meaning you transaction will go through faster — I recommended just staying with default or even using the slow option if you aren’t in a rush.

**Address:** This is where you put the Monero address you are sending to. I would recommend copying and pasting all addresses to prevent errors.

**Payment ID:** The payment ID is an identity attached to the transaction you are about to send. Often when sending to say an exchange they will give you a payment ID that you must include here. This is so they know that the Monero they get is from you.

*If you forget to add your payment ID you should still be able to recover your funds by contacting the party you sent Monero to.*

**Description:** This is for your record keeping. You can add some information regarding your transaction for future reference.

**Privacy level (ringsizes):** This setting increases the size of the ring signatures your transaction is a part of. Higher ring sizes ‘may’ increase privacy of the transaction but also increases the fees. I would recommend leaving this as the default 5. Learn more about ring signatures here.

**Sweep unmixable:** This allows you to get rid of outputs in your wallet which have strange amounts like 0.000006839355, and are unmovable without combining them with another output. You will more than likely never need to use this feature. Learn more here.

**Sign tx file:** This button allows you to cryptographically sign a file with your private key. This is useful if you want to verify a transaction on an offline wallet. Learn more here.

### Address Book
This section lets you save users you frequently transact with. Addresses you put in your address book can be easily copied over when sending a transaction.

# V. Receive Moneroj
![receive](https://cdn-images-1.medium.com/max/800/1*6Mq_O3aptEo1n8PfeQMMcg.png)
To receive Moneroj, you need to give at least your address, but you can also specify

**Payment ID:** If you want to know who sent you what you can generate and give payment IDs to individuals so you know who sent you Monero.

**Integrated address:** This is an address that combines your address and payment ID into one. This can be used instead of using the address and payment ID. Whether address + payment ID or intergrated address is used differs from site to site. Payment IDs and intergrated addresses will be obsolete once Monero sub-addresses are live.

**Amount:** How much Monero you are wanting to receive.

**QR code:** This is a QR code that has your wallet address embedded into it. It can be used as a way to give others your Monero address by simplying scanning the code.

# Advanced features

## Solo mining
![mining](https://cdn-images-1.medium.com/max/800/1*DLTdjQ4Bb9G-46KwdbYMSg.png)
This is a one click CPU miner that is embedded into the GUI. Having this on helps secure the Monero network. The more people that mine, the harder it is for the network to be attacked.

It is very unlikely that you will receive awards from doing this, but it is not outside the realm of possibility.
## Check payment
![Check payment](https://cdn-images-1.medium.com/max/800/1*5Xy_ZWSdR5PJqUjg9MVrkA.png)
When you send money to a party who then disputes the payment was made, you need to be able to prove the payment was made.

With Bitcoin, this is typically done by looking up the transaction ID, where the origin and destination addresses are shown, along with the amount transacted.

Monero, however, is private: that information is not available publicly on the blockchain. The steps are therefore a bit more involved.

**Address:** This is the wallet address of the recipient. This can be found by clicking on the details button next to the transaction in your history tab.

**Transaction ID:** This is the ID of the payment and can be found in the history tab and by clicking on details button next to the transaction (see below).

**Transaction Key:** When a transaction is made a one time key is automatically generated just for that transaction. This can also be found by clicking on details in the history tab.

Below is what should appear once entering the valid payment details.

![payment details](https://cdn-images-1.medium.com/max/800/1*3Y1cYmbjwZeJjhADBstANw.png)

## Sign/Verify
![sign/verify](https://cdn-images-1.medium.com/max/800/1*0Penmx3aAzaUNrznilXTyA.png)
In this section you can sign a message or file with your private key so that it can be used to show you have ownership of your Monero public key to others. This is a great want to prove accountability without having to sacrifice anonymity.

### Sign a message or file contents with your address

**Message or file:** This is where you will write your message (top box) or attach a file (second box). Upon clicking on ‘sign’ you will generate a signature.

**Signature:** This is where you unique signature will appear once you click sign. This is linked to your private key / message or file you entered and will be used to verify a message or file that either you (for testing purposes), or others, create.

### Verify a message or file signature from an address:

**Message or file:** This is where you will put a message or file that has been signed with a signature.

**Signing address:** This is where you will put the public Monero address you are wanting to verify.

**Signature:** This is where you paste the signature that the other user generated and gave to you.

Once all the required information has been inputted click verify. You should get a notification such as below if the signature is good.
![good signature](https://cdn-images-1.medium.com/max/800/1*O_2t5bM3jn5wj8aN3i4P5Q.png)
