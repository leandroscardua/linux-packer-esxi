Utiliza o packer para criar uma imagem customizada do Ubuntu 20.04 no ESXI ( Versão Gratuita )

 Programas:
--------
- Sistema Operacional : Ubuntu 20.04
- Packer : v1.6.6
- ESXI: 6.7.0 Update 3 (Build 17167734)
- Ovftool: 4.4.0 (build-16360108)

 Requerimentos:
--------
- Habilitar SSH no ESXI
- Habilitar GuestIPHack no ESXI ( https://www.packer.io/docs/builders/vmware/iso#building-on-a-remote-vsphere-hypervisor )
- Instalar o Ovftool no Linux ( https://code.vmware.com/tool/ovf )

 Arquivos:
--------

    .
    ├── ubuntu-2004.json        # arquivo de configuração do packer
    ├── variables.json          # arquivo de configuração para conectar no ESXI
    ├── cidata/user-data        # arquivo com a configuração necessaria para instalação automatizada.
    └── cidata/meta-data        # arquivo em branco.
     
 Execucao:
--------

    packer build -var-file variables.json ubuntu-2004.json
