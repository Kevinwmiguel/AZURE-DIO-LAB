# AZURE-DIO-LAB

# O que é computação em nuvem?
- Uso de servidores, redes, armazenamento e software através da internet (ao invés de servidores locais).

* Vantagens
- Escalabilidade
- Alta disponibilidade
- Pagamento sob demanda
- Backup e recuperação
- Segurança

** Azure é a nuvem da Microsoft.
** AZ-900 é teórico, AZ-104 é prático.
** VM = computador virtual, Storage = arquivos/discos.
** Resource Group = pasta de recursos.

* Diferença entre Nuvem Pública, Privada e Híbrida

# Nuvem Pública
 Infraestrutura compartilhada, acessível pela internet.

* Características:
- Fornecida por empresas como Azure, AWS, Google Cloud
- Usuários diferentes compartilham os mesmos datacenters, com isolamento lógico
- Recursos são alugados sob demanda (pay-as-you-go)
- Alta escalabilidade e flexibilidad

# Nuvem Privada
  Infraestrutura exclusiva, dedicada a uma única empresa.

* Características:
- Pode estar on-premises (no seu próprio datacenter) ou ser hospedada por terceiros
- Controle total de segurança, hardware, compliance
- Mais customizável, mas mais cara e menos escalável que pública

# Nuvem H+ibrida
  Combinação da nuvem pública + privada, com integração entre elas.

* Características:
- Parte da carga roda na nuvem pública (ex: site)
- Parte roda em nuvem privada (ex: dados sigilosos)
- Flexível: pode mover cargas conforme necessidade

----

# ExpressRoute
- Serviço do Azure que cria conexão privada (não passa pela internet pública) entre sua rede local (on-premises) e a rede da Microsoft.
- Mais seguro, estável e rápido que uma VPN comum.
- Usado quando se quer baixa latência e alta largura de banda para acesso ao Azure.

# VPN Gateway
- Dispositivo virtual no Azure que cria túneis criptografados entre sua rede local e uma VNet no Azure.
- Usa internet pública, mas com tráfego protegido (IPSec/IKE).
- Bom para cenários de custo mais baixo ou como backup do ExpressRoute.

# Containers
- Ambiente isolado para executar aplicações, mais leve que máquinas virtuais.
- No Azure, podem ser executados via Azure Container Instances, AKS (Kubernetes), ou outros serviços.
- Permitem portabilidade, escalabilidade rápida e consistência entre desenvolvimento e produção.

# Conjuntos de disponibilidade (Availability Sets)
- Estratégia para alta disponibilidade de VMs.
- Distribui máquinas virtuais entre domínios de falha (hardware diferente) e domínios de atualização (evita reboot simultâneo).
- Garante SLA maior (geralmente 99,95%).

# VNet (Virtual Network)
- Rede virtual privada dentro do Azure, isolada e personalizável.
- Permite definir sub-redes, rotas, NAT, firewall, peering e integração com redes locais.
- Base para conectar VMs, containers e serviços de forma segura.

# Azure Functions
- Serviço de serverless computing: você só escreve a função, a Microsoft cuida do servidor, escala e execução.
- Bom para tarefas event-driven, automações e integrações rápidas.
- Cobra apenas pelo tempo de execução e consumo.

# Emparelhamento de Rede (VNet Peering)
- Conecta duas VNets de forma privada e direta, como se fossem a mesma rede.
- Pode ser na mesma região ou entre regiões (Global VNet Peering).
- Baixa latência e alta velocidade, sem necessidade de VPN ou gateway.
