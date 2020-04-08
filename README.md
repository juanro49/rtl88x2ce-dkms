# RTL88x2CE dkms module driver

## Instalación

git clone https://github.com/juanro49/rtl88x2ce-dkms.git
sudo cp rtl88x2ce-dkms/rtw88_blacklist.conf /etc/modprobe.d/rtw88_blacklist.conf
sudo mkdir /usr/src/rtl88x2ce-35403
sudo cp -Rv rtl88x2ce-dkms/ /usr/src/rtl88x2ce-35403/
sudo dkms add -m rtl88x2ce
sudo dkms build -m rtl88x2ce -v 35403
sudo dkms install -m rtl88x2ce -v 35403

## Iniciar módulo

sudo modprobe rtl88x2ce
