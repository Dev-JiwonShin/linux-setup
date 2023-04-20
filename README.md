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
   
   99  history
  100  near login
  101  neard
  102  find -name login
  103  sudo find -name login
  104  find / -name "login" 2>/dev/null
  105  find /nearcore -name "login" 2>/dev/null
  106  find /nearcore/ -name "login" 2>/dev/null
  107  find /nearcore/ -exec grep -Hi login \;
  108  find /nearcore -exec grep -Hi login \;
  109  find ~/nearcore -exec grep -Hi login \;
  110  find ~/nearcore -name "login" 2>/dev/null
  111  find ~/nearcore -exec grep -Hi login \;
  112  find ~/nearcore/neard -exec grep -Hi login \;
  113  find ~/nearcore/neard -exec grep -Hi near \;\n
  114  find ~/nearcore/neard/ -exec grep -Hi login \;
  115  grep "login" ~/nearcore/neard/
  116  grep "login" ~/nearcore/neard
  117  grep "login" ~/nearcore/neard/*
  118  grep -r  "login" ~/nearcore/neard/
  119  grep -r  "login" ~/nearcore/
  120  grep -r  "localhost" ~/nearcore/
  121  grep -r  "localhost:4000" ~/nearcore/
  122  grep -r  "4000" ~/nearcore/
  123  grep -r  "'4000" ~/nearcore/
  124  grep -r  "=4000" ~/nearcore/
  125  grep -r  "address" ~/nearcore/
  126  grep -r  "config.js" ~/nearcore/
  127  grep -r  "wallet" ~/nearcore/
  128  find ~/nearcore/neard/ -name wallet
  129  find ~/nearcore/ -name wallet
  130  find ~/nearcore/ -name .rc
  131  find ~/nearcore/ -name .rs
  132  find ~/nearcore -name .rs
  133  find ./nearcore -name .rs
  134  find ./nearcore/ -name .rs
  135  find ~/nearcore -name .md
  136  find ~/nearcore -name *.md
  137  find ~/nearcore -name *
  138  find ~/nearcore --name *
  139  find -r ~/nearcore -name *.md
  140  find -r ~/nearcore -name *
  141  find --help
  142  find -H ~/nearcore -name *
  143  find ~/nearcore -name "*"
  144  find ~/nearcore -name "wallet"
  145  find ~/nearcore -name "*.rs"
  146  near login
  147  NEAR_ENV=local near login
  148  NEAR_ENV=testnet near login
  149  NEAR_ENV=mainnet near login
  150  find ~/nearcore -name "config.json"
  151  find ~/nearcore -name "config.js"
  152  find ~/nearcore -name "config"
  153  grep -r  "near login" ~/nearcore/
  154  grep -r  "near login" ~
  155  cd ..
  156  ls
  157  ls -al
  158  cd .near
  159  cd ..
  160  cd .near-config
  161  cd ..
  162  cd .near-credentials
  163  ls
  164  cd ..
  165  ls
  166  grep -r  "near login" ~/.near/
  167  grep -r  "login" ~/.near/
  168  grep -r  "3AEoJo4ak4RoPkp8rYBqCeLqDd6MBCgJPWNRQLBFUZqsky" ~/
  169  sudo grep -r  "3AEoJo4ak4RoPkp8rYBqCeLqDd6MBCgJPWNRQLBFUZqsky" ~/
  170  sudo grep -r  ":4000" ~
  171  sudo grep -r  ":4000" ~/nearcore
  172  sudo grep -r  "%3A" ~/nearcore
  173  sudo grep -r  "3A" ~/nearcore
  174  sudo grep -r  "Local address" ~/nearcore
  175  sudo grep -r  "Local address" ~
  176  sudo grep -r  "NetworkConfig" ~
  177  find ~/nearcore -name "NetworkConfig"
  178  find ~/ -name "NetworkConfig"
  179  find ~/ -name "network"
  180  sudo grep -r  "wallet.near" ~
  181  NEAR_ENV=mainnet near login
  182  NEAR_ENV=localnet near login
  183  ^[[200~'/home/teamnova/nearcore/target/quick-release/neard' init
  184  '/home/teamnova/nearcore/target/quick-release/neard' -h localnet\n
  185  '/home/teamnova/nearcore/target/quick-release/neard' localnet\n
  186  NEAR_ENV=localnet near login --help
  187  NEAR_ENV=localnet near login --nodeUrl
  188  NEAR_ENV=localnet near login --version
  189  NEAR_ENV=localnet near login --networkId local
  190  NEAR_ENV=localnet near login --networkId "local"
  191  NEAR_ENV=localnet near login --h
  192  NEAR_ENV=localnet near login --help
  193  near --help
  194  NEAR_ENV=localnet near login -v
  195  NEAR_ENV=testnet near login -v

