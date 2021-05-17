# Laboratório de Virtualização (Check Point #02)

O objetivo desse laboratório é configurar um ambiente básico utilizando o software Nagios.

![Arquitetura](/aws/nagios/images/arquitetura.png)

Escopo:

* Instalação e configuração do software Nagios Core em uma máquina virtual Linux utilizando os serviços AWS VPC, AWS EC2 e AWS EBS.

  - ref: https://assets.nagios.com/downloads/nagioscore/docs/nagioscore/4/en/quickstart.html
  - source:
    - nagioscore: https://github.com/NagiosEnterprises/nagioscore/archive/nagios-4.4.5.tar.gz
    - plugins: https://github.com/nagios-plugins/nagios-plugins/archive/release-2.2.1.tar.gz
  

* Instalação do software NSCA (aka Nagios agent) em máquinas Linux que serão gerenciadas pelo Nagios Core via porta TCP 5693.

  - ref: https://assets.nagios.com/downloads/nagioscore/docs/Installing_NSCA.pdf
  - source: https://assets.nagios.com/downloads/ncpa/ncpa-latest.el7.x86_64.rpm

* Instalação do SNMP Service em dispositivos gerenciados.

  - Linux: https://www.site24x7.com/help/admin/adding-a-monitor/configuring-snmp-linux.html

* Configuração do Nagios Core adicionando as máquinas para serem gerenciadas via NCPA, SNMP e ICMP (via ping).


* Referências

  - Nagios Core documentation: https://assets.nagios.com/downloads/nagioscore/docs/nagioscore/4/en/
  - Threshold and Ranges: http://nagios-plugins.org/doc/guidelines.html#THRESHOLDFORMAT
