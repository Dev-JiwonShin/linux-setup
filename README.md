#첫줄.. 이건설명안함
<br> sudo apt-get -y update

<br> #기본적인거 설치 1
<br> sudo apt-get install -y git wget zsh tzdata vim openssh-server mysql-server mysql-client sudo ufw curl fonts-powerline net-tools

<br> #bash에서 zsh로 변환
<br> #컴퓨터를 재부팅해야만 zsh가 적용됨
<br> sudo chsh -s $(which zsh)

<br> #install and setup 'oh-my-zsh'
<br> sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

<br> #install and setup 'zsh-autosuggestions'
<br> git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
<br> source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh

<br> #install and setup 'zsh-syntax-highlighting'
<br> git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

<br> #change zsh theme 
<br> perl -pi -w -e 's/ZSH_THEME=.*/ZSH_THEME="agnoster"/g;' ~/.zshrc 
<br> perl -pi -w -e 's/plugins=.*/plugins=(git zsh-autosuggestions zsh-syntax-highlighting)/g;' ~/.zshrc

<br> #기본적인거 설치 2
<br> sudo apt -y install build-essential cmake
<br> sudo apt -y install make clang pkg-config libssl-dev
<br> sudo apt -y install httpie
<br> sudo apt -y install nodejs
<br> sudo apt -y install npm
<br> sudo apt -y install librocksdb-dev
<br> sudo apt -y install jq

<br> #쓸모없는 파일들 함 정리해주고
<br> sudo apt-get autoclean 
<br> sudo apt-get autoremove -y 



<br> #install rust
<br> curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
<br> source "$HOME/.cargo/env"


<br> #zsh--autocomplete는 링크 참고해서 따로 다운로드 받을 것
<br> #https://github.com/marlonrichert/zsh-autocomplete


<br> #zshrc에 아래 내용 넣으면 터미널에 나타나는 유저명 짧아짐
<br> prompt_context() {
<br>   if [[ "$USER" != "$DEFAULT_USER" || -n "$SSH_CLIENT" ]]; then
<br>     prompt_segment black default "%(!.%{%F{yellow}%}.)$USER"
<br>   fi
<br> }


<br> #zshrc에 아래 내용 넣으면 단축키 편함
<br> alias v_zsh="vi ~/.zshrc"
<br> alias s_zsh="source ~/.zshrc"
<br> 
