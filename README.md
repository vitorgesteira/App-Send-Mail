# App-Send-Mail
## App de envio de emails com php
## Biblioteca PHPMailer 

https://github.com/PHPMailer/PHPMailer

Clique na aba "tags" ao lado direito da aba "Branches" e baixe a
versão 6.4.1 do PHPMailer inclui atualizações que deixaram o pacote mais compativel com a versão 7 e 8 do PHP

### configura o servidor responsavel por entregar o email

$mail->Host       = 'smtp.gmail.com'; - https://support.google.com/a/answer/176600?hl=pt

### configura quem vai mandar o email

$mail->Username   = 'exemplo@example.com';

$mail->Password   = 'secret'; 

### configura a criptografia e a porta

$mail->SMTPSecure = PHPMailer::ENCRYPTION_SMTPS; //Enable verbose debug output 

ob:para desabilitar usar false

$mail->Port       = 587;  //TCP port to connect to; use 587 if you have set `SMTPSecure = PHPMailer::ENCRYPTION_STARTTLS`

### configura o remetente do email
$mail->setFrom('ellen@example.com', 'nome do remetente');

### configura quem vai receber o email
$mail->addAddress('vitor.gesteira@gmail.com', 'Vitor Gesteira destinatario');

### configura mais destinatario se precisar enviar para mais de um destinatario
$mail->addAddress('ellen@example.com');

### configura quem vai ser o contato padrão caso o destinatario responda o remetente
$mail->addReplyTo('info@example.com', 'Information');

### assunto do email
$mail->Subject = 'Here is the subject';

### corpo do email
$mail->Body    = 'This is the HTML message body <b>in bold!</b>'; //usando html

### body alternativo sem tags html 
$mail->AltBody = 'This is the body in plain text for non-HTML mail clients';

----------------------------------------------------------------------------------------------------------------------------------
## IMPORTANTE - Ajustando as configurações de acesso ao SMTP do Gmail

Para configurar uma senha exclusiva para o seu projeto, acesse a conta de e-mail do Gmail que será utilizada em seu projeto e siga os passos:

1 - Clique na opção "Gerenciar sua Conta do Google":

![image](https://github.com/vitorgesteira/App-Send-Mail/assets/54457455/de809dc1-dc9b-4f86-b541-7c1966f68b4c)

2 - Clique na opção "Segurança":

![image](https://github.com/vitorgesteira/App-Send-Mail/assets/54457455/17f0f632-860a-44d0-842a-9d3cae0db459)

3 - Ative a opção de "Verificação em duas etapas":

![image](https://github.com/vitorgesteira/App-Send-Mail/assets/54457455/9cd19840-0243-4638-bb69-28a4248c74fa)

4 - Clique na opção "Senhas de app":

![image](https://github.com/vitorgesteira/App-Send-Mail/assets/54457455/bd69fc08-3733-4abf-aa1d-3e3a742495af)

5 - Clique na opção "Selecione o app e o dispositivo para o qual você quer gerar a senha de app" e escolha a opção "Outro":

![image](https://github.com/vitorgesteira/App-Send-Mail/assets/54457455/dae8a9d0-7879-4966-93e0-87d9030f0413)

6 - Defina um nome (pode ser qualquer nome) e depois clique em "gerar"

![image](https://github.com/vitorgesteira/App-Send-Mail/assets/54457455/a94c43ac-2a4e-4444-9c8e-18e4078a806e)

7 - A senha será gerada, basta copiá-la:

![image](https://github.com/vitorgesteira/App-Send-Mail/assets/54457455/79e4e606-6fbc-4fd7-b5f2-a76f7dcc95e6)

8 - Na próxima aula, utilize a senha copiada no passo 7 no arquivo de configuração de envio de e-mail (processa_envio.php):

![image](https://github.com/vitorgesteira/App-Send-Mail/assets/54457455/0dc10e00-b514-490f-b60a-6a26ddf2c6a2)

Após realizar estes passos o envio de e-mails deve funcionar normalmente.









