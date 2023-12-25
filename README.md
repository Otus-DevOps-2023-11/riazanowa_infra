# riazanowa_infra
riazanowa Infra repository

Подключение к someinternalhost в одну команду
ssh -i ~/.ssh/id_ed25519 -A -J appuser@158.160.34.38 appuser@10.128.0.11

--------------------------------------------------------------
Подключение из консоли при помощи команды ssh someinternalhost:
Добавить следующую конфигурацию в файл  ~/.ssh/config:
Host bastion
	HostName 158.160.34.38
	User appuser
	IdentityFile ~/.ssh/id_ed25519
Host bastion_vpn
        HostName 192.168.234.1
        User appuser
        IdentityFile ~/.ssh/id_ed25519
Host someinternalhost
	HostName 10.128.0.11
	User appuser
	IdentityFile ~/.ssh/id_ed25519


bastion_IP = 158.160.34.38
someinternalhost_IP = 10.128.0.11
