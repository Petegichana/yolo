FROM node:18-alpine
RUN mkdir /app
WORKDIR /app
COPY package.json /app
COPY package-lock.json /app
RUN npm install
COPY . /app
ENV PORT=3000
EXPOSE 3000
CMD ["npm" , "start"]