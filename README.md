# kube-news

## Build da imagem
Entre no diretório "src" e execute o comando abaixo:

docker build -t seurepo/kube-news:v1 .

## Deploy via kubernetes
Entre no diretório "k8s" e execute o comando abaixo:

sed 's/saiwmon\/kube-news:v1/seurepo\/kube-news:v1/' deployment.yaml

kubectl apply -f k8s/deployment.yaml

Abra o navegador de sua preferência e coloque na URL o IP do host que está hospedando a aplicação na porta 30000 => http://seu_ip:30000/