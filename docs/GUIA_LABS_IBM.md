# Guia dos Labs IBM - Skills Network & AI Classroom

> **Objetivo:** Maximizar aprendizado nas plataformas práticas da IBM  
> **Atualizado:** Janeiro/2026

---

## 🏫 IBM AI Classroom (Cursos 1-3)

### O que é?

Plataforma web interativa para experimentar com modelos de IA generativa durante os Cursos 1-3 do Bloco 1. Não requer código Python — tudo funciona no navegador.

### Como Acessar

1. Dentro do curso no Coursera, procure por "Lab" ou "Hands-on Lab"
2. Clique no botão "Launch Lab" ou "Open Tool"
3. Abre em nova aba — plataforma IBM AI Classroom
4. **NÃO fecha a aba do Coursera** (pode perder progresso)

### Funcionalidades Principais

**1. Prompt Playground**
- Interface para testar prompts
- Modelos disponíveis: IBM Granite, Meta Llama
- Ajustar parâmetros: temperatura, max tokens, top-p

**2. Comparação de Modelos**
- Testar mesmo prompt em diferentes modelos
- Ver diferenças de resposta lado a lado

**3. Histórico de Prompts**
- Salva seus experimentos na sessão
- ⚠️ **Atenção:** Histórico é perdido ao fechar aba — copie prompts importantes

### Dicas de Uso

✅ **Copie prompts interessantes** para seu arquivo de anotações  
✅ **Teste variações** — mude uma palavra e veja a diferença  
✅ **Anote parâmetros** que funcionaram bem (temperatura, etc)  
✅ **Tire screenshots** de resultados úteis  

❌ **NÃO confie na sessão** persistir — salve manualmente  
❌ **NÃO use para trabalho real** — é ambiente de aprendizado  

---

## 💻 IBM Skills Network Labs (Cursos 4-16)

### O que é?

Ambiente JupyterLab completo na nuvem com:
- Python 3.x pré-instalado
- Bibliotecas de Data Science/ML/GenAI
- Terminal bash
- Suporte a notebooks (.ipynb)
- Acesso a GPUs (cursos específicos)

### Como Acessar

1. No Coursera, procure "Hands-on Lab"
2. Clique em "Launch Lab" ou "Open Tool"
3. Aguarde ~30-60 segundos (provisioning do ambiente)
4. Interface JupyterLab abre em nova aba

### Limitações Importantes

⚠️ **Sessão expira após 2-4 horas de inatividade**  
⚠️ **Dados são deletados ao fechar** (ambiente efêmero)  
⚠️ **Recursos limitados** (CPU, RAM, GPU compartilhados)  
⚠️ **Pode haver fila** em horários de pico  

### Salvando Seu Trabalho

#### Opção 1: Download Manual (Recomendado)

```bash
# No JupyterLab:
# 1. Clicar com botão direito no arquivo
# 2. Download
# 3. Salvar em ~/certificacoes/ibm-genai/blocoX/...
```

#### Opção 2: Git dentro do Lab

```bash
# Terminal do JupyterLab
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"

# Clonar seu repo
git clone https://github.com/solon07/ibm-genai-engineering.git

# Trabalhar nos arquivos
cd ibm-genai-engineering

# Commit e push ao final
git add .
git commit -m "Lab: [descrição]"
git push
```

#### Opção 3: Copiar/Colar

- Abrir arquivo no lab
- Selecionar tudo (Ctrl+A)
- Copiar (Ctrl+C)
- Colar em arquivo local no VS Code
- Salvar e commitar

---

## 🗂️ Estrutura Típica de um Lab

```
lab-assignment/
├── instructions.md          # Instruções do lab
├── notebook.ipynb           # Notebook Jupyter principal
├── data/                    # Datasets fornecidos
│   ├── dataset.csv
│   └── images/
├── solution/                # ⚠️ Só abrir se travar!
│   └── solution.ipynb
└── README.md
```

### Como Abordar um Lab

