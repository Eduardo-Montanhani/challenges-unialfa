##  3 encriptar e descriptar

  * <?php
    $chave = random_bytes(SODIUM_CRYPTO_SECRETBOX_KEYBYTES);

    //cria um numero unico para a criptografia
    $nonce = random_bytes(SODIUM_CRYPTO_SECRETBOX_NONCEBYTES);

    //criptografando a mensagem
    $criptografada = sodium_crypto_secretbox('Ola mundo gg', $nonce, $chave);


    $conteudo = sodium_crypto_secretbox($criptografada, $nonce, $chave);

    echo sodium_bin2hex($conteudo);

    //a funcao sodium_crypto_secretbox_open é usada para descriptografar
    $descriptografada = sodium_crypto_secretbox_open($criptografada, $nonce, $chave);

    echo $descriptografada;

   