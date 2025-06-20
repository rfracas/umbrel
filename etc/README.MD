# Instruções pos instalação ou update


### Mapear disco extra
### Criar diretorio
```
mkdir /mnt/sda1
```
### Alterar o fstab
```
sudo nano /etc/fstab
```
- Copiar linhas do arquivo fstab contido nesse repositório
### Refresh do fstab
```
sudo systemctl daemon-reload
sudo mont -a
```
### Mudar porta padrão para 8081
```
sudo nano /etc/systemmd/system/umbrel.service
```

| Alterar | Para |
| ------- | ---- |
| `ExecStart=umbreld --data-directory=/home/umbrel/umbrel` | `ExecStart=umbreld --data-directory=home/umbrel/umbrel` **`--port=8001`** | 
### Recarregar sistema
```
sudo systemctl daemon-reload
```
### Recarregar umbrel
```
sudo systemctl restart umbrel
```
### Acessar umbrel na noval porta
http://umbrel.local:8001

