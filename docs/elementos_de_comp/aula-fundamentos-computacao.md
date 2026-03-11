<div align="center">

<img src="https://img.shields.io/badge/Disciplina-Fundamentos%20de%20Computa%C3%A7%C3%A3o-6366f1?style=for-the-badge&logoColor=white" alt="Disciplina"/>
<img src="https://img.shields.io/badge/N%C3%ADvel-Introdu%C3%A7%C3%A3o-22c55e?style=for-the-badge&logoColor=white" alt="Nível"/>
<img src="https://img.shields.io/badge/Formato-Diagramas%20Interativos-f59e0b?style=for-the-badge&logoColor=white" alt="Formato"/>

# 🖥️ Fundamentos de Computação

### Arquitetura · Sistemas de Arquivos · Terminal · Ambiente Python

---

*Material didático em diagramas interativos · Abrir cada link no navegador*

</div>

---

## 📚 Conteúdo da Aula

Esta aula cobre os fundamentos da computação em quatro blocos temáticos: **arquitetura do computador**, **sistemas de arquivos**, **comandos de terminal** e **ambientes de desenvolvimento Python**.

---

## 🔷 Bloco 1 — Arquitetura do Computador

Visão geral dos componentes físicos e lógicos de um computador e como se comunicam entre si.

### Diagramas

| # | Diagrama | Descrição |
|---|----------|-----------|
| 1.1 | [🖥️ Arquitetura Básica do Computador](diagrama-computador.html) | CPU, memória, disco e dispositivos de entrada e saída. Inclui o ciclo Fetch–Decode–Execute. |
| 1.2 | [⚡ CPU, Memória, Entradas e Saídas](diagrama-simplificado.html) | Os 4 elementos essenciais e fluxo de dados animado entre eles. |

### Conceitos abordados

- **CPU** (Unidade Central de Processamento): UC, ULA e Registradores
- **Memória**: hierarquia Cache → RAM → Memória Virtual
- **Barramento**: canais de dados, endereços e controle
- **Entrada/Saída**: teclado, mouse, monitor, impressora, rede
- **Ciclo de execução**: Busca → Decodificação → Execução

---

## 🔷 Bloco 2 — Sistemas de Arquivos

Organização hierárquica (em árvore) de diretórios e arquivos nos principais sistemas operacionais.

### Diagramas

| # | Diagrama | Descrição |
|---|----------|-----------|
| 2.1 | [🌳 Sistema de Arquivos Unix/Linux](diagrama-sistema-arquivos.html) | Árvore completa a partir da raiz `/`. Inclui caminhos absolutos, relativos e diretórios padrão FHS. |
| 2.2 | [🪟 Sistema de Arquivos Windows NTFS](diagrama-windows.html) | Estrutura com letras de unidade `C:\`, `D:\`. Explorer com árvore completa de `Users`, `Windows`, `Program Files`. |

### Conceitos abordados

- **Nó raiz**: ponto de partida único da hierarquia
- **Diretório**: contém outros arquivos ou pastas
- **Arquivo**: unidade de dados (nó folha)
- **Link simbólico**: atalho que aponta para outro nó
- **Caminhos**: absoluto, relativo, `~` (home), `..` (subir nível)
- **Diferenças Unix × Windows**: `/` vs `C:\`, separador `/` vs `\`, atributo oculto

---

## 🔷 Bloco 3 — Terminal e Linha de Comando

Comandos essenciais para navegar, criar, apagar e editar arquivos nos três principais sistemas operacionais.

### Diagramas

| # | Diagrama | Descrição |
|---|----------|-----------|
| 3.1 | [🪟 Comandos PowerShell (Windows)](diagrama-powershell-v2.html) | Navegação, criação, exclusão e edição. Aliases compactos (`cd`, `ls`, `rm`, `cp`) em destaque. |
| 3.2 | [🍎 Comandos Terminal macOS](diagrama-macos-terminal.html) | Mesmas categorias. Comandos nativos como `open`, `nano`, `touch`. Shell padrão `zsh`. |
| 3.3 | [🐧 Comandos Terminal Linux](diagrama-linux-terminal.html) | Mesmas categorias. Comandos `nano`, `vim`, `gedit`. Prompt `alice@ubuntu`. Shell `bash`/`zsh`. |

### Comandos comparados por sistema

| Ação | PowerShell | macOS | Linux |
|------|-----------|-------|-------|
| Diretório atual | `pwd` | `pwd` | `pwd` |
| Navegar | `cd` | `cd` | `cd` |
| Listar | `ls` / `dir` | `ls` | `ls` |
| Criar pasta | `mkdir` | `mkdir` | `mkdir` |
| Criar arquivo | `ni` (New-Item) | `touch` | `touch` |
| Copiar | `cp` | `cp` | `cp` |
| Mover/renomear | `mv` | `mv` | `mv` |
| Apagar | `rm` / `del` | `rm` | `rm` |
| Ver conteúdo | `cat` | `cat` | `cat` |
| Editar (GUI) | `notepad` | `open` | `gedit` |
| Editar (terminal) | — | `nano` / `vim` | `nano` / `vim` |
| Ajuda | `Get-Help` | `man` | `man` |

---

## 🔷 Bloco 4 — Ambiente de Desenvolvimento Python com Pixi

Gerenciamento moderno de ambientes e pacotes Python usando o **Pixi** (prefix.dev).

### Diagrama

| # | Diagrama | Descrição |
|---|----------|-----------|
| 4.1 | [✨ Pixi — Gerenciador de Ambientes Python](diagrama-pixi.html) | Instalação nos três sistemas, comandos de projeto, pacotes, execução e diagnóstico. |

### Por que Pixi?

- Instala pacotes de **conda-forge** e **PyPI** no mesmo ambiente
- Gera `pixi.lock` para reprodução exata do ambiente em qualquer máquina
- Substitui `venv` + `pip` + `conda` com um único fluxo de trabalho
- Funciona em Linux, macOS e Windows sem configuração extra

### Fluxo básico de trabalho

```bash
# 1. Criar projeto
pixi init meu-projeto
cd meu-projeto

# 2. Adicionar dependências
pixi add python numpy pandas

# 3. Ativar ambiente
pixi shell

# 4. Executar script
pixi run python script.py
```

---


### Instalação do VScode

[instalação](install_vscode.html)

[Pacote de extensões utilizadas no curso](https://marketplace.visualstudio.com/items?itemName=255ribeiro.pypixipack)

## 🗂️ Todos os Diagramas

| Arquivo | Tema |
|---------|------|
| [diagrama-computador.html](diagrama-computador.html) | Arquitetura básica do computador |
| [diagrama-simplificado.html](diagrama-simplificado.html) | CPU, memória, E/S |
| [diagrama-sistema-arquivos.html](diagrama-sistema-arquivos.html) | Sistema de arquivos Unix/Linux |
| [diagrama-windows.html](diagrama-windows.html) | Sistema de arquivos Windows NTFS |
| [diagrama-powershell-v2.html](diagrama-powershell-v2.html) | Comandos PowerShell |
| [diagrama-macos-terminal.html](diagrama-macos-terminal.html) | Comandos Terminal macOS |
| [diagrama-linux-terminal.html](diagrama-linux-terminal.html) | Comandos Terminal Linux |
| [diagrama-pixi.html](diagrama-pixi.html) | Pixi — gerenciador Python |

---

<div align="center">

*Fundamentos de Computação · Material didático · Diagramas interativos em HTML*

</div>
