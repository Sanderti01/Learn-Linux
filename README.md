# Learn-Linux

## Compartilhamento de Arquivos

### Instalação e explicação do modulo

Veremos a seguir explicações referente ao Samba e NFS, ambos são sistemas de compartilhamento de arquivos.

#### Instalação do Samba

Instalando em distros rhel8
```
dnf install samba samba-client -y
```
Iniciando e deixando inicializavel o serviço
```
systemctl start smb && systemctl enable --now smb
```
**Localizando os principais paths do Samba**

Path onde ficam os logs
```
cd /var/log/samba
```
Path dos arquivos de configuração

```
cd /var/etc/samba
```
Editando o principal arquivo de configuração do Samba,
```
vi /var/etc/samba/smb.conf
```
Adicionando um compartilhamento publico
```
[Publico]
comment = Compartilhamento Publico
path = /tmp
browseable = yes
writetable = yes
guest ok = yes
```

Comando para acessar o Samba

Ajuda do comando
```
smbclient --help
```
Comando Para acessar um compartilhamento do servidor do samba
```
smbclient //IP_DO_SAMBA/tmp -U USER_NAME
```
### Sheet cheat

### Exemplos de uso









## Nome do modulo

### Instalação e explicação do modulo
### Sheet cheat
### Exemplos de uso
