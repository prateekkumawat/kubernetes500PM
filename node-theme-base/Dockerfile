# add base image 
FROM node:18-alpine
# add working directory 
WORKDIR /app
# package installer add 
RUN npm install -g npm@9
# copy code base from source
COPY  evershop/package*.json .
COPY  evershop/packages ./packages
COPY  evershop/themes ./themes
COPY  evershop/extensions ./extensions
COPY  evershop/public ./public
COPY  evershop/media ./media
COPY  evershop/config ./config
COPY  evershop/translations ./translations
# update npm package 
RUN npm install
# run npm builder 
RUN npm run build
# expose port 
EXPOSE 3000
#start npm server
CMD ["npm", "run", "start"]
