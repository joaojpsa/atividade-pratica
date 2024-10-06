FROM nginx:alpine

#remove configuração padrão do nginx
RUN rm /etc/nginx/conf.d/default.conf

#copiar a configuração personalizada do nginx
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copia os arquivos
COPY . /usr/share/nginx/html

# Expor a porta 80
EXPOSE 80

