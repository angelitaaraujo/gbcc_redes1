<style>
    body {
        font-size: 12px;
    }
    pre {
        font-size: 11px;
    }
</style>
## Comandos úteis
Esta é uma lista de comandos essenciais para configurar os roteadores e switches da AngelCorp. Lembre-se de substituir os valores genéricos pelos endereços IP, máscaras, IDs de processo e AS corretos que você calcular e determinar para sua rede.

1. Acesso e Modos de Configuração

Acessar Modo Privilegiado
```
enable
```

Acessar Modo de Configuração Global:
```
configure terminal
```

2. Configurações Básicas do Dispositivo

Definir Nome do Dispositivo (Hostname):
```
hostname [NOME_DO_DISPOSITIVO]
```

Salvar a Configuração:
```
copy running-config startup-config
```
(Confirme a operação pressionando ENTER na próxima linha)

3. Configuração de Interfaces

Entrar no Modo de Configuração de Interface:
```
interface [TIPO_DE_INTERFACE] [NÚMERO_DA_INTERFACE]
```

Configurar Endereço IP e Máscara na Interface:
```
ip address [ENDEREÇO_IP] [MÁSCARA_DE_REDE]
```

Ativar a Interface (no shutdown):
```
no shutdown
```
(Interfaces seriais também podem precisar de clock rate se forem DCE)
```
clock rate 256000
```

Sair do Modo de Configuração de Interface:
```
exit
```


4. Roteamento Estático

Configurar uma Rota Estática para uma Rede Específica:
```
ip route [REDE_DE_DESTINO] [MÁSCARA_DA_REDE_DE_DESTINO] [PRÓXIMO_SALTO_IP]
```
Exemplo: ip route 172.16.0.0 255.255.255.0 10.0.0.2

Configurar uma Rota Estática Padrão (Default Route):
```
ip route 0.0.0.0 0.0.0.0 [PRÓXIMO_SALTO_IP]
```

5. Roteamento OSPF (Open Shortest Path First)

Entrar no Modo de Configuração OSPF:
```
router ospf [ID_DO_PROCESSO_OSPF]
```

Definir Router ID (Recomendado):
```
router-id [ENDEREÇO_IP_UNICO]
```

Anunciar Redes OSPF (em uma Área):
```
network [ENDEREÇO_DE_REDE] [WILDCARD_MASK] area [NÚMERO_DA_ÁREA]
```

Definir Interface como Passiva (para interfaces LAN, onde não há outro roteador OSPF):
```
passive-interface [TIPO_DE_INTERFACE] [NÚMERO_DA_INTERFACE]
```
Exemplo: passive-interface GigabitEthernet 0/0

Sair do Modo de Configuração OSPF:
```
exit
```


6. Roteamento BGP (Border Gateway Protocol)

Entrar no Modo de Configuração BGP:
```
router bgp [NÚMERO_DO_SISTEMA_AUTÔNOMO]
```

Configurar Vizinho (Neighbor):
```
neighbor [IP_DO_VIZINHO] remote-as [AS_DO_VIZINHO]
```

Anunciar Redes (para BGP):
```
network [ENDEREÇO_DE_REDE] mask [MÁSCARA_DE_REDE]
```

Redistribuir Rotas de Outros Protocolos (Ex: OSPF para BGP):
```
redistribute ospf [ID_DO_PROCESSO_OSPF]
```
Exemplo: redistribute ospf 1

Sair do Modo de Configuração BGP:
```
exit
```

### Comandos Úteis de Verificação (Modo Privilegiado Router#)

Mostrar Tabela de Rotas IP:
```
show ip route
```

Mostrar Status de Interfaces:
```
show ip interface brief
```

Mostrar Vizinhos OSPF:
```
show ip ospf neighbor
```

Mostrar Protocolos de Roteamento Configurados:
```
show ip protocols
```

Mostrar Sumário de Vizinhos BGP:
```
show ip bgp summary
```

Mostrar Tabela BGP:
```
show ip bgp
```

Testar Conectividade:
```
ping [ENDEREÇO_IP_DE_DESTINO]
```

Rastrear Rota:
```
traceroute [ENDEREÇO_IP_DE_DESTINO]
```