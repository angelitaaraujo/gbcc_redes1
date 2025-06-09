<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Atividade Prática: Projeto de Rede Wi-Fi Residencial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.5;
            margin: 10px;
            font-size: 12px;
            text-align: justify;
            color: #000; 
        }
        .header-container {
            display: flex; /* Usa Flexbox para alinhar itens lado a lado */
            align-items: center; /* Alinha verticalmente no centro */
            margin-bottom: 10px;
            border-bottom: 0.5px solid #5ca152;
            padding-bottom: 10px;
        }
        .header-logo {
            margin-right: 30px; /* Espaço entre o logo e o texto */
            max-width: 100px; /* Tamanho máximo do logo */
            height: auto;
        }
        .header-info {
            font-size: 11px;
            color: #000;     
            }
        .orientacoes {
            margin-bottom: 20px;
            padding-bottom: 10px;
            font-size: 9px;
            text-align: justify;
            color: #050505; 
            margin-top: 20px;
            border-bottom: 1px solid #e3e3e3;
        }
        h1 {
            font-size: 15px;
            font-weight: bold;
            border-bottom: 0.5px solid #e3e3e3;
        }
        h2 {
            font-size: 14px;
            font-weight: bold;
            border-bottom: 0.5px solid #e3e3e3;
        }
        h3 {
            font-size: 13px;
            font-weight: bold;
        }
        ul {
            list-style-type: disc;
            margin-left: 5px;
            padding-left: 5px;
        }
        ol {
            margin-left: 5px;
            padding-left: 5px;
        }
        li {
            margin-bottom: 5px;
            margin-left: 5px;
            padding-left: 5px;
        }
        .important-tip {
            padding: 14px;
            margin: 20px 0;
        }
        .note {
            font-style: italic;
            color: #666;
            margin-top: 10px;
            display: block;
        }
    </style>
</head>
<body>
    <div class="header-container">
        <img src="../../imagens/Logo_IFC.png" alt="Logotipo IFC" class="header-logo">
        <div class="header-info">
            <p><strong>Curso:</strong> Bacharelado em Ciência da Computação <br>
            <p><strong>Professora:</strong> Angelita Rettore de Araujo Zanella <br>
            <strong>Disciplina:</strong> Redes de Computadores I <br></p>
            <p><strong>Aluno:</strong> ________________________________________________ </p>
            <p><strong>Data:</strong> ____/_____/_______ </p>
        </div>
    </div>
    <div style="text-align: center; font-size: 1.5em; font-weight: bold; margin-top: 20px;">
        Avaliação Prática - Camada de Rede
    </div>
    <div class="orientacoes">
        <b>Orientações:</b><br>
        1. A avaliação é individual e sem consulta.<br>
        2. Durante a avaliaçaõ você poderá usar o computador do IFC e uma calculadora. Não é permitido o uso de qualquer outro dispositivo eletrônico durante a prova. Caso você seja ﬂagrado utilizando qualquer dispositivo, sua prova será zerada.<br>
        3. Não é permitido pesquisar na Internet ou usar recursos de Inteligência Artificial. Caso seja flagrado usando esses recursos, sua nota será zerada. <br>
        4. Não é permitido fechar o gerenciador de telas. Caso você tente fechar, sua nota será zerada.<br>
        5. Leia as instruções com atenção. A interpretação das questões faz parte da avaliação.<br><br>
     <b>Boa prova!</b><br>
    </div>
</body>

## Descrição do Cenário
Bem-vindo(a) à AngelCorp!

A AngelCorp é uma empresa do setor de tecnologia, referência em soluções de cloud computing e desenvolvimento de software. Nosso crescimento exponencial e a crescente demanda por serviços ágeis e escaláveis exigem uma infraestrutura de rede robusta, eficiente e, acima de tudo, inteligente. 

Recentemente, identificamos a necessidade urgente de otimizar nossa conectividade interna e expandir nossas parcerias estratégicas. A rede atual precisa ser redesenhada para suportar a comunicação vital entre nossos departamentos de Operações de Nuvem (Cloud Ops), Desenvolvimento e Infraestrutura, garantindo fluidez e resiliência. 

Além disso, como uma empresa que respira tecnologia, dependemos criticamente de serviços externos especializados: desde plataformas de licenciamento de software que garantem a legalidade e funcionalidade de nossas ferramentas, até provedores de serviços em nuvem parceiros que amplificam nossas capacidades de entrega. E, claro, a conectividade geral com a Internet é o oxigênio que nos mantém conectados ao mundo. Você foi convocado(a) para liderar esta missão crítica. 

