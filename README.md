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

## Por que usar o Amazon S3 para Hospedar Sites Estáticos?
O Amazon S3 é uma excelente opção para hospedar sites estáticos (como portfólios, blogs simples ou landing pages) devido ao baixo custo, alta disponibilidade e simplicidade. Para sites de baixo tráfego, é uma solução eficiente e econômica.

# Vamos iniciar a criação do Bucket S3

### Passo 1: Criando o Bucket

No console da AWS, Pesquise por S3 e clique em criar um Bucket.
![image](https://github.com/user-attachments/assets/19334bd3-0db0-4f23-a309-7d635875ab2b)
![image](https://github.com/user-attachments/assets/948f25eb-b893-44c6-b64a-5ce3bdd25ef2)


Na página seguinte, você verá as etapas para a criação do bucket. Preencha o Nome do bucket (lembrando que ele deve ser único globalmente) e escolha a Região de hospedagem.

Nome do bucket exemplo: meu-site-estatico-bucket

Região: Escolha a mais próxima de você ou do seu público.

Configurações adicionais:

Controle de acesso: Aqui você define quem pode acessar seu bucket e realizar gravações. Desmarque a opção de bloqueio de acesso público se você estiver hospedando um site público.

Criptografia: Você pode ativar a criptografia para maior segurança dos seus dados.

Versionamento: Ative o versionamento se precisar preservar versões anteriores dos arquivos.



## Passo 2

Coloque um nome para seu bucket.

![image](https://github.com/user-attachments/assets/e58984c6-1692-4df2-8087-c271fc8f44e9)


### Passo 2: Configurando o Acesso Público

Vá até as configurações de bloqueio de acesso público e desmarque a primeira opção. Isso permite que seu site seja acessado publicamente pela URL.

![image](https://github.com/user-attachments/assets/c4b175a6-ce2b-433d-ba32-6671ea3c7a43)

Atenção: Desbloquear o acesso público pode expor seus arquivos. Use essa opção apenas para sites que precisam ser públicos.

### Passo 3: Criando o Bucket

Clique em criar Bucket

![image](https://github.com/user-attachments/assets/e8a6578d-632c-49e1-b500-c5858e7ec8f5)

Bucket criado com sucesso!

![image](https://github.com/user-attachments/assets/e4f033fa-38b9-4cf4-9751-c5e1855146ed)

### Passo 4: Configurando a Hospedagem de Site Estático

No bucket criado, vá até Propriedades e role até a opção Hospedagem de site estático.

![image](https://github.com/user-attachments/assets/ff6b94cf-c23b-4dd2-aff9-89b8930b81d1)

Clique em Editar e ative a hospedagem de site estático. Defina o nome do arquivo de índice como index.html.

![image](https://github.com/user-attachments/assets/774224bb-467c-4ebf-bdd2-a8b817f2165a)

### Passo 5: Carregando os Arquivos do Site.

Dentro do bucket, clique em Carregar ou arraste os arquivos do site para dentro do bucket, e clique em Carregar.

![image](https://github.com/user-attachments/assets/54e797e3-ba5a-4dcc-bb04-18e3989ef385)

![image](https://github.com/user-attachments/assets/3b479360-6034-4d5e-84df-dd90495bb6b4)


### Passo 6: Configurando Permissões de Acesso.

 Vá até Permissões e clique em Política do bucket.
 
 ![image](https://github.com/user-attachments/assets/bb0350fe-bcfa-4af4-9a62-979fc488ef82)
 
Copie o ARN do bucket (encontrado no painel de propriedades) e clique em Gerador de Políticas.

![image](https://github.com/user-attachments/assets/d9478bb0-0eca-47c2-ab26-f69cd18920a4)

No Gerador de Políticas:

Tipo de Política: Selecione S3 Bucket.

Principal: Deixe como "*" (acesso público).

Ações: Escolha GetObject (permitir acesso aos arquivos).

ARN: Cole o ARN do seu bucket.

![image](https://github.com/user-attachments/assets/f056d207-3e88-4b8d-bfbb-6d1f786e6606)
![image](https://github.com/user-attachments/assets/01b39555-6997-46da-baf6-3959dbdd88f2)

Copie a política gerada e cole no campo de Política do bucket, adicionando /* após o ARN para permitir o acesso a todos os arquivos. Clique em Salvar Alterações.

![image](https://github.com/user-attachments/assets/bce309bf-7ad9-4897-ad87-3eef62da2d65)

### Passo 7: Finalizando e Acessando o Site
Site no ar! Vá até Propriedades > Hospedagem de site estático e copie o link gerado.

Cole o link no navegador para acessar seu site.

![image](https://github.com/user-attachments/assets/5b66b3e7-f4c9-46d4-815e-d9e644504f60)

# Parabéns! Seu site estático está hospedado com sucesso no Amazon S3!

![image](https://github.com/user-attachments/assets/db10f4d0-ade3-4f5d-94b2-2274c7daab3d)



