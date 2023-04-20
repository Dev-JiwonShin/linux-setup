# linux-setup


  1  apt-get -y install fonts-powerline\n
    2  sudo apt-get -y install fonts-powerline\n
    3  git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions\n
    4  perl -pi -w -e 's/ZSH_THEME=.*/ZSH_THEME="agnoster"/g;' ~/.zshrc 
    5  vi ~/.zshrc
    6  echo 'root:root' |chpasswd && \\n  sed -ri 's/^#?PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config && \\n  sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config && \\n  mkdir /root/.ssh && \\n  mkdir /var/run/sshd 
    7  sudo echo 'root:root' |chpasswd && \\n  sed -ri 's/^#?PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config && \\n  sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config && \\n  mkdir /root/.ssh && \\n  mkdir /var/run/sshd 
    8  apt-get clean && \\n    apt-get autoclean && \\n    apt-get autoremove -y && \\n    rm -rf /var/lib/cache/* && \\n    rm -rf /var/lib/log/*
    9  sudo apt-get clean && \\n    apt-get autoclean && \\n    apt-get autoremove -y && \\n    rm -rf /var/lib/cache/* && \\n    rm -rf /var/lib/log/*
   10  sudo apt-get clean && \\n    apt-get autoclean && \\n    apt-get autoremove -y 
   11  sudo apt-get clean
   12  sudo apt-get autoclean
   13  sudo apt-get autoremove
   14  zsh
   15  chsh -s /usr/bin/zsh
   16  source ~/.zshrc
   17  echo $SHELL
   18  sudo chsh -s $(which zsh)
   19  echo $SHELL
   20  sudo chsh -s $(which zsh)
   21  echo $SHELL
   22  vi ~/.zshrc
   23  ^[[200~git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git
   24  git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git\n
   25  cd zsh-autocomplete source\nzsh-autocomplete.plugin.zsh
   26  ls
   27  cd zsh-autocomplete 
   28  zsh-autocomplete.plugin.zsh\n
   29  source zsh-autocomplete.plugin.zsh\n
   30  ls
   31  source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh\n
   32  git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions\n
   33  source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh\n
   34  vi ~/.zshrc
   35  source ~/.zshrc
   36  vi ~/.zshrc
   37  source ~/.zshrc
   38  vi ~/.zshrc
   39  source ~/.zshrc
   40  vizsh
   41  sourcezsh
   42  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh\n
   43  source "$HOME/.cargo/env"\n
   44  rustup
   45  $ cargo run --profile quick-release -p neard -- --help\n
   46  cargo run --profile quick-release -p neard -- --help\n
   47  git clone https://github.com/near/nearcore
   48  cd nearcore
   49  cd neard
   50  ls
   51  cargo run --profile quick-release -p neard -- --help
   52  apt install build-essential cmake\n
   53  sudo apt install build-essential cmake\n
   54  cd ..
   55  rm -rf nearcore
   56  ls
   57  git clone https://github.com/near/nearcore
   58  cd nearcore/neard
   59  cargo run --profile quick-release -p neard -- --help
   60  history
   61  sudo apt install make clang pkg-config libssl-dev
   62  sudo apt install librocksdb-dev
   63  history
   64  cargo run --profile quick-release -p neard -- --help
   65  cargo run --profile quick-release -p neard -- init
   66  ls ~/.near
   67  cat ~/.near/genesis.json | jq '.records'
   68  apt install jq
   69  sudo apt install jq
   70  cat ~/.near/genesis.json | jq '.records'
   71  cat ~/.near/genesis.json | jq '.validators'
   72  cat ~/.near/validator_key.json
   73  cat ~/.near/config.json | jq '.network.boot_nodes'
   74  cargo run --profile quick-release -p neard -- run
   75  ls ~/.near/data
   76  http get http://localhost:3030/status
   77  apt install http
   78  sudo apt install http
   79  sudo apt install httpie
   80  http get http://localhost:3030/status
   81  http post http://localhost:3030/ method=query jsonrpc=2.0 id=1 \\n     params:='{"request_type": "view_account", "finality": "final", "account_id": "test.near"}'\nλ http post http://localhost:3030/ method=query jsonrpc=2.0 id=1 \\n           params:='{"request_type": "view_account", "finality": "final", "account_id": "test.near"}'\n
   82  sudo apt-get install -y curl
   83  sudo apt install nodejs
   84  sudo apt install npm
   85  npm install -g near-cli
   86  npm
   87  npm install -g near-cli
   88  sudo npm install -g near-cli
   89  history
   90* near -h
   91* NEAR_ENV=local near create-account alice.test.near --masterAccount test.near
   92* export NEAR_ENV=local
   93* near create-account bob.test.near --masterAccount test.near
   94* ls ~/.near-credentials/local
   95* http post http://localhost:3030/ method=query jsonrpc=2.0 id=1 \\n    params:='{"request_type": "view_account", "finality": "final", "account_id": "alice.test.near"}' \\n    | jq '.result.amount'\n"89999955363487500000000000"\n\n14:30:52|~\nλ http post http://localhost:3030/ method=query jsonrpc=2.0 id=1 \\n    params:='{"request_type": "view_account", "finality": "final", "account_id": "bob.test.near"}' \\n    | jq '.result.amount'\n"110000000000000000000000000"
   96* http post http://localhost:3030/ method=query jsonrpc=2.0 id=1 \\n    params:='{"request_type": "view_account", "finality": "final", "account_id": "alice.test.near"}' \\n    | jq '.result.amount'
   97* near login
   98* cargo run --profile quick-release -p neard -- run
