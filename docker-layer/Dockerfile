FROM ubuntu:latest

WORKDIR /app 

RUN apt-get update 
RUN apt-get install nodejs -y 
RUN apt-get install npm -y

COPY . .

RUN npm install
RUN npx prisma generate
RUN npm run build

EXPOSE 3000

CMD ["node", "dist/index.js"]



