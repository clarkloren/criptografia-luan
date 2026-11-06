# Cifra — laboratório de criptografia

Uma demonstração educativa, em português, de criptografia e descriptografia de texto. Funciona diretamente no navegador e aceita letras, números, espaços, acentos, emojis e símbolos.

## Como usar

1. Abra `index.html` em um navegador moderno via HTTPS ou `localhost`.
2. Na aba **Criptografar**, informe uma mensagem e uma chave secreta.
3. Guarde o JSON produzido. Ele contém o texto cifrado e os parâmetros públicos necessários para decifrá-lo.
4. Na aba **Descriptografar**, cole o JSON e use a mesma chave.
5. A explicação ao lado detalha as etapas de cada processo.

## Tecnologia

- **AES-GCM (256 bits)** para cifrar e autenticar os dados.
- **PBKDF2-SHA-256 (250.000 iterações)** para derivar uma chave da frase secreta.
- Salt aleatório de 16 bytes e IV aleatório de 12 bytes, gerados com a Web Crypto API.
- Tudo é processado localmente; nenhum dado é enviado a um servidor ou persistido.

> **Aviso:** este projeto é uma demonstração de aprendizado, não um gerenciador de senhas. Não use para proteger senhas reais ou dados sensíveis. Quem perder a chave não poderá recuperar a mensagem.

Não há dependências ou etapa de build: basta servir o arquivo `index.html` por HTTPS ou localhost para que a Web Crypto API esteja disponível.
