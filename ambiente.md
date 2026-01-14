# PAVO LiDAR SDK – Windows (C++)

Este repositório contém um exemplo funcional de uso do **SDK do LiDAR PAVO** em **C++**, compilado no **Windows** utilizando **Visual Studio** e **Boost**.

O projeto realiza a leitura das varreduras do LiDAR e detecta objetos dentro de um raio configurável (exemplo: 10 cm ou 1 metro), exibindo distância e ângulo da leitura.

---

## 🧰 Ambiente Utilizado

- **Sistema Operacional:** Windows 10 / Windows 11 (64 bits)
- **Compilador:** MSVC (Microsoft Visual C++)
- **IDE:** Visual Studio 2019
- **Toolset:** MSVC v141
- **Arquitetura:** x64
- **Padrão C++:** C++14

---

## ⚠️ IMPORTANTE (LEIA ANTES DE COMPILAR)

> **TODOS os comandos devem ser executados no:**
>
> 👉 **"Developer Command Prompt for VS 2019 – x64"**
>
> Não utilize:
> - Prompt de comando comum
> - PowerShell
> - Terminal x86
>
> Caso contrário, ocorrerão erros de linkagem (`LNK1104`, `LNK1181`, etc).

---

## 📦 Dependências

### Boost
- **Versão:** `1.66.0`
- **Link oficial:**  
  https://www.boost.org/users/history/version_1_66_0.html

Estrutura esperada:
