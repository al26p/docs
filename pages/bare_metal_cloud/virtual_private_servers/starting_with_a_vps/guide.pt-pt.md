---
title: Primeiros passos com um VPS
excerpt: Aprenda a gerir um VPS na sua Área de Cliente e descubra as primeiras etapas da sua utilização, nomeadamente as ligações remotas e as medidas de segurança
updated: 2024-01-10
---

> [!primary]
> Esta tradução foi automaticamente gerada pelo nosso parceiro SYSTRAN. Em certos casos, poderão ocorrer formulações imprecisas, como por exemplo nomes de botões ou detalhes técnicos. Recomendamos que consulte a versão inglesa ou francesa do manual, caso tenha alguma dúvida. Se nos quiser ajudar a melhorar esta tradução, clique em "Contribuir" nesta página.
>
 
## Objetivo

Um servidor privado virtual (VPS) é um servidor dedicado virtualizado. Ao contrário das ofertas de alojamento web da OVHcloud, que são geridas pela OVHcloud, a configuração e a manutenção de um sistema VPS são da sua responsabilidade enquanto administrador de sistemas.

**Descubra as informações necessárias para dar os primeiros passos num VPS.**


## Requisitos

- Ter um [VPS](https://www.ovhcloud.com/pt/vps/) na Área de Cliente OVHcloud
- Ter acesso à [Área de Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt)

## Instruções

Aceda à sua [Área de Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt), vá à secção `Bare Metal Cloud`{.action} e selecione o seu servidor na secção `Servidores privados virtuais`{.action}.

### Interface da Área de Cliente

O separador `Página`{.action} inicial contém informações importantes sobre o serviço e permite-lhe realizar operações essenciais.

![VPS Home](images/vpshome.png){.thumbnail}

#### O seu VPS <a name="yourvps"></a>

Esta secção apresenta informações básicas sobre este VPS e o estado do serviço.

##### **Nome**

Se clicar em `...`{.action} e selecionar `Alterar nome`{.action}, poderá introduzir um nome diferente para este VPS. Esta funcionalidade é útil para facilitar a navegação na Área de Cliente quando gere vários serviços VPS. O nome do serviço interno permanece no formato *vps-XXXXXXX.vps.ovh.net*.

##### **Boot**

O modo de arranque apresentado aqui é ou no modo « normal », no qual o sistema carrega o sistema operativo instalado (*LOCAL*), ou no **modo rescue** fornecido pela OVHcloud em caso de deteção e resolução de problemas. Utilize o botão `...`{.action} para [reiniciar o VPS](#reboot-current-range) ou inicie-o em modo rescue.

Pode encontrar mais informações no nosso guia sobre o [modo rescue](/pages/bare_metal_cloud/virtual_private_servers/rescue).

##### **SO / Distribuição**

Trata-se do sistema operativo atualmente instalado. Utilize o botão `...`{.action} para [reinstalar o mesmo sistema operativo ou selecione outro de entre as opções disponíveis](#reinstallvps).

Tenha em conta que uma reinstalação levará à eliminação de todos os dados alojados no VPS (com exceção dos discos adicionais).

> [!primary]
>
> Se adquiriu uma VPS **Windows**, só pode escolher um SO Windows para a reinstalação. Do mesmo modo, se o Windows não for selecionado durante a encomenda, não poderá ser instalado após a entrega do VPS.
>

Uma vez instalado, o sistema deverá implementar as atualizações de segurança. Encontrará mais informações [abaixo](#reinstallvps) e no nosso guia Como [Proteger um VPS](/pages/bare_metal_cloud/virtual_private_servers/secure_your_vps).

##### **Zona** / **Localização**

Estas secções fornecem informações sobre a localização do VPS. Isto pode ser útil, por exemplo, para identificar os impactos no seu serviço mencionados no [status reports](https://bare-metal-servers.status-ovhcloud.com/).

#### A sua configuração

##### **Modelo**

Este elemento indica a referência comercial que identifica o modelo de VPS correspondente às [ofertas VPS no nosso site](https://www.ovhcloud.com/pt/vps).

##### **vCores** / **Memória** / **Armazenamento**

Os recursos atuais do seu VPS são apresentados aqui e podem ser atualizados separadamente clicando no botão correspondente. As atualizações são limitadas pelo modelo de VPS selecionado e só podem estar disponíveis com a mudança para uma [gama superior](https://www.ovhcloud.com/pt/vps).

#### IP

##### **IPv4**

O endereço IPv4 público principal do VPS é configurado automaticamente durante a instalação. Encontre mais informações sobre a gestão dos IP no nosso guia [Configuring IP aliasing](/pages/bare_metal_cloud/virtual_private_servers/configuring-ip-aliasing).

##### **IPv6** / **Gateway**

Pode ver aqui o endereço IPv6 público e o endereço do gateway associado. Estes são automaticamente associados ao VPS aquando da instalação. Para mais informações, consulte [este guia](/pages/bare_metal_cloud/virtual_private_servers/configure-ipv6).

##### **DNS secundário**

Esta funcionalidade é útil para alojar serviços DNS. O nosso guia [Configurar o DNS secundário da OVHcloud num VPS](/pages/bare_metal_cloud/virtual_private_servers/adding-secondary-dns-on-vps) descreve-o em pormenor.

#### Resumo das opções

Estas opções referem-se a serviços VPS suplementares que podem ser encomendados na Área de Cliente.

- A opção `Snapshot` permite-lhe criar uma snapshot manual como ponto único de restauro.
- A opção `Backups automatizados` permite-lhe conservar várias snapshots do seu VPS (exceto discos adicionais).
- A opção `Discos adicionais` permite associar espaço de armazenamento ao seu VPS, por exemplo, para armazenar dados de backup.

Encontrará na [página do produto](https://www.ovhcloud.com/pt/vps/options/) e nos respetivos [manuais informações sobre as soluções de backup disponíveis para o serviço](/products/bare-metal-cloud-virtual-private-servers-backups).

#### Subscrição

Estas secções apresentam as informações mais importantes sobre a faturação do serviço. Encontre todas as informações sobre este assumpto na [documentação correspondente](/products/account-and-service-management-managing-billing-payments-and-services).

### Funções VPS disponíveis no separador Página Inicial

> [!warning]
>
> A OVHcloud fornece-lhe serviços cuja configuração e gestão são da sua responsabilidade. É da sua responsabilidade assegurar o seu bom funcionamento.
>
> Este guia tem como objetivo ajudá-lo a realizar as tarefas mais habituais. No entanto, se encontrar dificuldades ou dúvidas relativamente à administração, utilização ou implementação de serviços num servidor, recomendamos que contacte um [fornecedor de serviços especializado](https://partner.ovhcloud.com/pt/directory/) ou que contacte a [nossa comunidade](https://community.ovh.com/en/).
>

### Reinstalação do seu VPS <a name="reinstallvps"></a>

As reinstalações podem ser efetuadas a partir da Área de Cliente. Clique em `...`{.action} junto a **SO / Distribuição**, e em `Reinstalar o meu VPS`{.action}.

![VPSnewreinstall](images/2023panel_01.png){.thumbnail}

Na janela que aparece, escolha um sistema operativo da lista suspensa. As opções propostas são imagens [compatíveis com um VPS OVHcloud](/pages/public_cloud/compute/image-life-cycle) e são imediatamente funcionais após a instalação.

Pode também selecionar uma **chave SSH** a instalar no sistema, se tiver armazenado uma anteriormente na sua [Área de Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt). Para saber tudo sobre este assumpto, consulte o guia [Criar e utilizar chaves SSH](/pages/bare_metal_cloud/dedicated_servers/creating-ssh-keys-dedicated).

> [!primary]
>
> **Licenças**
>
> Alguns sistemas operativos ou plataformas proprietárias, como o Plesk ou cPanel, requerem licenças que implicam custos adicionais. As licenças são administradas a partir da Área de Cliente: aceda à secção `Bare Metal Cloud`{.action} e clique em `Licenças`{.action} na barra à esquerda.
>
> Para ter um sistema operativo **Windows** a correr num VPS, é preciso **selecionar no processo de encomenda**. Um VPS com outro SO instalado não pode ser reinstalado com Windows da forma descrita acima.
>

Aparece uma barra de progresso da instalação na Área de Cliente. Tenha em conta que este processo pode demorar até 30 minutos.

### Reinicialização do VPS <a name="reboot-current-range"></a>

Pode ser necessário reiniciar para aplicar configurações atualizadas ou resolver um problema. Sempre que possível, execute uma « de reinício de software » a partir da interface gráfica do servidor (Windows, Plesk, etc.) ou através da linha de comandos:

```bash
sudo reboot
```

No entanto, pode efetuar um « de reinício de hardware » a qualquer momento a partir da sua [Área de Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.pt/&ovhSubsidiary=pt). No separador `Página Inicial`{.action}, clique em `...`{.action} junto de `Boot` na secção **O seu VPS**. Selecione `Reiniciar o meu VPS`{.action} e clique em `Validar`{.action} na janela que se abrir.

![Reboot](images/reboot-vps01.png){.thumbnail}

### Ligação ao seu VPS (OS GNU/Linux)

Durante a primeira instalação ou ao reinstalar a partir do Painel de controle, um usuário com altas permissões é criado automaticamente. Este utilizador será nomeado em função do sistema operativo, por exemplo « ubuntu » ou « rocky ».

Receberá um e-mail com o nome de utilizador e a palavra-passe necessários para aceder ao seu VPS por SSH. O SSH é um protocolo de comunicação segura que é utilizado para estabelecer ligações encriptadas com um host remoto.

A maioria dos sistemas operativos de desktop atuais terão um cliente **Open SSH** instalado nativamente. Isto significa que as credenciais de acesso lhe permitem aceder rapidamente ao VPS através da aplicação de linha de comandos adequada (`Terminal`, `Command prompt`, `Powershell`, etc.). Introduza o seguinte comando:

```bash
ssh username@IPv4_VPS
```

Por exemplo:

```bash
ssh ubuntu@169.254.10.250
```

Também pode utilizar qualquer aplicação de terceiros compatível com **Open SSH**.

Uma vez ligado, pode alterar a palavra-passe predefinida do utilizador padrão para uma forte frase secreta utilizando este comando:

```bash
passwd
```

```console
Changing password for ubuntu.
Current password:
New password: 
Retype new password: 
passwd: password updated successfully
```

**Recomendamos que efetue o seguinte procedimento**:

- Familiarizar-se com as ligações SSH consultando o guia [Introdução ao SSH](/pages/bare_metal_cloud/dedicated_servers/ssh_introduction).
- Considere a utilização de chaves SSH como um método avançado e mais prático para as ligações remotas através do nosso manual [Criar e utilizar chaves SSH](/pages/bare_metal_cloud/dedicated_servers/creating-ssh-keys-dedicated).
- Utilize o nosso guia [Tornar seguro um VPS](/pages/bare_metal_cloud/virtual_private_servers/secure_your_vps) para proteger o seu sistema contra ataques automatizados de *brute force* e outras ameaças comuns.

> [!primary]
>
Tenha em conta que se selecionou uma **distribuição com aplicação** (Plesk, cPanel, Docker), as medidas de segurança genéricas podem não se aplicar ao seu sistema. Sugerimos que consulte os nossos manuais [Primeiros passos com as aplicações pré-instaladas](/pages/bare_metal_cloud/virtual_private_servers/apps_first_steps) e [Implementar o cPanel num VPS](/pages/bare_metal_cloud/virtual_private_servers/cpanel), assim como a documentação oficial do editor em causa.
>

#### Ativar ligações root

> [!warning]
>
> Por predefinição, a ligação ao utilizador « root » está desativada por razões de segurança. Consulte as instruções [deste guia](/pages/bare_metal_cloud/virtual_private_servers/root_password#enable-root-login) para verificar se pretende permitir estas ligações.
>

#### Atualização da palavra-passe root

Para alterar ou atualizar a sua palavra-passe « root », consulte as instruções [deste guia](/pages/bare_metal_cloud/virtual_private_servers/root_password).

### Ligação ao seu VPS Windows

Após a instalação do VPS Windows, receberá um e-mail com o nome de utilizador predefinido do `Windows user`.

De seguida, conclua a instalação do Windows definindo o idioma, o layout do teclado e a palavra-passe do administrador.

Para isso, utilize a nossa consola KVM: clique em `...`{.action} junto ao nome do seu VPS, na secção [O seu VPS](#yourvps) e selecione `KVM`{.action}. Pode encontrar mais informações sobre esta ferramenta no nosso [guia KVM](/pages/bare_metal_cloud/virtual_private_servers/secure_your_vps).

Para terminar a instalação do VPS Windows através do KVM, siga os passos descritos no guia [Configurar uma nova instalação do Windows Server](/pages/bare_metal_cloud/virtual_private_servers/windows_first_config).

No seu equipamento Windows local, pode utilizar a aplicação cliente `Remote Desktop Connection` para se ligar ao VPS.

![Windows Remote](images/windows-connect-03.png){.thumbnail}

Introduza o endereço IPv4 do seu VPS, depois o seu identificador e a sua passphrase. Normalmente, é apresentada uma mensagem a avisar-lhe para confirmar a ligação devido a um certificado desconhecido. Clique em `Sim`{.action} para iniciar sessão.

Também pode utilizar qualquer aplicação de terceiros compatível com RDP. Esta condição é necessária se o Windows não estiver instalado no seu dispositivo local.

> [!primary]
>
Se encontrar problemas com este procedimento, verifique se as ligações remotas (RDP) são permitidas no seu dispositivo verificando as definições do sistema, as regras da firewall e as restrições de rede possíveis.
>

### Como proteger o VPS

Enquanto administrador do seu VPS, é responsável pela segurança das aplicações e dos dados alojados.

Consulte o nosso manual sobre Como [proteger um VPS](/pages/bare_metal_cloud/virtual_private_servers/secure_your_vps) para obter conselhos essenciais sobre como proteger o seu sistema.

> [!primary]
>
Tenha em conta que se selecionou uma **distribuição com aplicação** (Plesk, cPanel, Docker), as medidas de segurança genéricas podem não se aplicar ao seu sistema. Sugerimos que consulte os nossos manuais [Primeiros passos com as aplicações pré-instaladas](/pages/bare_metal_cloud/virtual_private_servers/apps_first_steps) e [Implementar o cPanel num VPS](/pages/bare_metal_cloud/virtual_private_servers/cpanel), assim como a documentação oficial do editor em causa.
>

### Associar um nome de domínio

A passagem do seu VPS na web passa geralmente pela atribuição de um nome de domínio e a sua configuração DNS. Se gere o seu domínio na OVHcloud, pode consultar o nosso guia [Editar uma zona DNS da OVHcloud](/pages/web_cloud/domains/dns_zone_edit) para obter instruções.

### Proteger um nome de domínio com um certificado SSL

Depois de configurar o VPS, pode querer proteger o seu domínio e o seu website. Isto requer um certificado SSL, que permite o acesso à Internet do VPS através de *HTTPS* em vez de *HTTP* não seguro.

O certificado SSL pode ser instalado manualmente no VPS. Consulte a documentação oficial da sua distribuição VPS.

Para um processo mais automatizado, a OVHcloud propõe igualmente a solução SSL Gateway. Consulte a [página do produto](https://www.ovh.pt/ssl-gateway/) ou a [documentação de apoio](/products/web-cloud-ssl-gateway) para obter mais informações.

## Quer saber mais?

[VPS FAQ](/pages/bare_metal_cloud/virtual_private_servers/vps-faq)

[Introdução ao SSH](/pages/bare_metal_cloud/dedicated_servers/ssh_introduction)

[Como proteger um VPS](/pages/bare_metal_cloud/virtual_private_servers/secure_your_vps)

[Configurar uma nova instalação do Windows Server](/pages/bare_metal_cloud/virtual_private_servers/windows_first_config)

Junte-se à nossa comunidade de utilizadores em <https://community.ovh.com/en/>.
