# Criando um Amazon Bucket S3 e hospedando um site estático.

Iniciando meus estudos para a AWS Certified Solutions Architect - Associate, e colocando a mão na massa!

# O que é um Amazon Bucket S3 ?
Um bucket S3 é como uma pasta gigante na nuvem da Amazon (AWS) onde você pode armazenar diferentes tipos de arquivos, como fotos, vídeos, documentos e backups.

# Benefícios de Usar um Bucket S3:
1- Espaço Ilimitado: Você pode guardar quantos arquivos quiser, sem se preocupar com falta de espaço.

2- Segurança: Seus arquivos ficam seguros, com opções de criptografia e controle de quem pode acessá-los.

3- Sempre Disponível: Seus arquivos estão disponíveis a qualquer momento e de qualquer lugar, desde que você tenha acesso à internet.

4- Custo Baixo: Você paga apenas pelo espaço e uso que realmente precisa, o que ajuda a economizar.

5- Fácil Integração: Funciona bem com outros serviços da AWS e é fácil de usar em diferentes tipos de aplicativos.

6- Backup e Recuperação: Ideal para guardar cópias de segurança dos seus arquivos e recuperar facilmente se algo der errado.

# Vamos iniciar a criacao do Bucket S3

## Passo 1

No console da AWS, Pesquise por S3 e clique em criar um Bucket.
![image](https://github.com/user-attachments/assets/19334bd3-0db0-4f23-a309-7d635875ab2b)
![image](https://github.com/user-attachments/assets/948f25eb-b893-44c6-b64a-5ce3bdd25ef2)


Na pagina seguinte temos todas as etapas para a criacao de um bucket, temos a regiao onde sera hospedada o bucket,o tipo de bucket,nome (sendo um nome unico no mundo),podemos definir quem pode acessar nosso bucket e realizar gravacoes nele ou ate mesmo quem pode acessar com as configuracoes de acesso publico, podemos realizar criptografia,ativar o versionamento para preservar, recuperar e restaurar as versoes dos seus obejtos. 


## Passo 2

Coloque um nome para seu bucket.

![image](https://github.com/user-attachments/assets/e58984c6-1692-4df2-8087-c271fc8f44e9)


## Passo 3

Va ate as configuracoes de bloqueio do acesso publico e desmarque a primeira opcao.
Essa opcao faz com que ao hospedarmos nosso site, possamos acessesa-lo atraves da URL. 

![image](https://github.com/user-attachments/assets/c4b175a6-ce2b-433d-ba32-6671ea3c7a43)

## Passo 4 

Clique em criar Bucket

![image](https://github.com/user-attachments/assets/e8a6578d-632c-49e1-b500-c5858e7ec8f5)


## Passo 4 
Bucket criado com Sucesso!

![image](https://github.com/user-attachments/assets/e4f033fa-38b9-4cf4-9751-c5e1855146ed)

Para podermos hospedar o site, temos que ativar a opcao de Hospedagem de site estatico, Clicando no bucket que foi criado, indo em propiedades e seguindo ate a ultima opcao.

![image](https://github.com/user-attachments/assets/ff6b94cf-c23b-4dd2-aff9-89b8930b81d1)

Clique em editar, em ativar, para o bucket reconhecer a pagina inicial do site, o arquivo deve se chamar "index.html" depois salve as alteracoes.

![image](https://github.com/user-attachments/assets/774224bb-467c-4ebf-bdd2-a8b817f2165a)

# Hospedando site estático.

Dentro do Bucket, clique em Carregar, ou arraste os arquivos para dentro do Bucket e clique em carregar.

![image](https://github.com/user-attachments/assets/54e797e3-ba5a-4dcc-bb04-18e3989ef385)

![image](https://github.com/user-attachments/assets/3b479360-6034-4d5e-84df-dd90495bb6b4)





