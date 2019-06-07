FROM nginx:stable-alpine
COPY /dist /user/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]