# Fundamentos de Docker 🐋

### O que é um contêiner? 
  Um pacote isolado que providencia um abiente de execução que funcionará de mesma forma independente do ambiente, o que 
  facilita o desenvolvimento e o funcionamento das aplicações. Contêineres NÂO são uma máquina virtual!
  
#### Tecnologias chave do Docker:
  1. *Namespaces:* isolam processos, diretórios, discos e etc;
  2. *cgroups:* limitam aceso a recursos da CPU e memória;
  3. *union mounting:* sistema de arquivos que trabalho em camadas que podem ser compartilhadas.
  
  **Quando utilizar contêineres?**
  - Em aplicações voltadas para a cloud;
  - Quando criamos microsserviços;
  - Para aplicarmos práticas de CI/CD;
  - Quando o projeto precisa ser escalável.
  
### O que são máquinas virtuais?
  A máquina virtual é conhecida como uma máquina convidada, que roda em cima do sistema operacional host.
  
  **Diferenças:**
  
  ![image](https://user-images.githubusercontent.com/78767309/122418438-947d9400-cf60-11eb-9995-7b8dbf8ffaf7.png)
  _Curso de contêineres 4Linux_
  
  **Quando utilizar máquinas virtuais?**
  - Se o SO não for Linux;
  - Se queremos um nível de persistência maior dos dados da aplicação;
  - Se a arquitetura da aplicação for diferente da máquina hospedeira;
  
### O que é uma imagem?
  Funciona como um template que possui a aplicação, dependências, bibliotecas e outros arquivos. Permite que a aplicação seja instalada em diversos dispositivos. 
  É read only e é através das imagens que vamos criar nossos contêineres.
  
### O que são camadas? 
  Cada imagem é um conjunto de camadas que são, de certa forma, independentes uma das outras.
