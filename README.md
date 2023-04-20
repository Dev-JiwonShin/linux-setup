sudo apt-get -y update
sudo apt-get install -y git wget zsh tzdata vim openssh-server mysql-server mysql-client sudo ufw curl fonts-powerline

sudo chsh -s $(which zsh)
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting


 perl -pi -w -e 's/ZSH_THEME=.*/ZSH_THEME="agnoster"/g;' ~/.zshrc 
 perl -pi -w -e 's/plugins=.*/plugins=(git ssh-agent zsh-autosuggestions zsh-syntax-highlighting)/g;' ~/.zshrc

sudo apt-get install -y curl
sudo apt -y install build-essential cmake
sudo apt -y install make clang pkg-config libssl-dev
sudo apt -y install httpie
sudo apt -y install nodejs
sudo apt -y install npm
sudo apt -y install librocksdb-dev
sudo apt -y install jq


apt-get autoclean 
apt-get autoremove -y 



#install rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"


#zsh--autocomplete는 링크 참고해서 따로 다운로드 받을 것
#https://github.com/marlonrichert/zsh-autocomplete


#zshrc에 아래 내용 넣으면 터미널에 나타나는 유저명 짧아짐
prompt_context() {
  if [[ "$USER" != "$DEFAULT_USER" || -n "$SSH_CLIENT" ]]; then
    prompt_segment black default "%(!.%{%F{yellow}%}.)$USER"
  fi
}

#zshrc에 아래 내용 넣으면 단축키 편함
alias v_zsh="vi ~/.zshrc"
alias s_zsh="source ~/.zshrc"

