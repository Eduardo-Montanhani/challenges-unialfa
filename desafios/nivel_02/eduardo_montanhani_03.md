##  3 encriptar e descriptar

  * <?php 
 
 $texto = "Ola mundo !!";

 $textoCrip = base64_encode($texto);
 $textoDescri = base64_decode($textoCrip);

     echo "O texto criptografado é $textoCrip e seu texto verdadeiro $textoDescri";
