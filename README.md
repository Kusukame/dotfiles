git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim

cd ~/.vim/bundle/youcompleteme
python3 install.py --all
curl -fLo "${HOME}/.ycm_extra_conf.py" "https://raw.githubusercontent.com/Valloric/ycmd/master/.ycm_extra_conf.py"

vim +PlugInstall +"sleep 1000m" +qall

/bin/sh dotfilesLink.sh

:source %
:PluginInstall
