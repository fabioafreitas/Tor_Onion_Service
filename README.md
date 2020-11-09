> Configurações realizadas no linux

## Instale o tor

```
apt install tor
```

## Executar um servidor qualquer

Estou executando com o python3. Executar o comando abaixo dentro da folder que deseja hospedar os arquivos do servidor.
```
python -m http.server --bind 127.0.0.1 8080
```

## Editar o torrc

```
sudo nano /etc/tor/torrc
```

1. procure a linha com **############### This section is just for location-hidden services ###**. 
2. Abaixo da linha referida acima, descomente as linhas com **HiddenServiceDir** e **HiddenServicePort**.
3. Edite a porta do **HiddenServicePort** para 8080, que é a porta do servidor configurado acima.

## Executar o tor
```
sudo tor
```

## Endereço do servidor

Acesse o endereço retornado pelo comando abaixo no browser do tor e seu serviço será exibido
```
cat /var/lib/tor/hidden_service/hostname
```