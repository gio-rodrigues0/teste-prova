# teste-prova

RDS
- Criando o RDS (ele demora pra criar, não criar no modo fácil, coloca a senha admin123 pra ficar mais fácil)
- Adicionar o link do rds no local do backend
![rds1](https://github.com/gio-rodrigues0/teste-prova/rds1.png)
- Mudar regra de segurança (all tcps - 0.0.0.0/0)
![rds2](https://github.com/gio-rodrigues0/teste-prova/rds2.png)
![rds3](https://github.com/gio-rodrigues0/teste-prova/rds3.png)
![rds4](https://github.com/gio-rodrigues0/teste-prova/rds4.png)

EC2 Back
- Criar EC2 do back
- Associar ao IP elástico
- Mudar regra de segurança (5000 - 0.0.0.0/0)
- Conectar ao EC2

```
sudo apt update
sudo apt upgrade
sudo apt install python3 python3-pip -y
sudo git clone https://github.com/Murilo-ZC/M7-Inteli-Eng-Comp.git
cd M7-Inteli-Eng-Comp/src/encontro11/base01/
python3 -m pip install -r requirements.txt
python3 -m main.py create_db
python3 -m flask --app main run --host 0.0.0.0 --port 5000
```

EC2 Front
- Criar EC2 do Front
- Associar ao IP elástico
- Mudar o arquivo do front para fazer o fetch para ip da ic2 do back
- Conectar ao EC2

```
sudo apt update
sudo apt upgrade
sudo git clone https://github.com/Murilo-ZC/M7-Inteli-Eng-Comp.git
sudo cp repositório/lugar_do_front /var/www/html
```

Testa abrindo o ip da ec2 do front no navegador

