Устоновка и сборка этого ядра:
$git clone https://github.com/daemoner/kernelfreebsd.git
cd kernelfreebsd
Редактируем под свою железяку и после ректирования перекидываем его в /usr/src/amd64/config/   
$mv GENERIC MYKERNEL && sudo mv MYKERNEL /usr/src/sys/amd64/config/
$cd /usr/src/
Далее сборка ядра:
$sudo make buildkernel KERNCONF=MYKERNEL
Займет минут 15-20 зависит от проца после окончания сборки устонавливаем ядро
$sudo make installkernel KERNCONF=MYKERNEL 
Поздравляю вы собрали ядро freebsd теперь перезагрузитесь в его
$sudo reboot
