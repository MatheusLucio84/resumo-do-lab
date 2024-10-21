# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO
##Microsoft - Azure
Estou arpendendo muito sobre programação na nuvem, as aulas est~]ao sendo praticas e de bom conhecimento adiquirido.
passamos para os proximos passos.

##Criando Maquinas Virtuais
SLa é o tempo de disponibilidade da maquina virtual, quantos mais 99,999 maior a disponibilidade e tambem o custo, avaliar qual o melhor custo beneficio para a empresa.
analisar tambem a disponibilidade em varias regiões é importante para melhoria de custo.

##Tipos de Serviços na Nuvem
IaaS: Infraestrutura como serviço (maquina Virtual) – toda configuração do usuário, seu gerenciamento
Servidores e armazenamento / Firewalls, segurança e rede / Planta física, edifício datacenter.
PaaS: Plataforma como serviço (rodar apenas o banco de dados) sem focar na infraestrutura, maquina virtual pela plataforma. Focado o desenvolvimento.
Sistema Operacional, Ferramentas para os desenvolvedores, analise de negócio e data-base.
SaaS: Software como Serviço (licenças de uso, libera pacotes) pagamento conforme uso.
	Aplicativos e APPs hospedados.
Modulo 2
Componentes de Arquitetura:
Regiões, pares e regiões soberanas.
Recursos, assinaturas e grupos de gerenciamento.
Hierarquia de Grupos.

Regiões: 
Quanto mais perto do usuário mais rápido o acesso.
Custos, nem todos os recursos estão disponíveis em todas as regiões.
 Preview em teste.
Está disponível para todos. 
Flexível para escala para reduzir a latência do cliente.
Zona de disponibilidades tem proteção contra tempo de inatividades, separa fisicamente os dataceter dentro da mesma região.
Cada datacenter da zona é independente.
São conectados por meio de redes privadas de fibra óptica.

Pares de Regiões:
Replica automática para alguns serviços.
Recuperação de região priorizada em caso de interrupção.
Atualização são distribuídas sequencialmente para minimizar o tempo de inatividade.
Região Ativo-inativo, configurar após colapso para funcionar requisição.
Região Soberanas.
Azure governamental para o governo dos estados unidos.
Azure China, fisicamente e separado por nuvem operam 21Vianet, todos os dados tem de ficar dentro da china.
Recursos do Azure:
Maquinas virtuais, contas de armazenamento, redes virtuais, serviços de aplicativos, bancos de dados, funções.
Grupo de recursos: painel para organização, agregando recursos em uma única unidade.
Os recursos podem existir em apenas um grupo de recursos, os recursos podem existir em diferentes regiões.
Os recursos podem ser movidos entre recursos, o grupo de recurso não pode mudar de nome.
Os aplicativos podem utilizar vários grupos de recursos.
Assinaturas do Azure.
Uma conta pode ter varias assinaturas, mas uma assinatura pode ter apenas uma conta.
Organização na parte de quem vai pagar, via assinatura.
Limita também o controle de acesso.
Grupo de Gerenciamento => Assinaturas => Grupo de Recursos => Recursos
Grupos de Gerenciamento podem incluir várias assinaturas.
Assinaturas herdam as condições aplicadas pelo gerenciamento.

Componentes de arquitetura do Azure.
Computação na rede:
Tipos de computação: Máquina Virtual, aplicativo de serviços, Container de Instancias, AKS (Serviço de Kubernettes da Azure), Area de trabalho Virtual (computador para o funcionário trabalhar).
Maquibas Virtuais do Azure (VMs) são emulações de software de computadores físico.
Processador virtual, memória, armazenamento e rede.
Oferta de IaaS que oferece personalização e controle total;
Conjunto de dimensionamento, balanceamento de carga para dimensionar os recursos automaticamente.
Conjunto de Disponibilidades de VM
Maquinas em rack diferentes. Domínio de falha,  mínimo 3 domínio de falhas, domínio de atualização
Area de trabalho virtual:
Reduz o risco de que o recurso seja perdido, implantação reais de várias sessões.  Computador virtual.
Os Contêineres da Azure:
Ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional.
PaaS contêiner da Azure. Ou pod
Aplicativos de contêineres pode balancear a carga e escalar.
Kubernete – serviços de orquestração dos contêineres, organizar grandes volumes de contêineres.

Azure Functions:
Executar atividades em determinado eventos. Plataforma como serviço PaaS, sem necessidade de sistema operacional.
Lift-and-shift levar como está para nuvem.
Área de trabalho virtual rastreabilidade, e segurança.
Contêineres: ambiente leves em miniatura, aplicativos e serviços empacotados.
Serviços de Aplicativos:
Aplicativos Web e APIs rapidamente – Aceita Git / Github.
PaaS
Rede Virtual do Azure (Vnet):
Permite que os recursos se comuniquem uns com outros, com a internet e as redes locais. Precisa ser configurados para comunicação.
Comunicação publica e privados. Cuidados com ips iguais em redes diferentes.
Gateway de VPN – tráfego criptografado entre rede virtual do Azure e local.
ExpressRoute – comunicação via cabo. Proximidade ao Datacenter, rapides e confiabilidade.
DNS Azures: usa rede Anycast – confiabilidade e desempenho. Baseado no gerenciamento de recursos, habilitando o controle de acesso e monitoramento e registro log.

