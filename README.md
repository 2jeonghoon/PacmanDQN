# PacmanDQN

Installation in Windows
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
git clone https://github.com/2jeonghoon/PacmanDQN.git
conda create --name dqn python=3.7
conda activate dqn
cd PacmanDQN
pip install --user --upgrade -r requirements.txt
AutoROM --accept-license
```

Run in Windows
----
To train the model:
```shell
python tiny_dqn.py -v --number-steps [number of steps]
```
 recommended number of steps is 1000000

The model is saved to my_dqn.ckpt by default. To view it in action, run:
```shell
python tiny_dqn.py --test --render
```

https://github.com/ageron/tiny-dqn
