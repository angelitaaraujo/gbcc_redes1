<head>
  <link rel="stylesheet" href="estilos.css">
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
        Reavaliação
    </div>
    <div class="orientacoes">
        <b>Orientações:</b><br>
        1. A avaliação é individual e sem consulta.<br>
        2. Não é permitido o uso de qualquer dispositivo eletrônico durante a prova. Caso você seja ﬂagrado utilizando qualquer dispositivo, sua prova será zerada.<br>
        3. Leia a prova com atenção antes de responder. A interpretação das questões faz parte da avaliação. <br>
        4. As questões discursivas podem ser respondidas à lápis, porém as questões respondidas a lápis não poderão ser revisadas futuramente.<br>
        5. Responda de forma completa, correta, clara e concisa, focando na precisão e relevância das informações.<br><br>
     <b>Boa prova!</b><br>
    </div>
</body>

1. [1,5 pontos] A Camada de Enlace é um componente vital na arquitetura de redes, embora sua função e a importância de seus identificadores, como o endereço MAC, possam ser subestimadas.

Considerando o contexto da comunicação entre nós adjacentes em uma rede local, discorra sobre a Camada de Enlace e o endereço MAC, abordando os seguintes pontos em sua resposta:
- Definição e Responsabilidade Primária da Camada de Enlace: Explique qual é a principal função desta camada no processo de comunicação de rede, destacando sua responsabilidade pela transferência física de dados entre nós adjacentes. Mencione a Unidade de Dados de Protocolo (PDU) característica desta camada.
- Implementação da Camada de Enlace: Descreva onde a Camada de Enlace é implementada nos dispositivos de rede (hosts e roteadores) e como essa implementação se relaciona com a capacidade de um pacote ser transferido por diferentes tecnologias de enlace (ex: Wi-Fi, Ethernet).
- Endereço MAC como Identificador Único: Explique o que é o endereço MAC, qual seu tamanho (em bits) e como ele é atribuído aos dispositivos.
- Função do Endereço MAC na Entrega Local: Detalhe como o endereço MAC é utilizado para a entrega local de quadros entre interfaces fisicamente conectadas (dentro da mesma sub-rede), e como o adaptador de rede (NIC) utiliza esse endereço para filtrar quadros.
- Analogia e Diferenciação do Endereçamento: Utilize uma analogia clara (como a do CPF vs. Endereço Postal) para ilustrar a relevância do endereço MAC e diferenciá-lo do endereço IP, que opera em uma camada superior, explicando a distinção entre a entrega local (Camada de Enlace) e o roteamento global (Camada de Rede).
  
2. [1,5 pontos] As redes sem fio (wireless) revolucionaram a forma como nos conectamos, oferecendo flexibilidade e mobilidade. No entanto, o meio de transmissão sem fio possui características físicas e lógicas que o tornam fundamentalmente diferente e, em muitos aspectos, mais desafiador do que os enlaces cabeados tradicionais. Essas diferenças exigem abordagens distintas para o controle de acesso ao meio e a garantia da comunicação.

Com base em seus conhecimentos sobre redes de computadores e as particularidades dos enlaces sem fio, responda aos seguintes pontos de forma clara e detalhada:
<ol style="list-style-type: lower-alpha">
<li> Desafios Inerentes aos Enlaces Sem Fio: Explique as principais características e desafios que tornam a comunicação em enlaces sem fio inerentemente mais complexa e propensa a erros do que em enlaces cabeadas. Mencione e descreva pelo menos dois fenômenos físicos ou problemas lógicos que afetam a confiabilidade e o desempenho das redes sem fio.</li>
<li> O Problema do Terminal Oculto (Hidden Terminal Problem): Descreva detalhadamente o problema do terminal oculto em redes sem fio. Explique por que ele ocorre, como ele pode levar a colisões não detectadas e qual o seu impacto na eficiência da comunicação.</li>
<li> Protocolos de Acesso ao Meio para Redes Sem Fio (CSMA/CA): Considerando os desafios e o problema do terminal oculto, explique como os protocolos de acesso ao meio (MAC) para redes sem fio, como o CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance), abordam essas dificuldades.</li>
<li> Comparação CSMA/CA vs. CSMA/CD: Compare o funcionamento do CSMA/CA com o CSMA/CD (Carrier Sense Multiple Access with Collision Detection), utilizado em redes Ethernet cabeadas. Destaque as razões fundamentais pelas quais a detecção de colisão (CD) é inviável ou ineficiente em ambientes sem fio e por que a evitação de colisão (CA) é a abordagem preferida.</li>
</ol>