Azure Functions:
Executar atividades em determinado eventos. Plataforma como serviço PaaS, sem necessidade de sistema operacional.
Lift-and-shift levar como está para nuvem.
Área de trabalho virtual rastreabilidade, e segurança.
Contêineres: ambiente leves em miniatura, aplicativos e serviços empacotados.
Serviços de Aplicativos:
Aplicativos Web e APIs rapidamente – Aceita Git / Github.
PaaS
Rede Virtual do Azure (Vnet):
Permite que os recursos se comuniquem uns com outros, com a internet e as redes locais. Precisa ser configurados para comunicação.
Comunicação publica e privados. Cuidados com ips iguais em redes diferentes.
Gateway de VPN – tráfego criptografado entre rede virtual do Azure e local.
ExpressRoute – comunicação via cabo. Proximidade ao Datacenter, rapides e confiabilidade.
DNS Azures: usa rede Anycast – confiabilidade e desempenho. Baseado no gerenciamento de recursos, habilitando o controle de acesso e monitoramento e registro log.

Redundancia de armazenamento
LRS -3 copias em um único datacenter (não indicado para produção, arquivos sensíveis muito utilizado, para teste e desenvolvimento)
ZRS – 3 copias em datacenter diferentes espalhado na região (atualização assíncrono, com um pequeno delay)
Blob do Azures: otimizando para o armazenamento de quantidades massivas de dados não estruturados, como texto ou dados binários.
Disco do Azure: fornece discos para maquinas virtuais aplicativos. (a quente)
Fila do Azure: serviço de armazenamento de mensagens.
Arquivos do Azure: (files) compartilhamento de rede e arquivos altamente disponível.
Tabelas do Azure: Fornece uma opção de chave armazenamento de dados estruturados.
Migração Azure.
Plataforma unificada, ferramentas integras e autônomas, avaliação de migração.
Azure Data Box: 80 TB de transporte físico de dados. Caixa robusta durante do trânsito.
Snomobil carreta para movimentação de dados.
Transporte de arquivos criptografados.
AzCopy: utilitário linha de comando, sincronização em uma única direção. Copiar blobs ou arquivos para sua conta de armazenamento.
Gerenciador de armazenamento do azure.
Interface gráfica do usuário, semelhante ao Windows explores, compatível com o Windows, macos e Linux.
Sincronização com os arquivos da Azure e locais de forma bidirecional.

##Identidade, Acesso e Segurança.
Estratégias de segurança. Microsoft defender Cloud
Microsoft Entra ID e Domain Services
Entra ID: serviço de diretório controla identidade de acesso.
Validador de acesso. Logon único (SSO), negócios (B2B)
Cria usuário no on primisse, sistema local, migra para nuvem, se criar na nuvem não vem o usuário.
Autenticação:
Credenciais de acesso legítimo, identifica a pessoa.
Autorização:
controle de seguranças acesso a níveis de arquivos e sistemas.
Autenticação multifator MFA: segurança adicional, dois ou mais elementos. Token, cartão ou pop-up
Windows hello – proteção em 2 camadas
B2B – pode usar validação por meio de outras plataformas (google, facebook, azure, outros)
B2C – compartilhamento de dados compartilhado dados de identidade externa.
Acesso Condicional: sinais, autenticação em vários fatores. Monitora em detalhes de segurança. IP, localização, dispositivos.
Controle de acesso baseado em função: RBac seleção acesso fino aos usuários, quanto menos melhor.
Acesso liberado, á recursos ou grupos.
Quanto mais alto o acesso, vc herda o acesso abaixo.
Confiança Zero: sempre desconfia. Politica central protegendo cada recurso. Proteção por camadas.
Proteção completa, garante proteção de camadas isoladas. Vários níveis de proteção.
Defender para nuvem: proteção dos datacenters Azure e Local.
Controle just-in-time das portas, detectar malware, recomendações de segurança.

Usuários criados na nuvem não migram para o sistema local.
Usuário são permanentemente deletados após 30 dias.

##Gerenciamento de Custos na Azure
TCO – Custo total d propriedade
Fatores que afetam o custo:
Tipo de recursos – tem os custos especifico.
Consumo – pagar conforme o uso e Reserva para usar o recurso por um tempo determinado a longo prazo. (tempo de uso das maquias virtuais pode ser desligada)
Manutenção – volume de uso do ambiente, saber desligar maquinas e recursos.
Área Geográfica – podem alterar por conta de imposto.
Tráfego de rede – entradas seja gratuita, a saída ou consulta enre recursos e afetado por zonas de cobrança.
Assinatura – Tipo e configuração alteram o custo.
Marketplace – permite os clientes experimentem, compare e provisionem aplicativos dentro da plataforma.
	Software abertos, não nativo Microsoft, problema com eles deve procurar help desck do fornecedor.
Calculadora de preços – ajuda a estimar o custo dos produtos.
TCO – Compara a economia de custo para migrar para Azure. Relatório de custo das infraestruturas locais com custo de uso de produtos na nuvem.
Gerenciamento de custo - Configuração de alertas por uso de consumo acima da média.
Marcas ou Tags – Não são herdáveis, fornecem metadados aos recursos. Muito úteis para reunir informações de cobranças.



