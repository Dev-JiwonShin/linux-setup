sudo  apt-get -y update &&\
 sudo apt-get install -y git wget zsh tzdata vim openssh-server mysql-server mysql-client sudo ufw curl

sudo apt-get -y install fonts-powerline


sudo chsh -s $(which zsh)
 sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

 git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
 git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting
git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git


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




   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   source "$HOME/.cargo/env"
