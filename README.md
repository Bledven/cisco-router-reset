# cisco-router-reset

Сброс маршрутизатора (роутера) Cisco без доступа к системе
1 Alt+Break
2 confreg 0x2142 (заставит маршрутизатор принудительно игнорировать имеющийся startup-config во время загрузки)
3 reset
4 copy running-config startup-config
5 config-register 0x2102


Сброс маршрутизатора (роутера) Cisco с известным паролем
1 erase startup-config
2 reload

Сброс коммутатора (свитча) Cisco без доступа к системе
1 отключаем кабель питания из коммутатора и одной рукой зажимаем на нём кнопку «MODE»
2 Одновременно, другой рукой, снова подаём питание, вставив силовой провод, но «MODE» при этом не отпускаем до тех пор, пока системный индикатор не перестанет мигать. Как только он стабилизируется и станет просто гореть зелёным, можно расслабиться и отпустить кнопку
3 flash_init (инициализируем флеш-память) 
4 delete flash:config.text
5 delete flash:vlan.dat (удаление vlan'ов)

Сброс коммутатора (свитча) Cisco с известным паролем
1 erase startup-config
2 delete vlan.dat
3 reload"# cisco-router-reset" 
