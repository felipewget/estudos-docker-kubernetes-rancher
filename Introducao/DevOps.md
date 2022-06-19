## DevOps

- O que é DevOps
- Historia DevOps na Amazon
- AWS Code Services
- Servicos de DevOps na AWS

Software muda rapidamente, a capacidade de fazer realise rapida, mais ele se destaca, o ambiente que o software pode ser mudado rapidamente, só favorece a empresa

5x menos chances de falhas(containers menores)
440x mais rapido entro commit e o deploy (com micro serviços, não precisa validar toda a aplicação apenas o que foi subido e a chamada)
46x deploy mais frequentes
44% mais tempo gasto com novas funcionalidades e código

## O que é o DevOps

É um conjunto de filosifias culturais, práticas e ferramentas, usando certas ferramentas, nos obrigamos a usar certas páticas e aderir a alguams filosofias culturais

# Cultura DevOps

Dev & Ops caminham juntos
    -> Dev não é separado a operação, no mundo DevOps isso se mistura, o kra que é dev e vai ajustar a maquina e as configurações e todo o ambiente,
    porém ele ganha esse poder mas a responsabilidade de rodar isso em produção e o kra da operação tem q programar tbm
    Ex: o limite de memória foi muito baixo e deu problema em produção, então O DEV. teve que alterar a memória.

Microserviços
    -> Migrando aplicações monoliticas pra aplicações de microserviços, quando temos uma aplicação monilitica, temos um servidor usando
    muitas bibliotecas usando as msms dependencias e plugin, quando migra pra micro serviços, cada uma das funções(add usuario, register) tem so o codigo
    pra executar ela mas ela é conectada em varias outras e pode ser chamada ou não por varias outras e quando acaba, elas morrem 

    img -> img_dev_ops_1.png 

Integração contínua e deploy contínuo
    passar de um ambiente de passar de um ambiente pra outro é integração continue
    -> code v1.1 
    -> commit e push
    -> source control (AUTOMATIZADO)
        dispara um evento que o codigo foi alteracao para o build
    -> build (AUTOMATIZADO)
        Roda testes unitarios e recria/monta a aplicação
    -> Staging
        Roda testes de carga, load testes, testes de integração
    -> Produção

    Ou seja, exatamente aquele código vai ser publicado em produção 

Infraestrutura como um código
Todos os recursos que vamos utilizar tem q estar em código como parte da aplicação

img -> img_dev_ops_2.png

Monitoração e log
    -> Monitore e analise métricas e logs
    -> Compreenda o desemprenho da infra-estrutura e da aplicação em tempo real 

Benefícios
- Colaboração otimizada
- Entrega Rápida
- Confiabilidade
- Segurança
- Escala
- Velocidade

# Responsabilidade compartilhada
# Visibilidade e comunicação


## Problemas de CD/CI na AWS

img -> img_dev_ops_3.png

Melhorando a parte de deploy, mudou pra 

img -> img_dev_ops_4.png

Como fazer o ambiente de dev ops pra fazer essa entrega rapida? com ferramentas adequadas.

- Pipelines
Ações automatizadas... CD/CI... mais rápido, mais seguro, simplicação e padronização, visualização do processo... automatização.


E funcionou bem:

2014:
milhares de times de serviços na Amazon
Contruindo microserviços
utilizando entrega contínua
diversos ambientes(stagingm beta, production)

Entrega contínua = devs. mais felizes... pois pode desenvolver um codigo e colocar em produção logo e monitorar ele em produção.

Pipeline mais comum

img_default_pipeline.png

Tem outras formas como usando GitLab, GitLab faz o build... e envia pro Rancher, com essas 2 ferramentas, da pra fazer toda a integração contínua

img_default_pipeline_2.png