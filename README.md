Coding com AWS EMR e Python.
Neste repositório há os arquivos de configuração e execução de análise de dados.

## Instruções

* Acesse S3: https://s3.console.aws.amazon.com/s3/ 
  * Crie estrutura de data lake : _dio-live-datalake_
  * Crie estrutura de pastas:
    * _data_
    * _output_
    * _temp_
* Acesse EMR: https://console.aws.amazon.com/elasticmapreduce/
    * O cluster será criado pelo MrJob e não pelo console
    * Infraestrutura como código 
* Crie chave SSH
    * Acesse  Console do EC2: https://console.aws.amazon.com/ec2/ -> Key Pairs -> Create Key Pair	
    * Download .pem file
* Obtenha Id e chave secreta AWS para configurar MrJob
   * Profile
   * My Security Credentials: https://console.aws.amazon.com/iam/home?region={region}#/security_credentials
   * Access Keys - Create new access key
   * Fazer download - única chance de visualizar
* Ambiente linux
   * Crie ambiente virtual python: _virtualenv --python=python3.6 venv_diolive_
   * Acesse com o VScode
* Instalar vscode no Ubuntu
   *  code .
* Criar algoritmo de análise de palavras
   * wordcount-test.py
   * map-reduce-count : contar
   * Instale boto3: _pip install boto3_
   * Instale mrjob: _pip install mrjob_
* Acesse S3
   * Upload de arquivo para o bucket
* Ambiente virtual python: source venv_teste/bin/activate
  * _nano ~/.mrjob.conf_
  * _python3 wordcount-test.py -r emr s3://{your_s3_bucket_name}/data/livro.txt --output-dir=s3://{your_s3_bucket_name}/output/logs1 --cloud-tmp-dir=s3://{your_s3_bucket_name}/temp/_