3) [1,0 pontos] Em redes locais cabeadas, como as antigas redes Ethernet baseadas em barramento, múltiplos dispositivos compartilhavam um único meio físico de transmissão. Para que essa comunicação fosse eficiente e organizada, evitando o caos de colisões constantes, foi desenvolvido um protocolo de acesso ao meio muito importante: o CSMA/CD (Carrier Sense Multiple Access with Collision Detection).

Explique o que é o CSMA/CD, como ele opera e qual é a sua estratégia para tratar colisões. Sua resposta deve incluir a função do sensoriamento da portadora, da detecção de colisão e do recuo (backoff).

4) [1,5 pontos] A Camada de Rede é responsável por mover pacotes de dados de um host de origem para um host de destino, que podem estar em redes geograficamente distantes. O principal dispositivo que realiza essa função é o roteador. No plano de dados, a tarefa essencial de um roteador é o encaminhamento (forwarding), ou seja, pegar um datagrama IP que chega em uma de suas interfaces de entrada e enviá-lo para a interface de saída apropriada.

Discorra sobre o processo de encaminhamento de datagramas IP em um roteador, abordando os seguintes pontos:
- Função Primária do Roteador no Plano de Dados: Explique qual é a principal responsabilidade de um roteador no plano de dados da Camada de Rede e como essa função se diferencia do "roteamento".
- Utilização da Tabela de Encaminhamento (FIB): Descreva como um roteador utiliza sua Tabela de Encaminhamento (_Forwarding Information Base - FIB_) para tomar decisões sobre para onde enviar um datagrama IP que chega.
- Regra do Maior Prefixo Correspondente (Longest Prefix Matching): Explique detalhadamente a regra do "maior prefixo correspondente" e por que ela é um mecanismo crucial para a decisão de encaminhamento em redes IP.

- Aplicação Prática: Considere a seguinte Tabela de Encaminhamento simplificada de um roteador:

| Prefixo de Destino | Interface de Saída |
| ------------------ | ------------------ |
| 192.168.1.0/24     | Interface 1        |
| 192.168.1.128/25   | Interface 2        |
| 192.168.1.192/26   | Interface 3        |
| 10.0.0.0/8         | Interface 4        |
| Padrão (0.0.0.0/0) | Interface 5        |
|                    |

 Para cada um dos endereços IP de destino abaixo, indique qual Interface de Saída o roteador escolheria, justificando sua resposta com base na regra do maior prefixo correspondente: 

<ol style="list-style-type: lower-alpha">
<li>192.168.1.130</li>
<li>192.168.1.200</li>
<li>172.16.5.10</li>
<li>192.168.1.50</li>
</ol>

5. [1,5 pontos] O endereçamento IPv4 é a base da comunicação na Internet e em redes locais. Para otimizar o uso dos endereços e segmentar as redes de forma eficiente, utilizamos o conceito de subnetting (sub-redes). Isso permite dividir uma rede maior em sub-redes menores, cada uma com seu próprio identificador de rede e faixa de endereços.

Sua tarefa é analisar os endereços IPv4 listados na tabela abaixo, cada um com seu respectivo prefixo de rede (CIDR). Para cada entrada, você deverá calcular e preencher as colunas indicadas:
- Máscara de Sub-rede: A máscara de sub-rede em formato decimal pontuado.
- Endereço de Rede: O primeiro endereço da sub-rede (identificador da rede).
- Endereço de Broadcast: O último endereço da sub-rede (endereço de broadcast).
- Range de IPs Válidos: A faixa de endereços IP que podem ser atribuídos a hosts dentro dessa sub-rede (excluindo o endereço de rede e o de broadcast).
abela para Preenchimento:

