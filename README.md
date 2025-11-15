# Published-Papers
Papers and Patent Achievements during Master's study

- [Near-field AoA estimation with Complex Convolutional Kolmogorov-Arnold Network](https://ieeexplore.ieee.org/document/10889435)
- [Localization Optimization Algorithm Based on Phase Noise Compensation](https://www.mdpi.com/2079-9292/13/24/4947)
- [A Low-Complexity Post-Distortion Linearization for Satellite and mmWave Communication Systems](https://ieeexplore.ieee.org/document/10993887)

# Git: Settings for Folder Upload & normal usage
**1.configuration**

  git config -l  //查看 git config --list

  git config --global user.name "Seplov9"  //配置用户名

  git config --global user.email "zyytcyk@163.com"  //配置邮箱

  git config --global http.proxy http://127.0.0.1:7890
  
  git config --global https.proxy http://127.0.0.1:7890

  git config --global --unset user.name  //清楚git config配置
  
  git config --global --unset user.email

  ssh-keygen -t rsa  //生成密钥

  ssh-keygen -t ed25519  //生成密钥

  C:\Users\HUAWEI\.ssh\id_rsa.pub  //Windows中公钥位置

  cat ~/.ssh/id_ed25519.pub  //显示公钥

  cat ~/.ssh/id_rsa.pub  //显示公钥

  ip a  //ip addr show  // Linux中获取ip

  ssh root@192.168.48.128 "cat ~/.ssh/id_rsa.pub"  //在Windows中连接虚拟机获取公钥

  ssh -T git@github.com  //测试绑定
  
**2.clone**

  git clone https://github.com/Seplov9/repository.git

  git clone git@github.com:Seplov9/repository.git

  cd repository

**3.upload**

  //git init

  git add ./filename

  git status

  git commit -m "commit explaination"

  //git reset --soft HEAD~1

  git restore

  git status

  //git remote add origin https://xxx@xxx/test.git

  //git push origin master

  //git checkout main
  
  **4.branch**

  git pull origin main

  git checkout -b feature/add-login

  // git branch feature/add-login

  // git checkout feature/add-login

  git push -u origin feature/add-login

  git remote -v

  git fetch origin main

  git merge origin/main

  git log  //-n1

  git cherry-pick <commit-hash>

# WSL

  wsl --install  # https://learn.microsoft.com/zh-cn/windows/wsl/install

# ZSH

  //https://www.haoyep.com/posts/zsh-config-oh-my-zsh/

  sudo apt install zsh  # https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH

  sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" # https://github.com/ohmyzsh/ohmyzsh/

  // theme

  // https://github.com/romkatv/powerlevel10k

  //安装主题

  git clone --depth=1 https://gitee.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"

  //设置主题

  vi ~/.zshrc

  ZSH_THEME="powerlevel10k/powerlevel10k"

  // 安装字体

  <img width="236" height="106" alt="image" src="https://github.com/user-attachments/assets/575b3698-7c48-4586-bee8-85dc9b04fef0" />

  //设置字体

  <img width="2555" height="1387" alt="image" src="https://github.com/user-attachments/assets/8159ad21-b981-45a1-98c6-3d83003b04eb" /> 

  p10k configure  //source ~/.zshrc

# conda

  // 安装

  cd ~
  
  wget https://mirrors.tuna.tsinghua.edu.cn/anaconda/miniconda/Miniconda3-latest-Linux-x86_64.sh

  bash Miniconda3-latest-Linux-x86_64.sh

  conda activate

  // source ~/miniconda3/bin/activate

  conda --version

  conda create -n \<env\> python=3.13 -y

  conda init

  conda activate \<env\>

  conda deactivate

  conda remove -n \<env\> --all

  conda install

  conda list

  conda env list

  pip install

  pip list

# uv

  pip install uv

  // Windows
  
  // powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

  // Linux
  
  // curl -LsSf https://astral.sh/uv/install.sh | sh

  uv sync

  // uv init my_project
  
  // cd my_project
  
  // uv venv

  // Windows CMD
  
  .venv\Scripts\activate

  // Windows PowerShell
  
  .venv\Scripts\Activate.ps1

  // Linux
  
  source .venv/bin/activate

  uv pip install

  deactivate

# Vscode

  history  //查看历史命令

  python  //进入python编辑

  exit()/ctrl+z + Enter  //退出python编辑

# linux

  ls  //列出当前目录下的文件和文件夹，不显示隐藏文件（以'.'开头的文件）

  ls -l  //列出文件详细信息，不显示隐藏文件

  ls -a  //列出所有文件，包括隐藏文件

  ls -al  //组合"-a"和"-l"选项

  cd  //主目录

  cd ~  //主目录

  cd /  //根目录

  cd .  //当前目录

  cd ..  //上级目录

  tree

  /  //根目录
  
  ├── bin/
  
  ├── boot/
  
  ├── dev/
  
  ├── etc/
  
  ├── home/
  
  │   └── username/  //主目录
  
  ├── lib/
  
  │   └── x86_64-linux-gnu/
  
  ├── media/
  
  ├── mnt/
  
  ├── opt/
  
  ├── proc/
  
  ├── root/
  
  ├── run/
  
  ├── sbin/
  
  ├── srv/
  
  ├── sys/
  
  ├── tmp/
  
  ├── usr/
  
  │   ├── bin/
  
  │   ├── lib/
  
  │   ├── local/
  
  │  └── share/
  
  pwd

  touch

  cat

  mkdir

  rmdir

  rm

  mv

  cp

  uname -a

  uname -r

  uname -s  //查看当前环境

  vim

  i  //进入编辑模式

  Esc  //进入命令模式
  
  :wq  //退出并保存

  :x  //保存并退出

  :w  //保存不退出

  :wq!  //强制保存并退出

  :q  //退出不保存

  :q!  //强制退出不保存

  more

  Enter  //下一行

  Space  //下一页

  q  //退出查看

  tar -czvf

  unzip -l

  find /home -name "file.txt"  //find [路径] [选项] [表达式]

  grep "error" /var/log/syslog  //grep [选项] [关键字] [文件名]

  ps aux | grep ssh  //查找 SSH 进程

  ipconfig

  ip addr show  //ip a
