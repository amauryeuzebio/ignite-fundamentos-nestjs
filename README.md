# Fundamentos Nest

# Prisma
```bash
# Rodando migrations
yarn prisma migrate dev
```

# Chaves SSL para servidor
```bash
# Chave privada
openssl genpkey -algorithm RSA -out private_key.pem

# Chave publica
openssl rsa -pubout -in private_key.pem -out public_key.pem

# Converter arquivo para base64 devido a quebra de linhas difucultar usar no .env
base64 private_key.pem | tr -d '\n' > private_key-base64.txt
base64 public_key.pem | tr -d '\n' > public_key-base64.txt
```