**1. Leia as instruções ANTES de abrir o notebook (10 min)**
- Entenda o objetivo
- Identifique pré-requisitos
- Veja o que é esperado como entrega

**2. Execute células uma por uma (não "Run All")**
- Leia comentários
- Entenda o que cada célula faz
- Modifique e teste variações

**3. Complete os exercícios marcados com "TODO"**
- Geralmente têm `# TODO: Complete this section`
- Tente resolver sozinho primeiro
- Se travar >15min, veja a solução

**4. Salve incrementalmente**
- A cada seção completada: File → Download
- Ou commit via Git

**5. Revisão final**
- Execute tudo de novo (Kernel → Restart & Run All)
- Confirme que não há erros
- Salve versão final

---

## 🐛 Troubleshooting Comum

### Erro: "Module not found"

```bash
# No terminal do JupyterLab
pip install nome-do-pacote

# Depois reinicie o kernel:
# Kernel → Restart Kernel
```

### Lab travou / não responde

1. Salve o que conseguir (Download)
2. Recarregue a página (F5)
3. Se persistir: feche e reabra o lab
4. **Último recurso:** "End Lab" e iniciar novo

### Sessão expirou

**Não tem jeito — é perdido.**  
Por isso: salve frequentemente!

### Código não roda / erro estranho

**Checklist:**
- [ ] Rodou células anteriores? (ordem importa)
- [ ] Kernel foi reiniciado? (pode limpar variáveis)
- [ ] Dataset está no lugar certo?
- [ ] Versão do Python/biblioteca está correta?

---

## 📊 Comparação: AI Classroom vs Skills Network

| Aspecto | AI Classroom | Skills Network Labs |
|---------|--------------|---------------------|
| **Usado em** | Cursos 1-3 | Cursos 4-16 |
| **Tipo** | Interface web | JupyterLab |
| **Código?** | Não | Sim (Python) |
| **Persiste?** | Não | Não |
| **GPUs?** | N/A | Sim (alguns labs) |
| **Terminal?** | Não | Sim (bash) |
| **Limite de tempo** | Ilimitado | 2-4h |

---

## 💡 Melhores Práticas

### Antes de Iniciar um Lab

- [ ] Ler instruções completamente
- [ ] Revisar conceito relacionado (vídeo/anotações)
- [ ] Ter VS Code aberto localmente
- [ ] Água/café preparado (labs levam 30min-2h)

### Durante o Lab

- [ ] Seguir ordem das células
- [ ] Entender antes de copiar código
- [ ] Modificar e testar variações
- [ ] Salvar a cada 20-30min

### Após Completar

- [ ] Download final do notebook
- [ ] Salvar em `~/certificacoes/ibm-genai/blocoX/...`
- [ ] Git commit com mensagem descritiva
- [ ] Anotar insights no template de anotações

---

## 🎯 Estratégias por Tipo de Lab

### Labs de Exploração (Cursos 1-3)

**Objetivo:** Familiarizar com conceitos, não memorizar  
**Abordagem:** Teste livremente, foque em intuição

### Labs de Código (Cursos 4-9)

**Objetivo:** Praticar sintaxe e bibliotecas  
**Abordagem:** Digite código (não copie), experimente

### Labs de Projeto (Cursos 10-16)

**Objetivo:** Construir algo funcional  
**Abordagem:** Planeje antes, implemente incrementalmente, teste muito

---

## 🔗 Links Úteis

- [IBM Skills Network](https://skills.network/)
- [Documentação Labs](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%201/images/IDSNlogo.png)
- [Suporte Técnico](https://www.coursera.org/learn/introduction-to-ai/discussions)

---

## ⚠️ Lembretes Críticos

1. **Labs não substituem setup local** — use para prática, mas tenha ambiente próprio
2. **Sempre salve externamente** — sessões expiram
3. **Git é seu amigo** — versione tudo
4. **Erro é normal** — faz parte do aprendizado, não desanime

---

**Próximo passo:** Iniciar primeiro lab do Curso 1 amanhã! 🚀
