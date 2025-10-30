# Published-Papers
Papers and Patent Achievements during Master's study

- [Near-field AoA estimation with Complex Convolutional Kolmogorov-Arnold Network](https://ieeexplore.ieee.org/document/10889435)
- [Localization Optimization Algorithm Based on Phase Noise Compensation](https://www.mdpi.com/2079-9292/13/24/4947)
- [A Low-Complexity Post-Distortion Linearization for Satellite and mmWave Communication Systems](https://ieeexplore.ieee.org/document/10993887)

# Git: Settings for Folder Upload & normal usage
**1.configuration**

  git config -l  //查看

  git config --global user.name "Seplov9"  //配置用户名

  git config --global user.emai "zyytcyk@163.com"  //配置邮箱

  git config --global http.proxy http://127.0.0.1:7890
  
  git config --global https.proxy http://127.0.0.1:7890

  ssh-keygen -t rsa (C:\Users\HUAWEI\.ssh\id_rsa.pub)  //生成密钥

  ssh -T git@github.com  //测试绑定


**2.clone**

  git clone https://github.com/Seplov9/repository.git

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
  powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

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

  deactivate

# linux
