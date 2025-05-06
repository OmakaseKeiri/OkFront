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

# TypeScript型定義をインストール：個人追加
RUN yarn add -D @types/react @types/react-native

# expoパッケージをインストール
RUN yarn add expo

# React Native TypeScript設定をインストール
RUN yarn add -D @tsconfig/react-native

# 依存関係をインストール
RUN yarn install

# Expo を起動
CMD ["yarn", "start"]
