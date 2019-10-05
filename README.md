# glastobot
I just want some tickets

## Windows Steps:
```
Set-ExecutionPolicy unrestricted -force
$env:chocolateyUseWindowsCompression = 'false'
iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))

choco install -y googlechrome chromedriver
$env:CHROMEDRIVER='C:\ProgramData\chocolatey\lib\chromedriver\tools\chromedriver.exe'

git clone https://github.com/KevinBrooke/glastobot
cd glastoselenium
pip install -r requirements.txt
pip install glasto
python setup.py install
python scripts/glasto2020.py
```