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

comando para gerar o exe do sdk:

cl /std:c++14 /EHsc /MD /O2 ^
 /D_WIN32_WINNT=0x0601 ^
 /D BOOST_ALL_NO_LIB ^
 /D BOOST_CONFIG_SUPPRESS_OUTDATED_MESSAGE ^
 /I include ^
 /I C:\dev\boost_1_66_0 ^
 src\main.cpp ^
 src\pavo_driver.cpp ^
 src\data_filters.cpp ^
 src\utils.cpp ^
 /link ^
 /LIBPATH:C:\dev\boost_1_66_0\stage\lib ^
 boost_system-vc-mt-x64-1_66.lib ^
 boost_thread-vc-mt-x64-1_66.lib ^
 ws2_32.lib ^
 /OUT:pavo_sdk.exe