Seu desafio é montar e configurar a infraestrutura de rede da AngelCorp do zero, garantindo que cada pacote de dados encontre seu caminho, seja ele entre os departamentos internos, para os nossos parceiros estratégicos ou para qualquer canto da vasta Internet. Seja preciso(a), seja estratégico(a) e prepare-se para o desafio. 

## ROTEIRO DE ATIVIDADE

Esta atividade acompanha um arquivo do Cisco Packet Tracer com os dispositivos previamente instalados e algumas instruções adicionais.

### Parte 1: Cabeamento da Rede

Você deverá conectar fisicamente os dispositivos utilizando os tipos de cabo especificados. Você encontrará as opções de cabo na barra de ferramentas inferior, sob o ícone de um raio (Connections). Observe a tabela de endereçamento IP para escolher qual interface deverá receber o cabo.

1. Conexões LAN Internas da AngelCorp (PCs para Switches, Switches para Roteadores):
   - Utilize o cabo de Cobre Direto (Copper Straight-Through).
   - Conecte todos os PCs aos seus respectivos Switches (pode usar qualquer porta FastEthernet).
   - Conecte o Switch da subrede Cloud Ops a uma porta FastEthernet ou - GigabitEthernet livre no RTR-CLOUD-OPS.
   - Conecte o Switch da subrede Desenvolvimento a uma porta FastEthernet ou GigabitEthernet livre no RTR-DEV-INFRA.
   - Conecte o Switch da subrede Infraestrutura a uma porta FastEthernet ou GigabitEthernet livre no RTR-DEV-INFRA.
2. Conexões de Backbone Interno da AngelCorp (Roteadores entre si):
   - Utilize o cabo de Fibra Óptica (Fiber).
   - Conecte uma porta GigabitEthernet Fiber do RTR-CLOUD-OPS a uma porta GigabitEthernet Fiber do RTR-DEV-INFRA.
   - Conecte uma porta GigabitEthernet Fiber do RTR-DEV-INFRA a uma porta GigabitEthernet Fiber do RTR-BORDA.
   - Conecte uma porta GigabitEthernet Fiber do RTR-CLOUD-OPS a uma porta GigabitEthernet Fiber do RTR-BORDA.
3. Conexões Externas BGP (RTR-BORDA para Parceiros):
   - Utilize o cabo Serial DCE (Serial DCE). Este cabo tem um ícone de relógio no lado DCE.
   - Conecte uma porta Serial do RTR-BORDA (selecione a extremidade DCE) a uma porta Serial do RTR-PARCEIRO-CLOUD.
   - Conecte outra porta Serial do RTR-BORDA (selecione a extremidade DCE) a uma porta Serial do RTR-PARCEIRO-LICENCA.
4. Conexão Externa para a Internet Genérica (RTR-BORDA para RTR-INTERNET-GENERIC):
   - Utilize o cabo de Cobre Cruzado (Copper Cross-Over).
   - Conecte uma porta FastEthernet ou GigabitEthernet livre do RTR-BORDA a uma porta FastEthernet ou GigabitEthernet livre do RTR-INTERNET-GENERIC.
5. Conexões dos Servidores Externos (Roteadores Parceiros para Servidores):
Utilize o cabo de Cobre Direto (Copper Straight-Through).
   - Conecte o SERVER-PARCEIRO a uma porta FastEthernet ou GigabitEthernet livre no RTR-PARCEIRO-CLOUD.
   - Conecte o SERVER-LICENCAS a uma porta FastEthernet ou GigabitEthernet livre no RTR-PARCEIRO-LICENCA.
   - Conecte o WEB-SERVER-EXTERNAL a uma porta FastEthernet ou GigabitEthernet livre no RTR-INTERNET-GENERIC.

Ao final destas etapas, sua topologia física deve estar completamente montada e com os cabos corretos. Salve seu progresso antes de iniciar a parte de configuração lógica.

### Parte 2: Planejamento e Atribuição de Endereços IP
Agora sua tarefa é calcular e atribuir os endereços IP para todas as redes e interfaces. A AngelCorp utiliza o bloco indicado em material adicional para suas redes internas.

#### Cálculo das Subredes LAN e Links Internos:
Para cada uma das subredes, você deve calcular:
- A máscara de subrede em formato decimal.
- O endereço de rede.
- O endereço de broadcast.
- A faixa de endereços IP utilizáveis para hosts.
 
#### Subredes LAN:
Consulte o endereçamento recebido e Preencha a Tabela com o endereçamento correto
- Cloud Ops LAN: conectada ao RTR-CLOUD-OPS
- Desenvolvimento LAN: conectada ao RTR-DEV-INFRA
- Infraestrutura LAN: conectada ao RTR-DEV-INFRA

