# Configurações úteis no `php.ini` durante o desenvolvimento

Abaixo estão algumas configurações comumente ajustadas por programadores
ao iniciar um ambiente de desenvolvimento em PHP.

## Exibição e registro de erros

``` ini
display_errors = On
error_reporting = E_ALL
```

Ativa a exibição de erros na tela e define que **todos os tipos de
erro** devem ser reportados.

``` ini
log_errors = On
error_log = /tmp/php_errors.log
```

Ativa o registro de erros e define o arquivo onde esses logs serão
armazenados.

⚠️ **Atenção:** Ao colocar a aplicação em produção, **não** é
recomendável exibir erros na tela.

No ambiente de produção:

``` ini
display_errors = Off
log_errors = Off
```

------------------------------------------------------------------------

## Limites de memória e tempo de execução

``` ini
memory_limit = 256M
max_execution_time = 120
```

------------------------------------------------------------------------

## Upload de arquivos

``` ini
file_uploads = On
post_max_size = 100M
upload_max_filesize = 100M
```

------------------------------------------------------------------------

## Sessões

``` ini
session.gc_maxlifetime = 14000
```

------------------------------------------------------------------------

Essas configurações são típicas para desenvolvimento. Em produção,
desligue `display_errors` para evitar exposição de informações
sensíveis.

Fonte: Orientação a Objetos - 4ª Edição (Pablo Dall’Oglio) 
