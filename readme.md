# Tutorial de Configuração e Uso do LiDAR SimuLS30H

Este repositório contém um **tutorial completo** para configurar, conectar e testar o LiDAR **SimuLS30H**, utilizando o software oficial **PavoView**, seguindo as recomendações do manual do fabricante.

---

## 1. Download do Software PavoView

O SimuLS30H utiliza o software **PavoView** para visualização e configuração do LiDAR.

Faça o download do pacote oficial (arquivo `.zip`) no site do fabricante:

🔗 **Download do PavoView**  
[https://www.simulidar.com/download](https://www.siminics.shop/download.html)

> Procure pelo PavoView compatível com o modelo **SimuLS30H**.

Após o download:
1. Extraia o arquivo `.zip`
2. Execute o instalador do PavoView
3. Conclua a instalação normalmente

---

## 2. Configuração da Rede IPv4 no Computador

Para que o computador consiga se comunicar com o LiDAR, é necessário configurar manualmente o IPv4 da interface de rede Ethernet, conforme definido no manual do PavoView.

### 2.1 Acessar configurações de rede (Windows)

1. Abra **Configurações**
2. Vá em **Rede e Internet**
3. Clique em **Configurações avançadas de rede**
4. Selecione **Alterar opções do adaptador**
5. Clique com o botão direito na interface **Ethernet** conectada ao LiDAR
6. Selecione **Propriedades**
7. Clique em **Protocolo IP Versão 4 (IPv4)**
8. Clique em **Propriedades**

---

### 2.2 Configurar IPv4 manualmente (PC)

Configure o IPv4 do computador da seguinte forma:

- Endereço IP: `192.168.1.100`
- Máscara de sub-rede: `255.255.255.0`
- Gateway padrão: (deixe em branco)

Salve as configurações e feche todas as janelas.

---

## 3. Endereço IP Padrão do LiDAR (SimuLS30H)

De acordo com o manual do SimuViewer, o **SimuLS30H vem de fábrica com o seguinte IP**:

- IP do LiDAR: `192.168.1.201`
- Máscara de sub-rede: `255.255.255.0`

> ⚠️ Importante:  
> O computador e o LiDAR **devem estar no mesmo segmento de rede** (`192.168.1.x`).

---

## 4. Teste de Conectividade (Ping)

Antes de abrir o SimuViewer, é essencial confirmar que a comunicação de rede está funcionando.

### 4.1 Teste de Ping

1. Abra o **Prompt de Comando (CMD)**
2. Execute o comando:

```bash
ping 192.168.1.201
