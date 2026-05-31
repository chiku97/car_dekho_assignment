FROM node:20-alpine

WORKDIR /app

COPY car_dekho_backend/package*.json ./

RUN npm install

COPY car_dekho_backend .

RUN npx prisma generate

RUN chmod +x docker-start.sh

EXPOSE 5000

CMD ["sh", "./docker-start.sh"]