| Endereço IP/Prefixo | Máscara de Sub-rede | Endereço de Rede | Endereço de Broadcast | Range de IPs Válidos |
| ------------------- | ------------------- | ---------------- | --------------------- | -------------------- |
| 192.168.10.15/27    |
| 172.16.25.100/22    |
| 10.0.0.1/29         |
| 192.168.50.200/26   |
| 172.30.1.150/20     |
|                     |

6. [1,0 ponto] O IPv6, a próxima geração do Protocolo de Internet, utiliza endereços de 128 bits, o que os torna muito mais longos que os endereços IPv4. Para facilitar a leitura e a escrita desses endereços, foram estabelecidas regras de compactação. É fundamental compreender essas regras para trabalhar eficientemente com o IPv6.

Sua tarefa é aplicar as regras de compactação e expansão de endereços IPv6. Lembre-se das duas principais regras de compactação estudadas.Com base nessas regras, preencha a tabela abaixo, convertendo os endereços IPv6 para o formato solicitado:

| <div style="width:400px">Endereço Completo </div> | <div style="width:300px">Endereço Compactado</div> |
| ------------------------------------------------- | -------------------------------------------------- |
| 2001:0db8:0000:0000:0000:ff00:0042:0329           |
| fe80:0000:0000:0001:0000:00ca:fe00:0001           |
| 2001:0db8:00a3:0000:0000:000e:0370:0000           |
| fc00:0000:0000:0000:0000:0000:0000:0001           |
| 0000:0000:0000:0000:0000:0000:0000:0000           |
|                                                   | 2001:db8::1                                        |
|                                                   | fe80::21f:5bff:fe33:8588                           |
|                                                   | ::1                                                |
|                                                   | 2001:db8:0:0:1::                                   |
|                                                   | 2001:db8:0:1:1:1:1:1                               |


7. [2,0 pontos] A Camada de Rede é a responsável por levar pacotes de dados de um host de origem a um host de destino, mesmo que estejam em redes distintas e geograficamente separadas. Para que essa comunicação de fim a fim seja possível, os roteadores precisam saber "para onde" enviar os pacotes. Essa inteligência é construída através do roteamento, um processo dinâmico e complexo que envolve a troca de informações entre roteadores.

Discorra sobre o conceito de roteamento e seus protocolos, abordando os seguintes pontos:
- Roteamento vs. Encaminhamento (Forwarding): Explique a diferença fundamental entre os conceitos de roteamento (routing) e encaminhamento (forwarding). Descreva qual deles pertence ao plano de controle e qual pertence ao plano de dados de um roteador, e como eles se complementam para a entrega de pacotes.
- A Necessidade dos Protocolos de Roteamento: Por que os roteadores precisam de protocolos de roteamento? Qual é o objetivo principal desses protocolos na Camada de Rede?
- Classificação dos Protocolos de Roteamento: Apresente as duas principais categorias de protocolos de roteamento baseados em algoritmos (excluindo o BGP por enquanto) e explique a lógica geral por trás de cada uma.
- Protocolos de Roteamento Intra-AS (IGPs):
    - Explique o que é um Sistema Autônomo (AS) e qual a função dos protocolos de roteamento Intra-AS (IGPs) dentro desse contexto.
    - Descreva como o protocolo OSPF (Open Shortest Path First) opera para construir as tabelas de roteamento em um AS. Inclua os principais passos do algoritmo de estado de enlace que o OSPF utiliza, mencionando os tipos de mensagens e as estruturas de dados envolvidas.
- Protocolos de Roteamento Inter-AS (EGPs) - O BGP:
    - Explique por que um protocolo como o BGP (Border Gateway Protocol) é necessário para o roteamento entre Sistemas Autônomos (ASs), e por que os protocolos Intra-AS não são adequados para essa finalidade.
    - Descreva brevemente a principal característica do BGP que o diferencia dos protocolos Intra-AS (por exemplo, ser um protocolo de vetor de caminho).

