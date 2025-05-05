FROM node:20-slim
# FROM node:18-slim

WORKDIR /myapp

COPY . .

# 必要なパッケージをインストール
RUN apt update && \
    apt install -y bash git && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# expo-cli のインストール
RUN yarn global add expo-cli

# 依存関係をインストール
RUN yarn install

# Expo を起動
CMD ["yarn", "start"]
