# INFORMATION

This project is based on the [BitcoinPrivateKeyHunter](https://github.com/Henshall/BitcoinPrivateKeyHunter) repo. Several modifications are made to make it better and correct !

This script will generate bitcoin private keys, extract their bitcoin addresses and compare them with a list of addresses which have large amount of bitcoins (i.e., the [Dormant List](https://bitinfocharts.com/top-100-dormant_8y-bitcoin-addresses.html)).

It is hunting for treasure :).
If the program finds a matching paid it will send an email.

## SETUP

1. Make sure you have `Python 3.x` installed. Install the following packages: `ecdsa`, `smtplib`, `binascii`, and `bitcoinlib`.

2. Rename the env.example file to env.py. It contains a list of variables used by the script. Change the variables related to the email to suit your needs as they will be used to send you an email. The variable `MAX_SECONDS` sets the maximum number of seconds the script should run. You should usually set it to some value and then keep calling the script (e.g., using Unix crontab jobs) using the same frequency.

3. In your run jobs (or if run manually), call the script with `python3 bitcoin_finder.py` or set up a job to hit it every few seconds. It currently examines 10000 random private keys and looks for matches which takes much less then a minute in Intel Core i9 9th gen processor.

4. Have Fun ! If you were lucky and got some BTCs, remember to donate a little to my BTC address: `1MKHALEDqXhBzqa86hj8FbDGW5HvDdA5Tq`.
