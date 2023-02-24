# FROM node:12.13.0-alpine
FROM public.ecr.aws/docker/library/node:12.22-alpine3.15
WORKDIR /usr/src/app/api
COPY package*.json ./
RUN npm install
COPY . .

EXPOSE 3000

CMD ["npm", "run", "start"]