# simple-fastapi-container-to-ecr

👻👻👻 簡単なFastAPIアプリケーションをECRにデプロイしてみる！  

## ローカルでの開発

DevContainerに入り、以下のコマンドを実行してください。  

```shell
cd ./fastapi-app/
python -m venv /myenv/
source /myenv/bin/activate
pip install -r ./requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 80
```

実際のDockerコンテナで起動させる場合には、以下のコマンドを実行してください。  

```shell
docker build -t fastapi-app ./fastapi-app/
docker run --rm --name fastapi-app -p 80:80 fastapi-app
```
