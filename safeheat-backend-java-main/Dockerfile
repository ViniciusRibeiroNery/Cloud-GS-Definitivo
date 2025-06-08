# Imagem base com Java 21
FROM openjdk:21-jdk-slim

# Criar usuário não-root
RUN useradd -ms /bin/bash appuser

# Definir diretório de trabalho
WORKDIR /app

# Copiar JAR da aplicação para dentro do container
# (ajuste o nome do .jar conforme o gerado pelo Maven)
COPY safeheat-backend-java-main/target/safeheat-backend-java-0.0.1-SNAPSHOT.jar app.jar

# Definir variáveis de ambiente (pode adicionar mais se quiser)
ENV APP_ENV=production

# Expor a porta usada pela aplicação (ajuste se for diferente)
EXPOSE 8080

# Trocar para o usuário não-root
USER appuser

# (Opcional) Verifica se a aplicação está no ar
# HEALTHCHECK --interval=30s --timeout=5s --start-period=10s --retries=3 \
#   CMD curl -f http://localhost:8080/actuator/health || exit 1

# Comando padrão para rodar o app
ENTRYPOINT ["java", "-jar", "app.jar"]
