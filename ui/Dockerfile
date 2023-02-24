#FROM node:12.7-alpine 
FROM public.ecr.aws/docker/library/node:18.14.2-alpine3.17
WORKDIR /usr/src/app/ui
COPY package*.json ./
RUN npm cache clean --force
RUN npm install
RUN npm install -g @angular/cli
COPY . .

EXPOSE 4200

CMD ["npm", "run", "eb_start"]