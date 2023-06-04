# dotfiles

1. ルートディレクトリにインストール
  ```
  cd ~
  ```
  ```
  git clone https://github.com/hasebetakumi/dotfiles.git
  ```

2. vimプラグイン管理ツールのneobundleをインストール
  ```
  mkdir -p ~/.vim/bundle
  ```

  ```
  git clone https://github.com/Shougo/neobundle.vim ~/.vim/bundle/neobundle.vim
  ```

3. neobundleを用いてプラグインをインストール
  ```
  vi ~/dotfiles/.vimrc
  ```

  ```
  :NeoBundleInstall
  ```
  
4. vimが用いるバックアップフォルダを作る
  ```
  mkdir -p ~/.vim/backup
  ```
  
5. pynvimエラーで怒られたらpip installで入れる
  ```
    [deoplete] VimEnter Autocommands for "*"..function deoplete#enable[9]..deoplete#initialize[1]..deoplete#init#_initialize[10]..<SNR>78_init_internal_variables[11]..neovim_rpc#serveraddr, line 18
    Error detected while processing VimEnter Autocommands for "*"..function deoplete#enable[9]..deoplete#initialize[1]..deoplete#init#_initialize[10]..<SNR>78_init_internal_variables[35]..VimEnter Autocommands for "*"..function deoplete#enable[9]..deoplete#initialize[1].
    .deoplete#init#_initialize[10]..<SNR>78_init_internal_variables[29]..neovim_rpc#serveraddr:
    line   18:
    E605: Exception not caught: [vim-hug-neovim-rpc] requires one of `:pythonx import [pynvim|neovim]` command to work
  ```
  ```
    pip install pynvim

  ```
  
6. vimで用いる色ファイルをインストール
  ```
    mkdir -p ~/.vim/colors
  ```
  ```
    curl -L -o ~/.vim/colors/desert256.vim https://www.vim.org/scripts/download_script.php?src_id=12498
  ```

7. vimにcopilotを接続する
  ```
    git clone https://github.com/github/copilot.vim.git \
    ~/.vim/pack/github/start/copilot.vim
  ```
  ```
    :Copilot setup
  ```
  ここにワンタイムパスとURLが表示されるので、URLに飛んでパスを入力する。
  数秒後に、vimでpress Enterがでる。

8. gitconfig内のremote先を変更する。

