# Atividade de armazenamento no serviço AWS S3 #

O objetivo desta atividade é explorar na prática os conceitos de armazenamento utilizando o serviços AWS Simple Storage Service (S3). 

O Amazon S3 pode ser utilizado para hospedar sites estáticos.

Hospedar um site estático no Amazon S3 proporciona um site altamente escalável e de alto desempenho por uma fração do custo de um servidor Web tradicional.

Para hospedar um site estático no Amazon S3, configure um bucket do Amazon S3 para hospedagem e faça upload do conteúdo do seu site.

Usando o Console de Gerenciamento da AWS, você pode configurar seu bucket do Amazon S3 como um site estático sem programar qualquer código.

`Referência para a atividade em https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/WebsiteHosting.html`

1. Faça login no AWS Console (aws.amazon.com).

3. No menu de Serviços selecione **S3**.

4. Selecione o botão **Criar bucket**.

5. Na tela de criação de bucket preencha com as informações abaixo.

  nome: `fiap-cloud-vds-aws-s3`
  região: Selecione uma região de preferência
  versionamento: Habilite a opção Versionamento de Bucket

  ###### Mantenha as demais opções padrões. ######

6. Clique no nome do Bucket.

7. No menu **Propriedades**, navegue até a opção **Hospedagem de Site estático**, clique em **Editar** e preencha com as informações abaixo.

  Hospedagem de site estático: `Ativar`
  Documento de índice: `index.html`
  Documento de erro - opcional: `error.html`

8. No menu **Propriedades**, verifique se a opção **Endpoint de site de bucket** foi preenchida com a url abaixo.

  url: `http://fiap-cloud-vds-aws-s3.s3-website-us-east-1.amazonaws.com`

  ###### Guarde esta informação pois precisará a frente. ######

9. Faça download dos arquivos **index.html** e **error.html** disponíveis no repo GitHub abaixo.
 
  Github repository: `https://github.com/FIAP/vds/new/master/aws/s3/static-site`

10. No menu **Objetos** clique em **Carregar**.

  10.1. Selecione **Adicionar arquivos**.
  10.2. Busque pelos arquivos baixados e clique em **Carregar**.
  10.3. Clique em **Fechar**.

11. Abra uma nova guia do navegador e acesse o endpoint guardado.

  Você deverá receber uma mensagem **Access Denied**.

  ###### Isso demonstra que seu Bucket ou Objetos estão sem acesso público. ######

12. No menu **Objetos** selcione os arquivos html e clique em **Ações** e **Tornar público**.

13. Clique em **Tornar Público**.

  ###### Você deverá receber a mensagem **Falha ao editar o acesso público pois o Bucket está com acesso restrito**. ######
  ###### Isso demonstra que objetos não poder ser público se um Bucket for privado. ######

14. CLique em **Fechar**.

15. No menu **Permissões** clique em **Editar**.

16. Desmarque a opção **Bloquear todo o acesso público** e clique em **Salvar Alterações**.

17. Digite a palavra de confirmação e clique em **Confirmar**.

18. Abra uma nova guia do seu navegador e acesse novamente o endpoint.

19. No menu **Objetos** repita o passo de seleção dos arquivos html e clique em **Ações** e **Tornar público**.

20. Abra uma nova guia do seu navegador e acesse novamente o endpoint.

  ###### Você ainda deverá receber uma mensagem **Access Denied**. ######
  ###### Agora que você tornou o Bucket público, você ainda precisa tornar os objetos públicos. ######

21. No menu **Objetos** selcione novamente os arquivos html e clique em **Ações** e **Tornar público**.

22. Clique em **Tornar Público**.

23. Abra uma nova guia do seu navegador e acesso o endpoint.

  ###### Você deverá visualizar o conteúdo do arquivo index.html ######
