### 첫줄.. 이건설명안함
`sudo apt-get -y update`<br>

### 기본적인거 설치 1
 `sudo apt-get install -y git wget zsh tzdata vim openssh-server mysql-server mysql-client sudo ufw curl fonts-powerline net-tools`<br>
`sudo locale-gen`<br>

### bash에서 zsh로 변환(컴퓨터를 재부팅해야만 zsh가 적용됨)
 `sudo chsh -s $(which zsh)`<br>

### install and setup 'oh-my-zsh'
 `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`<br>

 ### install and setup 'zsh-autosuggestions'
 `git clone https://github.com/zsh-users/zsh-autosuggestions `<br>
 `vi ~/.zshrc`<br>
 `source ~/zsh-autosuggestions/zsh-autosuggestions.zsh`<br>

 ### install and setup 'zsh-syntax-highlighting'
 `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git `<br>
 `vi ~/.zshrc`<br>
 `source ~/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh`<br>
 

 ### change zsh theme 
 `perl -pi -w -e 's/ZSH_THEME=.*/ZSH_THEME="agnoster"/g;' ~/.zshrc `<br>
 `perl -pi -w -e 's/plugins=.*/plugins=(git )/g;' ~/.zshrc`<br>

### 기본적인거 설치 2
 `sudo apt -y install build-essential cmake make clang pkg-config libssl-dev httpie nodejs npm librocksdb-dev jq`<br>

### 쓸모없는 파일들 함 정리해주고
 `sudo apt-get -y autoclean autoremove`<br>



### install rust
`curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`<br>
 `source "$HOME/.cargo/env"`


### zsh--autocomplete는 링크 참고해서 따로 다운로드 받을 것
 `https://github.com/marlonrichert/zsh-autocomplete`<br>


### zshrc에 아래 내용 넣으면 터미널에 나타나는 유저명 짧아짐
 `prompt_context() { `<br>
`   if [[ "$USER" != "$DEFAULT_USER" || -n "$SSH_CLIENT" ]]; then`<br>
     `prompt_segment black default "%(!.%{%F{yellow}%}.)$USER"`<br>
`   fi`<br>
` }`<br>


### zshrc에 아래 내용 넣으면 단축키 편함
 `alias Vzsh="vi ~/.zshrc"`<br>
 `alias Szsh="source ~/.zshrc"`<br>
 `alias c='clear'`<br>
 `alias cc="clear && printf '\e[3J'"`<br>
 `alias cg='cargo'`<br>
 
 
### ssh
 `sudo apt install ssh`<br>
 `sudo vi /etc/ssh/sshd_config`(change your port)<br>
 `sudo /etc/init.d/ssh restart`<br>
 `sudo netstat -anp|grep LISTEN|grep sshd`<br>
 
 `https://hei-jung.github.io/linux/linux-remote-access/`<br>
 