| Nome da subrede | Subrede/Prefixo | Endereço de rede | Máscara de rede | Endereço de Broadcast |
| --------------- | --------------- | ---------------- | --------------- | --------------------- |
| LAN Cloud-OPS   |
| LAN DEV         |
| LAN INFRA       |
|                 |

  
**Importante:** Para as interfaces dos roteadores conectadas a essas LANs (que funcionarão como gateways para os PCs), atribua o **ÚLTIMO ENDEREÇO IP UTILIZÁVEL** da respectiva faixa.

#### Links de Interconexão Interna (Roteadores entre si):
- Link 1: RTR-CLOUD-OPS - RTR-DEV-INFRA: 172.31.0.0/30
- Link 2: RTR-DEV-INFRA - RTR-BORDA: 172.31.0.4/30
- Link 3: RTR-CLOUD-OPS - RTR-BORDA: 172.31.0.8/30

Preencha a tabela com os endereços dos dispositivos:

| Nome da subrede | Roteador      | <div style="width:190px">Endereço IP</div>  | <div style="width:190px">Máscara de subrede</div> |
| --------------- | ------------- | ----------- | ------------------ |
| Link 1          | RTR-CLOUD-OPS |
| Link 1          | RTR-DEV-INFRA |
| Link 2          | RTR-DEV-INFRA |
| Link 2          | RTR-BORDA     |
| Link 3          | RTR-CLOUD-OPS |
| Link 3          | RTR-BORDA     |
|                 |


#### Atribuição dos IPs nas Interfaces dos Roteadores:
Acesse cada roteador da AngelCorp (RTR-CLOUD-OPS, RTR-DEV-INFRA, RTR-BORDA).
- Configure o endereço IP e a máscara de subrede (calculada no passo anterior) para todas as interfaces Ethernet e de Fibra conectadas às LANs e aos links de interconexão interna.
- Lembre-se de ativar as interfaces.


#### Configuração de IPs nos PCs da AngelCorp:
- Para cada PC conectado às LANs da AngelCorp, atribua um endereço IP utilizável da sua subrede.
- Configure a máscara de subrede e o Gateway Padrão (que será o endereço IP da interface do roteador conectada àquela LAN).
  
### Configuração de IPs nas Redes Externas (Parceiros e Internet Genérica):

#### Links de Peering BGP (RTR-BORDA para Parceiros):
- Link RTR-BORDA - RTR-PARCEIRO-LICENCA: 10.0.0.0/30
   - Atribua o primeiro IP utilizável ao RTR-BORDA e o último ao RTR-PARCEIRO-LICENCA.
- Link RTR-BORDA - RTR-PARCEIRO-CLOUD: 10.0.0.4/30
   - Atribua o primeiro IP utilizável ao RTR-BORDA e o segundo ao RTR-PARCEIRO-CLOUD.
- Link de Rota Estática (RTR-BORDA para RTR-INTERNET-GENERIC):
   - Link RTR-BORDA - RTR-INTERNET-GENERIC: 10.0.0.20/30
Atribua o primeiro IP último ao RTR-BORDA e o primeiro ao RTR-INTERNET-GENERIC.

#### Redes LAN dos Servidores Externos:
##### RTR-PARCEIRO-LICENCA (LAN Servidor Licenças): 203.0.113.0/28
   - Atribua um IP para a interface do RTR-PARCEIRO-LICENCA nesta rede.
   - Configure o SERVER-LICENCAS com um IP utilizável, máscara e o gateway (IP da interface do RTR-PARCEIRO-LICENCA).

##### RTR-PARCEIRO-CLOUD (LAN Servidor Cloud): 198.51.100.0/27
   - Atribua um IP para a interface do RTR-PARCEIRO-CLOUD nesta rede.
   - Configure o SERVER-PARCEIRO com um IP utilizável, máscara e o gateway (IP da interface do RTR-PARCEIRO-CLOUD).

##### RTR-INTERNET-GENERIC (LAN Web Server): 1.1.1.0/23
   - Atribua um IP para a interface do RTR-INTERNET-GENERIC nesta rede.
   - Configure o WEB-SERVER-EXTERNAL com um IP utilizável, máscara e o gateway (IP da interface do RTR-INTERNET-GENERIC).

### Parte 3: Configuração do Roteamento Interno (OSPF)
A AngelCorp utiliza OSPF para gerenciar o roteamento dinâmico dentro de sua rede.

