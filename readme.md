Tutorial de Configuração e Uso do LiDAR SimuLS30H

Este repositório contém um tutorial completo para configurar, conectar e testar o LiDAR SimuLS30H, utilizando o software oficial SimuViewer, seguindo as recomendações do manual do fabricante.

1. Download do Software SimuViewer

O SimuLS30H utiliza o software SimuViewer para visualização e configuração do LiDAR.

Faça o download do pacote oficial (arquivo .zip) no site do fabricante:

🔗 Download do SimuViewer
https://www.simulidar.com/download

(Procure pelo SimuViewer correspondente ao SimuLS30H)

Após o download:

Extraia o arquivo .zip

Execute o instalador do SimuViewer

Conclua a instalação normalmente

2. Configuração da Rede IPv4 no Computador

Para que o computador consiga se comunicar com o LiDAR, é necessário configurar manualmente o IPv4 da interface de rede Ethernet, conforme definido no manual do SimuViewer.

2.1 Acessar configurações de rede (Windows)

Abra Configurações

Vá em Rede e Internet

Clique em Configurações avançadas de rede

Selecione Alterar opções do adaptador

Clique com o botão direito na interface Ethernet conectada ao LiDAR

Selecione Propriedades

Clique em Protocolo IP Versão 4 (IPv4)

Clique em Propriedades

2.2 Configurar IPv4 manualmente (PC)

Configure o IPv4 do computador da seguinte forma:

Endereço IP: 192.168.1.100

Máscara de sub-rede: 255.255.255.0

Gateway padrão: deixe em branco

Confirme e feche todas as janelas.

3. Endereço IP Padrão do LiDAR (SimuLS30H)

De acordo com o manual do SimuViewer, o SimuLS30H vem de fábrica com o seguinte IP:

IP do LiDAR: 192.168.1.201

Máscara: 255.255.255.0

⚠️ Importante:
O computador e o LiDAR devem estar no mesmo segmento de rede (192.168.1.x).

4. Teste de Conectividade (Ping)

Antes de abrir o SimuViewer, é essencial confirmar que a comunicação de rede está funcionando.

4.1 Teste de Ping

Abra o Prompt de Comando (CMD)

Execute:

ping 192.168.1.201

4.2 Resultado esperado

✅ Com resposta: a conexão física e de rede está funcionando

❌ Sem resposta: verifique:

Cabo Ethernet

IP configurado corretamente

LiDAR ligado e inicializado

Só avance para o próximo passo se o ping responder corretamente.

5. Teste no SimuViewer

Agora vamos testar a comunicação usando o software.

Abra o SimuViewer

Selecione a interface de rede correta (Ethernet)

Tente iniciar a visualização dos dados do LiDAR

5.1 Caso funcione

Se os dados aparecerem na tela, o LiDAR está corretamente configurado e pronto para uso.

6. Problema comum: SimuViewer bloqueado pelo Firewall

Se o ping funciona, mas o SimuViewer não recebe dados, isso normalmente significa que o Firewall do Windows está bloqueando a comunicação, pois a rede é considerada “não segura”.

Nesse caso, é necessário liberar o SimuViewer no Firewall, tanto para redes privadas quanto públicas.

7. Liberando o SimuViewer no Firewall do Windows
7.1 Acessar configurações do Firewall

Abra o Painel de Controle

Vá em Sistema e Segurança

Clique em Firewall do Windows Defender

Clique em Permitir um aplicativo pelo firewall

Clique em Alterar configurações

7.2 Liberar o SimuViewer

Clique em Permitir outro aplicativo

Selecione o executável do SimuViewer
Exemplo:

C:\Program Files\SimuViewer\SimuViewer.exe


Adicione o aplicativo

Marque as opções:

✅ Privado

✅ Público

Clique em OK

8. Teste Final

Após liberar o firewall:

Feche o SimuViewer

Abra novamente

Inicie a leitura do LiDAR

Se tudo estiver correto:

O SimuViewer exibirá os dados do LiDAR em tempo real

O SimuLS30H estará pronto para uso em aplicações de mapeamento, navegação ou pesquisa
