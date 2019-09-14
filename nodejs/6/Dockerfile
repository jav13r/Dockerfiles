FROM node:6.14.2-slim

RUN apt-get update && apt-get install -y curl git && npm cache clean -f && npm i -g \
    bower \
    grunt-cli \
    gulp-cli \
    grunt \
    webpack \
    typescript \
    ionic \
    cordova \
    create-react-app \
    create-react-native-app \
    vue-cli \
    @angular/cli \
    ember-cli \
    n

RUN curl -o- -L https://yarnpkg.com/install.sh | bash
