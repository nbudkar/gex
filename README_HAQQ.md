## Install GEX - terminal explorer for HAQQ 
very simple guide


Download GO:

    if ! [ -x "$(command -v go)" ]; then
     ver="1.18.2"
     cd $HOME
     wget "https://golang.org/dl/go$ver.linux-amd64.tar.gz"
     rm -rf /usr/local/go
     tar -C /usr/local -xzf "go$ver.linux-amd64.tar.gz"
     rm "go$ver.linux-amd64.tar.gz"
     echo "export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin" >> ~/.bash_profile
     source ~/.bash_profile
     fi

GEX install:

    cd
    go install github.com/cosmos/gex@latest

Starting GEX with your ip&port:

    gex -h 127.0.0.1 -p 22657

![enter image description here](https://github.com/nbudkar/gex/raw/main/gex_scr.png)
