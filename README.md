[![](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/images/0)](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/links/0)[![](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/images/1)](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/links/1)[![](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/images/2)](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/links/2)[![](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/images/3)](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/links/3)[![](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/images/4)](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/links/4)[![](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/images/5)](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/links/5)[![](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/images/6)](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/links/6)[![](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/images/7)](https://sourcerer.io/fame/juanro49/juanro49/rtl88x2ce-dkms/links/7)

# RTL88x2CE dkms module driver

Download complete driver package with guides [from this repo](https://github.com/XAIOThaifeng/realtek-linux/tree/master/RTL8822CE).

## Instalación

### [PatoJAD Repo](https://patojad.com.ar/repositorio/)
```
echo 'deb https://gitlab.com/patojad/repository/raw/patojad/debs/ patojad main
' | sudo tee /etc/apt/sources.list.d/patojad.list
wget -qO - https://gitlab.com/LynxOS/repository/raw/lynxos/LynxPub.gpg | apt-key add -
sudo apt update
sudo apt install rtl88x2ce-dkms
```

### Paquete deb
```
wget https://github.com/juanro49/rtl88x2ce-dkms/releases/download/5.7.3_35403/rtl88x2ce-dkms_35403_amd64.deb
sudo dpkg -i rtl88x2ce-dkms_35403_amd64.deb
```

### Desde código fuente
```
git clone https://github.com/juanro49/rtl88x2ce-dkms.git
sudo cp rtl88x2ce-dkms/rtw88_blacklist.conf /etc/modprobe.d/rtw88_blacklist.conf
sudo mkdir /usr/src/rtl88x2ce-35403
sudo cp -Rv rtl88x2ce-dkms/ /usr/src/rtl88x2ce-35403/
sudo dkms add -m rtl88x2ce
sudo dkms build -m rtl88x2ce -v 35403
sudo dkms install -m rtl88x2ce -v 35403
```

## Iniciar módulo

`sudo modprobe rtl88x2ce`
