display_errors = On
error_reporting = E_ALL
Ligar a exibição de erros em tela, bem como indicar que todo tipo de erro deva ser reportado.
log_errors = On // Desligue para entrar ao entrar em produção
error_log = /tmp/php_errors.log
Ligar o registro de logs de erros e indicar um caminho para o registro desses erros.
memory_limit = 256M
max_execution_time = 120
Aumentar o limite de memória (em Mb), bem como o tempo de execução máximo de cada script (em segundos).
file_uploads = On
post_max_size = 100M
upload_max_filesize = 100M
Permitir o upload de arquivos e aumentar os limites de upload e envio de formulários.
session.gc_maxlifetime = 14000
Aumentar o tempo de uma sessão de usuário.
Estas são algumas con gurações que tradicionalmente os programadores fazem antes de iniciar o desenvolvimento. O perigo está em desligar a exibição de erros (display_errors) e não visualizar os problemas de programação.
Quando a aplicação entrar em produção, não é interessante continuarmos a exibir os erros em tela, mas somente registrá-los em um arquivo de log.
Pois nas mensagens de erro podem ser encontrados dados sensíveis como a localização de arquivos, ou eventualmente até mesmo dados de acesso à base de dados. Então, quando a aplicação entrar em produção, desligue a exibição de erros:
log_errors = Off
Fonte: PHP Programando com Orientação a Objetos - 4ª Edição.