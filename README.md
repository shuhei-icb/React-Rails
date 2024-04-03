# React-Rails
React+Rails+Dockerの環境構築

Ruby  3.3.0  
Rails 7.0.8  
node  17.2  
mysql 8.3.0  

## 環境構築手順  
### 1. 任意のディレクトリにこのリポジトリのベアリポジトリをcloneする
```
git clone --bare https://github.com/shuhei-icb/React-Rails.git
```

### 2. cloneしたリポジトリに移動しミラープッシュする
```
cd React-Rails.git
git push --mirror https://github.com/ユーザー名/コピー先リポジトリ名.git
```

### 3. cloneしたベアリポジトリを削除する
```
cd ..
rm -rf React-Rails.git
```

### 4. 新しく作成したリポジトリにコピーが完了したら、任意のディレクトリにcloneする
```
git clone https://github.com/ユーザー名/コピー先リポジトリ名.git
```

### ５. コンテナイメージの作成と起動
```
docker compose build
docker compose up
```

### 6. backコンテナ内でデータベースの作成
```
rails db:create
```

### 7. frontコンテナ内でReactプロジェクトの作成
```
npx create-react-app . --template typescript
```

### 8. npm startする
```
npm start
```

