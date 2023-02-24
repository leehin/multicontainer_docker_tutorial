#FROM node:12.13.0-alpine
FROM public.ecr.aws/docker/library/node:18.14.2-alpine3.17
WORKDIR /usr/src/app/api
COPY package*.json ./
RUN npm install
COPY . .

EXPOSE 3000

CMD ["npm", "run", "start"]