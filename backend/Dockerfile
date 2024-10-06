FROM python:3.11-slim

WORKDIR /app

#copia o requirements.txt e instala as dependẽncias
COPY requirements.txt .
RUN pip install -r requirements.txt

#copia o codigo da aplicação
COPY . .


#copia o script wai-for-it.sh e especificar permissão para execução
COPY wait-for-it.sh /app/wait-for-it.sh
RUN chmod +x /app/wait-for-it.sh

#expor a porta 5000
EXPOSE 5000

#comando para iniciar a aplicação
CMD [ "./wait-for-it.sh", "db:3306", "--timeout=60", "--", "python", "app.py" ]