# Published-Papers
Papers and Patent Achievements during Master's study

- [Near-field AoA estimation with Complex Convolutional Kolmogorov-Arnold Network](https://ieeexplore.ieee.org/document/10889435)
- [Localization Optimization Algorithm Based on Phase Noise Compensation](https://www.mdpi.com/2079-9292/13/24/4947)
- [A Low-Complexity Post-Distortion Linearization for Satellite and mmWave Communication Systems](https://ieeexplore.ieee.org/document/10993887)

# Git: Settings for Folder Upload & normal usage
**1.configuration**

  git config -l  //查看

  git config --global user.name "Seplov9"  //配置用户名

  git config --global user.email "zyytcyk@163.com"  //配置邮箱

  git config --global http.proxy http://127.0.0.1:7890
  
  git config --global https.proxy http://127.0.0.1:7890

  git config --global --unset user.name  //清楚git config配置
  
  git config --global --unset user.email

  ssh-keygen -t rsa  //生成密钥

  ssh-keygen -t ed25519  //生成密钥

  C:\Users\HUAWEI\.ssh\id_rsa.pub  //Windows中公钥位置

  cat ~/.ssh/id_ed25519.pub  //Linux中显示公钥

  cat ~/.ssh/id_rsa.pub  //Linux中显示公钥

  ip a  //ip addr show  // Linux中获取ip

  ssh root@192.168.48.128 "cat ~/.ssh/id_rsa.pub"  //在Windows中连接虚拟机获取公钥

  ssh -T git@github.com  //测试绑定


**2.clone**

  git clone https://github.com/Seplov9/repository.git

  git clone git@github.com:Seplov9/repository.git

**3.upload**

  //git init

  git add ./filename

  git status

  git commit -m "commit explaination"

  //git reset --soft HEAD~1

  git status

  //git remote add origin https://xxx@xxx/test.git

  //git push origin master

  //git checkout main

  git push

  **4.branch**

  git pull origin main

  git checkout -b feature/add-login

  //git branch feature/add-login

  //git checkout feature/add-login

  git push -u origin feature/add-login

  git remote -v

  git fetch origin main

  git merge origin/main

# conda

  conda create -n <env> python=3.13 -y

  conda init

  conda activate <env>

  conda deactivate <env>

  conda remove -n <env> --all

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

  ls

  cd

  pwd

  mkdir

  rmdir

  rm

  mv

  cp

  vim

  i  //进入编辑模式

  Esc  //进入命令模式
  
  :wq  //保存并退出

  :q!  //退出不保存

  more

  Enter  //下一行

  Space  //下一页

  q  //退出查看

  tar -czvf

  unzip -l

  find /home -name "file.txt"  //find [路径] [选项] [表达式]

  grep "error" /var/log/syslog  //grep [选项] [关键字] [文件名]

  ps aux | grep ssh  //查找 SSH 进程

  uname -s  //查看当前环境
