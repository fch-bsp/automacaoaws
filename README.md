# CI/CD automação com AWS CodeDeploy e AWS CodePipeline 


Mostrar um Lab com ambiente de CI/CD numa aplicaçaão Web AWS-Pipeline de CI/CD práticas combinadas de integração contínua e entrega contínua preenche as lacunas entre as atividades e equipes de desenvolvimento e operação, reforçando a automação na compilação, teste e implantação de aplicativos.Ajuda na produtividade da equipe,cadeia de etapas que são realizadas até que a versão final de um software seja disponibilizado.


![codepipiline](https://user-images.githubusercontent.com/102867453/174445091-d99d6374-8c3c-4fc9-94dc-783a6bd1b713.jpg)

### Passo-Passo

1 criar stack da infra 
2 importa a satck ec2 para a stack infra
3 criar stack flow
4 acessar servidor web e validar de instalou o codedeploy-agent 
5 criar stack onde será recebido flow da aplicação e adicionar Bucket Versioning
6 subir 1 arquivo com aplicação mywebapp_1.0 >>> versão 1 <<<
7 criar via CLI cloddeploy com name > mywebapp
8 acessar codedeploy / Create deployment group -name>> WebupgroUp 
9 Create deployment > s3://stack-flow-mybucketwepappflow-1lhqrjr7yswnu/mywebapp.zip 
10 atualizar o bucket com versão v 2 para podermos criar codepipeline 
11 criação do codepipeline - esse processo será feito via console -
   a.name>> WebUp-Workflow
   c. escolha opção amazon S3 >>APONTE BUCKETS3 >> INFORMA EXTESSÃO .ZIP 
   c.SEM BUILD >>  build em skip build stage 
   d. opção: >> codedeploy >> mywebapp>> WebupgroUp
12 validar operação subindo outro arquivo.zip para bucket da aplicação com isso o processo tem que ocorrer automztizado 
   ou seja após upload o awspipeline junto com cloudwatch indentifica que tem outro arquivo atráves do versonamento avisa 
   codedeploy e atualizar a versão na Ec2 onde esta aplicação, simples assim!!
