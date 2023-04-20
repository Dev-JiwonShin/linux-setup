### 첫줄.. 이건설명안함
`sudo apt-get -y update`

### 기본적인거 설치 1
 `sudo apt-get install -y git wget zsh tzdata vim openssh-server mysql-server mysql-client sudo ufw curl fonts-powerline net-tools`

### bash에서 zsh로 변환(컴퓨터를 재부팅해야만 zsh가 적용됨)
 `sudo chsh -s $(which zsh)`

### install and setup 'oh-my-zsh'
 `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

 ### install and setup 'zsh-autosuggestions'
 `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
 `source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh`

 ### install and setup 'zsh-syntax-highlighting'
 `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`

 ### change zsh theme 
 `perl -pi -w -e 's/ZSH_THEME=.*/ZSH_THEME="agnoster"/g;' ~/.zshrc `
 `perl -pi -w -e 's/plugins=.*/plugins=(git zsh-autosuggestions zsh-syntax-highlighting)/g;' ~/.zshrc`

### 기본적인거 설치 2
 `sudo apt -y install build-essential cmake
 sudo apt -y install make clang pkg-config libssl-dev
 sudo apt -y install httpie
 sudo apt -y install nodejs
 sudo apt -y install npm
 sudo apt -y install librocksdb-dev
 sudo apt -y install jq`

### 쓸모없는 파일들 함 정리해주고
 `sudo apt-get autoclean 
 sudo apt-get autoremove -y `



### install rust
`curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`
 `source "$HOME/.cargo/env"`


### zsh--autocomplete는 링크 참고해서 따로 다운로드 받을 것
 `https://github.com/marlonrichert/zsh-autocomplete`


### zshrc에 아래 내용 넣으면 터미널에 나타나는 유저명 짧아짐
 `prompt_context() {
   if [[ "$USER" != "$DEFAULT_USER" || -n "$SSH_CLIENT" ]]; then
     prompt_segment black default "%(!.%{%F{yellow}%}.)$USER"
   fi
 }`


### zshrc에 아래 내용 넣으면 단축키 편함
 `alias v_zsh="vi ~/.zshrc"`
 `alias s_zsh="source ~/.zshrc"`
 