#### Ative o OSPF nos Roteadores da AngelCorp:
Nos roteadores RTR-CLOUD-OPS, RTR-DEV-INFRA e RTR-BORDA, ative o processo OSPF.
- Defina um Process ID específico para o OSPF (por exemplo, 1).
- Configure todos os roteadores OSPF para pertencerem à Área 0.
- Anunciar Redes no OSPF:
  - Anuncie todas as redes LAN da AngelCorp.
  - Anuncie todos os links de interconexão  entre roteadores.
  - Defina um Router ID exclusivo para cada roteador OSPF.

### Parte 4: Configuração do Roteamento Externo (BGP)
O RTR-BORDA será o ponto de interconexão da AngelCorp (AS 65100) com os AS externos dos parceiros.

#### Configurar BGP no RTR-BORDA (AS 65100):
- Ative o BGP no RTR-BORDA, especificando o AS da AngelCorp (65100).
- Estabeleça o peering eBGP com o RTR-PARCEIRO-LICENCA (AS 64001).
- Estabeleça o peering eBGP com o RTR-PARCEIRO-CLOUD (AS 64002).
- Configure o RTR-BORDA para redistribuir as rotas aprendidas via OSPF (todas as redes internas da AngelCorp) para o BGP. Isso permitirá que os parceiros saibam como chegar às suas redes internas.

#### Configurar BGP no RTR-PARCEIRO-LICENCA (AS 64001):
- Ative o BGP no RTR-PARCEIRO-LICENCA, especificando o AS do parceiro (64001).
- Estabeleça o peering eBGP com o RTR-BORDA (AS 65100).
Anuncie a rede 203.0.113.0/24 (onde está o SERVER-LICENCAS) para o BGP.
- Configurar BGP no RTR-PARCEIRO-CLOUD (AS 64002):
- Ative o BGP no RTR-PARCEIRO-CLOUD, especificando o AS do parceiro (64002).
- Estabeleça o peering eBGP com o RTR-BORDA (AS 65100).
- Anuncie a rede 198.51.100.0/24 (onde está o SERVER-PARCEIRO) para o BGP.

### Parte 5: Configuração de Rota Estática
Apesar do roteamento dinâmico, uma rota estática é necessária para alcançar a Internet genérica.

#### Configurar Rota Estática no RTR-BORDA:
- Crie uma rota estática padrão (0.0.0.0/0) no RTR-BORDA.
- Esta rota deve apontar para o endereço IP da interface do RTR-INTERNET-GENERIC no link de conexão (10.0.0.20/30).

##### Configurar Rota Estática no RTR-INTERNET-GENERIC:
- Crie uma rota estática no RTR-INTERNET-GENERIC para alcançar o bloco de redes internas da AngelCorp.
- Esta rota deve apontar para o endereço IP da interface do RTR-BORDA no link de conexão (10.0.0.20/30).
- Para garantir que o WEB-SERVER-EXTERNAL possa responder a qualquer requisição, você pode configurar uma rota estática padrão no RTR-INTERNET-GENERIC apontando para o próximo salto imaginário da "internet", ou simplesmente ter a rede 1.1.1.0/23 diretamente conectada.

### Parte 6: Verificação e Testes de Conectividade
- Após a configuração, é essencial verificar se tudo funciona conforme o esperado.
- Verificar Adjacências e Tabelas de Roteamento:
    - Em todos os roteadores, verifique a tabela de roteamento para confirmar que as rotas OSPF, BGP e estáticas estão corretas.
- No OSPF, verifique as adjacências de vizinhos.
- No BGP, verifique o resumo de vizinhos e a tabela BGP para as rotas aprendidas.

#### Testes de Conectividade Básicos:
- Realize pings entre os PCs de diferentes subredes dentro da AngelCorp.
- Realize pings de qualquer PC da AngelCorp para o SERVER-LICENCAS.
- Realize pings de qualquer PC da AngelCorp para o SERVER-PARCEIRO.
- Realize pings de qualquer PC da AngelCorp para o WEB-SERVER-EXTERNAL.

#### Testes de Rastreamento de Rota:
Utilize o traceroute de um PC da AngelCorp para o SERVER-LICENCAS, SERVER-PARCEIRO e WEB-SERVER-EXTERNAL para observar o caminho que os pacotes seguem e confirmar que o BGP e a rota estática estão sendo usados corretamente.

#### Teste de Serviço Web:
De um PC da AngelCorp, abra o navegador web e tente acessar o WEB-SERVER-EXTERNAL usando seu endereço IP.
Ao final desta fase, sua rede deverá estar plenamente operacional, refletindo os princípios de um projeto de rede moderno e resiliente.