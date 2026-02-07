FROM node:lts-alpine

RUN apk add --no-cache chromium nss freetype harfbuzz ca-certificates ttf-freefont font-noto-cjk git

RUN git clone --depth 1 https://github.com/Hoshino-Yumetsuki/boilerplate.git /boilerplate && rm -rf /boilerplate/.git

COPY ./entrypoint.sh /
RUN chmod +x /entrypoint.sh

VOLUME ["/koishi"]
WORKDIR "/koishi"
ENTRYPOINT ["/entrypoint.sh"]
CMD ["yarn", "start"]
