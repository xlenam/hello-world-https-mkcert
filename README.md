# Example Flask web server over https in localhost using mkcert

This is an example of flask web server taht deliver and html file over https in localhost without a selfsign certificate.
This method avoid to accept the certificate because the certificate is signed by the CA of the machine.

## Getting Started

Generate the foo.pem and foo-key.pem file with mkcert tool and start the server:

```
pip install -r requeriments.txt
python app.py
```

And open the example https://localhost:5000/

### Prerequisites

You need to generate the certificate and add to your CA with the mkcert utility

### Installing Windows

```
choco install mkcert
mkcert -install
mkcert localhost 127.0.0.1 ::1
//Copy the generated files to the example root folder
```

### Installing Linux

```
sudo apt install libnss3-tools
sh -c "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install.sh)"
PATH=/home/linuxbrew/.linuxbrew/bin/:$PATH
/home/linuxbrew/.linuxbrew/bin/brew install mkcert
mkcert -install
mkcert localhost 127.0.0.1 ::1
```

For more information related to mkcert tool: https://github.com/FiloSottile/mkcert