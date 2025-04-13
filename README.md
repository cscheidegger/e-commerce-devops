# E-commerce DevOps

Este repositório contém a configuração DevOps para o sistema de e-commerce, permitindo a execução de todos os componentes em containers Docker.

## Arquitetura

O sistema é composto por três componentes principais:

1. **Frontend** - Interface de usuário em React para o e-commerce
2. **API Backend** - API REST em Python/FastAPI para gerenciar operações de e-commerce
3. **FakeStore API** - Serviço externo para obtenção de dados de produtos

![Arquitetura](arquitetura.png)

## Requisitos

- Docker
- Docker Compose

## Instruções de Instalação

1. Clone este repositório:

 git clone https://github.com/cscheidegger/e-commerce-devops.git
cd e-commerce-devops

2. Crie um arquivo `.env` baseado no `.env.example`:
cp .env.example .env
3. Execute o sistema completo:
make up
4. Para parar todos os serviços:
make down
## Comandos Disponíveis

Utilize o Makefile para operações comuns:
- `make up` - Inicia todos os serviços
- `make down` - Para todos os serviços
- `make logs` - Visualiza logs
- `make build` - Reconstrói os containers
![arquitetura-ecommerce](https://github.com/user-attachments/assets/ff8190e0-59d6-49ae-bf76-4569b70012c9)
<svg viewBox="0 0 800 400" xmlns="http://www.w3.org/2000/svg">
  <!-- Background -->
  <rect width="800" height="400" fill="#f8f9fa" rx="10" ry="10"/>
  
  <!-- Title -->
  <text x="400" y="40" font-family="Arial" font-size="24" font-weight="bold" text-anchor="middle" fill="#333">Arquitetura do Sistema E-commerce</text>
  
  <!-- Components -->
  <!-- Frontend Box -->
  <rect x="100" y="100" width="180" height="100" fill="#6ea8fe" stroke="#0d6efd" stroke-width="2" rx="5" ry="5"/>
  <text x="190" y="140" font-family="Arial" font-size="16" font-weight="bold" text-anchor="middle" fill="#333">Interface (Front-End)</text>
  <text x="190" y="165" font-family="Arial" font-size="14" text-anchor="middle" fill="#333">React</text>
  <image x="135" y="115" width="25" height="25" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9Ii0xMS41IC0xMC4yMzE3NCAyMyAyMC40NjM0OCI+CiAgPHRpdGxlPlJlYWN0IExvZ288L3RpdGxlPgogIDxjaXJjbGUgY3g9IjAiIGN5PSIwIiByPSIyLjA1IiBmaWxsPSIjNjFkYWZiIi8+CiAgPGcgc3Ryb2tlPSIjNjFkYWZiIiBzdHJva2Utd2lkdGg9IjEiIGZpbGw9Im5vbmUiPgogICAgPGVsbGlwc2Ugcng9IjExIiByeT0iNC4yIi8+CiAgICA8ZWxsaXBzZSByeD0iMTEiIHJ5PSI0LjIiIHRyYW5zZm9ybT0icm90YXRlKDYwKSIvPgogICAgPGVsbGlwc2Ugcng9IjExIiByeT0iNC4yIiB0cmFuc2Zvcm09InJvdGF0ZSgxMjApIi8+CiAgPC9nPgo8L3N2Zz4K"/>
  
  <!-- API Box -->
  <rect x="400" y="100" width="180" height="100" fill="#a3cfbb" stroke="#198754" stroke-width="2" rx="5" ry="5"/>
  <text x="490" y="140" font-family="Arial" font-size="16" font-weight="bold" text-anchor="middle" fill="#333">API (Back-End)</text>
  <text x="490" y="165" font-family="Arial" font-size="14" text-anchor="middle" fill="#333">Python FastAPI</text>
  <image x="445" y="115" width="25" height="25" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMjggMTI4Ij48bGluZWFyR3JhZGllbnQgaWQ9ImEiIGdyYWRpZW50VW5pdHM9InVzZXJTcGFjZU9uVXNlIiB4MT0iNzAuMjUyIiB5MT0iMTIzOS4xMTAiIHgyPSIxNzAuNjU5IiB5Mj0iMTEzOC43MDMiIGdyYWRpZW50VHJhbnNmb3JtPSJtYXRyaXgoLjU2MyAwIDAgLS41NjggLTI5LjIxNSA3MDcuODE3KSI+PHN0b3Agb2Zmc2V0PSIwIiBzdG9wLWNvbG9yPSIjNWE5ZmQ0Ii8+PHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSIjMzA2OTk4Ii8+PC9saW5lYXJHcmFkaWVudD48cGF0aCBmaWxsPSJ1cmwoI2EpIiBkPSJNNjMuMzkxIDEuOTg4Yy00LjIyMi4wMi04LjI1Mi4zNzktMTEuOCAxLjAwNy0xMC40NSAxLjg0Ni0xMi4zNDYgNS43MS0xMi4zNDYgMTIuODM3djkuNDExaDI0LjY5M3YzLjEzN0gyOS45NzdjLTcuMTc2IDAtMTMuNDYgNC4zMTMtMTUuNDI2IDEyLjUyMS0yLjI2OCA5LjQwNS0yLjM2OCAxNS4yNzUgMCAyNS4wOTYgMS43NTUgNy4zMTEgNS45NDcgMTIuNTE5IDEzLjEyNCAxMi41MTloOC40OTF2LTExLjI4MmMwLTguMTUxIDcuMDUxLTE1LjM0IDE1LjQyNi0xNS4zNGgyNC42NjVjNi44NjYgMCAxMi4zNDYtNS42NTQgMTIuMzQ2LTEyLjU0OFYxNS44MzNjMC02LjY5My01LjY0Ni0xMS43Mi0xMi4zNDYtMTIuODM3LTQuMjQ0LS43MDYtOC42NDUtMS4wMjctMTIuODY2LTEuMDA4ek01MC4wMzcgOS41NTdjMi41NS4wMDEgNC42MzQgMi4xMTcgNC42MzQgNC43MXMtMi4wODQgNC43MS00LjYzNCA0LjcxYy0yLjU1IDAtNC42MzMtMi4xMTEtNC42MzMtNC43MXMyLjA4My00LjcxIDQuNjMzLTQuNzF6Ii8+PGxpbmVhckdyYWRpZW50IGlkPSJiIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSIgeDE9IjEzMi45OTkiIHkxPSIxMTQ3LjgxMSIgeDI9IjIzNC4xNDkiIHkyPSIxMDQ2LjY2MCIgZ3JhZGllbnRUcmFuc2Zvcm09Im1hdHJpeCguNTYzIDAgMCAtLjU2OCAtMjkuMjE1IDcwNy44MTcpIj48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiNmZmQ0M2IiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiNmZmU4NzMiLz48L2xpbmVhckdyYWRpZW50PjxwYXRoIGZpbGw9InVybCgjYikiIGQ9Ik05MS42ODIgMjguMzh2MTAuOTY2YzAgOC41LTcuMjA4IDE1LjY1NS0xNS40MjYgMTUuNjU1SDUxLjU5MWMtNi43NTYgMC0xMi4zNDYgNS43ODMtMTIuMzQ2IDEyLjU0OXYyMy41MTVjMCA2LjY5MSA1LjgxOCAxMC42MjggMTIuMzQ2IDEyLjU0NyA3LjgxNiAyLjI5NyAxNS4zMTIgMi43MTMgMjQuNjY1IDAgNi4yMTYtMS44MDEgMTIuMzQ2LTUuNDIzIDEyLjM0Ni0xMi41NDd2LTkuNDEySDYzLjkzOHYtMy4xMzhoMzcuMDEyYzcuMTc2IDAgOS44NTItNS4wMDUgMTIuMzQ4LTEyLjUxOSAyLjU3OC03LjczNSAyLjQ2Ny0xNS4xNzQgMC0yNS4wOTYtMS43NzQtNy4xNDUtNS4xNjEtMTIuNTIxLTEyLjM0OC0xMi41MjFoLTkuMjY4ek03OC4zNyA4MS4wOTljMi41NTEgMCA0LjYzNCAyLjExIDQuNjM0IDQuNzFzLTIuMDgzIDQuNzEtNC42MzQgNC43MWMtMi41NSAwLTQuNjMzLTIuMTEtNC42MzMtNC43MXMyLjA4My00LjcxIDQuNjMzLTQuNzF6Ii8+PC9zdmc+"/>
  
  <!-- External API Box -->
  <rect x="400" y="280" width="180" height="100" fill="#e7c6c6" stroke="#dc3545" stroke-width="2" rx="5" ry="5"/>
  <text x="490" y="320" font-family="Arial" font-size="16" font-weight="bold" text-anchor="middle" fill="#333">API Externa</text>
  <text x="490" y="345" font-family="Arial" font-size="14" text-anchor="middle" fill="#333">FakeStore API</text>
  <image x="445" y="295" width="25" height="25" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIj48IS0tISBGb250IEF3ZXNvbWUgRnJlZSA2LjUuMSBieSBAZm9udGF3ZXNvbWUgLSBodHRwczovL2ZvbnRhd2Vzb21lLmNvbSBMaWNlbnNlIC0gaHR0cHM6Ly9mb250YXdlc29tZS5jb20vbGljZW5zZS9mcmVlIENvcHlyaWdodCAyMDIzIEZvbnRpY29ucywgSW5jLiAtLT48cGF0aCBkPSJNOTkuNSAxNzQuOGwyMS42IDhjNS45IDIuMSA5LjggNy40IDEwLjEgMTMuNWwuMSAyLjRjMCAxMS4xLTYuMiAyMS4zLTE2LjEgMjYuNCAxLjkgMS44IDMuNyAzLjkgNS4zIDYuMXMzLjEgNC41IDQuNCA3YzMuNC4zIDYuOS0uMSA5LjgtMS40bDE0LjYtNi41YzMuNCAxMC4zIDEyLjkgMTguMiAyNC4zIDE4LjJoNDQuOWMzIDAgNS44LS40IDguNS0xLjJ2LTQ4LjRjLTE0LjEgNC45LTI5LjggNC4yLTQzLjQtMi00LjUtMi4xLTEwLjMtLjYtTTE0MS43IDE2aDMyLjFjMzguMiAwIDY5LjIgMzEgNjkuMiA2OS4ydj4MTAzLjJjOC4yLTEuNyAxNC0zczEzLjMgMjYuNCAxMy4zIDI2LjR2LTQyLjFsMTAuMSAxOC44LTE1LjUtM2MtMjUuNS00LjktNDQtMjYuOC00NC01MlYxNTJzMjguNS0zNi4yIDAtODguMVY0OGMwLTE3LjctMTQuMy0zMi0zMi0zMkg5Mi41Yy0xNy43IDAtMzIgMTQuMy0zMiAzMnY4OS43Ii8+PC9zdmc+" />

  <!-- Database Box -->
  <rect x="400" y="170" rx="5" ry="5" width="25" height="40" fill="#FFFFFF" stroke="#000000" stroke-width="2"/>
  <rect x="425" y="175" rx="2" ry="2" width="15" height="30" fill="#FFFFFF" stroke="#000000" stroke-width="2"/>
  <text x="470" y="195" font-family="Arial" font-size="14" text-anchor="middle" fill="#333">PostgreSQL</text>
  
  <!-- Arrows -->
  <!-- Frontend to API -->
  <path d="M280 150 H 400" stroke="#333" stroke-width="2" fill="none" marker-end="url(#arrowhead)"/>
  <text x="340" y="140" font-family="Arial" font-size="12" text-anchor="middle" fill="#333">REST API</text>
  
  <!-- API to Frontend -->
  <path d="M400 170 H 280" stroke="#333" stroke-width="2" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- API to External API -->
  <path d="M490 200 V 280" stroke="#333" stroke-width="2" fill="none" marker-end="url(#arrowhead)"/>
  <text x="520" y="240" font-family="Arial" font-size="12" text-anchor="middle" fill="#333">HTTP</text>
  
  <!-- External API to API -->
  <path d="M470 280 V 200" stroke="#333" stroke-width="2" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- Arrowhead Definition -->
  <defs>
    <marker id="arrowhead" markerWidth="10" markerHeight="7" refX="9" refY="3.5" orient="auto">
      <polygon points="0 0, 10 3.5, 0 7" fill="#333"/>
    </marker>
  </defs>
  
  <!-- Legend -->
  <rect x="620" y="100" width="150" height="120" fill="#f8f9fa" stroke="#333" stroke-width="1" rx="5" ry="5"/>
  <text x="695" y="120" font-family="Arial" font-size="14" font-weight="bold" text-anchor="middle" fill="#333">Legenda</text>
  
  <rect x="635" y="135" width="15" height="15" fill="#6ea8fe" stroke="#0d6efd" stroke-width="1"/>
  <text x="660" y="147" font-family="Arial" font-size="12" fill="#333" x-anchor="start">Interface de usuário</text>
  
  <rect x="635" y="160" width="15" height="15" fill="#a3cfbb" stroke="#198754" stroke-width="1"/>
  <text x="660" y="172" font-family="Arial" font-size="12" fill="#333" x-anchor="start">Backend API</text>
  
  <rect x="635" y="185" width="15" height="15" fill="#e7c6c6" stroke="#dc3545" stroke-width="1"/>
  <text x="660" y="197" font-family="Arial" font-size="12" fill="#333" x-anchor="start">Serviço Externo</text>
</svg>


