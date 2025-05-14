# PacmanDQN

Installation
----
Install Miniconda ([https://www.anaconda.com/docs/getting-started/miniconda/main](https://www.anaconda.com/docs/getting-started/miniconda/install))
- Open Windows PowerShell as Administrator

```shell
wget "https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe" -outfile ".\miniconda.exe"
Start-Process -FilePath ".\miniconda.exe" -ArgumentList "/S" -Wait
del .\miniconda.exe
```

- Run the following command in the Anaconda prompt:
```shell
conda create --name dqn python=3.7
conda activate dqn
pip install --user --upgrade pip
pip install --user --upgrade -r requirements.txt
pip install requests
pip install gym[atari,accept-rom-license]
pip install autorom
AutoROM --accept-license
```

Run
----
To train the model:
```shell
python tiny_dqn.py -v --number-steps 1000000
```

The model is saved to my_dqn.ckpt by default. To view it in action, run:
```shell
python tiny_dqn.py --test --render
```

https://github.com/ageron/tiny-dqn
