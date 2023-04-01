## Referencias

**[Upload Direto]** https://aws.amazon.com/pt/blogs/compute/uploading-to-amazon-s3-directly-from-a-web-or-mobile-application/ 

**[App Intermediário]** https://betterprogramming.pub/aws-s3-buckets-with-python-tutorial-uploading-deleting-and-managing-the-files-in-buckets-dd90d4fd45fe

**[App Intermediário - Exemplo]** https://medium.com/linkit-intecs/upload-and-view-files-in-amazon-s3-using-angular-spring-boot-325b118e7188

**[Data Transfer, aprofundamento]** https://medium.com/@hatim.zahid/serialization-and-deserialization-how-data-travels-in-a-computer-network-13f61dc225c4 

**[Processamento de arquivos grandes - recursivamente]** https://medium.com/swlh/processing-large-s3-files-with-aws-lambda-2c5840ae5c91

**[Processamento de arquivos grandes - SF + Lambda processamento por Chunks] https://github.com/changamire/stepfunction-lambda-fileprocessor/blob/master/fileprocessor.py


A melhor abordagem para fazer upload de arquivos para o AWS S3 dependerá das suas necessidades específicas. Ambas as abordagens têm vantagens e desvantagens, e a escolha dependerá dos seus requisitos de segurança, escalabilidade e complexidade do processo de upload.

A seguir, vou apresentar as vantagens e desvantagens de cada abordagem:

### URL de upload direta:

  Uma URL de upload direta é um link temporário que permite que os usuários façam upload de arquivos diretamente para um bucket S3. Ao fornecer uma URL de upload direta para os usuários, você pode permitir que eles enviem arquivos para o S3 sem precisar de uma aplicação intermediária.

  **Simplicidade:** a URL de upload direta é uma opção simples e fácil para permitir que os usuários façam upload de arquivos para o S3.
Escalabilidade: Como o upload é direto para o S3, ele pode lidar com grandes volumes de uploads sem a necessidade de escalar uma aplicação intermediária.
Desvantagens:

  **Segurança:** Com a URL de upload direta, você precisa compartilhar as credenciais de acesso ao S3 com os usuários, o que pode ser um risco de segurança.
Limitações: A URL de upload direta pode não ter recursos avançados, como gerenciamento de metadados ou validação de arquivos, que podem ser necessários para alguns casos de uso.

### Aplicação intermediária:

  Uma aplicação intermediária é uma aplicação personalizada que gerencia o processo de upload para o S3. Os usuários fazem upload de arquivos para essa aplicação, que, em seguida, faz o upload dos arquivos para o S3.
Vantagens:

  **Segurança:** Com uma aplicação intermediária, você pode manter as credenciais de acesso ao S3 seguras em um servidor controlado.

  **Flexibilidade:** Uma aplicação intermediária pode ser personalizada para atender às suas necessidades específicas, como validação de arquivos ou gerenciamento de metadados.
  
  **Controle:** Uma aplicação intermediária pode fornecer uma interface de gerenciamento para monitorar e controlar o processo de upload.
Desvantagens:

  **Complexidade:** Criar e gerenciar uma aplicação intermediária pode ser mais complexo do que fornecer uma URL de upload direta.

  **Escalabilidade:** Se a aplicação intermediária não for projetada adequadamente, ela pode se tornar um gargalo ao lidar com grandes volumes de uploads.

  Em resumo, ambas as abordagens têm vantagens e desvantagens, e a escolha dependerá dos seus requisitos específicos. Se você precisa de uma solução simples e rápida, uma URL de upload direta pode ser a melhor opção. No entanto, se você precisa de recursos avançados ou de maior segurança, pode ser melhor criar uma aplicação intermediária personalizada.



```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
+ ### Aplicação intermediária:
```
