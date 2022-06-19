## Containers

Containers Docker
Rancher
Kubernetes
Kubernetes - Arquitetura
Kubernetes - O que é possível
Kubernetes - Soluções

Docker é um projeto de código aberto que faz a auto implantação de aplicativos dentro de contêineres e é mantido pela empresa Docker, inc.

Docker faz a virtualização da virtualização, ele compartilha o kernel, mas fatia o CPU, o disco e td mais e essa fatia menor é o contêiner do Docker,
é uma "mini maquina virtual", é voltado pra um mundo de microserviços embora dê pra rodar aplicações monoliticas e é projetado pra rodar 
ou morrer e recriar em outro lugar do clustes e a aplicação continua rodando como se nada tivesse acontecido.

Fornece uma camada individual de virtualização utilizando recursos de isolamento do kernel do linux como o CGGROUPS e namespaces, e um sistema de arquivos
union mounting como padrao overlay FS dando possibilidade ao uso de outros sistemas de arquivos

https://en.wikipedia.org/wiki/OverlayFS
https://en.wikipedia.org/wiki/Cgroups

img -> img_container_1.png



A idéia é que o Docker Container rode apenas a aplicação ou serviços, e seus dados importantes fiquem fora do container, ou seja, deixando
o container como um ambiente descartável pra que possa descontruir e remontar sem comprometer a integridade da aplicação/serviço.

Há varios containers rodando serviços diferentes e o kernel é compartilhado entre eles, importante ver como 2 containers com processos diferentes 
dentro do mesmo barco pra qunado formos ver a ideia de clusterização de containers 

img -> img_container_2



Container virtualiza o sistema operacional configurado e a VM virtualiza o hardware

Infraestrutura, a maquina, host operating system(onde vai ficar a maquina fisica) e um Hypervisor e em cima dele eu começo a criar a maquina virutal,
a imagem a direita, nos containers, nos temos a maquina, o sistema operacional e o Docket Engine é o kra no lugar o HyperVisor(cria VM), ele pega
a própria estrutura e contrói as VMs em cima da estrutura

Se rodar o Docket Engine, vai ser mais eficiente, cada vez que adicionamos uma camada a mais, usamos CPU, mamória e tal pra todar em cima, ou seja
remove o Hyper Visor, joga o Docket Engine direto na infraestrutura e cria os containers

img -> img_container_3


Por que usar?

Implementações rapidas de aplicativos -> container incluem os resquisitos minimos de execução do aplicaditov e reduz o tamanho e permite que seja implementado rapidamento, e a aplicação ja roda como que precisa
ou seja, o container não tem 50GB, vai ter 10mega, 20... só tem código pra rodar a aplicação, tp o ambiente postgree

Portabilidade entre maquinas -> um aplicativo e todas as dependências podem ser empacotadas num unico container e independente do kernel Linux da distribuição ou modelo de implantação, o ambiente fica igual, ou seja, se tem gente trabalhando com Linux, Windows(Docker pra windows), MacOs, diferentes versões de S.O ou ambiente, o container garante que o ambiente vai ficar igual.

Controle de versão -> o que foi alterado e o que alterado e o histórico de alterações

Compartilhamento -> pode usar repositório local ou remoto pra compartilhar usas iamgens e deixar o ambiente igual em qualquer maquina.

Manutenção simplificada -> Docker reduz o esforço e o risco de problemas com dependência de aplicativos. A ideia é criar a aplicação
e criar o ambiente no Docker pra que não tenha problema com versão de dependências e td mais.




